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

# DrawingML 表格 - 样式

DrawingML表格可以具有适用于整个表格的各种属性—例如带状行或列的特殊格式，或首列、末列、首行或末行的特殊格式。表格也可以有标题。最后，表格可以设置为从右到左，而不是默认的从左到右。（请注意，尽管ECMA规范指示表格可以有表格范围的填充，但Microsoft PowerPoint似乎不支持它。填充似乎仅在单元格级别实现。）表格的属性在<a:tbl>元素的子元素<a:tblPr>中指定。<a:tbl>的子元素大多与表格填充相关。其他子元素与表格样式相关。<a:tbl>的属性与表格样式的操作相关，例如带状行和列，因此在下面的表格样式部分中涵盖。

## 表格样式

表格的样式可以通过两种方式之一指定。表格样式可以通过将其放在<a:tblpr>元素的子元素<a:tblStyle>元素中，与幻灯片部分中的表格规范一起内联指定。或者，表格样式可以在表格样式部分中单独定义，并从<a:tblStyleId>元素引用，该元素也是<a:tblpr>的子元素。

大多数情况下，表格样式将从<a:tblStyleId>引用。<a:tblStyleId>元素包含一个GUID，该GUID与包中表格样式部分内找到的<a:tblStyle>元素的styleId属性值匹配。每个演示文稿只有一个表格样式部分。它被命名为tableStyles.xml，在PowerPoint包中的ppt文件夹下找到。

表格样式部分在演示文稿的.rels文件（presentation.xml.rels）中被引用。

<Relationship Id="rId6" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/tableStyles" Target="tableStyles.xml"/>

下面首先是引用表格样式的表格规范（如它在演示文稿幻灯片中出现的那样）。在那下面是表格样式在表格样式部分中出现的规范。

<a:tbl>

<a:tblPr firstRow="1" bandRow="1">

<a:tableStyleId>{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}</a:tableStyleId>

. . .

</a:tbl>

在表格样式部分内，<a:tblStyleLst>中有一个或多个表格样式。下面是上面引用的表格样式：

<a:tblStyleLst . . .>

<a:tblStyle styleId="{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}" styleName="Medium Style 2 - Accent 3">

<a:wholeTbl>

. . .

</a:wholeTbl>

. . .

. . .

</a:tblStyleLst>

表格样式有十四个可能的子元素，可以确定表格的样式。它们提供表格各个方面的视觉格式，可以作为开关打开或关闭。这些开关是：

- 首行开/关 - 关联元素 <a:firstRow>
- 末行开/关 - 关联元素 <a:lastRow>
- 首列开/关 - 关联元素 <a:firstCol>
- 末列开/关 - 关联元素 <a:lastCol>
- 行带状开/关 - 关联元素 <a:band1H>, <a:band2H>。（带状依赖于交替样式，因此需要两种不同的样式。）
- 列带状开/关 - 关联元素 <a:band1V>, <a:band2V>。（带状依赖于交替样式，因此需要两种不同的样式。）

这些开关通过<a:tblPr>的属性打开和关闭。例如，以下表格属性规范打开首行和带状行格式：<a:tblPr firstRow="1" bandRow="1">。

有六个可能的属性与六个开关相关联。每个都是布尔值，可能的值为1或true和0或false。

- bandCol \- 值为true启用由<a:band1V>和<a:band2V>在表格样式中定义的带状列样式
- bandRow \- 值为true启用由<a:band1H>和<a:band2H>在表格样式中定义的带状行样式
- firstCol \- 值为true启用由<a:firstCol>定义的首列样式
- firstRow \- 值为true启用由<a:firstRow>定义的首行样式
- lastCol \- 值为true启用由<a:lastCol>定义的末列样式
- lastRow \- 值为true启用由<a:lastRow>定义的末行样式

除了上面提到的8个用于列和行样式的元素外，<a:tblStyle>还有四个特殊子元素来处理行和列样式相交的情况—即表格的四个角或东北单元格（<a:neCell>）、西北单元格（<a:nwCell>）、东南单元格（<a:seCell>）和西南单元格（<a:swCell>）。因此，例如，当末行和末列开关都打开时，将应用东南单元格元素指定的样式。

