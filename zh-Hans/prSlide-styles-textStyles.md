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
    讲义母版
    幻灯片属性
  - [大小](prSlide-size.md)
  - [背景](prSlide-background.md)
  - [页眉和页脚](prSlide-footer.md)
    样式和格式
    - [填充、字体、轮廓、效果](prSlide-styles-themes.md)
    - [文本样式](prSlide-styles-textStyles.md)
  - [配色方案](prSlide-color.md)
    幻灯片编号

# PresentationML 幻灯片 - 属性 - 文本和备注样式

## 文本样式

演示文稿中文本的格式在幻灯片母版上的<p:txStyles>元素中指定，该元素是幻灯片母版根元素<p:sldMaster>的子元素。在<p:txStyles>元素内，正文文本、标题文本和其他文本的样式在相应的子元素<p:bodyStyle>、<p:titleStyle>和<p:otherStyle>中指定。这三种主要样式类型中的每一种都具有相同的模型。每种都可以指定一组默认段落属性（在<a:defPPr>内），这些属性在未指定其他属性时应用，并且每种都可以指定级别1到9的列表样式（<a:lvl1pPr>到<a:lvl9pPr>）。请注意，这些都位于带有前缀'a'的主drawingML命名空间中。级别和默认属性的可能属性列表（有时指定为子元素，有时指定为属性）如下，有关更多详细信息，请参阅[绘图ML中的列表样式](drwSp-text-lstPr.md)的相关讨论。

## 备注样式

备注幻灯片中文本的格式在备注母版上的<p:notesStyles>元素中指定，该元素是备注母版根元素<p:notesMaster>的子元素。在<p:notesStyles>内，可能有一组默认段落属性（在<a:defPPr>内），这些属性在未指定其他属性时应用。也可能有级别1到9的样式列表（<a:lvl1pPr>到<a:lvl9pPr>）。请注意，这些都位于带有前缀'a'的主drawingML命名空间中。级别和默认属性的可能属性列表（有时指定为子元素，有时指定为属性）如下，有关更多详细信息，请参阅[绘图ML中的列表样式](drwSp-text-lstPr.md)的相关讨论。

| 元素                                            | 描述                                                                      |
| ----------------------------------------------- | ------------------------------------------------------------------------- |
| <a:buAutoNum/> (自动编号项目符号)               | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buBlip> (图片项目符号)                       | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buChar/> (字符项目符号)                      | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buClr> (项目符号颜色)                        | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buClrTx> (项目符号颜色与文本运行相同)        | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buFont/> (项目符号字体)                      | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buFontTx> (项目符号字体与文本运行相同)       | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buNone> (无项目符号)                         | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buSzPct> (项目符号字符的百分比大小)          | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buSzPts/> (项目符号字符的磅值大小)           | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:buSzTx> (项目符号字符大小与文本运行大小相同) | 参见[绘图ML - 项目符号和编号](drwSp-text-paraProps-numbering.md)。        |
| <a:defRPr> (默认文本运行属性)                   | 参见[绘图ML - 列表属性和默认样式](drwSp-text-lstPr.md)。                  |
| <a:lnSpc> (行间距)                              | 参见[绘图ML - 文本 - 间距、缩进和边距](drwSp-text-paraProps-margins.md)。 |
| <a:spcAft> (段后间距)                           | 参见[绘图ML - 文本 - 间距、缩进和边距](drwSp-text-paraProps-margins.md)。 |
| <a:spcBef> (段前间距)                           | 参见[绘图ML - 文本 - 间距、缩进和边距](drwSp-text-paraProps-margins.md)。 |
| <a:tabLst> (段落中的制表位列表)                 | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |

| 属性                                                      | 描述                                                                      |
| --------------------------------------------------------- | ------------------------------------------------------------------------- |
| algn (对齐方式)                                           | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |
| defTabSz (默认制表符大小)                                 | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |
| fontAlgn (字体对齐)                                       | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |
| hangingPunct (指定悬挂文本的处理方式)                     | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |
| indent (文本首行的缩进)                                   | 参见[绘图ML - 文本 - 间距、缩进和边距](drwSp-text-paraProps-margins.md)。 |
| latinLnBrk (指定是否断词)                                 | 参见[绘图ML - 文本 - 对齐、制表符、其他](drwSp-text-paraProps-align.md)。 |
| lvl (文本的级别 — 仅适用于<a:defPPr>；九个级别的值为0到8) | 参见[绘图ML - 列表属性和默认样式](drwSp-text-lstPr.md)。                  |
| marL 和 marR (左边距和右边距)                             | 参见[绘图ML - 文本 - 间距、缩进和边距](drwSp-text-paraProps-margins.md)。 |

以下是来自幻灯片母版的示例xml。请注意二级文本（lvl="1"）的右对齐（以红色突出显示）。实际幻灯片的xml对第二个2级项目符号（文本为"Second level 2 bullet"）有一些样式覆盖。请参阅下面关于样式覆盖的讨论。

<p:sldMaster . . . >

<p:cSld>

