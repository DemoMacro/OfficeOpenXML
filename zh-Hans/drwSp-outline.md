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

轮廓

形状轮廓的样式使用<a:ln>元素指定。由此元素确定的属性包括轮廓的大小或粗细、颜色、填充类型和连接器端点。（线条连接处的接头样式也由此元素确定，但此处不涉及。）

下面是两个形状（圆角矩形和线条）的示例，每个形状具有不同的轮廓属性。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1066800" y="514350"/>

<a:ext cx="1504950" cy="800100"/>

</a:xfrm>

<a:prstGeom prst="roundRect">

<a:avLst/>

</a:prstGeom>

<a:solidFill>

<a:schemeClr val="accent6">

<a:lumMod val="75000"/>

</a:schemeClr>

</a:solidFill>

<a:ln w="50800" cap="rnd" cmpd="dbl">

<a:solidFill>

<a:srgbClr val="FFFF00"/>

</a:solidFill>

</a:ln>

</xdr:spPr>

. . .

</xdr:sp>

<xdr:cxnSp macro="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="790575" y="1438275"/>

<a:ext cx="1847850" cy="266700"/>

</a:xfrm>

<a:prstGeom prst="line">

<a:avLst/>

</a:prstGeom>

<a:ln w="57150" cap="rnd">

<a:solidFill>

<a:srgbClr val="00B0F0"/>

</a:solidFill>

<a:round/>

<a:headEnd type="oval" w="sm" len="sm"/>

<a:tailEnd type="triangle" w="lg" len="lg"/>

</a:ln>

</xdr:spPr>

</xdr:cxnSp>

![Two shapes with various line properties](drwImages\drwSp-outline1.gif)

## 轮廓的粗细或大小

线条的粗细由<a:ln>元素的w属性指定。值以EMU（英制公制单位）为单位。1pt = 12700 EMU。如果省略该属性，则假定为0。上面示例中的线条宽度为4.5磅，或w="57150"。

## 单线或复合线

轮廓的线型由<a:ln>元素的cmpd属性指定。可能的值有dbl（双线）、sng（单线）、thickThin（双线；一条粗，一条细）、thinThick（双线；一条细，一条粗）、tri（三条线；细、粗、细）。如果省略该属性，默认为sng。上面的矩形有双线：cmpd="dbl"。

## 虚线模式

可以使用<a:ln>内的空<a:prstDash>元素指定预设虚线模式。虚线的样式由<a:prstDash>元素的val属性指定。可能的值有：

- 虚线
- 点划线
- 点线
- 长虚线（大虚线）
- 长点划线
- 长双点划线
- 实线
- 系统虚线
- 系统点划线
- 系统双点划线
- 系统点线

如果我们给上面的矩形添加虚线，会得到以下结果：

<a:ln w="50800" cap="rnd" cmpd="dbl">

<a:solidFill>

<a:srgbClr val="FFFF00"/>

</a:solidFill>

<a:prstDash val="dash"/>

</a:ln>

![Two shapes with dashed line](drwImages\drwSp-outlineDash.gif)

也可以使用<a:custDash>元素指定自定义虚线模式。此元素包含虚线停止元素（<a:ds>）的列表，这些元素是虚线方案的构建块。每个<a:ds>元素都有一个d属性，表示虚线相对于线宽的长度（以百分比表示），以及一个sp属性，表示相对于线宽的间距（也以百分比表示）。

## 填充类型

线条的填充类型由<a:ln>元素的子元素指定。可能的填充类型包括形状本身可用的大多数填充类型：[纯色](dwrSp-SolidFill.md) (<a:solidFill>)、[图案](dwrSp-PattFill.md) (<a:pattFill>)、[渐变](dwrSp-GradFill.md) (<a:gradFill>)或[无](drwSp-shapeFill.md) (<a:noFill>)。（没有图片或组填充。）它们使用与形状填充相同的子元素指定，因此此处不详细讨论。相反，请参考上面链接中的相应形状填充。下面是上面矩形轮廓的示例图案填充。

<a:ln w="50800" cap="rnd" cmpd="dbl">

<a:pattFill>

<a:fgClr>

<a:prstClr val="gray"/>

</a:fgClr>

<a:bgClr>

<a:prstClr val="blue"/>

</a:bgClr>

</a:pattFill>

<a:prstDash val="dash"/>

</a:ln>

![Rectangle with pattern outline fill](drwImages\drwSp-outline-PattFill.gif)

## 线条首端和末端样式

可以使用<a:headEnd>和<a:tailEnd>元素在线条的首端和末端添加"装饰"。这些元素中的每一个都是空元素，具有三个属性，用于指定首端或末端的特征。

len属性指定首端或末端相对于线宽的长度。可能的值有lg（大）、med（中）和sm（小）。

type属性指定装饰。可能的值有arrow（箭头）、diamond（菱形）、none（无）、oval（椭圆形）、stealth（隐形箭头）和triangle（三角形）。

w属性指定线条首端或末端相对于线宽的宽度。可能的值与len属性的值相同。

下面是一个线条的示例，该线条具有中等大小和大长度的隐形箭头首端，以及小宽度和大长度的菱形末端。

<a:headEnd type="stealth" w="med" len="lg"/>

<a:tailEnd type="diamond" w="sm" len="lg"/>

![Rectangle with pattern outline fill](drwImages\drwSp-outline-ends.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
