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

概述

形状可以出现在每种文档类型中。然而，关于形状和文档类型，有一个重要的区别需要记住。字处理文档中的形状与电子表格和演示文稿中的形状实现方式不同，这反映在ECMA规范中。电子表格中的形状使用<xdr:sp>（形状）元素指定，该元素在ECMA规范第20.5节的电子表格ML绘图ML规范中定义；形状元素位于xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing"命名空间中。同样，演示文稿中的形状使用<p:sp>（形状）元素指定，该元素在ECMA规范第19节的演示文稿规范中定义；形状元素位于xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"命名空间中。这些形状中的每一个都使用[在电子表格中的放置](drwPicInSpread.md)和[在演示文稿中的放置](drwPicInPresentation.md)中讨论的放置方法插入到其各自的文档类型中。简而言之，电子表格将形状放在三个锚定标记之一中，整个绘图ML对象或形状放置在单独的绘图部分中。演示文稿将形状与幻灯片的其他内容内联放置，它们包含在<p:spTree>或<p:grpSp>元素中。对于这些文档类型中的每一种，尽管在文档中的放置因文档类型而异，但形状本身的实际细节在大多数方面是相同的。字处理文档在文档中的放置和形状细节方面都以不同的方式实现形状。

在早期版本的Microsoft Word中，形状使用VML实现。在Word 2010中，文档的XML中同时包含VML和drawingML，使用<mc:AlternateContent>和一对子元素：<mc:Choice Requires="wps">，包含drawingML XML，和<mc:Fallback>，包含VML。Requires属性的wps指的是Microsoft字处理形状的命名空间：xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"。因此，如果应用程序支持该形状命名空间，则使用drawingML XML；否则使用VML。在drawingML选择中有一个容器<w:drawing>元素。它使用[在字处理文档中的定位](drwPicInWord.md)中概述的方法定位在文档中，将对象内联放置或锚定在特定位置。形状的实际规范包含在<a:graphicData>元素中，它是各种可能的图形内容的通用容器。该元素有一个uri属性，指定可以处理数据类型的"服务器"。对于Word中的形状，uri值与上面显示的字处理形状命名空间相同。因此，对于较新版本的Word，形状在文档中的定位方式与图片或图像的定位方式相同，但形状的实际细节位于与电子表格和演示文稿不同的命名空间中，并且这些细节特定于Microsoft（或任何其他支持字处理形状的供应商）。因此，此处的讨论将仅关注电子表格和演示文稿中的形状，因为它们被定义为ECMA OOXML规范的一部分。但是请注意，Word中形状的内容模型似乎接近电子表格和演示文稿中形状的模型，模型中的差异与形状内的文本有关。

形状使用<xdr:sp>或<p:sp>元素指定。形状可以基于预设几何图形或自定义几何图形。形状有四个基本组件，对应于四个子元素：

1. <nvSpPr> \- 非视觉形状属性。参见[形状 - 非视觉属性](drwSp-nvSpPr.md)。
2. <spPr> \- 形状属性。参见[形状 - 形状属性](drwSp-SpPr.md)。
3. <style> \- shape styles. See [Shapes - Styles](drwSp-styles.md).
4. <txBody> \- 形状内的文本。参见[形状 - 文本](drwSp-text.md)。

下面是电子表格文档中形状的示例。

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="2" name="圆角矩形 1"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

<a:xfrm>

<a:off x="1371600" y="514350"/>

<a:ext cx="1038225" cy="542925"/>

</a:xfrm>

<a:prstGeom prst="roundRect">

<a:avLst/>

</a:prstGeom>

</xdr:spPr>

<xdr:style>

<a:lnRef idx="2">

<a:schemeClr val="accent1">

<a:shade val="50000"/>

</a:schemeClr>

</a:lnRef>

<a:fillRef idx="1">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="lt1"/>

</a:fontRef>

</xdr:style>

<xdr:txBody>

<a:bodyPr vertOverflow="clip" rtlCol="0" anchor="ctr"/>

<a:lstStyle/>

<a:p>

<a:pPr algn="ctr"/>

<a:endParaRPr lang="en-US" sz="1100"/>

</a:p>

</xdr:txBody>

</xdr:sp>

![Shape in spreadsheet](drwImages\drwSp.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 19.3.1.43（演示文稿）和§ 20.5.2.29（电子表格）。

形状可以具有以下属性。

| 属性                       | 描述                                                                                                    |
| -------------------------- | ------------------------------------------------------------------------------------------------------- |
| fLocksText（仅限电子表格） | 指示在保护工作表时是否允许在空间内进行文本编辑。                                                        |
| fPublished（仅限电子表格） | 指示在发送到服务器时是否应随工作表一起发布形状。                                                        |
| macro（仅限电子表格）      | 指定与形状关联的自定义函数。例如，macro="DoWork()"。                                                    |
| textlink（仅限电子表格）   | 指定链接到电子表格单元格数据的公式。                                                                    |
| useBgFill（仅限演示文稿）  | 指定形状填充应与幻灯片背景相同。请注意，这不会将形状设置为透明—它将填充设置为与形状后面的背景部分相同。 |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
