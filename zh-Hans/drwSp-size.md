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

# DrawingML形状

边界框大小

形状的边界框大小由<a:xfrm>元素内的<a:ext>或extents元素指定，<a:xfrm>是<a:spPr>（形状属性）元素的子元素。<a:ext>是一个空元素；边界框的长度和宽度由<a:ext>的两个属性指定：cx指定以EMU为单位的宽度，cy指定以EMU为单位的高度。下面是一个三角形形状的示例，后面是同一三角形但高度已扩展的示例。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="371475" cy="428625"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-size1.gif)

下面是同一个三角形，其高度已从428625 EMU扩展到1514475 EMU。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="371475" cy="1514475"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-size2.gif)

注意：如果形状放置在单元格的角落，没有偏移，那么<xdr:to>元素（表示右下角）的值应该与<a:ext>元素指示的大小相同。有关电子表格中的定位和<xdr:to>元素的更多信息，请参见[电子表格文档中的定位 - 双单元格锚定](drwPicInSpread-twoCell.md)。

<xdr:twoCellAnchor>

<xdr:from>

<xdr:col>1</xdr:col>

<xdr:colOff>0</xdr:colOff>

<xdr:row>1</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

<xdr:to>

<xdr:col>1</xdr:col>

<xdr:colOff>876300</xdr:colOff>

<xdr:row>1</xdr:row>

<xdr:rowOff>990600</xdr:rowOff>

</xdr:to>

. . .

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="876300" cy="990600"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

</xdr:twoCellAnchor>

![Shape size](drwImages\drwSp-size3.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
