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

# PresentationML 幻灯片 - 内容 - 形状树

幻灯片的大部分内容都附加到形状和表格上。（有关形状的更多信息，请参阅[绘图ML - 形状](drwShape.md)；有关表格的更多信息，请参阅[绘图ML - 表格](http://www.officeopenxml.com/drwTable.md)。）演示文稿幻灯片内的形状和表格本身都包含在一个父级 <p:spTree> 元素中。形状树可以包含图片、形状、连接线和表格（在 <p:graphicFrame> 元素内 — 请参阅[绘图ML - 概述](http://www.officeopenxml.com/drwOverview.md)），以及形状组和形状组的属性。该树还可能包含 ECMA-376 规范中未定义的内容。

<p:spTree> 中的每个形状或其他对象都有一个唯一的 z 轴顺序级别。这意味着形状和对象在 <p:spTree> 中出现的顺序决定了它们在重叠时彼此堆叠的顺序。树中的第一个形状具有最低的 z 轴顺序，最后一个形状具有最高的 z 轴顺序。例如，下面是三个重叠的形状。

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

. . [blue] . .

</p:sp>

<p:sp>

. . [orange] . .

</p:sp>

<p:sp>

. . [green] . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sld>

![Presentation slide](pptxImages\ppSlide-z-order1.gif)

如果我们将第三个形状移动到第一个位置，我们会得到以下结果。

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

. . [green] . .

</p:sp>

<p:sp>

. . [blue] . .

</p:sp>

<p:sp>

. . [orange] . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sld>

![Presentation slide](pptxImages\ppSlide-z-order2.gif)

### <p:spTree> 的子元素：

| 元素             | 描述                                                                                                                                                                                                                                                                                                                                      |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p:contentPart>  | 指定对 ECMA-376 规范未定义的格式中的 XML 内容的引用，从而允许本地使用其他交换格式，如 MathML、SMIL 和 SVG。此处不再进一步讨论。                                                                                                                                                                                                           |
| <p:cxnSp>        | 指定用于连接两个 <p:sp> 元素的连接形状。有关更多信息，请参阅[绘图ML - 连接线](drwCxnSp.md)。                                                                                                                                                                                                                                              |
| <p:extLst>       | 允许指定可用于存储各种数据的扩展。此处不涉及。                                                                                                                                                                                                                                                                                            |
| <p:graphicFrame> | 指定由外部 xml 源生成的图形，如表格或其他对象。此元素充当此类图形数据的容器。请参阅[绘图ML - 在演示文稿文档中的放置](http://www.officeopenxml.com/drwPicInPresentation.md)和[绘图ML - 概述](http://www.officeopenxml.com/drwOverview.md)。                                                                                                |
| <p:grpSp>        | 指定一个组形状或两个或更多形状组合在一起，以便在应用变换时它们被视为单个形状。其内容模型与 <p:spTree> 元素的内容模型相同。也就是说，它可以包含组形状、组形状属性、非视觉组形状属性、形状、图片、连接线等。                                                                                                                                |
| <p:grpSpPr>      | 指定组形状的一组属性。内容模型与形状的属性非常相似，只是它不包含任何几何图形，因为显然组的形状由组成它的各个形状的几何图形决定。此外，2D 变换（<a:xfrm>，定义边界框的大小（<a:ext>）和位置（<a:off>））包含额外的子元素 <a:chExt> 和 <a:chOff>。这些表示子范围和子偏移量。有关更多信息，请参阅[绘图ML - 形状 - 视觉属性](drwSp-SpPr.md)。 |
| <p:nvGrpSpPr>    | 指定组形状的一组非视觉属性。内容模型与形状的非视觉属性非常相似，只是子元素不是 <p:cNvSpPr> 而是 <p:cNvGrpSpPr>。另请注意，对于演示文稿，有一个 <p:nvPr> 元素，其中包含与对象关联的多媒体内容以及形状占位符（请参阅[幻灯片 - 概述](prSlide.md)）。有关更多信息，请参阅[绘图ML - 形状 - 非视觉属性](drwSp-nvSpPr.md)。                      |

### <p:nvGrpSpPr> 的子元素：

| 元素           | 描述                                                                                                                                                                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p:cNvGrpSpPr> | 指定与组上的锁定相关的非视觉组形状属性（组是否可以移动、调整大小、旋转等）。请参阅单个形状的 <p:spLocks> 元素的[讨论](drwSp-nvSpPr.md)，这对应于此处组的 <p:grpSpLocks>。 |
| <p:cNvPr>      | 指定绘图画布的非视觉属性，如 id、名称、描述、组是否隐藏等。请参阅单个形状的 <p:cNvPr> 元素的[讨论](drwSp-nvSpPr.md)。                                                     |
| <p:nvPr>       | 指定与对象关联的多媒体（请参阅[幻灯片 - 内容 - 多媒体](prSlide-multiMedia.md)）以及幻灯片内容的占位符（<p:ph> 元素）（请参阅[幻灯片 - 概述](prSlide.md)）。               |
| <p:pic>        | 指定图片的存在。有关详细信息，请参阅[绘图ML - 图片](drwPic.md)。                                                                                                          |
| <p:sp>         | 指定形状的存在。有关详细信息，请参阅[绘图ML - 形状](drwShape.md)。                                                                                                        |

下面是一个 <p:spTree> 示例。

<p:spTree>

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

<a:xfrm>

</p:grpSpPr>

<p:sp>

<p:sp>

. . .

</p:sp>

<p:sp>

. . .

</p:sp>

<p:sp>

. . .

</p:sp>

</p:spTree>

页脚
