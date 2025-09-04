![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

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
      - [定位和内边距](drwSp-text-bodyPr-inset.md)
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

# DrawingML对象定位

电子表格文档中的定位

工作表的所有绘图对象都在一个绘图部件中。包含绘图对象的工作表有多少个，绘图部件就有多少个。（注意，例如图像的实际数据是单独存储的，通常在包的媒体子文件夹中—对于Word，在媒体子文件夹中。）

![File structure for drawing in spreadsheet](drwImages\drwInSpread-fileStruct.gif)

工作表部件将包含一个<drawing>元素，该元素具有引用关系的关系ID属性。

<worksheet . . .>

. . .

<drawing r:id="rId1"/>

. . .

</worksheet>

工作表的关系(.rels)部件包含引用目标绘图部件的关系。

<Relationships . . .>

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/drawing" Target="../drawings/drawing1.xml"/>

</Relationships>

在绘图部件(drawing1.xml)中，容器元素是根<xdr:wsDr>元素。工作表中图片的命名空间是：xlms:xdr="http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing"。有三种可能的子元素，表示对象可以在工作表中锚定的三种不同方式。

1. <wp:absoluteAnchor> \- 用于将对象绝对锚定在工作表中的相同位置；不随单元格移动或调整大小
2. <wp:oneCellAnchor> \- 用于锚定到单个单元格；随单元格移动
3. <wp:twoCellAnchor> \- 用于锚定到两个单元格；随单元格移动

<xdr:wsDr xlms:xdr="http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing xlms:a="http://schemas.openxmlformats.org/drawingml/2006/main">

<xdr:twoCellAnchor editAs="oneCell">

. . .

</xdr:twoCellAnchor>

</xdr:wsDr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.5.2.35。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
