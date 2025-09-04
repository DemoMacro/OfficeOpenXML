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

# PresentationML 幻灯片 - 属性 - 背景

幻灯片的背景被指定为幻灯片、幻灯片布局或幻灯片母版的通用幻灯数据元素（<p:cSld>）的子元素。它在<p:bg>元素内指定。有两种指定背景的方法：（1）在<p:bgPr>元素内指定背景的属性，或（2）通过使用<p:bgRef>元素引用演示文稿主题部分中定义的背景样式。

使用<p:bgPr>元素指定的背景可以是形状允许的任何填充、图像或效果。有关指定填充的详细信息，请参阅[DrawingML - 形状 - 形状填充](drwSp-shapeFill.md)。下面是一个具有简单纯色填充背景的幻灯片。

<p:cSld>

<p:bg>

<p:bgPr>

<a:solidFill>

<a:schemeClr val="bg2">

<a:lumMoc val="75000"/>

<a:alpha val="75000"/>

</a:schemeClr>

</a:solidFill>

<a:effectLst/>

</p:bgPr>

</p:bg>

<p:spTree>

. . .

</p:spTree>

</p:cSld>

![Slide background - bgPr](pptxImages\ppSlide-background1.gif)

背景引用使用<p:bgRef>元素指定。它有一个idx属性，该属性是演示文稿主题部分的背景填充样式（在<a:bgFillStyleLst>内）或填充样式（在<a:fillStyleLst>内）的索引。有关主题组件以及背景和填充样式的更多信息，请参阅[DrawingML - 样式](drwSp-styles.md)。idx属性值为0或1000表示没有背景。值1-999指的是填充样式的索引，值1001及以上指的是背景填充样式的索引（1001对应第一个背景填充样式）。下面是母版幻灯片对第二个背景填充样式的引用（<p:bgRef idx="1002">）。

<p:cSld>

<p:bg>

<p:bgRef idx="1002">

<a:schemeClr val="bg2"/>

</p:bgRef>

</p:bg>

<p:spTree>

. . .

</p:spTree>

</p:cSld>

主题部分中对应的背景填充样式是渐变填充。请参阅[DrawingML - 形状 - 渐变填充](drwSp-GradFill.md)。上面的<a:schemeClr val="bg2"/>表示要在渐变填充中使用的颜色。这里示例说明使用配色方案的第二个背景颜色。该背景颜色可以在母版幻灯片的颜色映射（<p:clrMap>）中找到。在示例中，母版幻灯片的颜色映射如下所示：

<p:clrMap bg1="dk1" tx1="lt1" bg2="dk2" tx2="lt2" accent1="accent1" accent2="accent2" accent3="accent3" accent4="accent4" accent5="accent5" accent6="accent6" hlink="hlink" folHlink="folHlink"/>

颜色dk2在主题部分中指定为：

<a:clrScheme name="Foundry">

. . .

<a:dk2>

<a:srgbClr val="676A55"/>

</a:dk2>

. . .

</a:clrScheme>

![Slide background - bgRef](pptxImages\ppSlide-background2.gif)

页脚
