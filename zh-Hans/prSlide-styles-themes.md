![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 放映
  - [切换效果](prSlide-transitions.md)
  - 动画和计时
  - 自定义放映
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

# PresentationML 幻灯片 - 属性 - 填充、轮廓、字体、效果

演示文稿的格式可以在许多不同的地方指定，使用样式和主题的组合，以及覆盖这些样式和主题的直接格式。主题指定属性，如形状的填充颜色属性、形状的轮廓属性、字体和形状效果。

主题（也称为共享样式表）位于包中的单独部分（在主题子文件夹内）。应用于演示文稿的主题在演示文稿的presentation.xml.rels文件中的关系内指定。一个包中可能包含多个主题，但presentation.xml.rels文件中只引用一个。主题的结构在主要的drawingML规范中定义。有关主题组件的更多信息，请参见[DrawingML - 样式](drwSp-styles.md)。

演示文稿的大部分内容包含在形状和图片中。因此，幻灯片的大部分样式是在形状和图片级别确定的。<p:style>元素是形状元素<p:sp>的子元素，指定要应用于形状的样式。样式元素（<a:lnRef>、<a:fillRef>、<a:effectRef>和<a:fontRef>）都通过index或idx属性引用相应的主题元素。例如，形状的<p:style>元素内的<a:fillRef idx="1">引用主题部分的<a:fillStyleLst>中定义的第一个填充样式。

当然，主题指定的并由形状的<p:style>元素引用的样式可以被覆盖。这些覆盖可以在相关项目的属性元素中找到。例如，要指定与主题内指定的不同的背景颜色，会在形状的<p:spPr>元素中放置一个填充元素。在下面的示例中，使用RGB值(45D768)指定了纯色填充，以红色突出显示。要更改文本颜色或字体值，会在形状内段落的相关运行的<a:rPr>元素中设置值。在下面的示例中，字体类型和颜色样式已在运行属性元素中被覆盖，以紫色显示。

<p:sp>

. . .

<p:spPr>

. . .

<a:solidFill>

<a:srgbClr val="45D768"/>

</a:solidFill>

</p:spPr>

<p:style>

<a:lnRef idx="2">

<a:schemeClr val="accent1">

<a:shade val="50000"/>

</a:schemeClr>

</a:lnRef>

<a:fillRef idx="1">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="lt1"/>

</a:fontRef>

</p:style>

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr"/>

<a:lstStyle/>

<a:p>

<a:pPr algn="ctr"/>

<a:r/>

<a:rPr lang="en-US" dirty="0" smtClean="0">

<a:solidFill>

<a:srgbClr val="B9477B"/>

</a:solidFill>

<a:latin typeface="Arial Black" pitchFamily="34" charset="0"/>

</a:rPr>

<a:t>此形状具有自定义填充颜色。</a:t>

</a:r/>

</a:p>

</p:txBody>

![Slide styles - bgPr](pptxImages\ppSlide-styles1.gif)

主题中定义的线条、填充和字体样式在下面的主题部分上下文中显示。（效果样式引用指定索引为0（<a:effectRef idx="0">属性），因此不使用效果样式。）

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Flow">

<a:themeElements>

<a:clrScheme name="Flow">

. . .

</a:clrScheme>

<a:fontScheme>

<a:majorFont>

. . .

</a:majorFont>

<a:minorFont>

. . .

</a:minorFont>

</a:fontScheme>

<a:fmtScheme>

<a:fillStyleLst>

. . .

</a:fillStyleLst>

<a:lnStyleLst>

. . .

</a:lnStyleLst>

<a:effectStyleLst>

. . .

</a:effectStyleLst>

<a:bgFillStyleLst>

. . .

</a:bgFillStyleLst>

</a:fmtScheme>

</a:themeElements>

. . .

</a:theme>

页脚
