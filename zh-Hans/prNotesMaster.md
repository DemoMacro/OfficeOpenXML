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

# PresentationML 幻灯片 - 备注母版

备注母版幻灯片是构建备注幻灯片所基于的模板。它指定形状和对象作为备注幻灯片上内容的占位符，以及占位符内内容的格式。当然，备注母版上指定的内容和格式可以被备注幻灯片本身更改，但在没有此类覆盖的情况下，备注母版确立了备注幻灯片的整体外观和感觉。有关占位符的更多信息，请参见[幻灯片 - 概述](prSlide.md)。备注幻灯片与任何其他幻灯片非常相似，只是它会有一个用于备注的占位符（类型为'body'）。

备注母版是notesMasters目录内的一个单独部分。只能有一个备注母版。演示文稿部分（presentation.xml）通过<p:notesMasterIdLst>元素引用备注母版，该元素是<p:presentation>的子元素。

<p:presentation . .. >

<p:notesMasterIdLst>

<p:notesMasterId r:id="rId4"/>

</p:notesMasterIdLst>

在presentation.xml.rels中的关系是：<Relationship Id="rId4" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/notesMaster" Target="/notesMasters/notesMaster1.xml"/>

每个备注幻灯片都与备注母版有关系。因此，在备注幻灯片的.rels文件中有一个指定备注母版幻灯片的关系。例如，在第二个备注幻灯片的notesSlide2.xml.rels文件中有以下关系：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/notesMaster" Target="../notesMasters/notesMaster1.xml"/>。

备注母版的根元素是<p:notesMaster>元素。下面是一个显示根元素可能子元素的表格。

### 元素：

| 元素           | 描述                                                                                              |
| -------------- | ------------------------------------------------------------------------------------------------- |
| <p:clrMap>     | 指定配色方案。有关详细信息，请参见[幻灯片属性 - 配色方案](prSlide-color.md)。                     |
| <p:cSld>       | 指定幻灯片内容。有关详细信息，请参见[幻灯片 - 通用幻灯片数据](prCommonSlideData.md)。             |
| <p:hf>         | 指定幻灯片的页眉和页脚信息。有关详细信息，请参见[属性 - 页眉和页脚](prSlide-footer.md)。          |
| <p:notesStyle> | 指定备注幻灯片内的文本样式。有关详细信息，请参见[属性 - 文本样式](prSlide-styles-textStyles.md)。 |

页脚
