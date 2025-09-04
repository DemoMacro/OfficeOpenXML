![OfficeOpenXML.com](images/banner1.png)

[主页](index.md) | [字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

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

# 字处理表格

相关Open Office/ODF讨论  
相关HTML/CSS讨论

单元格

表格单元格包含表格内容，并由<w:tc>元素指定。表格单元格必须至少包含一个块级元素，即使是一个空的&ltp/>。单元格可以包含任何块级内容，包括嵌套的段落和表格。

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

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.66。

Word 2007示例：

![Table Cell](images\wp-tableCell-1.gif)

---

### 元素：

<w:tc>元素可以包含大量元素，主要与跟踪修订和添加自定义XML相关。核心元素如下所示。

| 元素 | 描述                                                                                                                                                                               |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| p    | 指定单元格的内容段落 参见[段落](WPparagraph.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.22。                                                              |
| tbl  | 指定表格作为单元格的内容。参见[表格](WPtable.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.38。                                                               |
| tcPr | 指定要应用于当前单元格的属性。此类属性会覆盖冲突的表格或行属性。参见[表格单元格属性](WPtableCellProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.70。 |

### 属性：

<w:tc>元素可以包含一个属性。

| 属性 | 描述                                                                                                                                                |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| id   | 指定单元格的唯一标识符。它在表格内必须是唯一的，并用于使用headers元素将单元格标识为表格中其他单元格的标题单元格。例如，<w:tc w:id="januaryeight">。 |

---

# 相关开放文档格式(ODF)属性：

表格单元格使用<table:table-row>元素内的<table:table-cell>元素定义。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 9.1.4。

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A" table:number-columns-repeated="3"/>

<table:row>

<table:table-cell table:style-name="Table1.A1" office:value="string">

<text:p text:style-name="Table_20_Contents">AAA</text:p>

</table:table-cell>

. . .

<table:row>

. . .

</table:table>

### 属性：

最常用的属性如下。

| 属性                          | 描述                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- |
| table:number-columns-spanned  | 指定单元格跨越的列数。注意，当值大于1时，表格中必须出现<table:covered-table-cell>来表示被覆盖的单元格。 |
| table:number-rows-spanned     | 指定单元格跨越的行数。注意，当值大于1时，表格中必须出现<table:covered-table-cell>来表示被覆盖的单元格。 |
| table:style-name              | 指定单元格的样式。                                                                                      |
| table:number-columns-repeated | 指定单元格重复的连续列数                                                                                |

### 元素：

最常用的元素如下。

| 元素                      | 描述           |
| ------------------------- | -------------- |
| <table:table>             | 指定表格。     |
| <text:h>                  | 指定标题。     |
| <text:list>               | 指定列表。     |
| <text:numbered-paragraph> | 指定编号段落。 |
| <text:p>                  | 指定段落。     |
| <text:section>            | 指定节。       |
| <text:table-of-content>   | 指定目录。     |

# 相关HTML/CSS属性：

<td>AAA</td>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
