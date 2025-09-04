![OfficeOpenXML.com](images/banner1.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [内容概述](WPcontentOverview.md)
- [示例Docx视图](WPsampleDoc.md)
- [Document](WPdocument.md)
- 段落
  - [Overview](WPparagraph.md)
  - [Properties](WPparagraphProperties.md)
    - [水平对齐](WPalignment.md)
    - [Borders](WPborders.md)
    - [分隔符](WPtextSpecialContent-break.md)
    - [Indentation](WPindentation.md)
    - [底纹和背景](WPshading.md)
    - [Spacing](WPspacing.md)
    - [Styles](WPstyleParStyles.md)
    - [Tabs](WPtab.md)
    - [垂直对齐](WPborders.md)
- [文本框](WPparagraph-textFrames.md)
- 文本
  - [Overview](WPtext.md)
  - [Properties](WPtextFormatting.md)
    - [Borders](WPtextBorders.md)
    - [Fonts](WPtextFonts.md)
    - [Shading](WPtextShading.md)
    - [Spacing](WPtextSpacing.md)
    - [特殊内容](WPtextSpecialContent.md)
      - [分隔符](WPtextSpecialContent-break.md)
      - [符号](WPtextSpecialContent-symbol.md)
    - [Styles](WPstyleCharStyles.md)
- 表格
  - 结构
    - [Overview](WPtable.md)
    - [定义列或表格网格](WPtableGrid.md)
    - [Rows](WPtableRow.md)
    - [Cells](WPtableCell.md)
  - [表格属性](WPtableProperties.md)
    - [Alignment](WPtableAlignment.md)
    - [Borders](WPtableBorders.md)
    - [边框冲突](WPtableCellBorderConflicts.md)
    - [Captions](WPtableCaption.md)
    - [Indentation](WPtableIndent.md)
    - [Shading](WPtableShading.md)
    - [Width](WPtableWidth.md)
    - [Styles](WPstyleTableStyles.md)
    - [单元格边距](WPtableCellMargins.md)
    - [单元格间距](WPtableCellSpacing.md)
    - [自动调整/宽度布局](WPtableLayout.md)
    - [绝对定位或浮动表格](WPfloatingTables.md)
    - [条件格式](WPtblLook.md)
  - [表格属性例外](WPtablePropertyExceptions.md)
  - [行属性](WPtableRowProperties.md)
  - [单元格属性](WPtableCellProperties.md)
    - [边框](WPtableCellProperties-Borders.md)
    - [单元格边框冲突](WPtableCellBorderConflicts.md)
    - [边距](WPtableCellProperties-Margins.md)
    - [底纹](WPtableCellProperties-Shading.md)
    - [垂直对齐](WPtableCellProperties-verticalAlignment.md)
    - [宽度](WPtableCellProperties-Width.md)
    - [隐藏单元格结束标记](WPhideMark.md)
- 编号、级别和列表
  - [Overview](WPnumbering.md)
  - [定义编号方案](WPnumberingAbstractNum.md)
  - [定义特定级别](WPnumberingLvl.md)
    - [编号级别文本](WPnumberingLevelText.md)
    - [编号格式](WPnumbering-numFmt.md)
    - [仅显示为数字](WPnumbering-isLgl.md)
    - [重新开始编号](WPnumbering-restart.md)
    - [图片或图像作为编号符号](WPnumbering-imagesAsSymbol.md)
    - [对齐方式](WPnumbering-lvlJc.md)
  - [覆盖编号定义](WPnumberingOverride.md)
- 节
  - [Overview](WPsection.md)
  - [Columns](WPsectionCols.md)
  - [Footers](WPsectionFooterReference.md)
  - [Headers](WPsectionHeaderReference.md)
  - [Borders](WPsectionBorders.md)
  - [页边距](WPsectionPgMar.md)
  - [页码](WPSectionPgNumType.md)
  - [行号](WPsectionLineNumbering.md)
- 样式
  - [Overview](WPstyles.md)
  - [定义默认格式](WPstyleDefaults.md)
  - [定义样式](WPstyle.md)
    - [常规样式属性](WPstyleGenProps.md)
    - [字符样式](WPstyleCharStyles.md)
    - [段落样式](WPstyleParStyles.md)
    - [表格样式](WPstyleTableStyles.md)
      - [条件格式](WPstyleTableStylesCond.md)
    - [编号样式](WPstyleNumStyles.md)
- [Fonts](WPfonts.md)
- [Headers](WPheaders.md)
- [Footers](WPfooters.md)
- [页码](WPSectionPgNumType.md)
- 链接
  - [Overview](WPhyperlink.md)
  - [Bookmarks](WPbookmark.md)
- 域
  - [Overview](WPfields.md)
  - [域指令](WPfieldInstructions.md)
  - [域定义](WPfieldDefinitions.md)
  - [常规域格式](WPgeneralFieldSwitches.md)
  - [日期和时间域格式](WPdateTimeFieldSwitches.md)
  - [数字域格式](WPnumericFieldSwitches.md)
- [目录](WPtableOfContents.md)

# 文字处理表格

浮动表格

浮动表格是不属于文档中文本主流部分的表格，而是相对于文档中的非框架内容具有特定大小和位置的绝对定位表格。浮动表格通过<w:tblPr>元素内的<w:tblpPr>元素指定。

![](images/note.png)注意：表格的定位是相对于其左上角。锚点（例如，边距、页面或文本）在属性（tblpX和tblpY）中指定，从中指定表格放置的测量值（也在属性中指定）。与周围文本的距离也可以在其他属性中指定。

<w:tblPr>

<w:tblpPr w:leftFromText="144" w:rightFromText="144" w:topFromText="144" w:bottomFromText="144" w:vertAnchor="page" w:horzAnchor="page" w:tblpX="4320" w:tblpY="4320"/>

</w:tblPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.58。

Word 2007 示例：

![Floating Table](images\wp-floatingTable-1.gif)

---

### 属性：

属性如下：

| 属性       | 描述                                                                                 |
| ---------- | ------------------------------------------------------------------------------------ |
| horzAnchor | 指定水平锚点或基础对象，应从该对象确定tblpX或tblpXSpec属性中的水平定位。可能的值有： |

- margin - 相对于任何文本运行之前的文本边距的垂直边缘（对于从左到右的段落为左边缘）
- page - 相对于任何文本运行之前的页面的垂直边缘（对于从左到右的段落为左边缘）
- text - 相对于锚点段落所在列的文本边距的垂直边缘

如果省略，则假定值为page。  
vertAnchor | 指定垂直锚点或基础对象，应从该对象确定tblpY属性中的垂直定位。可能的值有：

- margin - 相对于任何文本运行之前的文本边距的水平边缘（对于从上到下的段落为上边缘）
- page - 相对于任何文本运行之前的页面的水平边缘（对于从上到下的段落为上边缘）
- text - 相对于锚点段落所在列的文本边距的水平边缘

如果省略，则假定值为page。  
tblpX | 指定表格的绝对水平位置，相对于horzAnchor锚点。值以点的二十分之一为单位。请注意，该值可以为负，在这种情况下，表格将按照水平文本流的方向定位在锚点对象之前。如果还指定了tblpXSpec，则忽略tblpX属性。如果省略该属性，则假定值为零。  
tblpXSpec | 指定表格的相对水平位置，相对于horzAnchor属性。这将取代tblpX属性。可能的值有：

- center - 表格应相对于锚点水平居中
- inside - 表格应在锚点内部
- left - 表格应相对于锚点左对齐
- outside - 表格应在锚点外部
- right - 表格应相对于锚点右对齐

tblpY | 指定表格的绝对垂直位置，相对于vertAnchor锚点。值以点的二十分之一为单位。请注意，该值可以为负，在这种情况下，表格将按照垂直文本流的方向定位在锚点对象之前。如果还指定了tblpYSpec，则忽略tblpX属性。如果省略该属性，则假定值为零。  
tblpYSpec | 指定表格的相对垂直位置，相对于vertAnchor属性。这将取代tblpY属性。可能的值有：

- center - 表格应相对于锚点垂直居中
- inside - 表格应垂直对齐到锚点的边缘并在锚点内部
- bottom - 表格应垂直对齐到锚点的底部边缘
- outside - 表格应垂直对齐到锚点的边缘并在锚点外部
- inline - 表格应与周围文本垂直对齐（以便不允许任何文本环绕它）
- top - 表格应垂直对齐到锚点的顶部边缘

bottomFromText | 指定表格与表格下方段落中文本顶部之间应保持的最小距离。值以点的二十分之一为单位。如果省略，则假定值为零。  
topFromText | 指定表格与表格上方段落中文本底部边缘之间应保持的最小距离。值以点的二十分之一为单位。如果省略，则假定值为零。  
leftFromText | 指定表格与表格左侧段落中文本边缘之间应保持的最小距离。值以点的二十分之一为单位。如果省略，则假定值为零。  
rightFromText | 指定表格与表格右侧段落中文本边缘之间应保持的最小距离。值以点的二十分之一为单位。如果省略，则假定值为零。

重叠表格

由于浮动表格位于正常文本流之外，并且可以绝对定位，因此存在多个浮动表格重叠的可能性。但是，可以通过<w:tblPr>元素内的<w:tblOverlap>元素防止重叠。此元素指定表格是否允许其他浮动表格与其重叠。

<w:tblOverlap>只有一个属性val，具有以下可能的值：

- never \- 父表格不能显示在会与另一个浮动表格重叠的位置
- overlap \- 父表格可以显示在与另一个浮动表格重叠的位置

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.57。

### 允许重叠

<w:tblPr>

<w:tblpPr w:leftFromText="144" w:rightFromText="144" w:topFromText="144" w:bottomFromText="144" w:vertAnchor="page" w:horzAnchor="page" w:tblpX="4120" w:tblpY="4120"/>

.. . . JJJ . . . KKK . . . 等等。

</w:tblPr>

<w:tblPr>

<w:tblpPr w:leftFromText="144" w:rightFromText="144" w:topFromText="144" w:bottomFromText="144" w:vertAnchor="page" w:horzAnchor="page" w:tblpX="4320" w:tblpY="4320"/>

.. . . AAA . . . BBB . . . 等等。

</w:tblPr>

Word 2007 示例：

![Overlapping Tables](images\wp-tableOverlap-1.gif)

---

### 不允许重叠

<w:tblPr>

<w:tblpPr w:leftFromText="144" w:rightFromText="144" w:topFromText="144" w:bottomFromText="144" w:vertAnchor="page" w:horzAnchor="page" w:tblpX="4120" w:tblpY="4120"/>

<w:tblOverlap w:val="never"/>

.. . . JJJ . . . KKK . . . 等等。

</w:tblPr>

<w:tblPr>

<w:tblpPr w:leftFromText="144" w:rightFromText="144" w:topFromText="144" w:bottomFromText="144" w:vertAnchor="page" w:horzAnchor="page" w:tblpX="4320" w:tblpY="4320"/>

<w:tblOverlap w:val="never"/>

.. . . AAA . . . BBB . . . 等等。

</w:tblPr>

Word 2007 示例：

![Overlapping Tables](images\wp-tableOverlap-2.gif)

---

### 相关CSS属性：

OOXML浮动表格的某些方面可以用CSS复制，但存在严重限制。可以使用position属性定位表格，但这样表格会从内容流中移除，可能会发生重叠。可以使用float属性使表格相对于其包含块向左或向右浮动，但这样特定的或绝对定位就不可用了。

我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。过去隐藏在领域之外的某个地方，超出智力的范围，在我们不怀疑的某个物质对象中（在该物质对象将给我们的感觉中）。

<table style="position: relative; left:50px; top:10px;">

. . .

</table>

至于那个物体，在我们自己必须死去之前，我们是否偶然发现它取决于机会。

<table style="float: right;">

. . .

</table>

许多年过去了，在这期间，除了我在那里上床睡觉的剧院和戏剧中所包含的内容外，康布雷对我来说没有任何存在，直到有一天冬天，当我回家时，我的母亲看到我很冷，给了我一些茶，这是我通常不喝的东西。

CSS 示例：

我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。过去隐藏在领域之外的某个地方，超出智力的范围，在我们不怀疑的某个物质对象中（在该物质对象将给我们的感觉中）。

| AAA                                                                      | BBB | CCC |
| ------------------------------------------------------------------------ | --- | --- |
| DDD                                                                      | EEE | FFF |
| 至于那个物体，在我们自己必须死去之前，我们是否偶然发现它取决于机会。 GGG | HHH | III |
| ---                                                                      | --- | --- |
| JJJ                                                                      | KKK | LLL |

许多年过去了，在这期间，除了我在那里上床睡觉的剧院和戏剧中所包含的内容外，康布雷对我来说没有任何存在，直到有一天冬天，当我回家时，我的母亲看到我很冷，给了我一些茶，这是我通常不喝的东西。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
