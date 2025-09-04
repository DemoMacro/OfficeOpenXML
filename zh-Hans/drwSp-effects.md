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
    - [文本主体属性](drwSp-text-bodyPr.md)
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

# DrawingML 形状

效果

效果在<a:spPr>（形状属性）元素内的容器<a:effectLst>元素中指定。一个或多个效果可以指定为<a:effectLst>的子元素，效果由渲染引擎或文字处理器按默认顺序应用。可能的效果包括模糊、填充叠加、发光、内阴影、外阴影、预设阴影、反射和柔边。下面是一个应用了发光和反射效果的三角形形状的示例。

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

<a:effectLst>

<a:glow rad="101600">

<a:schemeClr val="accent6">

<a:satMode val="175000"/>

<a:alpha val="40000"/>

</a:schemeClr>

</a:glow>

<a:reflection blurRad="6350" stA="50000" endA="300" endPos="38500" dist="50800" dir="5400000" sy="-100000" algn="bl" rotWithShape="0"/>

</a:effectLst>

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-effects1.gif)

## 模糊

模糊效果通过空元素<a:blur>应用于形状。模糊效果的特征由两个属性指定。grow属性指定模糊效果是否应扩展到形状的原始边界之外。值为true表示模糊效果扩展到边界之外，值为false则不扩展。rad属性指定模糊的程度（或模糊的半径）。它以EMU（英制公制单位）指定。下面是一个三角形示例，其模糊效果应用于形状边界之外，半径为100,000 EMU。

<a:effectLst>

<a:blur grow="1" rad="100000"/>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-blur.gif)

## 填充叠加

可以为形状指定两种填充。第一种指定为<SpPr>的子元素。参见[形状填充](dwrSp-shapeFill.md)。然后可以通过在<a:effectLst>元素内指定<a:fillOverlay>作为效果，在第一种填充类型之上指定叠加填充。<a:fillOverlay>可以包含与对象主填充相同的填充类型：

- Blip填充（BLIP = 二进制大图像或图片）。参见[图片填充](drwSp-PictFill.md)。
- 渐变填充。参见[渐变填充](drwSp-GradFill.md)。
- 组填充。
- 无填充，由空元素<noFill/>指定。
- 图案填充。参见[图案填充](drwSp-PattFill.md)。
- 纯色填充。参见[纯色填充](drwSp-SolidFill.md)。

<a:fillOverlay>元素还有一个blend属性，用于指定如何混合填充。可能的值有：

- 变暗
- 变亮
- 正片叠底
- 覆盖
- 滤色

下面是一个示例，它有一个基础blip填充，叠加填充是点网格图案的图案叠加，前景为白色，背景为红色。混合值为覆盖。

<a:effectLst>

<a:fillOverlay blend="over">

<a:pattFill prst="dotGrid">

<a:fgClr>

<a:prstClr val="white"/>

</a:fgClr>

<a:bgClr>

<a:prstClr val="red"/>

</a:bgClr>

</a:pattFill>

</a:fillOverlay>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-fillOverlay.gif)

下面是相同的叠加效果，但混合值为正片叠底。

![Shape size](drwImages\drwSp-effects-fillOverlay2.gif)

## 发光

发光效果在形状外部添加一个颜色模糊的轮廓。它通过<a:glow>元素指定。轮廓的颜色通过子元素使用以下颜色选项之一指定：作为预设颜色(<a:prstClr>)，使用色相、饱和度和亮度(<a:hslClr>)，方案颜色(<a:schemeClr>)，系统颜色(<a:sysClr>)，或作为RGB百分比或十六进制数(<a:scrgbClr>或<a:srgbClr>)。模糊的量或半径由<a:glow>元素上的rad属性（以EMU为单位）指定。下面是一个蓝色轮廓颜色和半径为1000000 EMU的示例。

<a:effectLst>

<a:glow rad="100000">

<a:prstClr val="blue"/>

</a:glow>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-glow.gif)

## 内阴影

内阴影应用于形状边缘内部，并通过<a:innerShdw>元素指定。阴影的颜色通过子元素使用与上述发光部分中所述相同的可能颜色元素指定。阴影的其他特征由三个属性指定：blurRad，指定模糊的半径（以EMU为单位）；dir，指定偏移阴影的方向（以1/60000度为单位）；dist，指定偏移阴影的距离。下面是一个三角形形状的示例，具有150度的红色内阴影，模糊因子为15磅，距离为10磅。

<a:effectLst>

