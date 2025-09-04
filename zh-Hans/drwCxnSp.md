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

# DrawingML 连接线

概述

连接线只是一种特殊类型的形状，用于连接电子表格或演示文稿文档中的两个形状（<xdr:sp> 或 <p:sp>）。

电子表格中的连接形状使用电子表格ML绘图命名空间中的 <xdr:cxnSp> 元素指定 - xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing"。同样，演示文稿中的连接形状使用主演示文稿ML命名空间中定义的 <p:cxnSp> 元素指定 - xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"。

与任何形状一样，连接线使用[在电子表格中的放置](drwPicInSpread.md)和在演示文稿中的放置中讨论的放置方法插入到文档的包中。简而言之，电子表格将形状放在单独的绘图部分中。演示文稿将形状与幻灯片的其他内容内联放置，并且形状包含在 <p:spTree> 或 <p:grpSp> 元素中。然而，与其他形状不同，连接线没有定义的位置；相反，它们的位置由它们连接的形状定义。一旦指定了连接，就由生成应用程序决定连接线采用的确切路径。

对于每种文档类型，虽然在文档中的放置因文档类型而异，但连接形状本身的实际细节在大多数方面是相同的。字处理文档在形状的放置和形状细节方面实现方式不同。有关字处理ML文档中形状的更多信息，请参见[形状 - 概述](drwShape.md)。

连接形状有三个基本组件，对应于三个子元素。请注意，与其他形状不同，连接形状可以没有文本，因此没有子 <txBody> 元素。

1. <nvCxnSpPr> \- 连接形状的非视觉属性。参见[连接线 - 非视觉属性](drwSp-nvCxnSpPr.md)。
2. <spPr> \- 形状属性。参见[形状 - 形状属性](drwSp-SpPr.md)。
3. <style> \- shape styles. See [Shapes - Styles](drwSp-styles.md).

连接线的类型和样式主要由两件事决定 — (1) 形状的指定几何结构，和 (2) 形状的轮廓。几何结构在 <spPr> 内指定为形状属性的一部分 — 例如，<a:prstGeom prst="bentConnector2">。有关可能的连接线形状类型的完整列表，请参见[形状 - 预设几何](drwSp-prstGeom.md)。形状的轮廓也在 <a:ln> 元素内指定为形状属性的一部分。轮廓决定了连接线的大小或粗细、颜色以及端点样式等特征。有关轮廓属性的详细信息，请参见[形状 - 轮廓](drwSp-outline.md)。

下面是演示文稿文档中两个形状之间的连接线形状（红色）示例。

<p:cxnSp>

<p:nvCxnSpPr>

<p:cNvPr id="9" name="Straight Arrow Connector 8"/>

<p:cNvCxnSpPr>

<a:stCxn id="4" idx="3"/>

<a:endCxn id="5" idx="1"/>

</p:cNvCxnSpPr/>

<p:nvPr/>

</p:nvCxnSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2514600" y="3086100"/>

<a:ext cx="1143000" cy="38100"/>

</a:xfrm>

<a:prstGeom prst="StraightConnector1">

<a:avLst/>

</a:prstGeom>

<a:ln w="57150">

<a:solidFill>

<a:srgbClr val="FF0000"/>

</a:solidFill>

<a:headEnd type="oval" w="med" len="med"/>

<a:tailEnd type="triangle" w="med" len="med"/>

</a:ln>

</p:spPr>

<p:style>

<a:lnRef idx="1">

<a:schemeClr val="accent1"/>

</a:lnRef>

<a:fillRef idx="0">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="tx1"/>

</a:fontRef>

</p:style>

</p:cxnSp>

![Connector in a presentation](drwImages\drwSp-connector.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
