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

# DrawingML对象定位

字处理文档中的定位 - 浮动图片 - 定位

浮动对象锚定在文本内，但可以在文档中相对于页面进行绝对定位。它们被插入到带有<wp:anchor>元素的<w:drawing>元素中。子元素决定放置位置。

## 使用<wp:simplePos>进行定位

使用<wp:anchor>元素控制放置有两种方法。首先，可以使用子元素<wp:simplePos x="0" y="0"/>将对象相对于页面左上边缘定位，该元素有两个属性x和y。这些属性分别指定x轴和y轴上的坐标。可能的值可以是EMU单位，也可以是紧跟着单位标识符的数字。同样重要的是要记住，要使用<wp:simplePos>元素进行定位，<wp:anchor>标签上的simplePos属性必须设置为true。否则，将使用第二种定位方法。无论是否使用，<wp:simplePos>元素都应包含在XML中。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.13。

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="1" relativeHeight="251658240" behindDoc="0" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="1847850" y="914400"/>

. . .

</wp:anchor

</w:drawing>

![](images/note.png)注意：Microsoft Word似乎不完全支持使用<wp:simplePos>进行定位。

## 使用<wp:positionH>和<wp:positionV>进行定位

如果<wp:anchor>的simplePos属性为false，则使用<wp:positionH>和<wp:positionV>子元素定位对象，分别对应于水平和垂直定位。

这些定位元素中的每一个都有两个重要组成部分：(1) 定位基准，即计算定位所依据的文档部分，以及 (2) 相对于该基准的定位。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.10 和 § 20.4.2.11。

### 相对于什么进行定位？

使用<wp:positionH>和<wp:positionV>进行定位的第一个组成部分由<wp:positionH>和<wp:positionV>的relativeFrom属性给出。对于水平定位，可能的值是：

- character \- 相对于锚点在运行内容中的位置
- column \- 相对于包含锚点的列的范围
- insideMargin \- 相对于奇数页的左边距，偶数页的右边距
- leftMargin \- 相对于左边距
- margin \- 相对于页面边距
- outsideMargin \- 相对于奇数页的右边距，偶数页的左边距
- page \- 相对于页面边缘
- rightMargin \- 相对于右边距

对于垂直定位，可能的值是：

- bottomMargin \- 相对于底边距
- insideMargin \- 相对于当前页的内边距
- line \- 相对于包含锚点字符的行
- margin \- 相对于页面边距
- outsideMargin \- 相对于当前页的外边距
- page \- 相对于页面边缘
- paragraph \- 相对于包含锚点的段落
- topMargin \- 相对于顶边距

以下是顶部对齐的垂直定位示例。第一个示例是相对于边距的对齐。

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

![Vertical alignment - relativeFrom margin](drwImages\drw-relativeFrom-margin.gif)

第二个示例是相对于页面的对齐。

<wp:positionV relativeFrom="page">

<wp:align>top</wp:align>

</wp:positionV>

![Vertical alignment - relativeFrom page](drwImages\drw-relativeFrom-page.gif)

使用<wp:positionH>和<wp:positionV>进行定位的第二个组成部分由这两个元素的子元素给出：要么是用于指定相对对齐的align元素（例如，center、left、right、top、bottom等），要么是用于指定绝对位置偏移的<wp:posOffset>元素。

### 使用<wp:align>进行定位

相对于relativeFrom属性中给出的基准的实际位置在<wp:align>元素中指定。对于水平定位，可能的值是：

- center \- 对象应相对于relativeFrom的值居中
- inside \- 对象应在relativeFrom值的内部
- left \- 对象应相对于relativeFrom的值左对齐
- outside \- 对象应在relativeFrom值的外部
- right \- 对象应相对于relativeFrom的值右对齐

以下是相对于右边距右对齐的水平定位示例。

<wp:positionH relativeFrom="rightMargin">

<wp:align>right</wp:align>

</wp:positionH>

![Horizontal alignment - relativeFrom rightMargin, align right](drwImages\drw-positionH.gif)

对于垂直定位，可能的值是：

- bottom \- 对象应相对于relativeFrom的值位于底部
- center \- 对象应相对于relativeFrom的值居中
- inside \- 对象应在relativeFrom值的内部
- outside \- 对象应在relativeFrom值的外部
- top \- 对象应相对于relativeFrom的值位于顶部

以下是相对于底边距内部定位的垂直定位示例。

<wp:positionV relativeFrom="bottomMargin">

<wp:align>inside</wp:align>

</wp:positionV>

![Horizontal alignment - relativeFrom bottomMargin, align inside](drwImages\drw-positionV.gif)

### 使用<wp:posOffset>进行定位

可以使用<wp:posOffset>元素指定绝对测量值。测量值以EMU单位给出，并相对于relativeFrom属性中给出的定位基准的左上边缘计算。以下是相对于页面的绝对放置。

![](images/note.png)注意：Microsoft Word使用<wp:posOffset>进行定位似乎不可靠。

<wp:positionH relativeFrom="page">

<wp:posOffset>914400</wp:posOffset>

</wp:positionH>

<wp:positionV relativeFrom="page">

<wp:posOffset>2743200</wp:posOffset>

</wp:positionV>

![Horizontal alignment - relativeFrom page, posOffset](drwImages\drw-posOffset.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.12。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
