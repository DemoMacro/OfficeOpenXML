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

文字处理文档中的定位 - 内联

内联对象与文本内联，并影响行高和行的布局，就像相同大小的字符会影响行一样。它们通过<wp:inline>元素插入到<w:drawing>元素中。

<w:drawing>

<wp:inline distT="0" distB="0" distL="0" distR="0">

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:docPr id="1" name="Picture 0" descr="Blue hills.jpg"/>

<wp:cNvGraphicFramePr>

<a:graphicFrameLocks xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" noChangeAspect="1"/>

</wp:cNvGraphicFramePr>

<a:graphic xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main">

<a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/picture">

<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">

. . .

</pic:pic>

</a:graphicData>

</a:graphic>

</wp:inline>

</w:drawing>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.8。

Word 2007示例：

下面是一个内联图片的示例。

![Inline Picture](drwImages\drwInline.gif)

<wp:inline>元素可以具有多个与图片和周围文本之间距离相关的属性。但是，当图片以内联方式显示时，这些属性不起作用。这些属性可以保留，并且在图片更改为浮动时将生效。

以下是<wp:inline>可能的子元素。

### 元素：

| 元素            | 描述                                                                                                                                                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cNvGraphicFrame | 指定图片的锁定属性。<wp:cNvGraphicFrame>元素包含一个空的<a:graphicFrameLocks>元素，该元素具有多个可能的属性，用于确定锁定属性。如果未指定这些属性，则假定可以更改这些属性。例如，要禁止更改纵横比，请将noChangeAspect属性指定为true。 |

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.4。以下是最有用的属性：

- noChangeAspect - 注意：当用户通过拖动鼠标直接操作调整大小时，Microsoft Office会忽略此属性，但如果用户通过输入所需尺寸调整大小，则不会忽略它。
- noCrop
- noMove - 注意：Microsoft Office未实现此属性，将忽略它。
- noResize - 注意：Microsoft Office未实现此属性，将忽略它。
- noRot（无旋转）
- noSelect

下面是锁定纵横比的示例。<wp:cNvGraphicFramePr> <a:graphicFrameLocks xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" noChangeAspect="1"/> </wp:cNvGraphicFramePr> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.2.2.19。  
docPr | 指定通用的非视觉DrawingML属性。另请参见[图片 - 图像属性 - 非视觉属性](drwPic-nvPicPr.md)。可以使用<wp:docPr>元素的属性为图片指定id、名称、标题和描述：<wp:docPr id="222" name="Blue hills.jpg" title="This is the title" descr="This is the description"/>。id是一个整数，指定唯一标识符。name是一个字符串，通常存储原始文件名。title是一个字符串，指定标题。descr是用于不显示图片的辅助技术的替代文本。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.5。  
effectExtent | 指定将绘图效果应用于图像时应该添加到图像每边的量。图像的大小使用<wp:extent>元素指定。容纳效果所需的额外大小存储在<wp:effectExtent>元素中，并将用于计算内联对象或环绕的适当行高。该元素有四个属性，每个属性存储EMU单位的长度值：b（底部）、l（左侧）、r（右侧）和t（顶部）。下面是一个在底部应用了反射效果的图像，并添加了781050 EMU以容纳该反射。<wp:extent cx="2438400" cy="1828800"/> <wp:effectExtent l="0" t="0" r="0" b="781050"/> ![效果范围](drwImages\drwEffectExtent.gif) 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.6。  
extent | 使用两个属性指定对象的高度和宽度：cx表示EMU单位的矩形长度，cy表示EMU单位的矩形宽度。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.4.2.7。  
graphic | 指定单个图形对象。对象的规范由文档作者/应用程序决定。它可以包含一个<a:graphicData>元素，该元素本身可以包含任何命名空间中的任何元素，并且还具有一个uri属性，用于标识存储的数据或可以处理标记内容的"服务器"。对于Microsoft Word，图片在pic命名空间（xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"）中指定。可以插入其他类型的图形，如图表。Microsoft Office支持一组特定的uri值，包括图片、图表、图表等的值。<a:graphic xmlns:a=http://schemas.openxmlformats.org/drawingml/2006/main"> <a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/picture"> <pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"> . . . </pic:pic> </a:graphicData> </a:graphic> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.2.2.16。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
