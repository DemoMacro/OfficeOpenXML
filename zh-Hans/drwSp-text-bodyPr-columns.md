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

文本 - 正文属性 - 列、垂直文本和旋转

## 列：

形状内文本的列可以通过在<a:bodyPr>上添加numCols属性来指定。该值表示列数。应用列时，边界框的宽度除以列数。然后这些列被视为溢出容器—当前一列填满时，文本会流向下一列。当所有列都已填满时，将使用溢出属性。请参阅[形状 - 文本 - 适应、环绕、弯曲和3D](drwSp-text-bodyPr-fit.md)中的文本适应。

下面是一个具有三列的形状示例(<a:bodyPr anchor="ctr" numCols="3"/>)。

![Shape with text - anchoring](drwImages\drwSp-text-col1.gif)

要将列顺序更改为从右到左的顺序，请添加rtlCol属性(<a:bodyPr anchor="ctr" numCols="3" rtlCol="1" />)。如果省略此属性，则假定为false值。

![Shape with text - anchoring](drwImages\drwSp-text-col2.gif)

列之间的间距可以使用spcCol属性指定。该值以EMU为单位。下面是与上面相同的形状，但列之间有半英寸的间距(<a:bodyPr anchor="ctr" numCols="3" rtlCol="1" spcCol="457200"/>)。

![Shape with text - anchoring](drwImages\drwSp-text-col3.gif)

## 垂直文本：

形状内的文本可以通过在<a:bodyPr>上指定vert属性来垂直显示。此属性的可能值是：

- eaVert (东亚垂直)
- horz (水平—默认值)
- mongolianVert (某些字体显示为旋转90度，而其他字体—主要是东亚字体—垂直显示；文本从上到下，从左到右流动)
- vert (垂直)
- vert270 (每行顺时针旋转270度，因此它从下到上，每行都在前一行的右侧)
- wordArtVert ("一个字母在另一个字母之上")
- wordArtVertRtl (垂直艺术字应从右到左显示，而不是从左到右)

下面是一个文本垂直显示的形状(<a:bodyPr anchor="ctr" vert="vert"/>)。

![Shape with text - anchoring](drwImages\drwSp-text-vert1.gif)

## 文本旋转：

形状边界框内的文本可以通过在<a:bodyPr>上使用rot属性指定旋转来独立于形状进行旋转。值以度的六万分之一为单位。下面是一个示例形状和文本，首先没有旋转，然后是45度旋转(<a:bodyPr anchor="ctr" rot="2700000"/>)。

![带文本的形状 - 旋转](drwImages\drwSp-text-rotate1.gif) ![带文本的形状 - 旋转](drwImages\drwSp-text-rotate2.gif)

为了显示形状和文本独立旋转，下面是一个90度旋转的示例形状和45度旋转的文本。

<p:spPr>

<a:xfrm rot="5400000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" rot="2700000"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-rotate3.gif)

为了防止文本在形状旋转时旋转，文本可以使用与形状旋转相同量的负值进行旋转。下面是一个旋转45度的形状和旋转-45度的文本。形状看起来保持固定。

<p:spPr>

<a:xfrm rot="2700000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" rot="-2700000"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-rotate4.gif)

请注意，使用下面讨论的upright属性也可以实现类似的结果。

## 文本直立：

可以使用<a:bodyPr>上的upright属性指定文本保持直立。无论对文本或伴随形状应用何种变换，这都将使文本保持直立。值为true或false；false是默认值。下面是与上面相同的形状（已应用45度旋转），但文本被指定为保持直立。

<p:spPr>

<a:xfrm rot="2700000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" upright="1"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-upright1.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
