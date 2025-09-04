![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [字处理文档格式 (docx)](anatomyofOOXML.md) | [电子表格格式 (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿格式 (pptx)](anatomyofOOXML-pptx.md)

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

# PresentationML 幻灯片 - 属性 - 页眉和页脚

页脚可以出现在任何类型的幻灯片中。页眉可以出现在备注、备注母版和讲义母版中（但不能出现在幻灯片、幻灯片布局或布局母版中）。页脚和页眉文本、幻灯片编号和日期在形状内指定，即在<p:sp>元素内。为形状指定了形状的非视觉属性内的占位符元素，该占位符元素具有一个type属性值，指定在占位符内找到的内容类型。对于页眉和页脚内的内容，可能的值包括ftr、hdr、dt或sldNum，分别对应页脚文本、页眉文本、日期和幻灯片编号。有关占位符的更多信息，请参见[幻灯片 - 概述](prSlide.md)。请注意，日期和幻灯片编号等内容作为字段嵌入在形状内。有关drawingML文档中的字段的更多信息，请参见[DrawingML - 文本 - 内容](drwSp-text-paragraph.md)。

母版幻灯片中有一个元素，指定是否在页眉和页脚中启用特定的占位符 - 即母版幻灯片、备注母版幻灯片、讲义母版幻灯片和幻灯片布局根元素中的<p:hf>元素。该元素为空，并有四个可能的布尔值属性，指定是否启用占位符中的特定页眉和页脚信息：dt表示日期和时间占位符，ftr表示页脚占位符，hdr表示页眉占位符，sldNum表示幻灯片编号占位符。如果未指定属性，则假定占位符已启用。例如，<p:hf hdr="0" />启用除页眉占位符外的所有占位符。

下面是一个示例母版幻灯片，其中包含页脚文本、幻灯片页脚中的日期以及幻灯片的页脚中的幻灯片编号。请记住，尽管这些形状及其页脚占位符位于母版幻灯片中，但如果要显示它们，它们也必须位于每个幻灯片中。

<p:sldMaster . . . >

<p:cSld>

. . .

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="页脚占位符 2"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="3"/>

</p:nvPr>

</p:nvSpPr>

. . .

<p:txBody>

. . .

<a:p>

<a:r>

. . .

<a:t>我的页脚文本</a:t>

</a:r>

. . .

</a:p>

. . .

</p:txBody>

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="14" name="日期占位符 13"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="2"/>

</p:nvPr>

</p:nvSpPr>

. . .

<p:txBody>

. . .

<a:p>

<a:fld id="{CD6D8A93-66E1-43C3-961E-08F5AB2E9179}" type="datetime1">

. . .

</a:fld>

. . .

</a:p>

. . .

</p:txBody>

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="23" name="幻灯片编号占位符 22"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="4"/>

</p:nvPr>

</p:nvSpPr>

. . .

<p:txBody>

. . .

<a:p>

<a:fld id="{2F48A7AD-349E-4E69-B4D2-764EE05B2523}" type="slidenum">

. . .

</a:fld>

. . .

</a:p>

. . .

</p:txBody>

</p:sp>

</p:spTree>

</p:cSld>

. . .

<p:hf hdr="0" />

. . .

</p:sldMaster>

![Presentation slide](pptxImages\ppSlide-footers.gif)

页脚
