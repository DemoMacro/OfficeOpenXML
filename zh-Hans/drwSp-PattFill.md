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

# DrawingML形状

图案填充

图案填充指定用于填充对象的重复图案。它使用<a:pattFill>元素指定。图案有三个基本属性：(1)要使用的实际图案，由prst属性指定，(2)前景色，指定为子元素<a:fgClr>，以及(3)背景色，指定为子元素<a:bgClr>。

<a:pattFill prst="dotGrid">

<a:fgClr>

<a:prstClr val="gray"/>

</a:fgClr>

<a:bgClr>

<a:prstClr val="blue"/>

</a:bgClr>

</a:pattFill>

![Shape with pattern fill in spreadsheet](drwImages\drwSp-patternFill.gif)

### 元素：

<a:pattFill>具有以下元素。

| 元素  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| bgClr | 指定图案填充的背景色。可以使用以下颜色选项之一指定颜色：作为预设颜色(<a:prstClr>)，使用色调、饱和度和亮度(<a:hslClr>)，方案颜色(<a:schemeClr>)，系统颜色(<a:sysClr>)，或作为RGB百分比或十六进制数(<a:scrgbClr>或<a:srgbClr>)。请注意，这些对应于颜色规范方法的元素也可以具有转换基础颜色的子元素。因此，例如，在下面的示例中，方案或主题颜色被指定为accent6，但对该基础颜色应用了亮度调制。此处不详细讨论颜色。<a:schemeClr val="accent6"> <a:lumMod val="75000"/> </a:schemeClr> |
| fgClr | 指定图案填充的前景色。有关颜色的讨论，请参见上面的bgClr。                                                                                                                                                                                                                                                                                                                                                                                                                         |

<pattFill>可以具有以下属性。

| 属性 | 描述                                         |
| ---- | -------------------------------------------- |
| prst | 指定一组预设图案之一来填充对象。可能的值是： |

- 十字
- 虚线向下对角线
- 虚线水平
- 虚线向上对角线
- 虚线垂直
- 对角砖块
- 对角交叉
- 草皮痕
- 深色向下对角线
- 深色水平
- 深色向上对角线
- 深色垂直
- 向下对角线
- 点状菱形
- 点状网格
- 水平
- 水平砖块
- 大棋盘
- 大五彩纸屑
- 大网格
- 浅色向下对角线
- 浅色水平
- 浅色向上对角线
- 浅色垂直
- 窄水平z
- 窄垂直
- 开放菱形
- 百分比5 (5%)
- 百分比10 (10%)
- 百分比20 (20%)
- 百分比25 (25%)
- 百分比30 (30%)
- 百分比40 (40%)
- 百分比50 (50%)
- 百分比60 (60%)
- 百分比70 (70%)
- 百分比75 (75%)
- 百分比80 (80%)
- 百分比90 (90%)
- 格子图案
- 屋顶板
- 小棋盘
- 小五彩纸屑
- 小网格
- 实心菱形
- 球体
- 格架
- 向上对角线
- 垂直
- 波浪
- 宽向下对角线
- 宽向上对角线
- 编织
- 锯齿形

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