. . .

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="文本占位符 2"/>

. . .

<p:nvPr>

<p:ph type="body" idx="1"/>

</p:nvPr>

</p:nvSpPr>

<p:spPr>

. . .

</p:spPr>

<p:txBody>

<a:bodyPr . . .>

. . .

</a:bodyPr>

<a:lstStyle/>

<a:p>

<a:pPr lvl="0"/>

. . .

</a:p>

<a:p>

<a:pPr lvl="1"/>

. . .

</a:p>

. . .

<p:txBody>

. . .

</p:sp>

. . .

</p:spTree>

</p:cSld>

<p:clrMap . . ./>

<p:sldLayoutIdLst>

. . .

</p:sldLayoutIdLst>

<p:txStyles>

<p:titleStyle>

. . .

<p:titleStyle>

<p:bodyStyle>

. . .

<a:lvl2pPr marL=""868680" indent="-283464" algn="r" rtl="0" ealnBrk="1" latinLnBrk="0" hangingPunct="1" >

<a:spcBef>

<a:spcPct val="20000"/>

</a:spcBef>

<a:buClr>

<a:schemeClr val="tx1"/>

</a:buClr>

<a:buSzPct val="80000"/>

<a:buFont typeface="Wingdings2"/>

<a:buChar char="•"/>

<a:defRPr sz="2400" kern="1200">

. . .

</a:defRPr>

</a:lvl2pPr>

<p:bodyStyle>

<p:otherStyle>

. . .

<p:otherStyle>

</p:txStyles>

</p:sldMaster>

![Slide text styles](pptxImages\ppSlide-textStyles1.gif)

## 覆盖形状的样式

当然，幻灯片母版的<p:txStyles>元素中定义的样式可以通过为形状指定不同的样式来覆盖，无论是在幻灯片母版或幻灯片布局的形状内，还是在特定幻灯片内的形状中。例如，下面我们为幻灯片上形状内的2级文本指定了样式，将样式从右对齐更改为居中对齐。

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="内容占位符 2"/>

. . .

<p:nvPr>

<p:ph idx="1"/>

</p:nvPr>

</p:nvSpPr>

<p:spPr/>

<p:txBody>

<a:bodyPr/>

<a:lstStyle>

<a:lvl2pPr marL=""868680" indent="-283464" algn="ctr" rtl="0" ealnBrk="1" latinLnBrk="0" hangingPunct="1" >

<a:spcBef>

<a:spcPct val="20000"/>

</a:spcBef>

<a:buClr>

<a:schemeClr val="tx1"/>

</a:buClr>

<a:buSzPct val="80000"/>

<a:buFont typeface="Wingdings2"/>

<a:buChar char="•"/>

<a:defRPr sz="2400" kern="1200">

. . .

</a:defRPr>

</a:lvl2pPr>

</a:lstStyle>

. . .

</p:txBody>

</p:sp>

. . .

</p:spTree>

</p:cSld>

</p:sld>

![Slide text styles - override at shape level](pptxImages\ppSlide-textStyles2.gif)

## 覆盖形状内段落的样式

在幻灯片母版级别指定的样式，甚至演示文稿幻灯片中特定幻灯片的样式，本身可以通过在形状内文本段落的段落或运行属性中指定不同的样式来覆盖。下面是与上面相同的示例，只是为第一个二级段落指定了左对齐的段落属性。请注意，第二个2级段落不会覆盖为形状指定的段落对齐方式，但它确实覆盖了项目符号字体和项目符号字符。

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

. . .

<p:cNvPr id="3" name="内容占位符 2"/>

. . .

<a:lstStyle>

<a:lvl2pPr marL=""868680" indent="-283464" algn="ctr" rtl="0" ealnBrk="1" latinLnBrk="0" hangingPunct="1" >

<a:spcBef>

<a:spcPct val="20000"/>

</a:spcBef>

<a:buClr>

<a:schemeClr val="tx1"/>

</a:buClr>

<a:buSzPct val="80000"/>

<a:buFont typeface="Wingdings2"/>

<a:buChar char="•"/>

<a:defRPr sz="2400" kern="1200">

. . .

</a:defRPr>

</a:lvl2pPr>

</a:lstStyle>

<a:p>

<a:r>

<a:rPr lang="en-US"/>

<a:t>这里有一些带项目符号的文本</a:t>

</a:r>

</a:p>

<a:p>

<a:pPr lvl="1" algn="l"/>

<a:r>

<a:rPr lang="en-US"/>

<a:t>还有更多文本</a:t>

</a:r>

</a:p>

<a:p>

<a:pPr lvl="1">

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="F0D8"/>

</a:pPr lvl="1">

<a:r>

<a:rPr lang="en-US"/>

<a:t>第二个2级项目符号</a:t>

</a:r>

</a:p>

</p:txBody>

. . .

</p:sp>

. . .

</p:spTree>

</p:cSld>

</p:sld>

![Slide text styles - override at paragraph](pptxImages\ppSlide-textStyles3.gif)

页脚
