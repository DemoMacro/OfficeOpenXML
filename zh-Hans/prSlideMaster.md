![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

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

# PresentationML 幻灯片 - 母版幻灯片

母版幻灯片是构建演示文稿幻灯片所基于的模板。它指定形状和对象作为演示文稿幻灯片上内容的占位符，以及占位符内内容的格式。当然，母版幻灯片上指定的内容和格式可以被布局幻灯片和演示文稿幻灯片本身更改，但在没有此类覆盖的情况下，母版幻灯片确立了演示文稿的整体外观和感觉。

母版幻灯片是slideMasters目录中的一个单独部分。可以有多个母版幻灯片。演示文稿部分(presentation.xml)通过<p:sldMasterIdLst>元素引用母版幻灯片，该元素是<p:presentation>的子元素。

<p:presentation . .. >

<p:sldMasterIdLst>

<p:sldMasterId id="2147483660" r:id="rId1"/>

</p:sldMasterIdLst>

在presentation.xml.rels中的关系为：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideMaster" Target="/slideMasters/slideMaster1.xml"/>

每个幻灯片布局都与母版幻灯片有关系。因此，在幻灯片布局的.rels文件中有一个关系，指定该布局引用或关联到哪个母版幻灯片。例如，在第一张幻灯片的slideLayout1.xml.rels文件中有以下关系：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideMaster" Target="../slideMasters/slideMaster1.xml"/>。母版幻灯片也有关系（在slideMaster1.xml.rels中）指向基于它的幻灯片布局，以及指向主题。

母版幻灯片的根元素是<p:sldMaster>元素。下面是一个显示根元素可能的子元素的表格。

### 元素：

| 元素             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p:clrMap>       | 指定配色方案。有关详细信息，请参阅[幻灯片属性 - 配色方案](prSlide-color.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <p:cSld>         | 指定幻灯片内容。有关详细信息，请参阅[幻灯片 - 通用幻灯片数据](prCommonSlideData.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p:hf>           | 指定幻灯片的页眉和页脚信息。有关详细信息，请参阅[属性 - 页眉和页脚](prSlide-footer.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p:sldLayoutLst> | 指定幻灯片母版中使用的幻灯片布局列表。此元素包含一个或多个<p:sldLayoutId>元素，每个元素代表一个幻灯片布局，每个元素都有一个关系标识符，唯一地将其与使用它的母版幻灯片标识。每个元素还有一个唯一的id，用于在演示文稿中标识它。下面是一个示例布局列表：<p:sldMaster . .. > . . . <p:sldLayoutIdLst> <p:sldLayoutId id="2147483661" r:id="rId1"/> <p:sldLayoutId id="2147483662" r:id="rId2"/> . . . </p:sldLayoutIdLst> </p:sldMaster> 在母版幻灯片的.rels文件(slideMaster1.xml.rels)中，id = rId1的关系如下所示：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideLayout" Target="../slideLayouts/slideLayout1.xml"/>。第一个布局幻灯片的.rels文件(slideLayout1.xml.rels)有一个指向母版幻灯片的关系：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideMaster" Target="../slideMasters/slideMaster1.xml"/>。 |
| <p:timing>       | 指定幻灯片内动画和计时事件的计时信息。有关详细信息，请参阅[动画和计时](prAnimation.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p:transition>   | 指定从上一张幻灯片切换到当前幻灯片应使用的切换效果类型。有关详细信息，请参阅[属性 - 切换效果](prSlide-transitions.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <p:txStyles>     | 指定母版幻灯片内的文本样式，包括标题、正文和其他文本的样式。有关详细信息，请参阅[属性 - 文本样式](prSlide-styles-textStyles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

页脚
