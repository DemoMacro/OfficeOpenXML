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
    - [文本正文属性](drwSp-text-bodyPr.md)
      - [定位和内边距](drwSp-text-bodyPr-inset.md)
      - [适应、环绕、弯曲和3D](drwSp-text-bodyPr-fit.md)
      - [列、垂直文本和旋转](drwSp-text-bodyPr-columns.md)
    - [段落](drwSp-text-paragraph.md)
      - [段落属性](drwSp-text-paraProps.md)
        - [项目符号和编号](drwSp-text-paraProps-numbering.md)
        - [间距、缩进和边距](drwSp-text-paraProps-margins.md)
        - [对齐、制表符、其他](drwSp-text-paraProps-align.md)
      - [文本运行属性](drwSp-text-runProps.md)
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

# DrawingML图片

在电子表格文档中的定位 - 单单元格锚定

可以使用<xdr:oneCellAnchor>元素将对象锚定到电子表格中的单个单元格。对象随锚定单元格一起移动。锚的位置通过子元素<xdr:from>指定。<xdr:from>元素通过首先指定锚的列和行来定义；原点位于单元格的左上角。列由<xdr:col>元素给出，行由<xdr:row>元素给出。这些元素中的每一个的内容都是列和行的从零开始的索引。

从单元格的左上角可以指定与列和行的任何偏移量。也就是说，锚不必正好位于单元格的左上角，而是可以落在单元格内。从单元格左上角边缘的任何偏移量通过指定与列(<xdr:colOff>)和行(<xdr:rowOff>)的偏移量来定义；两者都以EMU为单位，或者以数字后紧跟单位标识符的形式表示（例如，2in）。请记住drawingML坐标系。原点在左上角；x轴从左到右增加，y轴从上到下增加。因此，锚的完整规范包含<xdr:col>和<xdr:colOff>，以及<xdr:row>和<xdr:rowOff>。下面是一个起始锚位于第四列和第四行，与列有半英寸偏移量，与行没有偏移量的示例。

<xdr:wsDr . . .>

<xdr:oneCellAnchor>

<xdr:from>

<xdr:col>3</xdr:col>

<xdr:colOff>457200</xdr:colOff>

<xdr:row>3</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

<xdr:ext cx="2438400" cy="1828800"/>

<xdr:pic>

. . .

</xdr:pic>

<xdr:clientData/>

</xdr:oneCellAnchor>

</xdr:wsDr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.24。

Word 2007示例：

![Spreadsheet Picture - One Anchor](drwImages\drwInSpread-oneAnchor.gif)

下面是一个当调整单元格大小时图片如何跟随锚定的示例。底层XML是相同的。

![Spreadsheet Picture - One Anchor - Resized cells](drwImages\drwInSpread-oneAnchor2.gif)

以下是<xdr:oneCellAnchor>可能的子元素。没有属性（与<xdr:twoCellAnchor>比较）。

### 元素：

| 元素         | 描述                                                                                                                                                                                                                                                                                                                                                   |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| clientData   | 一个空元素，它（通过属性）指定与绘图对象的打印和选择相关的某些属性。fLocksWithSheet属性（true或false）确定在保护工作表时是否禁用选择，fPrintsWithSheet属性（true或false）确定打印工作表时是否打印该对象。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.3。                                                                           |
| contentPart  | 指定对ECMA-376规范未定义的格式中的XML内容的引用，例如MathML或SVG内容。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.12。                                                                                                                                                                                                             |
| cxnSp        | 指定连接形状的属性，例如连接其他两个形状的线条。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.13。                                                                                                                                                                                                                       |
| ext          | 以EMU为单位指定对象显示时的长度和宽度（包括任何缩放）。该元素是一个具有两个属性的空元素：cx属性给出长度，cy属性给出宽度。例如，<xdr:ext cx="2438400" cy="1828800"/>。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.14。                                                                                                              |
| from         | 通过指定包含锚的单元格的列和行，以及与单元格左上角的任何偏移量来指定起始锚。子元素是<xdr:col>、<xdr:colOff>、<xdr:row>和<xdr:rowOff>。列和行值基于列和行的从零开始的索引。偏移量以EMU为单位，或者以数字后紧跟单位标识符的形式给出（例如，2in）。x轴从左到右增加，y轴从上到下增加。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.15。 |
| graphicFrame | 指定包含图形对象（例如，图表、图表或表格）的电子表格的图形对象框架。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.16。                                                                                                                                                                                                   |
| grpSp        | 指定组形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.17。                                                                                                                                                                                                                                                           |
| pic          | 指定电子表格中图片的存在。请参阅[绘图 - 图片 - 概述](drwPic.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.25。                                                                                                                                                                                                                  |
| sp           | 指定形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.29。                                                                                                                                                                                                                                                             |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
