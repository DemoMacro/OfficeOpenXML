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

相关Open Office/ODF讨论  
相关HTML/CSS讨论

结构

表格由行和单元格组成，其结构非常类似于HTML表格。它使用<w:tbl>元素定义。

<w:tbl>

<w:tblPr>

<w:tblStyle w:val="TableGrid"/>

<w:tblW w:w="5000" w:type="pct"/>

</w:tblPr>

<w:tblGrid>

<w:gridCol w:w="2880"/>

<w:gridCol w:w="2880"/>

<w:gridCol w:w="2880"/>

</w:tblGrid>

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>AAA</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>BBB</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>CCC</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

. . .

</w:tbl>

![](images/note.png)注意：当两个具有相同样式的相邻表格一起出现且中间没有<w:p>元素时，这些表格将被视为单个表格。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.38。

Word 2007 示例：

![Table](images\wp-table-1.gif)

---

### 元素：

<w:tbl>元素可以包含大量元素，主要与跟踪修订和添加自定义XML有关。核心元素如下所示。

| 元素    | 描述                                                                                                                                                                                         |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| tblGrid | 指定表格的列。参见表格[表格列](WPtableGrid.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.49。                                                                           |
| tblPr   | 指定表格的表格范围属性。这些属性可以被单个表格级别例外、行和单元格级别属性覆盖。参见表格[表格属性](WPtableProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.60。 |
| tr      | 指定表格行。参见表格[表格行](WPtableRow.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.79。                                                                              |

---

# 相关开放文档格式（ODF）属性：

ODF格式中的表格使用<table:table>元素指定。表格由行和列组成。行被划分为单元格，列是通过取行中具有相同位置的所有单元格来隐含的。表格可以出现在<office:text>中、节中、表格单元格中、页眉或页脚中等。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 9.1.2。

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A" table:number-columns-repeated="3"/>

<table:row>

<table:table-cell table:style-name="Table1.A1" office:value="string">

<text:p text:style-name="Table_20_Contents">AAA</text:p>

</table:table-cell>

<table:table-cell table:style-name="Table1.A1" office:value="string">

<text:p text:style-name="Table_20_Contents">BBB</text:p>

</table:table-cell>

<table:table-cell table:style-name="Table1.C1" office:value="string">

<text:p text:style-name="Table_20_Contents">CCC</text:p>

</table:table-cell>

<table:row>

. . .

</table:table>

### 属性：

最常用的属性如下。

| 属性             | 描述                                                    |
| ---------------- | ------------------------------------------------------- |
| table:name       | 指定唯一名称。                                          |
| table:style-name | 指定表格的表格样式。                                    |
| xml:id           | 指定唯一ID，并由W3C（xml-id）标准化。                   |
| table:protected  | 指定表格是否受保护，使用户无法编辑它。值为true和false。 |

### 元素：

最常用的元素如下。

| 元素                         | 描述                                               |
| ---------------------------- | -------------------------------------------------- |
| <table:table-column>         | 指定一个或多个相邻列的属性。                       |
| <table:table-column-group>   | 对相邻列进行分组                                   |
| <table:table-columns>        | 包含不随表格跨页重复的<table:table-column>元素组。 |
| <table:table-header-columns> | 表示列标题。                                       |
| <table:table-header-rows>    | 表示行标题。                                       |
| <table:table-row>            | 表示一行。                                         |
| <table:table-row-group>      | 对不显示为表格标题的相邻行进行分组。               |
| <table:table-rows>           | 包含不随表格跨页重复的<table:table-row>元素组。    |
| <table:title>                | 指定表格的标题。                                   |

# 相关HTML/CSS属性：

<table style="width:100%;">

<tr>

<td>AAA</td>

<td>BBB</td>

<td>CCC</td>

</tr>

. . .

</table>

HTML/CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
