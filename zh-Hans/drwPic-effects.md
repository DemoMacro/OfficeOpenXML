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

# DrawingML图片

效果

可以将多种效果应用于图片。这些效果被指定为<a:blip>元素的子元素，而<a:blip>元素本身又是<pic:pic>元素内<pic:blipFill>元素的子元素。

<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">

<pic:nvPicPr>

<pic:cNvPr id="0" name="Blue hills.jpg"/>

<pic:cNvPicPr/>

</pic:nvPicPr>

<pic:blipFill>

<a:blip r:embed="rId4" cstate="print">

<a:duotone>

<a:prsClr val="black"/>

<a:schemeClr val="accent3">

<a:tint val="45000"/>

<a:satMode val="400000">

</a:schemeClr>

<a:duotone>

</a:blip>

<a:stretch>

<a:fillRect/>

</a:stretch/>

</pic:blipFill>

<pic:spPr>

<a:xfrm>

<a:off x="0" y="0"/>

<a:ext cx="2438400" cy="1828800"/>

</a:xfrm>

<a:prstGeom rst="rect>

<a:avLst/>

</a:prstGeom>

</pic:spPr>

</pic:pic>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.13。

以下是一些更常见的效果。

## Alpha反转：

此效果通过从100%中减去来反转alpha（不透明度）值。该效果使用<a:alphaInv>元素指定。颜色被指定为子元素。颜色可以通过多种不同方式指定—作为预设颜色（<a:prstClr>），使用色相、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为RGB百分比或十六进制数（<a:scrgbClr>或<a:srgbClr>）。

<a:blip r:embed="rId4" cstate="print">

<a:alphaInv>

<a:srgbClr val="97E4FE"/>

</a:alphaInv>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.4。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![alpha反转](drwImages\effects9.gif)

## Alpha替换：

此效果指定一个新的固定不透明度值。该效果使用<a:alphaRepl>元素指定。a属性以百分比形式指定新的不透明度值。

<a:blip r:embed="rId4" cstate="print">

<a:alphaRepl a="25000"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.8。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![alpha替换](drwImages\effects10.gif)

## Alpha调制固定效果：

此效果为不透明度值指定一个固定的百分比乘数。该效果使用<a:alphaModFix>元素指定。amt属性指定百分比乘数。

<a:blip r:embed="rId4" cstate="print">

<a:alphaModFix a="15000"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.6。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![alpha调制固定效果](drwImages\effects11.gif)

## 黑白效果（双色调）：

如果输入的亮度小于指定的阈值，此效果会将颜色更改为黑色。否则颜色将更改为白色。该效果使用<a:biLevel>元素指定，thresh属性指定亮度的阈值。

<a:blip r:embed="rId4" cstate="print">

<a:biLevel thresh="75%"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.11。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![黑白效果](drwImages\effects3.gif)

## 模糊：

此效果使用<a:blur>元素指定模糊。grow属性指定对象的边界是否应因模糊而扩大。值为true或false。rad属性指定模糊的半径，以EMU为单位。

<a:blip r:embed="rId4" cstate="print">

<a:blur rad="20"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.15。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![模糊效果](drwImages\effects1.gif)

## 颜色更改：

此效果使用<a:clrChange>元素指定颜色更改。由<a:clrFrom>元素指定的颜色实例将被替换为由<a:clrTo>元素指定的颜色实例。可以使用以下颜色选项之一指定颜色：作为预设颜色（<a:prstClr>），使用色相、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为RGB百分比或十六进制数（<a:scrgbClr>或<a:srgbClr>）。

<a:blip r:embed="rId4" cstate="print">

<a:clrChange>

<a:clrFrom>

<a:srgbClr val="97E4FE"/>

</a:clrFrom>

<a:clrTo>

<a:srgbClr val="FF3399"/>

</a:clrTo>

</a:clrChange>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.16。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![颜色更改](drwImages\effects8.gif)

## 纯色替换：

此效果指定纯色替换值。所有效果颜色都将更改为固定颜色。Alpha值不受影响。该效果使用<a:clrRepl>元素指定。替换颜色可以使用多个不同的子元素之一指定：作为预设颜色（<a:prstClr>），使用色相、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为RGB百分比或十六进制数（<a:scrgbClr>或<a:srgbClr>）。

<a:blip r:embed="rId4" cstate="print">

<a:clrRepl>

<a:srgbClr val="FF3399"/>

</a:clrRepl>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.18。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![纯色替换](drwImages\effects7.gif)

## 双色调（为每个像素组合两种颜色）：

该效果使用<a:duotone>元素指定。要组合的颜色使用子元素指定。颜色可以通过多种不同方式指定—作为预设颜色（<a:prstClr>），使用色相、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为RGB百分比或十六进制数（<a:scrgbClr>或<a:srgbClr>）。

<a:blip r:embed="rId4" cstate="print">

<a:duotone>

<a:prstClr val="black"/>

<a:schemeClr val="accent3">

<a:tint val="45000"/>

<a:satMod val="400000"/>

</a:schemeClr>

</a:duotone>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.23。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![双色调](drwImages\effects2.gif)

## 灰度：

此效果将所有颜色值转换为对应其亮度的灰色阴影。不透明度不受影响。该效果使用<a:grayscl>元素指定。

<a:blip r:embed="rId4" cstate="print">

<a:grayscl/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.34。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![灰度](drwImages\effects4.gif)

## 亮度：

此效果指定亮度效果。该效果使用<a:lum>元素指定。亮度将所有颜色向白色或黑色靠近，而对比度则缩放所有颜色使其更接近或更远离。bright属性指定更改亮度的百分比，contrast属性指定更改对比度的百分比。

<a:blip r:embed="rId4" cstate="print">

<a:lum bright="65%" contrast="30%"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.42。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![亮度](drwImages\effects5.gif)

## 色调：

此效果指定色调效果。该效果使用<a:tint>元素指定。它按指定量将颜色值向/远离色相移动。amt属性指定颜色值移动的量，hue属性指定要着色的色相。范围从0到360度，以1/60000度为单位。

<a:blip r:embed="rId4" cstate="print">

<a:tint amt="50%" hue="3000000"/>

</a:blip>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.8.60。

Word 2007示例：

![无效果](drwImages\effects0.gif) ![色调](drwImages\effects6.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
