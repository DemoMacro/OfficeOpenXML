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
      - [定位和插入](drwSp-text-bodyPr-inset.md)
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

# DrawingML对象定位

在字处理文档中的定位 - 浮动对象

浮动对象锚定在文本内，但可以在文档中相对于页面进行绝对定位。它们被插入到带有<wp:anchor>元素的<w:drawing>元素中。子元素决定放置位置。

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="0" relativeHeight="251658240" behindDoc="0" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="1847850" y="914400"/>

<wp:positionH relativeFrom="margin">

<wp:align>right</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:wrapSquare wrapText="bothSides"/>

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

</wp:anchor>

</w:drawing>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.4.2.3。

Word 2007示例：

下面是一个浮动图片的示例。

![Floating Picture](drwImages\drwFloat.gif)

<wp:anchor>元素可以具有多个与定位、对象重叠以及图片与周围文本之间距离相关的属性。

### 属性：

| 属性                           | 描述                                                                                                                                                                                                                                                                                                                                |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| allowOverlap                   | 指定与另一个对象相交的drawingML对象是否允许重叠。可能的值为true和false。                                                                                                                                                                                                                                                            |
| behindDoc                      | 指定在重叠情况下drawingML对象是否显示在文本后面。如果对象应该位于顶部，则值应为false。下面是一个behindDoc="0"的图片示例，后面是一个behindDoc="1"的图片示例。两个示例中的文本环绕都是<wp:wrapTight>和simplePos="1"。![behindDoc is false](drwImages\drwFloat-behindDocF.gif) ![behindDoc is true](drwImages\drwFloat-behindDocT.gif) |
| distB, distL, distR, and distT | 指定对象的底部、左侧、右侧和顶部边缘与文本之间的最小距离。以EMU为单位指定。下面的示例指定了距离左侧一英寸（distL="914400"）。![Floating Picture - distB](drwImages\drwFloat-distB.gif)                                                                                                                                              |
| hidden                         | 指定drawingML对象是显示还是隐藏。请注意，应用程序可能有设置允许查看对象，而不考虑此属性。                                                                                                                                                                                                                                           |
| layoutInCell                   | 指定当对象锚定在表格单元格中且其位置会导致其与表格单元格相交时的行为方式。值可以是true或false。如果为true，则对象定位在单元格内，单元格会调整大小，所有定位都相对于单元格，而不是表格出现的行。当为false时，对象按指定方式定位，表格会调整大小或重新定位以容纳对象。                                                                |
| locked                         | 指定锚定位置不应被修改。例如，应用程序可能希望根据用户操作将对象移动到另一页，此属性告诉应用程序不要这样做。值可以是true或false。                                                                                                                                                                                                   |
| relativeHeight                 | 指定Z顺序或对象重叠时的显示顺序。请注意，这仅对具有相同behindDoc属性值的对象相关。所有behindDoc值为false的对象都显示在值为true的对象之上。值为整数；值越高，显示优先级越高。                                                                                                                                                        |
| simplePos                      | 属性值可以是true或false，当为true时，将使用子元素<wp:simplePos>中的信息定位对象。有关浮动图片定位的更多信息，请参见[浮动图片 - 定位](drwPicFloating-position.md)。                                                                                                                                                                  |

以下是<wp:anchor>可能的子元素。

### 元素：

| 元素            | 描述                                                                                                                                                                                                                                                                                                                |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cNvGraphicFrame | 指定图片的锁定属性。<wp:cNvGraphicFrame>元素包含一个空的<a:graphicFrameLocks/>元素，该元素具有多个可能的属性，用于确定锁定属性。如果未指定属性，则假定属性可以更改。例如，要禁止更改纵横比，请将noChangeAspect属性指定为true。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.4.2.4。以下是最有用的属性： |

- noChangeAspect - 注意：当用户通过拖动鼠标直接操作调整大小时，Microsoft Office会忽略此属性，但如果用户通过输入所需尺寸调整大小，则不会忽略它。
- noCrop
- noMove - 注意：Microsoft Office不实现此属性，将忽略它。
- noResize - 注意：Microsoft Office不实现此属性，将忽略它。
- noRot（无旋转）
- noSelect

下面是锁定纵横比的示例。<wp:cNvGraphicFramePr> <a:graphicFrameLocks xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" noChangeAspect="1"/> </wp:cNvGraphicFramePr> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.1.2.2.19。  
docPr | 指定常见的非视觉DrawingML属性。另请参见[图片 - 图像属性 - 非视觉属性](drwPic-nvPicPr.md)。图片的id、名称、标题和描述可以通过<wp:docPr>元素的属性指定：<wp:docPr id="222" name="Blue hills.jpg" title="This is the title" descr="This is the description"/>。id是一个整数，指定唯一标识符。名称是一个字符串，通常存储原始文件名。标题是一个字符串，指定标题。descr是用于不显示图片的辅助技术的替代文本。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.4.2.5。  
effectExtent | 指定当对图像应用绘图效果时，应添加到图像每一边的量。图像的大小使用<wp:extent>元素指定。容纳效果所需的额外大小存储在<wp:effectExtent>元素中，并将用于计算内联对象或环绕的适当行高。该元素有四个属性，每个属性存储EMU单位的长度值：b（底部）、l（左侧）、r（右侧）和t（顶部）。下面是一个在底部应用了反射效果，并添加了781050 EMU以容纳反射的图像。<wp:extent cx="2438400" cy="1828800"/> <wp:effectExtent l="0" t="0" r="0" b="781050"/> ![Effect Extent](drwImages\drwEffectExtent.gif) 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.4.2.6。  
extent | 使用两个属性指定对象的高度和宽度：cx表示矩形的长度（EMU单位），cy表示矩形的宽度（EMU单位）。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.4.2.7。  
graphic | 指定单个图形对象。对象的规范由文档作者/应用程序决定。它可以包含一个<a:graphicData>元素，该元素本身可以包含任何命名空间中的任何元素，并且还具有一个uri属性，用于标识存储的数据或可以处理标签内容的"服务器"。对于Microsoft Word，图片在pic命名空间中指定（xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"）。可以插入其他类型的图形，如图表。<a:graphic xmlns:a=http://schemas.openxmlformats.org/drawingml/2006/main"> <a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/picture"> <pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture"> . . . </pic:pic> </a:graphicData> </a:graphic> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§20.1.2.2.16。  
positionH, positionV, simplePos | 有关定位的子元素，请参见[浮动图片 - 定位](drwPicFloating-position.md)。  
wrapNone, wrapSquare, wrapThrough, wrapTight, and wrapTopAndBottom | 有关文本环绕的子元素，请参见[浮动图片 - 文本环绕](drwPicFloating-textWrap.md)。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
