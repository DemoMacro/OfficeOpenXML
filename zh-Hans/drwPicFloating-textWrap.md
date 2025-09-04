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
    - [2D 变换](drwSp-rotate.md)
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

# DrawingML 对象定位

在字处理文档中的定位 - 浮动图片 - 文本环绕

围绕锚定对象（<wp:anchor>）的文本环绕是通过五个与文本环绕相关的子元素之一来指定的。（注意，对于内联对象<wp:inline>，该对象只是成为行或文本运行内容的一部分，因此没有环绕的概念。）五个可能的子元素是：

- <wrapNone>
- <wrapSquare>
- <wrapThrough>
- <wrapTight>
- <wrapTopAndBottom>

## <wrapNone>

要指定不应执行文本环绕，将一个空的<wp:wrapNone/>元素放置在<wp:anchor>内。然后，文本根据<wp:anchor>元素的behindDoc属性值显示在图片的前面或后面。如果behindDoc为true，则文本在前面。如果behindDoc为false，则文本在后面。

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>right</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:wrapNone/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - None](drwImages\drw-textWrap-none.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.15。

## <wrapSquare>

要指定围绕对象的虚拟矩形的文本环绕，将<wp:wrapSquare>元素放置在<wp:anchor>内。虚拟矩形由父<wp:anchor>的<wp:effectExtent>元素指定，或者如果存在，则由子<wp:effectExtent>元素指定。

文本与对象各边的距离在<wp:wrapSquare>元素的属性中指定：distB（与对象底部的距离）、distL（与对象左边缘的距离）、distR（与对象右边缘的距离）和distT（与对象顶部的距离）。值以EMU（English Metric Units，英制公制单位）给出。还可以使用wrapText属性来指定文本应该环绕对象的哪一侧。可能的值是：

- bothSides（两侧）
- largest（文本环绕最大的一侧；如果对象居中，则文本环绕首先遇到文本的一侧）
- left（左侧）
- right（右侧）

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:wrapSquare wrapText="left" distT="360000" distB="360000" distL="360000" distR="0"/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - Square Wrapping](drwImages\drw-wrapSquare.gif)

下面是另一个示例，两侧都有环绕，但右侧的文本和对象之间没有距离。

<wp:wrapSquare wrapText="bothSides" distT="360000" distB="360000" distL="360000" distR="0"/>

![Text Wrapping - Square Wrapping](drwImages\drw-wrapSquare2.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.17。

## <wrapThrough>

使用<wrapThrough>，可以指定围绕对象或在对象内部的多边形形状，文本将围绕该多边形而不是围绕对象环绕。多边形通过<wrapThrough>的子元素<wrapPolygon>指定。<wp:wrapPolygon>元素本身首先通过使用子元素<wp:start>（以及指定x和y坐标的x和y属性，相对于对象的左上角）指定起点（和终点）来定义。还指定两个或多个<wp:lineTo>元素（具有相同的x和y属性）作为子元素来定义多边形的点。x和y属性可以是EMU，也可以是紧跟着单位标识符的数字（例如，2in）。<wp:wrapThrough>元素也可以具有distL（与对象左边缘的距离）和distR（与对象右边缘的距离）属性，如上面的<wp:wrapSquare>一样，以及wrapText属性。（注意，DrawingML的坐标系使用二维坐标，原点(0,0)在左上角。x轴从左到右正向增长，y轴从上到下正向增长。）

下面是一个以英寸为单位为对象定义矩形多边形的示例。

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="0" distR="0" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="0" t="0" r="0" b="0"/>

<wp:wrapThrough wrapText="bothSides">

<wp:wrapPolygon>

<wp:start>x="0in" y="0in"/>

<wp:lineTo>x="0in" y="-1in"/>

<wp:lineTo>x="1in" y="-1in"/>

<wp:lineTo>x="1in" y="0in"/>

<wp:lineTo>x="0in" y="0in"/>

</wp:wrapPolygon>

</wp:wrapThrough>

</wp:anchor>

</w:drawing>

![](images/note.png)注意：Microsoft Word 似乎不完全支持这种环绕功能。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.18。

## <wrapTight>

<wp:wrapTopAndBottom>与<wp:wrapThrough>非常相似。指定一个多边形，文本围绕该多边形环绕。但是，<wp:wrapTight>不允许文本出现在多边形最大和最小范围内的任何位置。下图描述了这种差异。

![Text Wrapping - Tight Wrapping](drwImages\drw-wrapTight.gif)

![](images/note.png)注意：Microsoft Word 似乎不完全支持这种环绕功能。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.19。

## <wrapTopAndBottom>

这种环绕指定文本应该围绕对象的顶部和底部环绕，而不是侧面。它可以具有distB（与对象底部的距离）和distT（与对象顶部的距离）属性，以指定文本与对象底部和顶部的距离。它还可以具有子元素<wp:effectExtent>，以添加到对象的范围中，以考虑效果。

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="0" distR="0" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="0" t="0" r="0" b="0"/>

<wp:wrapTopAndBottom/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - Top and Bottom](drwImages\drw-wrapTopAndBottom.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.20。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
