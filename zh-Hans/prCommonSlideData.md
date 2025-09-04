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

# PresentationML 幻灯片 - 通用幻灯片数据

任何类型的幻灯片的内容都包含在父级 <p:cSld>（通用幻灯片数据）元素中。也就是说，如果信息仅适用于特定类型的幻灯片（例如演示幻灯片或 <p:sld> 的切换效果），则它包含在 <p:cSld> 元素之外。任何可能出现在任何幻灯片类型中的内容都在 <p:cSld> 元素内。<p:cSld> 元素是特定幻灯片类型的根元素的子元素（因此是 <p:sld> 或 <p:sldMaster> 或 <p:sldLayout> 等的子元素）。

幻灯片内容主要由位于幻灯片上的形状和表格组成；形状和表格本身包含文本或其他内容。有关形状和表格的更多信息，请参阅 [DrawingML - 形状](http://www.officeopenxml.com/drwShape.md) 和 [DrawingML - 表格](http://www.officeopenxml.com/drwTable.md)。这些形状和表格包含在 <p:spTree> 元素中，该元素是 <p:cSld> 的子元素。因此，大多数幻灯片内容位于幻灯片的 <p:cSld> 中，而 <p:cSld> 的大部分内容位于 <p:spTree> 中。因此，当谈到幻灯片内容时，大部分讨论都是关于 <p:spTree> 的。下面是一个包含两个形状的示例幻灯片。

<p:sld . . . >

<p:nvGrpSpPr>

<p:cNvPr id="1" name=""/>

<p:cNvGrpSpPr/>

<p:nvPr/>

</p:nvGrpSpPr>

<p:grpSpPr>

<a:xfrm>

<a:off x="0" y="0"/>

<a:ext cx="0" cy="0"/>

<a:chOff x="0" y="0"/>

<a:chExt cx="0" cy="0"/>

</a:xfrm>

</p:grpSpPr>

<p:cSld>

<p:spTree>

<p:sp>

. . .

</p:sp>

<p:sp>

. . .

</p:sp>

</p:spTree>

</p:cSld>

<p:clrMapOvr>

<p:clrMapOvr>

<p:masterClrMapping/>

</p:sld>

<p:cSld> 元素可能包含如下所示的子元素。请注意，有一个可能的属性：name，可用于标识通用幻灯片数据。

### 元素：

| 元素            | 描述                                                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| <p:bg>          | 指定幻灯片的背景。有关详细信息，请参阅 [幻灯片属性 - 背景](prSlide-background.md)。                                       |
| <p:controls>    | 指定幻灯片的嵌入控件列表。此处不涉及。                                                                                    |
| <p:custDataLst> | 允许指定客户定义的数据。此处不涉及。                                                                                      |
| <p:extLst>      | 允许指定可用于存储各种数据的扩展。此处不涉及。                                                                            |
| <p:spTree>      | 指定幻灯片上所有基于形状的对象，无论是否分组。有关形状树的更多信息，请参阅 [幻灯片 - 内容 - 形状](prSlide-shapeTree.md)。 |

页脚
