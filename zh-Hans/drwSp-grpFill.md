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

组填充

一组形状可以通过<xdr:grpSp>（或<p:grpSp>）元素组合在一起。这组形状具有一组属性（在<grpSpPr>内），其中一种属性可以是填充。形状组内的各个形状可以指定自己的填充类型，或者通过为其填充指定<a:grpFill/>来使用组的填充类型。下面是一个电子表格中三个形状组合在一起的示例。组填充被指定为黑色的纯色填充。三角形使用组填充，这是通过在其<spPr>内为三角形形状的填充指定<a:grpFill/>元素来实现的。矩形和椭圆都指定了自己的纯色填充。

<xdr:grpSp>

. . .

<xdr:grpSpPr>

. . .

<a:solidFill>

<a:prstClr val="black"/>

<a:solidFill>

</xdr:grpSpPr>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="2" name="矩形 1"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:solidFill>

<a:srgbClr val="FFFF00"/>

</a:solidFill>

</xdr:spPr>

</xdr:sp>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="3" name="等腰三角形 2"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:grpFill/>

</xdr:spPr>

</xdr:sp>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="4" name="椭圆 3"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:solidFill>

<a:srgbClr val="00B0F0"/>

</a:solidFill>

</xdr:spPr>

</xdr:sp>

</xdr:grpSp>

![Shape with solid fill in spreadsheet](drwImages\drwSp-grpFill.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
