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
    - [文本主体属性](drwSp-text-bodyPr.md)
      - [定位和边距](drwSp-text-bodyPr-inset.md)
      - [适应、环绕、变形和3D](drwSp-text-bodyPr-fit.md)
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

# DrawingML 表格 - 结构

表格在<a:tbl>元素中定义，该元素本身包含表格结构的定义（在<a:tblGrid>元素内）、表格属性（在<a:tblPr>元素内）和内容（在一个或多个<a:tr>表格行元素内）。

表格的列由<a:tblGrid>元素定义。<a:tblGrid>为表格中每个可能的单元格大小（有时称为逻辑列）包含一个<a:gridCol>元素。表格的<a:tblGrid>所需的<a:gridCol>元素数量是通过延伸每个单元格的垂直边框并计算由线条定义的列总数来确定的。例如，一个具有三列且没有合并单元格的表格在其<a:tblGrid>中需要3个<a:gridCol>元素。

当单元格在行与行之间的长度不相等时，情况变得更加复杂。例如，下面的表格有四个可能的或逻辑列，因此在其<a:tblGrid>元素中需要4个<a:gridCol>元素。

![DrawingML - Table](drwImages\drwTableGrid2.png)

此表格的<a:tblGrid>如下。

<a:tbl>

. . .

<a:tblGrid>

<a:gridCol w="1219200"/>

<a:gridCol w="1143000"/>

<a:gridCol w="2362200"/>

<a:gridCol w="1371600"/>

</a:tblGrid>

<a:tblGrid>元素包含一个或多个<a:gridCol>元素—每列一个。<a:gridCol>元素有一个属性w，它以EMU（英制公制单位）指定列的宽度。

### 单元格跨距

上面显示的表格包含垂直和水平跨距的单元格示例。例如，单元格1-1、1-2、2-1和2-2已被合并，并包含文本"垂直和水平合并"。在drawingML表格中，单元格跨距的表示方式与WordprocessingML表格中的不同。首先，在WordprocessingML表格中，已合并的单元格不会出现在该行的XML中。也就是说，行中的单元格元素数量与视觉上显示的单元格数量相同。在drawingML表格中，每行包含的<a:tc>元素数量与逻辑列或<a:gridCol>元素的数量相同。其次，WordprocessingML中的单元格跨距是用元素（<w:gridSpan>和<w:vMerge>）表示的。然而，在drawingML中，单元格跨距是用<a:tc>的属性表示的。

表格包含行或<a:tr>元素。每个<a:tr>元素包含的<a:tc>元素数量与<a:gridCol>元素的数量相同。如果两个或更多单元格水平合并，则第一个单元格包含一个gridSpan属性，指定合并的单元格数量。后续合并的单元格包含一个设置为true的hMerge属性（hMerge="1"）。如果两个或更多单元格垂直合并，则第一个单元格（即包含内容的单元格）包含一个rowSpan属性，指定单元格跨度的行数。该单元格下方行中的相应单元格（即与上方单元格合并的单元格）包含一个设置为true的vMerge属性（vMerge="1"）。

下面的示例显示了上面表格的XML。垂直或水平跨度的单元格的相关属性（gridSpan和hMerge="1"，或rowSpan和vMerge）具有匹配的颜色。

<a:tbl>

. . .

<a:tblGrid>

<a:gridCol w="1219200"/>

<a:gridCol w="1143000"/>

<a:gridCol w="2362200"/>

<a:gridCol w="1371600"/>

</a:tblGrid>

<a:tr h="370840">

<a:tc rowSpan="2" gridSpan="2">

. . .

<a:t>垂直和水平合并</a:t>

. . .

</a:tc>

<a:tc rowSpan="2" hMerge="1">

. . .

</a:tc>

<a:tc>

. . .

<a:t>单元格1-3</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>单元格1-4</a:t>

. . .

</a:tc>

</a:tr>

<a:tr h="370840">

<a:tc gridSpan="2" vMerge="1">

. . .

</a:tc>

<a:tc hMerge="1" vMerge="1">

. . .

</a:tc>

<a:tc gridSpan="2">

. . .

<a:t>水平合并</a:t>

. . .

</a:tc>

<a:tc hMerge="1">

. . .

</a:tc>

</a:tr>

<a:tr h="370840">

<a:tc>

. . .

<a:t>单元格3-1</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>单元格3-2</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>单元格3-3</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>单元格3-4</a:t>

. . .

</a:tc>

</a:tr>

. . .

</a:tbl>

![DrawingML - Table](drwImages\drwTableGrid1.png)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
