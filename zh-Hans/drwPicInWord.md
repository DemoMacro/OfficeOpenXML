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

# DrawingML对象定位

字处理文档中的定位

字处理文档中的drawingML对象由<w:drawing>元素指定，该元素通常放置在运行(<w:r>)内。它也可以是背景(<w:background>)或项目符号的图片(<w:numPicBullet>)。

<w:r>

<w:rPr>

. . .

</w:rPr>

<w:drawing>

. . .

</w:drawing>

</w:r>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.9。

<w:drawing>元素指定一个DrawingML对象。对象及其定位的细节在DrawingML命名空间中指定，Word中的前缀如wp、pic和a。字处理文档中的DrawingML对象可以是内联的或浮动的。内联对象与文本内联，并影响行的高度和布局。它们通过<wp:inline>元素插入到<w:drawing>元素中。注意不同的命名空间。<w:drawing>元素位于主要的字处理命名空间内：xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"。图片放置的XML位于字处理drawingML命名空间内：xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"。而图片本身的定义位于图片命名空间内：xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"。有关内联放置的详细信息，请参见[字处理文档中的定位 - 内联](drwPicInline.md)。

Word 2007示例：

下面是一个内联图片的示例。

![Inline Picture](drwImages\drwInline.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.8。

浮动对象在文本内锚定，但可以在文档中相对于页面进行绝对定位。文本围绕对象浮动。它们通过<wp:anchor>元素插入到<w:drawing>元素中。有关详细信息，请参见[字处理文档中的定位 - 浮动](drwPicFloating.md)。下面是一个浮动图片的示例。

Word 2007示例：

![Anchored Picture](drwImages\drwAnchor.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.3。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
