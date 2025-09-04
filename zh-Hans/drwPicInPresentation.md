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

# DrawingML对象放置

在演示文稿文档中的放置

演示文稿被组织成幻灯片或<p:sld>元素。给定幻灯片上的图片、形状、表格和文本在该幻灯片的部件中内联指定（例如，slide1.xml、slide2.xml等）。<p:sld>元素包含一个<p:cSld>元素，该元素充当常见幻灯片数据（如图片、形状和表格）的容器。（<p:sld>元素还可以包含有关计时和过渡的信息。此处不涵盖此信息。）所有形状、图片和其他内容都进一步嵌套在形状树或<p:spTree>元素中。

注意：用于在演示文稿中将形状、图片和表格放置到幻灯片中的高级元素位于主要的presentationML命名空间xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"内。

形状树包含组形状的非视觉属性、所有形状共有的视觉属性（可被各个形状中的属性覆盖），然后是一个或多个形状、图片、连接形状、组形状和/或图形框架（即，从外部源生成的表格和图形的容器）。因此，幻灯片的所有形状和其他内容都包含在<p:spTree>元素中。每个形状和图片在幻灯片上的位置都在该特定形状或图片的属性内指定。例如，对于形状，位置在<a:xfrm>内，该元素位于包含形状属性的<p:spPr>元素中。参见[形状 - 边界框位置](drwSp-location.md)。

<p:spTree>元素内形状和其他内容的顺序很重要，因为顺序决定了幻灯片上对象的z顺序。列出的第一个对象具有最低的z顺序（因此位于对象堆栈的底部），最后一个具有最高的顺序（位于对象堆栈的顶部）。当对象重叠时，z顺序很重要，它还决定了Tab键或导航顺序，对象按z顺序升序进行导航。下面是幻灯片上四个对象堆栈的示例，首先是椭圆形，然后是一张图片，接着是另一张图片，最后是箭头形状。

<p:sld . . .>

<p:cSld>

<p:nvGrpSpPr>

. . .

<p:nvGrpSpPr>

<p:grpSpPr>

. . .

<p:grpSpPr>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="椭圆 3"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="5" name="图片 4" descr="蓝色山丘.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="8" name="图片 7" descr="冬季.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="9" name="右箭头 8"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:cSld>

. . .

</p:sld>

![Placement of shapes within a presentation](drwImages\drwInPresentation1.gif)

如果我们颠倒最后两个对象的顺序，将箭头形状放在冬季图片之前，我们会得到以下结果，冬季图片覆盖在箭头上：

<p:sld . . .>

<p:cSld>

<p:nvGrpSpPr>

. . .

<p:nvGrpSpPr>

<p:grpSpPr>

. . .

<p:grpSpPr>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="椭圆 3"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="5" name="图片 4" descr="蓝色山丘.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="9" name="右箭头 8"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="8" name="图片 7" descr="冬季.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:cSld>

. . .

</p:sld>

![Placement of shapes within a presentation](drwImages\drwInPresentation2.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
