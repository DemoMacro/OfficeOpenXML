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
      - [定位和插入](drwSp-text-bodyPr-inset.md)
      - [适合、环绕、变形和3D](drwSp-text-bodyPr-fit.md)
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

电子表格文档中的定位 - 绝对锚定

对象可以使用<xdr:absoluteAnchor>元素通过坐标在电子表格中按照绝对位置进行锚定。当单元格调整大小时，对象不会移动。位置由子元素<xdr:pos>指定，这是一个空元素，具有两个属性，用于指定对象左上角的两个坐标：x和y。请记住drawingML坐标系。原点在左上角；x轴从左到右增加，y轴从上到下增加。下面是一个绝对锚定的示例，距离左边缘两英寸，距离顶部半英寸。

<xdr:wsDr . . .>

<xdr:absoluteAnchor>

<xdr:pos x="1828800" y="45722"/>

<xdr:ext cx="2438400" cy="1828800"/>

<xdr:pic>

. . .

</xdr:pic>

<xdr:clientData/>

</xdr:absoluteAnchor>

</xdr:wsDr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.1。

Word 2007示例：

![Spreadsheet Picture - Absolute Anchor](drwImages\drwInSpread-absoluteAnchor.gif)

下面是一个示例，展示了当单元格调整大小时图片如何保持锚定。

![Spreadsheet Picture - Absolute Anchor - Resized cells](drwImages\drwInSpread-absoluteAnchor2.gif)

下面是<xdr:absoluteAnchor>可能的子元素。没有属性（与[<xdr:twoCellAnchor>](drwPicInSpread-twoCell.md)比较）。

### 元素：

| 元素         | 描述                                                                                                                                                                                                                                                                                                     |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| clientData   | 一个空元素，通过属性指定与绘图对象打印和选择相关的某些属性。fLocksWithSheet属性（true或false）确定在保护工作表时是否禁用选择，fPrintsWithSheet属性（true或false）确定在打印工作表时是否打印该对象。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.3。                                   |
| contentPart  | 指定对ECMA-376规范未定义格式的XML内容的引用，例如MathML或SVG内容。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.12。                                                                                                                                                                   |
| cxnSp        | 指定连接形状的属性，例如连接其他两个形状的线条。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.13。                                                                                                                                                                         |
| ext          | 以EMU为单位指定对象显示时的长度和宽度（包括任何缩放）。该元素是一个空元素，具有两个属性：cx属性给出长度，cy属性给出宽度。例如，<xdr:ext cx="2438400" cy="1828800"/>。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.14。                                                                |
| graphicFrame | 指定包含图形对象（例如图表、图表或表格）的电子表格的图形对象框架。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.16。                                                                                                                                                       |
| grpSp        | 指定组形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.17。                                                                                                                                                                                                             |
| pic          | 指定电子表格中图片的存在。请参阅[绘图 - 图片 - 概述](drwPic.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.25。                                                                                                                                                                    |
| pos          | 指定drawingML对象的位置。这是一个空元素，具有两个属性，以EMU或数字后紧跟单位标识符（例如2in）的方式指定坐标（x和y）。例如，<xdr:pos x="1828800" y="45722"/>。请记住drawingML坐标系。原点在左上角；x轴从左到右增加，y轴从上到下增加。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.26。 |
| sp           | 指定形状。此处不讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.5.2.29。                                                                                                                                                                                                               |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