当所有开关都关闭（每个的默认值为false）时，表格的格式在<a:wholeTbl>元素中指定。表格样式的14个可能子元素中的最后一个是<a:tblBg>或表格背景元素，它指定表格的背景。

上述每个命名元素（除了<a:tblBg>）都可以包含指定表格单元格样式（<a:tcStyle>）和表格单元格文本样式（<a:tcTxStyle>）的子元素。

## 表格单元格样式

表格单元格的样式可以包括填充和/或边框。（单元格可以具有3D属性，如斜角，但这些属性在此不讨论。）表格单元格填充可以在<a:tcStyle>元素内内联指定，在<a:fill>元素内部，或者可以使用<a:fillRef>元素引用演示文稿主题中的填充规范。<a:fillRef>元素具有一个idx属性，它是主题填充样式的索引。更多信息请参见[PresentationML - 幻灯片 - 属性 - 填充](http://www.officeopenxml.com/prSlide-styles-themes.md)。

填充的指定如drawingML形状填充上下文中所讨论的—作为图像填充、渐变填充、纯色填充、图案填充或无填充。参见[DrawingML - 形状 - 填充](http://www.officeopenxml.com/drwSp-shapeFill.md)。

表格单元格样式可以在<a:tcBdr>元素中指定最多8个边框。每个都是子元素：

- <a:bottom> \- 底部边框
- <a:insideH> \- 内部水平边框
- <a:insideV> \- 内部垂直边框
- <a:left> \- 左边框
- <a:right> \- 右边框
- <a:tl2br> \- 左上到右下边框
- <a:top> \- 顶部边框
- <a:tl2br> \- 右上到左下边框

每个边框元素都有一个线条元素（<a:ln>）或线条引用元素（<a:lnRef>）。有关<a:ln>元素的更多信息，请参见[DrawingML - 形状 - 轮廓](http://www.officeopenxml.com/drwSp-outline.md)中的讨论。有关<a:lnRef>元素的更多信息，请参见[DrawingML - 形状 - 样式](http://www.officeopenxml.com/drwSp-styles.md)中的讨论。

## 表格单元格文本样式

单元格内文本的属性在<a:tcTxStyle>元素中指定。可以为文本指定两个主要属性：字体和文本颜色。字体可以在<a:font>元素内内联指定，或者可以在<a:fontRef>元素中引用字体。<a:fontRef>元素是一个具有两个属性的空元素：script，指定语言；typeface，指定字体。<a:fontRef>元素仅引用主题内指定的字体。有关字体引用的详细信息，请参见[DrawingML - 形状 - 样式](http://www.officeopenxml.com/drwSp-styles.md)。

文本的颜色可以使用用于指定颜色的熟悉元素来指定，所有这些元素都是<a:tcTxStyle>的子元素：<a:hslClr>（色相、饱和度和亮度）、<a:prstClr>（预设颜色）、<a:schemeClr>（方案或主题颜色）、<a:sysClr>（系统颜色）、<a:scrgbClr>（RGB颜色 - 百分比）和<a:srgbClr>（RGB颜色 - 十六进制）。有关颜色的更多信息，请参见[PresentationML - 幻灯片 - 属性 - 颜色方案](http://www.officeopenxml.com/prSlide-color.md)。

除了作为<a:tcTxStyle>的子元素表示的字体和颜色属性外，<a:tcTxStyle>还有两个可能的属性，它们指定文本要加粗（b）和斜体（1），这两个属性都可以具有on或off的值。

## 表格标题

将单元格标识为标题有两个方面。首先，要作为标题的单元格在<a:tc>元素的id属性中被赋予唯一标识符。例如，<a:tc id="HeaderA"/>。其次，具有一个或多个标题（即垂直和/或水平标题）的单元格必须通过在<a:tcPr>元素内包含<a:headers>元素中的标题列表来标识其标题单元格。与单元格关联的每个标题显示为空的<a:header val="HeaderA"/>元素。考虑下面的表格，其中包含标题单元格A、B、C和D。

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles4.gif)

具有此类标题的表格的XML如下。

<a:tbl>

. . .

<a:tr>

. . .

<a:tc>

. . .

</a:tc>

<a:tc id="HeaderA">

. . .

<a:p>

<a:r>

<a:t>A</a:t>

</a:r>

</a:p>

</a:tc>

. . .

</a:tr>

<a:tr>

. . .

<a:tc>

. . .

</a:tc>

<a:tc id="HeaderC">

. . .

<a:p>

<a:r>

<a:t>C</a:t>

</a:r>

</a:p>

</a:tc>

<a:tc>

<a:p>

<a:r>

<a:t>x1</a:t>

</a:r>

</a:p>

<a:tcPr>

. . .

<a:headers>

<a:header val="HeaderA"/>

<a:header val="HeaderC"/>

</a:headers>

. . .

</a:tcPr>

</a:tc>

. . .

</a:tr>

. . .

</a:tbl>

## 表格样式示例

现在将所有内容整合在一起，让我们看一个带有表格样式的示例表格。下面的表格应用了具有带状行和首列样式的样式。

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles1.gif)

首先，在幻灯片部分，我们有对表格样式的引用：

<a:tbl>

<a:tblPr firstCol="1" bandRow="1">

<a:tableStyleId>{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}</a:tableStyleId>

</a:tblPr>

. . .

</a:tbl>

包根目录下的表格样式部分具有以下样式：

<a:tblStyle styleId="{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}" styleName="Medium Style 2 - Accent 3">

. . .

<a:band1H>

<a:tcStyle>

<a:tcBdr/>

<a:fill>

<a:solidFill>

<a:schemeClr val="accent3">

<a:tint val="40000"/>

</a:schemeClr>

</a:solidFill>

</a:fill>

</a:tcStyle>

</a:band1H>

<a:band2H>

<a:tcStyle>

<a:tcBdr/>

</a:tcStyle>

</a:band2H>

. . .

<a:firstCol>

<a:tcStyle>

<a:tcTxStyle b="on">

<a:fontRef idx="minor">

<a:prstClr val="black"/>

</a:fontRef>

<a:schemeClr val="lt1"/>

</a:tcTxStyle>

<a:tcBdr/>

<a:fill>

<a:solidFill>

<a:schemeClr val="accent3"/>

</a:solidFill>

</a:fill>

</a:tcStyle>

</a:firstCol>

. . .

</a:tblStyle>

现在让我们修改样式。我们将首列的填充更改为黑色，将填充从<a:schemeClr val="accent3"/>更改为<a:prstClr val="black"/>。结果表格将如下表所示。

注意：在旧版本的Microsoft Word中，对表格样式的更改并不总是反映在表格中。

<a:tblStyle styleId="{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}" styleName="Medium Style 2 - Accent 3">

. . .

<a:band1H>

. . .

</a:band1H>

<a:band2H>

. . .

</a:band2H>

. . .

<a:firstCol>

<a:tcStyle>

. . .

<a:fill>

<a:solidFill>

<a:prstClr val="black"/>

</a:solidFill>

</a:fill>

</a:tcStyle>

</a:firstCol>

. . .

</a:tblStyle>

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles2.gif)

现在让我们也修改<a:band1H>元素中找到的水平带的文本样式。让我们将文本设置为斜体和红色，如下所示。

<a:tblStyle styleId="{F5AB1C69-6EDB-4FF4-983F-18BD219EF322}" styleName="Medium Style 2 - Accent 3">

. . .

<a:band1H>

<a:tcTxStyle i="on">

<a:fontRef idx="minor"/>

<a:prstClr val="red"/>

</a:tcTxStyle>

<a:tcStyle>

<a:tcBdr/>

<a:fill>

<a:solidFill>

<a:schemeClr val="accent3">

<a:tint val="40000" />

</a:schemeClr>

</a:solidFill>

</a:fill>

</a:tcStyle>

</a:band1H>

<a:band2H>

. . .

</a:band2H>

. . .

<a:firstCol>

. . .

</a:firstCol>

. . .

</a:tblStyle>

结果如下。

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles3.gif)

## 从右到左的表格

通过将<a:tblPr>元素上的rtl属性设置为true值，表格可以排列为从右到左，而不是默认的从左到右。例如，<a:tblPr rtl="1"/>。下面首先是一个从左到右的表格。

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles6.gif)

以下是同一表格排列为从右到左。

![DrawingML - Table - Styles](drwImages\drwTable-tableStyles5.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
