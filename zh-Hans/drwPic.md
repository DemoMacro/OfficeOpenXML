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

概述

图片可以添加到文字处理文档、电子表格或演示文稿中。向任何这些文档类型添加图片需要两个组件—(1)关于图片本身的信息，以及(2)关于其在文档中放置位置的信息。前者对于所有文档类型都是通用的，并且此信息的大部分XML都在主要的drawingML命名空间内(xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main")。关于文档中的放置和定位的信息，包括高级元素和非视觉属性，在单独的命名空间中指定，并根据文档类型而有所不同。有关命名空间的更多信息，请参阅[DrawingML概述](drwOverview.md)。

图片使用<pic>元素指定。文字处理文档中的命名空间在drawingML的图片命名空间中xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"。这是这些页面上大多数示例XML所使用的内容。在电子表格中，它是电子表格drawingML命名空间xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/spreadsheetDrawing"。在演示文稿中，它在主要的演示文稿命名空间中xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"。

图片可以具有边框、调整大小行为、叠加填充和其他效果等特性。下面显示了文字处理文档中的示例图片。

<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">

<pic:nvPicPr>

<pic:cNvPr id="0" name="Blue hills.jpg"/>

<pic:cNvPicPr/>

</pic:nvPicPr>

<pic:blipFill>

<a:blip r:embed="rId4" cstate="print"/>

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

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.2.2.5（文字处理），§ 20.5.2.25（电子表格）和§ 19.3.1.37（演示文稿）。

### 元素：

图片有三个基本组件—填充图片矩形的填充或内容、非视觉属性和形状属性。电子表格和演示文稿还有关联的样式。这些组件使用下面的元素指定。

| 元素                                 | 描述                                                                                                                                                                                                                                                                                                                           |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| blipFill [BLIP = 二进制大图像或图片] | 指定图片所具有的图片填充类型。图片已经有填充，但如果图片有透明像素，可以通过指定例如渐变填充在<spPr>元素内添加另一个填充。有关blipFill的详细信息，请参阅[图像数据](drwPic-ImageData.md)、[平铺或拉伸图像以填充](drwPic-tile.md)和[效果](drwPic-effects.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.2.2.1。 |
| nvPicPr                              | 指定图片的非视觉属性，如锁定属性、名称、id和标题，以及图片是否隐藏。有关详细信息，请参阅[非视觉属性](drwPic-nvPicPr.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.2.2.4。                                                                                                                                    |
| spPr                                 | 指定可以应用于图片的视觉形状属性。它们是可以应用于形状的相同属性。有关更多信息，请参阅[形状 - 视觉属性](drwSp-SpPr.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.2.2.6。                                                                                                                                     |
| style（仅适用于电子表格和演示文稿）  | 指定应用于图片或形状的样式以及每个样式组件的引用，如线条、填充、字体和效果。有关更多信息，请参阅[形状 - 样式](drwSp-styles.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 19.3.1.46和§ 20.5.2.31。                                                                                                               |

电子表格文档中的<xrd:pic>元素可以具有以下属性。

### 属性：

| 属性值                         | 描述                                               |
| ------------------------------ | -------------------------------------------------- |
| fPublished（仅适用于电子表格） | 指示当发送到服务器时，图片是否应与工作表一起发布。 |
| macro（仅适用于电子表格）      | 指定与对象关联的函数。例如，macro="DoWork()"。     |

---

---

# 相关HTML/CSS属性：

没有对应的HTML属性。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
