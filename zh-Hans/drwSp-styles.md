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

# DrawingML形状

样式

形状的样式信息通过<p:Sp>内的<p:style>元素指定。首先请注意，<p:style>元素不在主要的drawingML命名空间内；相反，它位于presentationML主命名空间（前缀p）或spreadsheetDrawing命名空间（前缀xdr）中。使用此元素指定形状的四个特征：填充类型、轮廓类型、要应用的效果和字体。然而，没有任何样式特征实际在<p:style>元素内定义。相反，该元素仅包含对主题部分中找到的样式细节的引用。包含这些引用的相应元素位于主要的drawingML命名空间内，分别是：<a:effectRef>、<a:fillRef>、<a:fontRef>和<a:lnRef>。这些引用元素中的每一个都包含一个idx属性，该属性是主题部分内相应属性列表的索引。因此，首先了解一些关于主题部分的内容很重要。

主题部分的核心是<a:themeElements>元素，它包含主题的大部分样式信息，分布在三个子元素中：<a:clrScheme>、<a:fmtScheme>和<a:fontScheme>。<a:fmtScheme>包含四个子元素：<a:bgFillStyleLst>、<a:effectStyleLst>、<a:fillStyleLst>和<a:lnStyleLst>。<p:style>内的四个ref子元素引用主题部分内<a:themeElements>元素的子元素。下面首先是演示文稿幻灯片中形状定义内的示例<p:style>元素，后跟主题部分的概要。颜色表示引用关系。

<p:style>

<a:lnRef idx="2">

<a:schemeClr val="accent1">

<a:shade val="50000"/>

</a:schemeClr>

</a:lnRef>

<a:fillRef idx="1">

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent2"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:srgbClr val="00B0F0"/>

</a:fontRef>

</p:style>

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Office Theme">

<a:themeElements>

<a:clrScheme name="Office">

. . .

</a:clrScheme>

<a:fontScheme>

<a:majorFont>

. . .

</a:majorFont>

<a:minorFont>

. . .

</a:minorFont>

</a:fontScheme>

<a:fmtScheme>

<a:fillStyleLst>

. . .

</a:fillStyleLst>

<a:lnStyleLst>

. . .

</a:lnStyleLst>

<a:effectStyleLst>

. . .

</a:effectStyleLst>

<a:bgFillStyleLst>

. . .

</a:bgFillStyleLst>

</a:fmtScheme>

</a:themeElements>

. . .

</a:theme>

## 填充

如上所述，填充样式由样式元素内的<a:fillRef>元素指定。<a:fillRef>引用主题部分中<a:fillStyleLst>或<a:bgFillStyleLst>的子元素。特定的子元素由<a:fillRef>上的idx属性中给出的索引指定。值为0或1000表示无背景；值1-999指<a:fillStyleLst>中填充样式的索引；值1001及以上指<a:bgFillStyleLst>内背景填充样式的索引。例如，在上面的示例中，我们有<a:fillRef idx="1">，因此它引用主题部分的<a:fillStyleLst>中的第一个填充样式。下面是相应的<a:fillStyleLst>和形状。第一个填充样式是使用主题颜色accent2的纯色填充，该颜色在主题部分的<a:clrScheme>中定义。（有关填充的更多信息，请参见[形状填充](drwSp-shapeFill.md)。）

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Office Theme">

<a:themeElements>

<a:clrScheme name="Office">

. . .

<a:accent2>

<a:srgbClr val="C0504D"/>

</a:accent2>

. . .

</a:clrScheme>

. . .

<a:fmtScheme>

<a:fillStyleLst>

<a:solidFill>

<a:schemeClr val="accent2"/>

</a:solidFill>

. . .

</a:fillStyleLst>

. . .

</a:fmtScheme>

</a:themeElements>

. . .

</a:theme>

![Shape with text - styles - fill](drwImages\drwSp-text-style-fill1.gif)

## 线条

线条样式由样式元素内的<a:lnRef>元素指定。<a:lnRef>引用主题部分中<a:lnStyleLst>元素的子元素。特定的子元素由<a:lnRef>上的idx属性中给出的索引指定。（有关轮廓的更多信息，请参见[形状轮廓](drwSp-outline.md)。）在下面的示例中，形状引用主题中找到的第二个线条样式：<a:lnRef idx="2">。

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Office Theme">

<a:themeElements>

<a:clrScheme name="Office">

. . .

</a:clrScheme>

. . .

<a:fmtScheme>

. . .

<a:lnStyleLst>

<a:ln . . .>

. . .

</a:ln>

<a:ln w="254000" cap="flat" cmpd="dbl" algn="ctr">

<a:solidFill>

<a:srgbClr val="000000"/>

</a:solidFill>

<a:prstDash val="dot"/>

</a:ln>

. . .

</a:lnStyleLst>

. . .

</a:fmtScheme>

</a:themeElements>

. . .

</a:theme>

![Shape with text - styles - line](drwImages\drwSp-text-style-ln1.gif)

## 效果

效果样式由样式元素内的<a:effectRef>元素指定。<a:effectRef>引用主题部分中<a:effectStyleLst>元素的子元素。特定的子元素由<a:effectRef>上的idx属性中给出的索引指定。（有关形状效果的更多信息，请参见[形状效果](drwSp-effects.md)。）在下面的示例中，形状引用主题中找到的第一个效果样式：<a:effectRef idx="1">。它将蓝色阴影应用于形状的底部。

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Office Theme">

<a:themeElements>

<a:clrScheme name="Office">

. . .

</a:clrScheme>

. . .

<a:fmtScheme>

. . .

<a:effectStyleLst>

<a:effectStyle>

<a:effectLst>

<a:outerShdw blurRad="400000" dist="200000" dir="5400000" rotWithShape="0">

<a:srgbClr val="0000FF"/>

</a:outerShdw>

</a:effectLst>

</a:effectStyle>

. . .

</a:effectStyleLst>

. . .

</a:fmtScheme>

</a:themeElements>

. . .

</a:theme>

![Shape with text - styles - effect](drwImages\drwSp-text-style-effect1.gif)

## 字体

字体样式由样式元素内的<a:fontRef>元素指定。<a:fontRef>引用主题部分中<a:fontScheme>元素的子元素。特定字体由<a:fontRef>上的idx属性中给出的索引指定。<a:fontRef>元素还指定颜色选择。在下面的示例中，形状引用主题中找到的次要拉丁字体，颜色为白色。

<p:style>

. . .

<a:fontRef idx="minor">

<a:srgbClr val="FFFFFF"/>

</a:fontRef>

</p:style>

<a:theme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="Office Theme">

<a:themeElements>

. .

<a:fontScheme name="Office">

<a:majorFont>

. . .

</a:majorFont>

<a:minorFont>

<a:latin typeface="Courier"/>

. . .

</a:minorFont>

</a:fontScheme>

. . .

</a:themeElements>

. . .

</a:theme>

![Shape with text - styles - font](drwImages\drwSp-text-style-font1.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
