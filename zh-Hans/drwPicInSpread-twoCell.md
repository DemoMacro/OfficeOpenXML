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

电子表格文档中的定位 - 双单元格锚定

可以使用<xdr:twoCellAnchor>元素将对象锚定到电子表格中的两个单元格。顶部和左侧（起始锚点）使用子元素<xdr:from>锚定，底部和右侧（结束锚点）使用子元素<xdr:to>元素锚定。当起始和结束锚点之间的单元格被移动或调整大小时，图片将（或不会）根据<xdr:twoCellAnchor>上的editAs属性的值被移动和/或调整大小。

<xdr:wsDr . . .>

<xdr:twoCellAnchor editAs="absolute">

<xdr:from>

<xdr:col>1</xdr:col>

<xdr:colOff>0</xdr:colOff>

<xdr:row>2</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

<xdr:to>

<xdr:col>5</xdr:col>

<xdr:colOff>0</xdr:colOff>

<xdr:row>11</xdr:row>

<xdr:rowOff>114300</xdr:rowOff>

</xdr:to>

<xdr:pic>

. . .

</xdr:pic>

<xdr:clientData/>

</xdr:twoCellAnchor>

</xdr:wsDr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.33。

Word 2007示例：

下面是一个锚定在两个单元格的图片示例。

![Spreadsheet Picture - Two Anchors](drwImages\drwInSpread-TwoAnchor.gif)

下面是<xdr:twoCellAnchor>的子元素和属性

### 属性：

| 属性   | 描述                                                                                                          |
| ------ | ------------------------------------------------------------------------------------------------------------- |
| editAs | 指定当起始和结束锚点之间的行和列被调整大小，或者添加额外的行或列时，应如何移动和/或调整对象的大小。可能的值是 |

- absolute \- 不随基础行/列移动或调整大小。保持当前的起始和结束位置；如果添加了额外的行或列，对象锚点将根据需要移动以保持相同位置。
- oneCell \- 随单元格移动但不调整大小。如果添加了额外的行或列，对象锚点将根据需要移动以保持相同位置。
- twoCell \- 随锚定单元格移动和调整大小。

下面是使用editAs="absolute"调整E列大小的示例。请注意，图像没有被调整大小。![电子表格图片 - 双锚点 - editAs absolute](drwImages\drwInSpread-TwoAnchor-editAs-absolute.gif) 下面是使用editAs="twoCell"调整E列大小的示例。请注意，图像被调整了大小。![电子表格图片 - 双锚点 - editAs absolute](drwImages\drwInSpread-TwoAnchor-editAs-twoCell.gif)

下面是<xdr:twoCellAnchor>可能的子元素。

### 元素：

| 元素         | 描述                                                                                                                                                                                                                                                                             |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| clientData   | 一个空元素，它（通过属性）指定与绘图对象的打印和选择相关的某些属性。fLocksWithSheet属性（true或false）确定在工作表受保护时是否禁用选择，fPrintsWithSheet属性（true或false）确定在打印工作表时是否打印该对象。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.3。 |
| contentPart  | 指定对ECMA-376规范未定义的格式中的XML内容的引用，例如MathML或SVG内容。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.12。                                                                                                                                       |
| cxnSp        | 指定连接形状的属性，例如连接其他两个形状的线条。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.13。                                                                                                                                                 |
| from         | 指定起始锚点。有关定义锚点的更多信息，请参见下文。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.15。                                                                                                                                                           |
| graphicFrame | 指定包含图形对象（例如图表、图表或表格）的电子表格的图形对象框架。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.16。                                                                                                                               |
| grpSp        | 指定组形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.17。                                                                                                                                                                                     |
| pic          | 指定电子表格中图片的存在。请参见[绘图 - 图片 - 概述](drwPic.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.25。                                                                                                                                            |
| sp           | 指定形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.29。                                                                                                                                                                                       |
| to           | 指定结束锚点。有关定义锚点的更多信息，请参见下文。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.32。                                                                                                                                                           |

## 定义起始和结束锚点

### 起始锚点 (<xdr:from>)

起始锚点确定对象的顶部和左侧位置，并使用<xdr:from>元素指定。锚点通过列出起点的列和行来指定，这些列和行使用<xdr:col>和<xdr:row>元素指定。这些元素中的每个内容都是列和行的从零开始的索引。但是，起始锚点不必正好在列和行的交叉点处。它可以落在单元格内，这是通过指定从列(<xdr:colOff>)和行(<xdr:rowOff>)的偏移量来定义的；两者都以EMU为单位，或者以数字后紧跟单位标识符的形式（例如，2in）。请记住drawingML坐标系。原点在左上角；x轴从左到右增加，y轴从上到下增加。因此，起始锚点的完整规范包含<xdr:col>和<xdr:colOff>，以及<xdr:row>和<xdr:rowOff>。下面是一个起始锚点在第二列和第三行，没有偏移量的示例。

<xdr:twoCellAnchor editAs="absolute">

<xdr:from>

<xdr:col>1</xdr:col>

<xdr:colOff>0</xdr:colOff>

<xdr:row>2</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

. . .

</xdr:twoCellAnchor>

![Spreadsheet Picture - Starting Anchor - No Offset](drwImages\drwInSpread-TwoAnchor-from1.gif)

下面是一个起始锚点在第二列和第三行，具有来自列和行的偏移量的示例。

<xdr:twoCellAnchor editAs="absolute">

<xdr:from>

<xdr:col>1</xdr:col>

<xdr:colOff>314325</xdr:colOff>

<xdr:row>2</xdr:row>

<xdr:rowOff>95250</xdr:rowOff>

</xdr:from>

. . .

</xdr:twoCellAnchor>

![Spreadsheet Picture - Starting Anchor - No Offset](drwImages\drwInSpread-TwoAnchor-from2.gif)

### 结束锚点 (<xdr:to>)

结束锚点定义底部和右侧，并使用<xdr:to>元素指定。<xdr:to>元素的定义与<xdr:from>元素相同—使用<xdr:col>和<xdr:colOff>，以及<xdr:row>和<xdr:rowOff>元素。请注意，如果<xdr:twoCellAnchor>的editAs是absolute并且锚定列或行被调整，那么列和行元素的值将会改变。但是，如果属性值是twoCell，那么列和行元素的值不会改变，但对象大小会改变。下面是一个结束锚点在第五列和第十一行，两者都有偏移量的示例。

<xdr:twoCellAnchor editAs="absolute">

. . .

<xdr:to>

<xdr:col>4</xdr:col>

<xdr:colOff>609600</xdr:colOff>

<xdr:row>10</xdr:row>

<xdr:rowOff>114300</xdr:rowOff>

</xdr:to>

. . .

</xdr:twoCellAnchor>

![Spreadsheet Picture - Starting Anchor - No Offset](drwImages\drwInSpread-TwoAnchor-to1.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
