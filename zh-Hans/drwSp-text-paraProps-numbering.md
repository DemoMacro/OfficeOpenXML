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
      - [适应、换行、弯曲和3D](drwSp-text-bodyPr-fit.md)
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

文本 - 项目符号和编号

形状中的段落可以通过使用列表样式或在段落的<a:pPr>元素（<a:p>）内直接应用格式来添加项目符号和编号/字母。本页涵盖与项目符号和编号/字母段落相关的各个属性。这些属性中的每一个都可以指定为列表样式的一部分。有关列表样式的定义和应用，请参见[列表属性](drwSp-text-lstPr.md)。

项目符号和编号是使用<a:pPr>的属性和子元素指定的。但是，两者都受到<a:pPr>上的lvl属性为段落指定的级别的影响。级别被指定为0到8之间的数值，因为定义了9个可能的级别。例如，<a:pPr lvl="1"/>表示该段落是第2级，应使用<a:txBody>内定义的lvl2pPr列表样式。参见[列表属性](drwSp-text-lstPr.md)。下面是一个具有两个段落的示例形状—第一个指定为第2级（<a:pPr lvl="1"/>），第二个指定为第3级（<a:pPr lvl="2"/>）。这是在指定任何编号或项目符号之前的状态。

![Shape with text - auto numbering](drwImages\drwSp-text-numbering1.gif)

## 项目符号

### 图像作为项目符号

项目符号可以是字符或图像。<a:buBlip>元素用于将图像指定为项目符号。此元素包含一个<a:blip>元素，该元素通过r:embed属性的值引用图像。（有关blips的更多信息，请参见图片的[概述](drwPic.md)及相关页面。）例如，下面是与上面相同的形状，但是使用了一个简单的图像作为形状内段落的项目符号。<r:embed="rId2"/>引用演示幻灯片的.rels文件中的<Relationship>，该关系的类型为"http://schemas.opemxmlformats.org/officeDocument/2006/relationships.image"，目标为"../media/image1.gif"，引用包内的图像文件。

<a:pPr lvl="1">

<a:buBlip>

<a:blip r:embed="rId2"/>

</a:buBlip>

</a:pPr>

. . .

<a:pPr lvl="2">

<a:buBlip>

<a:blip r:embed="rId2"/>

</a:buBlip>

</a:pPr>

![Shape with text - image as bullet](drwImages\drwSp-text-bullet1.gif)

### 字符作为项目符号

字符通过<a:buChar>元素指定为项目符号。字符可以是系统支持的任何字体中的任何字符，它在<a:buChar>的char属性中指定。字符指的是<a:buFont>元素指定的字体中的字符，该元素是<a:pPr>的子元素。<a:buFont>元素指定一个在应用程序中注册的字体。该字体将仅应用于项目符号—而不应用于后面的文本。字体在typeface属性中指定为字符串（例如，Arial）；如果字体不可用，将执行字体替换。还有charset和pitchFamily属性。这里不进一步讨论这些属性。要将项目符号的字体设置为与包含项目符号的文本运行相同，请指定空元素<a:buFontTx>。

<a:pPr lvl="1">

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="q"/>

</a:pPr>

. . .

<a:pPr lvl="2">

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="J"/>

</a:pPr>

![Shape with text - character as bullet](drwImages\drwSp-text-bullet2.gif)

### 项目符号字符颜色

项目符号字符的颜色可以通过<a:buClr>元素指定。与形状内的其他颜色一样，颜色被指定为子元素（在此上下文中，是<a:buClr>的子元素），使用以下颜色选项之一：作为预设颜色（<a:prstClr>），使用色调、饱和度和亮度（<a:hslClr>），方案颜色（<a:schemeClr>），系统颜色（<a:sysClr>），或作为RGB百分比或十六进制数字（<a:scrgbClr>或<a:srgbClr>）。请注意，这些对应于颜色指定方法的元素也可以具有转换基础颜色的子元素。因此，例如，方案或主题颜色可以指定为accent6，但也可以对该基础颜色应用亮度调制。这里不详细讨论颜色。

