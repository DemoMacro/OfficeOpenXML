![PresentationXML.com](images\PresentationMLBanner.png)

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

# DrawingML 表格 - 单元格属性 - 边框和填充

表格单元格的边框和填充由表格单元格属性元素<a:tcPr>的子元素指定，该元素是<a:tc>元素的子元素。请记住，这是应用表格单元格直接格式化的方式。要将表格单元格样式应用于单元格，请参阅[DrawingML - 表格 - 样式](drwTableStyles.md)。

## 边框

单元格可以在四边有边框，加上两条对角线（从左下到右上和从左上到右下），总共可以有6种可能的边框，每种边框都由表格单元格属性元素的子元素指定。每个边框可以通过一组所有边框共有的属性和子元素进行进一步自定义。下面是一个示例表格，第一行的第二个单元格中有边框—一个橙色虚线顶部边框和一个从左上到右下的红色虚线边框。

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">

<a:solidFill>

<a:schemeClr val="accent6"/>

</a:solidFill>

<a:prstDash val="sysDash"/>

<a:round/>

<a:headEnd type="none" w="med" len="med"/>

<a:tailEnd type="none" w="med" len="med"/>

</a:lnT>

<a:lnTlToBr w="76200" cap="flat" cmpd="sng">

<a:solidFill>

<a:prstClr val="red"/>

</a:solidFill>

<a:prstDash val="sysDash"/>

<a:round/>

<a:headEnd type="none" w="med" len="med"/>

<a:tailEnd type="none" w="med" len="med"/>

</a:lnTlToBr>

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder1.gif)

六种可能边框的元素如下。

| 元素     | 描述                                                                                   |
| -------- | -------------------------------------------------------------------------------------- |
| lnB      | 指定底部边框线及其属性。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。     |
| lnBlToTr | 指定从左下到右上运行的线条。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。 |
| lnL      | 指定左边框。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。                 |
| lnR      | 指定右边框。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。                 |
| lnT      | 指定顶部边框。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。               |
| lnTlToBr | 指定从左上到右下运行的边框。请参阅下文，了解可以进一步指定线条属性的各种属性和子元素。 |

### 边框颜色、填充和粗细/厚度

边框线厚度通过线元素上的w属性指定。例如，<a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">。值以EMU（英制公制单位）为单位。

颜色和特殊线条填充的指定方式与drawingML其他区域中的方式相同。有关详细信息，请参阅[DrawingML - 形状 - 填充](http://www.officeopenxml.com/drwSp-shapeFill.md)。在上面的示例中，颜色通过纯色填充和预设颜色红色指定：<a:solidFill><a:prstClr val="red"/></a:solidFill>

### 边框线类型（虚线等）

虚线类型可以指定为预设类型或自定义类型。（此处不涉及自定义类型）。预设虚线类型通过<a:prstDash>元素指定，该元素具有一个指定线条类型的val属性。例如，<a:prstDash val="sysDash"/>。可能的预设值为：

- 虚线
- 点划线
- 点线
- lgDash（长虚线）
- lgDashDotDot
- sysDash（系统虚线）
- sysDashDot
- sysDashDotDot
- sysDot

边框线也可以是复合线。复合线的类型通过线元素上的cmpd属性指定。例如，<a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">。可能的值为：

- dbl（双线）
- sng（单线 - 默认值）
- thickThin
- thinThick
- tri（细粗细）

下面是一个示例顶部边框，具有双线和设置为dashDot的预设虚线：

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">

<a:solidFill>

<a:schemeClr val="accent6"/>

</a:solidFill>

<a:prstDash val="dashDot"/>

. . .

</a:lnT>

. . .

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder2.gif)

### 对齐

下划线或边框的对齐方式可以通过线元素上的algn属性指定。例如，<a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">。可能的值为ctr（指定线条位于路径描边的中心）和in（指定线条位于内侧边缘）。请注意，在上面的示例中，该值设置为ctr。如果我们将其设置为in，我们将得到如下所示的线条。

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder3.gif)

### 线条端点

线条端点也可以通过线元素的以下两个子元素指定：<a:headEnd>和<a:tailEnd>。这些元素可以具有指定端点类型（type）、长度（len）和宽度（w）的属性。长度和宽度的值可以是lg（大）、med（中）或sm（小），并且与线宽相关。类型可以具有以下值：

- 箭头
- 菱形
- 无
- 椭圆形
- stealth
- 三角形

下面是一个示例顶部边框，具有椭圆形头部端点和箭头尾部端点。

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">

. . .

<a:headEnd type="oval" w="med" len="med"/>

<a:tailEnd type="arrow" w="med" len="med"/>

</a:lnT>

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder4.gif)

每个线元素上还有一个cap属性，其值可以是flat、rnd（圆形端点）或sq（方形端点）。因此，没有指定头部或尾部端点元素的线条仍然可以通过应用其中一种cap类型来更改端点。例如，下面是一个具有圆形端点的顶部边框的单元格：<a:lnT w="76200" cap="rnd" cmpd="sng" algn="ctr">

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder5.gif)

线条连接处的连接点可以通过将<a:bevel/>、<a:miter/>或<a:round/>指定为线元素的子元素来自定义，以指定连接点应为斜角、尖角或圆角。例如，下面是指定为尖角的顶部、左侧和右侧边框的示例。

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder6.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
