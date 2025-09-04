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

# DrawingML形状

自定义几何

由几乎任何一系列线条和曲线组成的自定义几何形状可以用<a:custGeom>元素指定。<a:custGeom>最重要的组成部分是形状所采用路径的规范。这是通过子元素<a:pathLst>指定的。但是，自定义形状还有其他可以指定的可选组件。形状调整手柄的位置可以通过子元素<a:ahLst>指定（此处不涉及）。连接点（对象上可以放置线条或连接器的位置）的位置可以通过子元素<a:cxnLst>指定。形状内文本的矩形边界框可以通过子元素<a:rect>指定。最后，形状的边缘可以基于公式而不是静态放置来动态确定或调整。这是使用调整值（<a:avLst>）和形状指南（<a:gdLst>）完成的。自定义几何的这方面在此处不涉及。

## 定义形状的路径

形状由包含在<a:pathLst>元素中的一个或多个路径指定。每个路径是包含在<a:path>子元素中的一组移动、线条和弧线。本质上，每个路径可以被视为一个单独的形状。前一个路径的终点将连接到新路径的第一个点，除非前一个路径指定了<a:close>元素。请注意，由于允许多个路径，后面的路径会绘制在前面的路径之上。

路径具有由<a:path>元素的高度（h）和宽度（w）属性指定的空间。然后，路径使用在路径空间内使用x-y坐标定义的点（由<a:pt>元素表示）来指定。注意图像中所示的坐标系。![自定义形状中点的坐标系](drwImages\drwSp-coordinateSystem.gif) <a:pt>具有定义点坐标的x和y属性。确保不要将形状坐标系与路径坐标系混淆；它们是不同的。形状坐标系或形状边界框由<a:xfrm>元素内的<a:ext>定义，并以EMU（English Metric Units，英制公制单位）指定。路径坐标系由<a:path>元素的h和w属性定义，可能不是以EMU为单位。路径点是相对于路径坐标系定义的。

如上所述，路径是通过绘制一系列线条（<a:lnTo>）、弧线（<a:arcTo>）、三次贝塞尔曲线（<a:cubicBezTo>）和二次贝塞尔曲线（<a:quadBezTo>）来定义的。线条和曲线的绘制可以通过移动到新坐标并从新位置绘制来中断；这是通过<a:moveTo>元素指定的。刚才提到的每个元素都有一个、两个或三个<a:pt>子元素。

<a:path>具有以下元素。

| 元素       | 描述                                                                                                                                                                                                                                                                                                                  |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| arcTo      | 一个空元素，指定从当前笔位置到新点的弧线。弧线是基于假想圆的形状弯曲的线条。长度由起始角度和结束角度决定。arcTo元素有四个可能的属性来定义弧线：hR（以EMU为单位的半径高度或紧跟着单位标识符的数字）、stAng（以六万分之一度为单位的起始角度；正值表示顺时针）、swAng（摆动角度）和wR（宽度半径）。                      |
| close      | 一个空元素，指定一系列线条和曲线的结束，并向应用程序发出信号，表示路径已关闭，任何进一步的线条或曲线都应被忽略。当最后一个点与路径中的第一个点不重合时，应用程序应将最后一个点与第一个点用直线连接，以创建一个闭合形状。<a:close>还意味着后续路径（如果有）将不会连接到前一个路径。如果路径未闭合，则形状将没有填充。 |
| cubicBezTo | 指定沿着指定点绘制三次贝塞尔曲线。必须指定三个子<a:pt>点。前两个是用于三次贝塞尔计算的控制点，最后一个是结束点。                                                                                                                                                                                                      |
| lnTo       | 指定绘制一条直线。它包含一个子<a:pt>元素。                                                                                                                                                                                                                                                                            |
| moveTo     | 指定一组坐标，将形状光标移动到该位置。它不绘制线条或曲线；它只是将光标移动到新位置。它包含一个子<a:pt>元素。                                                                                                                                                                                                          |
| quadBezTo  | 指定沿着指定点绘制二次贝塞尔曲线。必须有两个子<a:pt>点元素。                                                                                                                                                                                                                                                          |

<a:path>具有以下属性。

| 属性        | 描述                                                                                                                                                                                                                                |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| extrusionOk | 指定允许3D拉伸。如果省略，则假定值为false。                                                                                                                                                                                         |
| fill        | 指定相应路径应如何填充。可能的值为darken（变暗）、darkenLess（轻微变暗）、lighten（变亮）、darkenLess（轻微变暗）、none（无）和normal（正常）（如果省略该属性，则假定为normal）。请参阅下面的两个路径示例。第二个路径的填充已变暗。 |
| h           | 指定应使用的高度或最大y坐标。它确定路径中所有点的垂直位置，因为它们都是使用此属性作为最大y坐标计算的。                                                                                                                              |
| stroke      | 指定相应路径是否应显示路径描边。如果省略，则假定值为true。                                                                                                                                                                          |
| w           | 指定应使用的宽度或最大z坐标。它确定路径中所有点的水平位置，因为它们都是使用此属性作为最大x坐标计算的。                                                                                                                              |

