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
    - [2D 变换](drwSp-rotate.md)
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

渐变填充

渐变填充指定从一种颜色到下一种颜色的平滑、渐进过渡。它使用 <a:gradFill> 元素指定。在其最简单的形式中，它在两种颜色之间过渡。但是，它可以在任意数量的颜色之间过渡。过渡有三个基本属性：(1) 颜色，(2) 位置，和 (3) 着色样式。颜色和位置在 <a:gsLst> 或渐变停止列表中定义，该列表在其子元素中定义过渡颜色和位置。着色样式定义为 <a:gradFill> 的单独子元素：<a:lin/>（线性）或 <a:path>（路径）。最后，渐变填充可以选择性地指定形状的矩形区域，渐变应用于该区域，该区域平铺在形状的其余部分。这是使用 <a:tileRect> 元素指定的。

<a:gradFill>

<a:gsLst>

<a:gs pos="0">

<a:schemeClr val="accent1">

<a:tint val="66000"/>

<a:satMod val="160000"/>

</a:schemeClr>

</a:gs>

<a:gs pos="50000">

<a:schemeClr val="accent1">

<a:tint val="44500"/>

<a:satMod val="160000"/>

</a:schemeClr>

</a:gs>

<a:gs pos="100000">

<a:schemeClr val="accent1">

<a:tint val="23500"/>

<a:satMod val="160000"/>

</a:schemeClr>

</a:gs>

</a:gsLst>

<a:lin ang="5400000" scaled="0"/>

</a:gradFill>

![Shape with gradient fill in spreadsheet](drwImages\drwSp-gradientFill.gif)

### 元素：

<a:gradFill> 具有以下元素。

| 元素     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gsLst    | 指定渐变停止列表，它是一组 <a:gs> 或渐变停止元素。这些定义了渐变颜色和颜色带中的相对位置。每个 <a:gs> 元素包含一个指定颜色的子元素。可以使用以下颜色选项之一指定颜色：作为预设颜色 (<a:prstClr>)，使用色相、饱和度和亮度 (<a:hslClr>)，方案颜色 (<a:schemeClr>)，系统颜色 (<a:sysClr>)，或作为 RGB 百分比或十六进制数 (<a:scrgbClr> 或 <a:srgbClr>)。请注意，这些对应于颜色指定方法的元素也可以具有转换基本颜色的子元素。因此，例如，在下面的示例中，方案或主题颜色指定为 accent6，但对该基本颜色应用了亮度调制。每个 <a:gs> 元素都有一个属性 pos，它指定停止点应出现的位置。该值是一个百分比，对应于停止点应沿颜色带的位置。下面是一个具有四个渐变停止点的示例，一个使用主题颜色，其他使用 RGB 值指定。<a:gradFill> <a:gsLst> <a:gs pos="40000"> <a:schemeClr val="accent6"> <a:lumMod val="75000"/> </a:schemeClr> </a:gs> <a:gs pos="39999"> <a:srgbClr val="85C2FF"/> </a:gs> <a:gs pos="70000"> <a:srgbClr val="C4D6EB"/> </a:gs> <a:gs pos="100000"> <a:srgbClr val="FFEBFA"/> </a:schemeClr> </a:gs> </a:gsLst> <a:lin ang="16200000" scaled="1"/> </a:gradFill> ![具有四个渐变停止点的形状](drwImages\drwSp-gradientFill-gsLst.gif) |
| lin      | 指定线性渐变。它包含两个属性。首先，ang，指定渐变的方向（顺时针），以度为单位，范围从 0 到 360。但是，值以度的 60000 分之一给出。其次，scaled 指定角度是否随填充区域缩放。值是布尔值。下面是一个 90 度角的线性渐变示例。<a:lin ang="5400000" scaled="0"/> ![具有线性渐变填充的形状](drwImages\drwSp-gradientFill-lin.gif)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| path     | 指定渐变填充应遵循指定路径而不是线性路径。它有一个属性 path，指定要遵循的路径。可能的值是 circle、rect 和 shape（渐变应遵循形状）。<a:path> 元素还包含一个子元素 <a:fillToRect>，它定义了相对于填充平铺矩形的中心着色的焦点矩形。着色将填充整个平铺，但可以通过属性指定边距。属性是 b（底部）、l（左侧）、r（右侧）和 t（顶部）；值是百分比，正值表示内边距，负值表示偏移。下面是一个遵循形状路径的示例。<a:path path="shape"> <a:fillToRect l="50000" t="50000" r="50000" b="0"/> </a:path> ![具有形状路径中渐变填充的形状](drwImages\drwSp-gradientFill-pathShape.gif) 下面是一个遵循圆形路径的示例。![具有形状路径中渐变填充的形状](drwImages\drwSp-gradientFill-pathCircle.gif)                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| tileRect | 一个空元素，指定形状的矩形区域，渐变应用于该区域。该区域平铺在形状的剩余区域以完成填充。矩形通过从形状边界框的边的百分比偏移量指定。正数指定内边距（边界框的右侧），负数指定外边距或偏移量。四个边的偏移量使用以下四个属性指定，其值为百分比：b（底部）、l（左侧）、r（右侧）和 t（顶部）。下面是一个从底部 75% 内边距的示例：<a:tileRect b="75000"/>。![具有渐变填充和 50% 偏移的 tileRect 的形状](drwImages\drwSp-gradientFill-tileRect.gif)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

<gradFill> 可以具有以下属性。

| 属性         | 描述                                                                                                                                                                                                                                                                                |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| flip         | 指定在平铺时翻转渐变的方向。这仅在指定了 tileRect 时才相关，因此渐变必须平铺以填充形状。可能的值是 none、x（水平）、xy（水平和垂直）和 y（垂直）。                                                                                                                                  |
| rotWithShape | 指定填充是否在形状旋转时随形状一起旋转。下面是一个带旋转的示例 (rotWithShape="1")。![具有渐变填充的形状 - 随形状旋转](drwImages\drwSp-gradientFill-Rot.gif) 这是一个不带旋转的示例 (rotWithShape="0")。![具有渐变填充的形状 - 不随形状旋转](drwImages\drwSp-gradientFill-NoRot.gif) |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
