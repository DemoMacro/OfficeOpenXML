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
      - [组合填充](drwSp-grpFill.md)
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

# DrawingML 形状

3D 形状属性

3D 属性在容器 <a:sp3d> 元素中指定，该元素位于 <a:spPr>（形状属性）元素内。有三种可能的 3D 属性—顶部和底部斜角、轮廓和挤压—它们被指定为子元素或作为 <a:sp3d> 的子元素和属性的组合。下面是一个带有顶部斜角和模糊轮廓的形状。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

. . .

</a:xfrm>

<a:prstGeom>

. . .

</a:prstGeom>

<a:solidFill>

. . .

</a:solidFill>

<a:scene3d>

. . .

</a:scene3d>

<a:sp3d contourW="40000" prstMaterial="metal">

<a:bevelT w="165100" prst="coolSlant"/>

<a:contourClr>

<a:prstClr val="blue"/>

</a:contourClr>

</a:sp3d>

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-3D.gif)

除了与轮廓和挤压相关的属性外，还有两个属性影响形状的 3D 属性。它们是 prstMaterial 和 z。prstMaterial 属性指定预设材质类型，这是旨在模仿材质的光照特性的组合。可能的值是：

- 透明
- 暗边缘
- 平面
- 传统哑光
- 传统金属
- 传统塑料
- 传统线框
- 哑光
- 金属
- 塑料
- 粉末
- 柔和边缘
- 柔和金属
  半透明粉末

- 暖色哑光

下面是上面显示的相同形状，只是 prstMaterial 属性已设置为 powder 而不是 metal。

z 属性定义 3D 形状的 z 坐标。它是一个简单的坐标，以 EMU 为单位指定，或者是一个数字后紧跟单位标识符。

![Shape size](drwImages\drwSp-3D-prstMaterial.gif)

## 斜角

底部和顶部斜角分别用 <a:bevelB> 和 <a:bevelT> 指定。两个斜角元素都是空元素，具有三个定义斜角特征的属性。prst 属性指定定义斜角外观的预设斜角类型。可能的值是：

- 角度
- 装饰艺术
- 圆形
- 凸面
- 冷斜角
- 十字
- 小凹痕
- 硬边缘
- 松散嵌入
- 小棱纹
- 斜坡
- 柔和圆形

h 属性指定斜角的高度（以 EMU 为单位）或应用于形状上方的距离。w 属性指定斜角的宽度，或应用于形状内部的距离。下面是一个带有顶部和底部斜角的示例形状。底部斜角是 coolSlant 类型，宽度为 13 点，高度为 10 点。顶部斜角是 softRound 类型，宽度为 12 点，高度为 10 点。

<a:bevelT w="152400" h="127000" prst="softRound"/>

<a:bevelB w="165100" h="127000" prst="coolSlant"/>

![Shape size](drwImages\drwSp-3D-bevel.gif)

## 轮廓

轮廓是围绕形状外边缘的实心填充线。轮廓的颜色指定为 <a:sp3d> 元素的子元素 <a:contourClr>。颜色指定为 <a:contourClr> 的子元素，使用以下颜色选项之一：作为预设颜色（<a:prstClr>），使用色相、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为 RGB 百分比或十六进制数字（<a:scrgbClr> 或 <a:srgbClr>）。请注意，这些对应于颜色规范方法的元素也可以具有转换基础颜色的子元素。因此，例如，方案或主题颜色可以指定为 accent6，但也可以对该基础颜色应用亮度调制。此处不详细讨论颜色。

轮廓的宽度（以 EMU 为单位）通过 <a:sp3d> 元素上的 contourW 属性指定。下面是一个带有 5 点浅蓝色轮廓的形状。请注意，通过设置轮廓形状属性可以实现相同的效果。参见[形状轮廓](drwSp-outline.md)。

<a:sp3d contourW="63500">

<a:contourClr>

<a:srgbClr val="00B0F0"/>

</a:contourClr>

</a:sp3d>

![Shape size](drwImages\drwSp-3D-contour.gif)

## 挤压

挤压是应用于形状的人工高度。挤压的颜色指定为 <a:sp3d> 元素的子元素 <a:extrusionClr>。颜色指定为 <a:extrusionClr> 的子元素，使用与轮廓颜色相同的颜色元素。参见上文。挤压的高度（以 EMU 为单位）通过 <a:sp3d> 元素上的 extrusionH 属性指定。下面是一个带有 20 点红色挤压的形状。

<a:sp3d extrusionH="254000">

<a:extrusionClr>

<a:srgbClr val="FF0000"/>

</a:extrusionClr>

</a:sp3d>

![Shape size](drwImages\drwSp-3D-extrusion.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
