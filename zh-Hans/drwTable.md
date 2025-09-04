![PresentationXML.com](images\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

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
    - 几何图形
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
    - [文本正文属性](drwSp-text-bodyPr.md)
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
- 在文档中的放置
  - [Overview](drwPicInWord.md)
  - [内联对象](drwPicInline.md)
  - [浮动对象](drwPicFloating.md)
    - [定位](drwPicFloating-position.md)
    - [文本环绕](drwPicFloating-textWrap.md)
- 在电子表格中的放置
  - [Overview](drwPicInSpread.md)
  - [绝对锚定](drwPicInSpread-absolute.md)
  - [单单元格锚定](drwPicInSpread-oneCell.md)
  - [双单元格锚定](drwPicInSpread-twoCell.md)
- [在演示文稿中的放置](drwPicInPresentation.md)

# DrawingML 表格

DrawingML中的表格主要出现在演示文稿中。核心表格模型在ECMA OOXML规范（第3版）的第21.1节中的主drawingML命名空间（xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main）中定义。如[DrawingML概述](drwOverview.md)中所述，OOXML有三种不同的表格模型—一种用于文字处理，一种用于电子表格，一种用于drawingML（主要用于presentationML文档）。drawingML表格模型与文字处理模型类似，但它允许在表格或单元格上应用drawingML效果。

表格通过<p:graphicFrame>容器添加到演示文稿幻灯片中，该容器位于主presentationML命名空间（前缀'p'）内。在<p:graphicFrame>容器内是drawingML命名空间中的<a:graphic>元素。在该元素内是<p:graphicData>元素，其uri属性将数据类型声明为表格数据：uri="http://schemas.openxmlformats.org/drawingml/2006/table"。

<p:graphicFrame>容器位于幻灯片的形状树（<p:spTree>）中，与幻灯片上的其他形状和图片一起。形状树元素本身包含在幻灯片的公共幻灯片数据容器元素<p:cSld>中。有关表格放置的详细信息，请参阅[DrawingML概述](drwOverview.md)和[绘图对象放置](drwPicInPresentation.md)。下面是一个包含一个形状和一个表格的示例演示文稿幻灯片。

<p:sld . . . >

. . .

<p:cSld>

<p:spTree>

<p:sp>

. . .

</p:sp>

<p:graphicFrame>

. . .

<a:graphic>

<a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/table">

<a:tbl>

<. . .

</a:tbl>

</a:graphicData>

</a:graphic>

</p:graphicFrame>

</p:spTree>

</p:cSld>

. . .

</p:sld>

![DrawingML - Table](drwImages\drwTable.gif)

表格本身在<a:tbl>元素中定义，该元素本身包含表格结构的定义（在<a:tblGrid>元素内）、表格属性（在<a:tblPr>元素内）和内容（在一个或多个<a:tr>表格行元素内）。drawingML表格只能包含文本。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
