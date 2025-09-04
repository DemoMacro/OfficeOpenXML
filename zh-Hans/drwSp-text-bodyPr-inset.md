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
      - [适应、环绕、变形和3D](drwSp-text-bodyPr-fit.md)
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

# DrawingML 形状

文本 - 正文属性 - 定位和内边距

## 文本定位或锚定：

形状内文本的锚定位置通过<a:bodyPr>上的anchor属性指定。可能的值有：

- b（边界框底部）
- ctr（边界框中间）
- dist（文本垂直分布。当文本为水平时，这会使实际的文本行间隔开来，与下面的值相同。当文本为垂直时，它会垂直分布字母，这与下面的值不同，因为它总是强制分布单词。）
- just（文本垂直两端对齐。当文本为垂直时，它会使字母垂直两端对齐。这与上面的dist不同，因为在某些情况下，例如当一行中只有很少的文本时，它不会两端对齐。）
- t（边界框顶部）。这是默认值。

下面是一个居中定位的示例（<a:bodyPr rtlCol="0" anchor="ctr" />），接着是顶部定位（<a:bodyPr rtlCol="0" anchor="t" />）。

![带文本的形状 - 锚定](drwImages\drwSp-text-anchor1.gif) ![带文本的形状 - 锚定](drwImages\drwSp-text-anchor2.gif)

边界框的水平居中可以使用<a:bodyPr>上的anchorCtr属性设置。值为true或false。此属性使文本的最小可能边界框居中。它与段落对齐不同，段落对齐是在边界框内对齐文本。此属性适用于所有不同的垂直锚定值。下面是一个具有水平文本的形状，段落右对齐，边界框垂直居中，而框不水平居中。

<a:bodyPr vert="horz" rtlCol="0" anchor="ctr" anchorCtr="0"/>

![Shape with text - anchoring](drwImages\drwSp-text-anchor3.gif)

下面是相同的形状，但边界框也水平锚定。

<a:bodyPr vert="horz" rtlCol="0" anchor="ctr" anchorCtr="1"/>

![Shape with text - anchoring](drwImages\drwSp-text-anchor4.gif)

## 文本内边距：

边界框的内边距由<a:bodyPr>上的四个属性指定，每边一个：bIns（底部内边距）、tIns（顶部内边距）、lIns（左侧内边距）和rIns（右侧内边距）。内边距用作形状内文本框的内部边距。属性值以EMU为单位指定，或以数字后紧跟单位标识符的形式指定—例如，0.5in。如果某边未指定属性，则默认值为45720或0.05英寸。

下面是一个形状的示例，底部有0.1英寸的内边距，顶部有0.5英寸的内边距，左右两侧没有内边距。

<xdr:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" bIns="91440" tIns="475200" lIns="0" rIns="0"/>

<a:lstStyle/>

. . .

</xdr:txBody>

![Shape with text - inset](drwImages\drwSp-text-inset2.gif)

如果移除内边距属性，我们将得到如下所示的形状和文本。

![Shape with text - inset](drwImages\drwSp-text-inset1.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