下面是一个具有一条路径的自定义几何形状的示例。首先，光标按照<a:moveTo>元素的指定移动到新坐标(0,428263)。然后绘制一系列三条线。在示例中，指定了<a:close>元素，向应用程序发出信号，表示路径已关闭，任何进一步的线条或曲线都应被忽略。当最后一个点与路径中的第一个点不重合时，应用程序应将最后一个点与第一个点用直线连接，以创建一个闭合形状。<a:close>还意味着后续路径（如果有）将不会连接到前一个路径。如果路径未闭合，则形状将没有填充。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1238250" y="504825"/>

<a:ext cx="1685925" cy="638175"/>

</a:xfrm>

<a:custGeom>

<a:pathLst>

<a:path w="2824222" h="590309">

<a:moveTo>

<a:pt x="0" y="428263"/>

</a:moveTo>

<a:lnTo>

<a:pt x="1620455" y="590309"/>

</a:lnTo>

<a:lnTo>

<a:pt x="2824222" y="173620"/>

</a:lnTo>

<a:lnTo>

<a:pt x="1562582" y="0"/>

</a:lnTo>

<a:close/>

</a:path>

</a:pathLst/>

</a:custGeom>

<a:solidFill>

<a:schemeClr val="accent6"/>

<a:lumMod val="75000"/>

</a:schemeClr>

</a:solidFill>

</xdr:spPr>

. . .

</xdr:sp>

![Shape with custom geometry](drwImages\drwSp-custGeom-onePath.gif)

下面是相同的形状，只是初始的<a:moveTo>已被移除，因此绘图从原点开始。

![Shape with custom geometry - from origin](drwImages\drwSp-custGeom-onePath-fromOrig.gif)

下面是自定义形状的另一个示例。这次有两条路径。第一条与上面显示的第一条路径相同。它是闭合的，因此该路径和后续路径不连接。第二条路径使用fill="darken"属性变暗。首先，光标移动到(1000000,334000)；然后路径绘制两条线。然后它再次移动，这次是到(500000,500000)。最后，它绘制另一条线并闭合。

<a:pathLst>

<a:path w="2824222" h="590309">

<a:moveTo>

<a:pt x="0" y="428263"/>

</a:moveTo>

<a:lnTo>

<a:pt x="1620455" y="590309"/>

</a:lnTo>

<a:lnTo>

<a:pt x="2824222" y="173620"/>

</a:lnTo>

<a:lnTo>

<a:pt x="1562582" y="0"/>

</a:lnTo>

<a:close/>

</a:path>

</a:pathLst/>

<a:path fill="darken" w="2824222" h="590309">

<a:moveTo>

<a:pt x="1000000" y="334000"/>

</a:moveTo>

<a:lnTo>

<a:pt x="2900455" y="400000"/>

</a:lnTo>

<a:lnTo>

<a:pt x="900222" y="50000"/>

</a:lnTo>

<a:moveTo>

<a:pt x="500000" y="500000"/>

</a:moveTo>

<a:lnTo>

<a:pt x="1500000" y="0"/>

</a:lnTo>

<a:close/>

</a:path>

</a:pathLst/>

![Shape with custom geometry - two paths](drwImages\drwSp-custGeom-twoPaths.gif)

## 定义形状的连接点

形状可以有连接点，连接器可以附加到这些点，以便在形状重新定位时保持连接。每个连接点用<a:cxn>元素指定。所有<a:cxn>元素都在容器<a:cxnLst>父元素内。每个连接点通过子元素<a:pos>定位，该元素通过其x和y属性指定坐标。应该注意的是，连接是使用包含整个形状的形状坐标系放置在边界框内的，该坐标系由<a:ext>元素指定。<a:pos>元素还有一个ang属性，指定传入连接器的角度。这允许连接器知道形状相对于连接点的位置，并路由连接器以避免放置在形状上。下面是位于形状中间的连接点的示例。

<a:custGeom>

<a:cxnLst>

<a:cxn ang="0">

<a:pos x="1000000" y="300000"/>

</a:cxn>

</a:cxnLst>

<a:pathLst>

<a:path w="2824222" h="590309">

<a:path w="2824222" h="590309">

<a:moveTo>

<a:pt x="0" y="428263"/>

</a:moveTo>

<a:lnTo>

<a:pt x="1620455" y="590309"/>

</a:lnTo>

<a:lnTo>

<a:pt x="2824222" y="173620"/>

</a:lnTo>

<a:lnTo>

<a:pt x="1562582" y="0"/>

</a:lnTo>

<a:close/>

</a:path>

</a:pathLst/>

</a:custGeom>

![Shape with custom geometry - two paths](drwImages\drwSp-custGeom-cxn.gif)

下面是附加两个连接器的示例—一个在形状中间的指定连接点处，一个不在连接点处。右侧的图像是相同的形状，但它已被重新定位。连接点处的连接器与形状一起保持，而另一个连接器则没有保持。

![Shape with custom geometry - two paths](drwImages\drwSp-custGeom-cxn-beforeMove.gif)

![Shape with custom geometry - two paths](drwImages\drwSp-custGeom-cxn-afterMove.gif)

## 定义形状的文本边界框

默认情况下，自定义形状内的文本放置在形状的边界框内。但是，这可以通过<a:rect>元素修改，该元素具有内缩或扩展文本边界框的属性。这些属性是b（底边的y坐标）、l（左边的x坐标）、r（右边的x坐标）和t（顶边的y坐标）。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