下面是与上面相同的形状，使用相同的字符作为项目符号，但为第一个项目符号应用了颜色。

<a:pPr lvl="1">

<a:buClr>

<a:srgbClr val="00B0F0"/>

</a:buClr>

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="q"/>

</a:pPr>

. . .

<a:pPr lvl="2">

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="J"/>

</a:pPr>

![Shape with text - character with color as bullet](drwImages\drwSp-text-bullet3.gif)

可以将项目符号的颜色设置为与包含项目符号的文本运行相同的颜色。这是通过空<a:buClrTx>元素指定的。当然，如果没有为运行指定颜色，则项目符号的颜色将遵循默认文本颜色。

### 项目符号大小

项目符号字符的大小可以指定为周围文本的百分比或以磅为单位。百分比通过<a:buSzPct>元素指定。实际值通过val属性指定，必须在25%到400%之间。以磅为单位的大小通过<a:buSzPts>元素指定。同样，实际值通过val属性指定，100表示一磅大小。下面是与上面相同的形状，只是第一个项目符号字符设置为周围文本的350%。

<a:pPr lvl="1">

<a:buClr>

<a:srgbClr val="00B0F0"/>

</a:buClr>

<a:buSzPct val="350000"/>

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="q"/>

</a:pPr>

. . .

<a:pPr lvl="2">

<a:buFont typeface="Wingdings" pitchFamily="2" charset="2"/>

<a:buChar char="J"/>

</a:pPr>

![Shape with text - bullet size](drwImages\drwSp-text-bullet4.gif)

可以将项目符号的大小设置为与包含项目符号的文本运行相同的磅大小。这是通过空<a:buSzTx>元素指定的。当然，如果没有为运行指定大小，则项目符号的大小将遵循默认文本大小。

### 无项目符号/h3>

要指定形状内的段落不应用任何项目符号格式，请将空<a:buNone>元素指定为<a:pPr>的子元素。

## 自动编号

段落的自动编号可以通过<a:pPr>内的<a:buAutoNum>元素指定。要使用的编号方案以及缩进和其他特征受到<a:buAutoNum>的属性以及为段落指定的级别的影响，如上所述。自动编号元素有两个属性：startAt和type。startAt指定开始编号序列的数字。当编号是字母时，数字应映射到适当的字母—例如，2映射到'b'，27映射到'aa'等。type指定要使用的编号方案。可能的值包括：

- alphaLcParenBoth — (a), (b), (c), …
- alphaLcParenR — a), b), c), …
- alphaLcPeriod — a., b., c., …
- alphaUcParenBoth — (A), (B), (C), …
- alphaUcParenR — A), B), C), …
- alphaUcPeriod — A., B., C., …
- arabicParenBoth — (1), (2), (3), …
- arabicParenR — 1), 2), 3), …
- arabicPeriod — 1., 2., 3., …
- arabicPlain — 1, 2, 3, …
- romanLcParenBoth — (i), (ii), (iii), …
- romanLcParenR — i), ii), iii), …
- romanLcPeriod — i., ii., iii., …
- romanUcParenBoth — (I), (II), (III), …
- romanUcParenR — I), II), III), …
- romanUcPeriod — I., II., III., …

下面是与上面相同的形状，但是为两个段落设置了自动编号。第一个从D开始，使用alphaUcPeriod方案，第二个从I开始，使用romanUcParenBoth方案。

<a:pPr lvl="1">

<a:buAutoNum type="alphaUcPeriod" startAt="4"/>

</a:pPr>

. . .

<a:pPr lvl="2">

<a:buAutoNum type="romanUcParenBoth" startAt="1"/>

</a:pPr>

![Shape with text - auto numbering](drwImages\drwSp-text-numbering2.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
