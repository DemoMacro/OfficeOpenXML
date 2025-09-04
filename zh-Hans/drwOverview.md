![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

[主页](index.md) | [字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [Overview](drwOverview.md)
- 图片
  - [Overview](drwPic.md)
  - 图像属性
    - [图像数据](drwPic-ImageData.md)
    - [平铺或拉伸图像以填充](drwPic-tile.md)
    - [效果](drwPic-effects.md)
  - [非视觉属性](drwPic-nvPicPr.md)
  - [形状属性](drwSp-SpPr.md)
- 形状
  - [Overview](drwShape.md)
  - [非视觉属性](drwSp-nvSpPr.md)
  - [视觉属性](drwSp-SpPr.md)
    - [边界框大小](drwSp-size.md)
    - [边界框位置](drwSp-location.md)
    - 几何
      - [预设](drwSp-prstGeom.md)
      - [自定义](drwSp-custGeom.md)
    - [形状填充](drwSp-shapeFill.md)
      - [纯色填充](drwSp-SolidFill.md)
      - [图片填充](drwSp-PictFill.md)
      - [渐变填充](drwSp-GradFill.md)
      - [图案填充](drwSp-PattFill.md)
      - [组填充](drwSp-grpFill.md)
    - [效果](drwSp-effects.md)
    - [轮廓样式](drwSp-outline.md)
    - [2D变换](drwSp-rotate.md)
    - 3D
      - [形状属性](drwSp-3dProps.md)
      - [场景属性](drwSp-3dScene.md)
  - [样式](drwSp-styles.md)
  - [文本](drwSp-text.md)
    - [文本主体属性](drwSp-text-bodyPr.md)
      - [定位和插入](drwSp-text-bodyPr-inset.md)
      - [适应、环绕、弯曲和3D](drwSp-text-bodyPr-fit.md)
      - [列、垂直文本和旋转](drwSp-text-bodyPr-columns.md)
    - [段落](drwSp-text-paragraph.md)
      - [段落属性](drwSp-text-paraProps.md)
        - [项目符号和编号](drwSp-text-paraProps-numbering.md)
        - [间距、缩进和边距](drwSp-text-paraProps-margins.md)
        - [对齐、制表符、其他](drwSp-text-paraProps-align.md)
      - [运行属性](drwSp-text-runProps.md)
    - [列表属性](drwSp-text-lstPr.md)
- [Connectors](drwCxnSp.md)
  - [非视觉属性](drwSp-nvCxnSpPr.md)
- [文本](drwSp-textbox.md)
- 图表
- 图表
- [Tables](drwTable.md)
  - [定义结构](drwTableGrid.md)
  - [行、单元格、单元格内容](drwTableRowAndCell.md)
  - 单元格属性
    - [对齐、边距、方向](drwTableCellProperties-alignment.md)
    - [边框和填充](drwTableCellProperties-bordersFills.md)
  - [表格样式和属性](drwTableStyles.md)
- 文档中的放置
  - [Overview](drwPicInWord.md)
  - [内联对象](drwPicInline.md)
  - [浮动对象](drwPicFloating.md)
    - [定位](drwPicFloating-position.md)
    - [文本环绕](drwPicFloating-textWrap.md)
- 电子表格中的放置
  - [Overview](drwPicInSpread.md)
  - [绝对锚定](drwPicInSpread-absolute.md)
  - [单单元格锚定](drwPicInSpread-oneCell.md)
  - [双单元格锚定](drwPicInSpread-twoCell.md)
- [演示文稿中的放置](drwPicInPresentation.md)

# DrawingML概述

DrawingML是用于在ooxml文档中定义图形对象（如图片、形状、图表和图表）的语言。它还指定了整个包的外观特征，即包的主题。DrawingML不是独立的标记语言；它支持并出现在字处理ML、电子表格ML和演示文稿ML文档中。DrawingML与SVG和VML不同。SVG（可缩放矢量图形）是XML中二维图形的图形文件格式。它主要用于网页和桌面出版。VML是矢量图形文件的竞争语言。现在它基本上已被弃用，取而代之的是SVG。根据ECMA OOXML规范，"DrawingML格式是一种更新、更丰富的格式，创建的目的是最终取代Office Open XML格式中VML的任何使用。VML是一种过渡格式；它仅出于遗留原因包含在Office Open XML中。"VML在Microsoft Word中仍广泛用于某些图形组件，特别是形状和文本框。

DrawingML是一套庞大、令人困惑的规范，用于办公文档中的许多不同视觉组件。它由许多不同的命名空间组成，必须小心确保对于特定文档类型中的给定元素，您拥有正确的命名空间和命名空间前缀。还必须注意对象规范与对象在文档中放置之间的区别。有时，对象的定义（和命名空间）在三种文档类型中是相同的，只有放置规范因文档类型而异。在其他情况下，对象和放置都是每种文档类型独有的。

以下是三种文档类型中各种对象类型及其对应命名空间的简要摘要。任何文档类型中的DrawingML对象（如图表和图表）都放置在<a:graphic>元素内，该元素又包含<a:graphicData>元素。这些元素是主要的drawingML命名空间的一部分：xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"。<a:graphicData>元素基本上是未定义的，因此应用程序可以支持或不支持其中定义的特定对象。该元素具有uri属性，用于指定可以处理元素内容的数据类型和/或"服务器"。例如，Word中图片的uri是"http://schemas.openxmlformats.org/drawingml/2006/picture"。Microsoft Office支持一组对象，包括图表、图表、锁定画布、表格、ole等。其他应用程序将有自己的支持对象类型集。

| 字处理  
---|---  
图片 | 图片对象与其他内容一起在内容部分document.xml中的<pic:pic>元素内定义。这被包装在常规字处理命名空间内的<w:drawing>元素中：xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"。图片定义的命名空间是xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"。图片放置的XML（例如，它是内联的[<wp:inline>]还是锚定的[<wp:anchor>]）在字处理drawingML命名空间内：xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"。  
形状 | 请参阅下面的文本框。  
图表 | 图表在常规内容（document.xml）部分之外定义，而是在单独的部分（每个图表一个）chart1.xml（或chart2.xml等）中定义。图表通过在<a:graphicData>的属性中放置对图表部分的引用，放置在document.xml中的<a:graphicData>元素内，如上所述。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:dgm="http://schemas.openxmlformats.org/drawingml/2006/chart"。图表放置的XML（例如，它是内联的[<wp:inline>]还是锚定的[<wp:anchor>]）在字处理drawingML命名空间内：xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"。  
图表 | 图表在常规内容（document.xml）部分之外定义，而是在四个单独部分（每个图表一组）的组中定义：colors#.xml、data#.xml、layout#.xml和quickStyle#.xml。还有第五个部分drawing#.xml，这是Microsoft添加的用于持久化图表布局信息的扩展。图表通过使用<dgm:relIds>元素放置对图表部分的引用，放置在document.xml中的<a:graphicData>元素内，如上所述。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:dgm="http://schemas.openxmlformats.org/drawingml/2006/diagram"。图表放置的XML（例如，它是内联的[<wp:inline>]还是锚定的[<wp:anchor>]）在字处理drawingML命名空间内：xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"。  
文本框 | Microsoft Word 2003和2007中的形状和文本框使用VML实现，VML已被大量弃用，本网站不涉及。使用Word 2010，Microsoft已转向使用与图表和图表相同的数据结构。Word 2010在文档的XML中同时包含VML和drawingML，使用<mc:AlternateContent>和一对子元素：<mc:Choice Requires="wps">，其中包含drawingML xml，和<mc:Fallback>，其中包含VML。Requires属性的wps指的是新的命名空间word字处理形状（以及<a:graphicData>的uri属性值）：xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"。文本框和形状使用<wps:wsp>元素插入<a:graphicData>元素内。Microsoft对Word的drawingML扩展在此未详细涉及。最后，请注意文本框在许多方面与文本框相似，但它们的底层XML非常不同。它们不是drawingML的一部分。相反，它们在字处理ML内，它们的规范是段落规范的一部分。请参阅[字处理ML - 文本框](WPparagraph-textFrames.md)。  
主题 | 主题实现跨文档类型的通用样式，并在主要的drawingML命名空间内定义：xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"。它们在单独的theme1.xml部分中定义。

| 电子表格  
---|---  
图片 | 图片通过<drawing>元素放置在工作表内，该元素仅引用单独的drawing1.xml（或drawing2.xml等）部分。图片的放置或锚定在绘图部分内使用所需的锚点（例如<xdr:twoCellAnchor>元素）指定。绘图部分包含定义图片的<xdr:pic>元素。命名空间是xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing"。请注意，它不在<a:graphicData>元素内。  
形状 | 形状通过<drawing>元素放置在工作表内，该元素仅引用单独的drawing1.xml（或drawing2.xml等）部分。图表的放置或锚定在绘图部分内使用xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing"命名空间和所需的锚点（例如<xdr:twoCellAnchor>元素）指定。绘图部分又包含定义形状的<xdr:sp>元素。请注意，它不在<a:graphicData>元素内。  
图表 | 图表通过<drawing>元素放置在工作表内，该元素仅引用单独的drawing1.xml（或drawing2.xml等）部分。图表的放置或锚定在绘图部分内使用xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing"命名空间和所需的锚点（例如<xdr:twoCellAnchor>元素）指定。绘图部分又包含上面提到的典型<a:graphicData>元素，该元素包含<c:chart>元素。该元素引用定义图表的单独部分chart1.xml（或chart2.xml等）。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"。  
图表 | 图表通过<drawing>元素放置在工作表内，该元素仅引用单独的drawing1.xml（或drawing2.xml等）部分。图表的放置或锚定在绘图部分内使用xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing"命名空间和所需的锚点（例如<xdr:twoCellAnchor>元素）指定。绘图部分又包含上面提到的典型<a:graphicData>元素，该元素包含<dgm:relIds>元素。该元素引用四个单独部分（每个图表一组）的组：colors#.xml、data#.xml、layout#.xml和quickStyle#.xml，它们共同定义图表。还有第五个部分drawing#.xml，这是Microsoft添加的用于持久化图表布局信息的扩展。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:dgm="http://schemas.openxmlformats.org/drawingml/2006/diagram"。  
文本框 | 文本框是通过将文本插入形状来创建的。请参阅上面的电子表格中的形状。  
主题 | 主题实现跨文档类型的通用样式，并在主要的drawingML命名空间内定义：xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"。它们在单独的theme1.xml部分中定义。

| 演示文稿  
---|---  
图片 | 图片对象与幻灯片的其他内容一起在slide1.xml（或slide2.xml等）中的<p:pic>元素内定义。命名空间是xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"。请注意，它不在<a:graphicData>元素内。  
形状 | 形状与幻灯片的其他内容一起在slide1.xml（或slide2.xml等）中的<p:sp>元素内定义。命名空间是xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"。请注意，它不在<a:graphicData>元素内。  
图表 | 图表通过<p:graphicFrame>元素放置在幻灯片内，该元素又包含上面提到的典型<a:graphicData>元素，该元素包含<c:chart>元素。该元素引用定义图表的单独部分chart1.xml（或chart2.xml等）。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"。  
图表 | 图表通过<p:graphicFrame>元素放置在幻灯片内，该元素又包含上面提到的典型<a:graphicData>元素，该元素包含<dgm:relIds>元素。该元素引用四个单独部分（每个图表一组）的组：colors#.xml、data#.xml、layout#.xml和quickStyle#.xml，它们共同定义图表。还有第五个部分drawing#.xml，这是Microsoft添加的用于持久化图表布局信息的扩展。图表规范的命名空间（和<a:graphicData>的uri属性值）是xmlns:dgm="http://schemas.openxmlformats.org/drawingml/2006/diagram"。  
文本 | 文本是通过将文本插入形状来创建的。请参阅上面的演示文稿中的形状。  
表格 | OOXML有三种不同的表格模型—一种用于字处理表格，一种用于电子表格表格，一种用于演示文稿。最后一种是drawingML的一部分。表格通过<p:graphicFrame>元素放置在幻灯片内，该元素又包含上面提到的典型<a:graphicData>元素，该元素包含<a:tbl>元素。该元素内联包含表格的数据—表格不在单独的部分中。<a:graphicData>的uri属性值是"http://schemas.openxmlformats.org/drawingml/2006/table"。表格规范的命名空间是drawingML主命名空间xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"。  
主题 | 主题实现跨文档类型的通用样式，并在主要的drawingML命名空间内定义：xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"。它们在单独的theme1.xml部分中定义。

ECMA OOXML规范（第3版）对drawingML被分成不同的部分，主要是为了反映不同的命名空间。

![ECMA Specification TOC for DrawingML](drwImages\ecmaSpecTOC.gif)

有一个部分（20.1）涉及命名空间xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"中的大部分主要功能，包括形状、非视觉属性、颜色和样式。另一个部分（201.1）涵盖了主要drawingML命名空间的其余部分，包括文本和文本格式、项目符号和编号以及表格，所有这些主要用于演示文稿文档。有一个单独的部分（20.2）一般涉及图片；图片的命名空间随文档类型而异。然后有一个部分（21.2）用于图表命名空间（xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"）和一个部分（21.4）用于图表命名空间（mlns:dgm="http://schemas.openxmlformats.org/drawingml/2006/diagram"）。有一个部分（20.4）用于drawingML对象在字处理文档中的放置/定位（xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"），和一个部分（20.5）用于drawingML对象在电子表格文档中的放置/定位（xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing）。最后，有关于锁定画布（20.3，此处未涉及）和图表内的绘图（21.3）（xmlns:cdr="http://schemas.openxmlformats.org/drawingml/2006/chartDrawing"）的单独部分。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
