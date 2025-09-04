![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 演示
  - [切换效果](prSlide-transitions.md)
  - 动画和计时
  - 自定义演示
- 演示文稿属性
- 视图属性
- 幻灯片
  - [Overview](prSlide.md)
  - [内容（通用幻灯片数据）](prCommonSlideData.md)
    - [形状](prSlide-shapeTree.md)
    - [Tables](drwTable.md)
    - [音频和视频](prSlide-multiMedia.md)
  - [幻灯片母版](prSlideMaster.md)
  - [幻灯片布局](prSlideLayout.md)
  - [Slide](prPresentationSlide.md)
  - [备注母版](prNotesMaster.md)
  - [备注幻灯片](prNotesSlide.md)
  - 讲义母版
- 幻灯片属性
  - [大小](prSlide-size.md)
  - [背景](prSlide-background.md)
  - [页眉和页脚](prSlide-footer.md)
  - 样式和格式
    - [填充、字体、轮廓、效果](prSlide-styles-themes.md)
    - [文本样式](prSlide-styles-textStyles.md)
  - [配色方案](prSlide-color.md)
  - 幻灯片编号

# PresentationML 幻灯片 - 演示幻灯片

演示文稿至少包含一张幻灯片。演示幻灯片包含内容—文本、形状、图表、图表等。演示文稿的每张幻灯片都包含在幻灯片部件中（在幻灯片文件夹内），每个幻灯片部件都是演示文稿部件关系的目标。也就是说，幻灯片在演示文稿部件的presentation.xml.rels文件中被明确引用。例如，存在与slide1.xml的关系：<Relationship Id="rId2" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slide" Target="../slides/slide1.xml"/>。（演示文稿还在<p:sldIdLst>中列出了要在演示中显示的幻灯片。请参阅[演示文稿](prPresentation.md)。）演示幻灯片将与其内容应用的布局幻灯片有关系，该关系将位于该幻灯片的.rels文件中（即，对于幻灯片1，位于slide1.xml.rels中）。以下是应用于第二张幻灯片的布局的关系：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideLayout" Target="../slideLayouts/slideLayout2.xml"/>

幻灯片布局的内容模型与母版幻灯片类似，不同之处在于它不包含文本样式元素，并且它具有颜色映射覆盖而不是颜色映射。（当然，也没有幻灯片布局列表。）有关各种幻灯片类型的内容模型的比较，请参阅[幻灯片 - 概述](prSlide.md)。幻灯片布局的根元素是<p:sldLayout>元素。下面是一个显示根元素可能的子元素的表格，然后是一个显示根<p:sldLayout>元素属性的表格。

### 元素：

| 元素           | 描述                                                                                                                  |
| -------------- | --------------------------------------------------------------------------------------------------------------------- |
| <p:clrMapOvr>  | 指定母版幻灯片的<p:clrMap>中指定的配色方案的覆盖。有关详细信息，请参阅[幻灯片属性 - 配色方案](prSlide-color.md)。     |
| <p:cSld>       | 指定幻灯片内容。有关详细信息，请参阅[幻灯片 - 通用幻灯片数据](prCommonSlideData.md)。                                 |
| <p:timing>     | 指定幻灯片内动画和计时事件的计时信息。                                                                                |
| <p:transition> | 指定应该用于从上一张幻灯片切换到当前幻灯片的切换类型。有关详细信息，请参阅[属性 - 切换效果](prSlide-transitions.md)。 |

属性如下：

### 属性：

| 属性             | 描述                                                                                                                                                                                                                                                                                                                                                                                                           |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| matchingName     | 指定用于替代<p:cSld>上的name属性的名称。请参阅[幻灯片 - 通用幻灯片数据](prCommonSlideData.md)。它用于布局匹配。                                                                                                                                                                                                                                                                                                |
| preserve         | 指定当所有遵循该布局的幻灯片被删除时，是否应删除该布局。默认值为false，因此如果未指定该属性，则布局将被删除。                                                                                                                                                                                                                                                                                                  |
| showMasterPhAnim | 指定是否显示母版幻灯片上占位符的动画。值为布尔值。                                                                                                                                                                                                                                                                                                                                                             |
| showMasterSp     | 指定是否应在幻灯片上显示母版中的形状。值为布尔值。                                                                                                                                                                                                                                                                                                                                                             |
| type             | 指定布局类型，该类型提供幻灯片上占位符的内容类型和位置的高级描述。应用程序可以使用此信息来帮助在不同布局之间进行映射；应用程序可以选择提供哪些布局（如果有）。可能的值的完整列表可以在ECMA-376第3版（2011年6月）的基础知识和标记语言参考§19.7.15中找到。示例包括blank（空白）、picTx（标题、图片和说明文本）、secHead（节标题和副标题文本）、title（具有居中标题和副标题占位符的标题布局）和tx（标题和文本）。 |
| userDrawn        | 指定对象是否由用户绘制，因此不应被删除。值为布尔值。                                                                                                                                                                                                                                                                                                                                                           |

页脚
