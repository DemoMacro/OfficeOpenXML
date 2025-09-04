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
      - [定位和边距](drwSp-text-bodyPr-inset.md)
      - [适应、环绕、变形和3D](drwSp-text-bodyPr-fit.md)
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

文本 - 列表属性和默认样式

## 列表属性

形状内的段落可以分配一个级别。该级别由段落的<a:pPr>上的lvl属性分配。级别被指定为0到8之间的数值，因为有9个可能的级别。例如，<a:pPr lvl="1"/>表示该段落是级别2。每个级别可以使用样式分配一组属性。因此，例如，分配给级别2（<a:pPr lvl="1"/>）的段落将使用lvl2pPr列表样式（如果定义了这样的样式）。请注意，段落既可以具有与关联列表样式一起分配的级别，也可以具有在段落的<a:pPr>内指定的其他属性。在这种情况下，在更接近实际文本的级别上定义的属性优先，在此示例中，这意味着<a:pPr>中的属性将优先于列表样式中定义的冲突属性。

形状内<a:txBody>的各种列表样式包含在<a:lstStyle>中。<a:lstStyle>可以定义九种可能的样式：<a:lvl1pPr>（级别1）、<a:lvl2pPr>（级别2）、<a:lvl3pPr>（级别3）… <a:lvl9pPr>（级别9）。下面是分配给级别1和级别2的样式示例，以及这些级别的相应段落。

<a:txBody>

<a:bodyPr rtlCol="0" anchor="ctr"/>

<a:lstStyle>

<a:lvl1pPr algn="r">

<a:buAutoNum type="alphaUcPeriod" startAt="2"/>

</a:lvl1pPr>

<a:lvl2pPr>

<a:buClr>

<a:srgbClr val="00B0F0"/>

</a:buClr>

<a:buFont typeface="Wingdings"/>

<a:buChar char="q"/>

</a:lvl2pPr>

</a:lstStyle>

<a:p>

<a:pPr lvl="0"/>

. . .

</a:p>

<a:p>

<a:pPr lvl="1"/>

. . .

</a:p>

</a:txBody>

![Shape with text - list styles](drwImages\drwSp-text-lstPr1.gif)

每个级别样式的特定属性与可以直接作为段落属性应用的属性相同。然而，它们不是段落<a:pPr>元素的子元素或属性，而是级别样式特定元素的子元素或属性—即<a:lvl1pPr>、<a:lvl2pPr>、<a:lvl3pPr>等。

有关属性的详细信息，请参阅[形状 - 文本 - 段落属性](drwSp-text-paraProps.md)以及[项目符号和编号](drwSp-text-paraProps-numbering.md)、[间距、缩进和边距](drwSp-text-paraProps-margins.md)和[对齐、制表符、其他](drwSp-text-paraProps-align.md)的相关页面。

## 默认段落样式

对于形状内没有分配其他属性的段落，可以在<a:lstStyle>中使用子元素<a:defPPr>指定默认段落样式。此元素是上述讨论的列表样式的同级元素，并以相同的方式定义，具有相同的属性。请注意，默认文本运行属性可以通过<a:defRPr>子元素与其他默认段落属性一起指定，该子元素本身可以包含[形状 - 文本 - 文本运行属性](drwSp-text-runProps.md)中讨论的属性。以下是默认段落属性的示例定义，具有粗体的默认文本运行属性。

<a:txBody>

<a:bodyPr rtlCol="0" anchor="ctr"/>

<a:lstStyle>

<a:defPPr>

<a:defRPr b="1"/>

</a:defPPr>

</a:lstStyle>

. . .

<a:txBody>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