<a:innerShdw blurRad="190500" dist="127000" dir="9000000">

<a:srgbClr val="FF0000">

<a:alpha val="50000"/>

</a:srgbClr>

</a:innerShdw>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-innerShadow.gif)

## 外阴影

外阴影应用于形状边缘之外，并通过<a:outerShdw>元素指定。阴影的颜色通过子元素使用与上述发光部分中所述相同的可能颜色元素指定。阴影的其他特征由几个属性指定：

- algn，指定阴影对齐方式。可能的值有b（底部）、bl（左下）、br（右下）、ctr（中心）、l（左）、r（右）、t（顶部）、tl（左上）和tr（右上）。
- blurRad，指定模糊的半径（以EMU为单位）
- dir，指定偏移阴影的方向（以1/60000度为单位）
- dist，指定偏移阴影的距离
- kx，指定水平倾斜角度（以1/60000度为单位）
- ky，指定垂直倾斜角度（以1/60000度为单位）
- rotWithShape，指定如果形状旋转，阴影是否随形状一起旋转
- sx，指定水平缩放因子（以百分比表示）。负缩放会导致翻转。
- sy，指定垂直缩放因子（以百分比表示）。负缩放会导致翻转。

下面是一个三角形形状的示例，具有0度的浅蓝色外阴影，模糊因子为27磅，距离为10磅。

<a:effectLst>

<a:outerShdw blurRad="342900" dist="127000" algn="bl" rotWithShape="0">

<a:srgbClr val="0070C0">

<a:alpha val="51000"/>

</a:srgbClr>

</a:outerShdw>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-outerShadow.gif)

## 预设阴影

预设阴影是具有预定特征集的外阴影；它通过<a:prstShdw>元素指定。预设阴影的类型通过prst属性指定。可能的值是shdw1到shdw20。有关每个示例，请参阅ECMA-376第3版（2011年6月），基础和标记语言参考§20.1.10.51。请注意，虽然某些特征是预设的，但其他特征可以指定。与其他阴影一样，颜色指定为子元素。有关颜色子元素的详细信息，请参见上面讨论的其他阴影效果。除了颜色外，还可以指定dir和dist属性。再次，请参阅其他阴影效果以了解详细信息。请注意，对于预设阴影，rotWithShape始终为false。下面是一个示例预设黑色阴影效果。

<a:effectLst>

<a:prstShdw dist="38100" dir="18900000" prst="shdw1">

<a:prstClr val="black">

<a:alpha val="40000"/>

</a:prstClr>

</a:prstShdw>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-prstShadow.gif)

## 反射

反射效果通过<a:reflection>元素（一个空元素）指定。反射的特征由几个属性给出：

- algn，指定阴影对齐方式。可能的值有b（底部）、bl（左下）、br（右下）、ctr（中心）、l（左）、r（右）、t（顶部）、tl（左上）和tr（右上）。
- blurRad，指定模糊的半径（以EMU为单位）
- dir，指定偏移阴影的方向（以1/60000度为单位）
- dist，指定偏移阴影的距离
- endA，指定结束反射不透明度，以百分比表示
- endPos，指定结束alpha值的结束位置，以百分比表示。
- fadeDir，指定偏移反射的方向（以1/60000度为单位）
- kx，指定水平倾斜角度（以1/60000度为单位）
- ky，指定垂直倾斜角度（以1/60000度为单位）
- rotWithShape，指定如果形状旋转，阴影是否随形状一起旋转
- stA，指定起始反射不透明度，以百分比表示
- stPos，指定起始alpha值的起始位置，以百分比表示。
- sx，指定水平缩放因子（以百分比表示）。负缩放会导致翻转。
- sy，指定垂直缩放因子（以百分比表示）。负缩放会导致翻转。

下面是一个示例反射，对齐在左下角，垂直翻转，起始不透明度为50%。

<a:effectLst>

<a:reflection blurRad="6350" stA="50000" endA="300" endPos="90000" dir="5400000" sy="-100000" algn="bl" rotWithShape="0"/>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-reflection.gif)

## 柔边

可以指定柔边，使形状的边缘模糊但填充不受影响。柔边通过<a:softEdge>元素（一个空元素）指定。边缘模糊的半径通过rad属性（以EMU为单位）指定。下面是一个模糊为10磅的三角形形状。

<a:effectLst>

<a:softEdge rad="127000"/>

</a:effectLst>

![Shape size](drwImages\drwSp-effects-softEdge.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
