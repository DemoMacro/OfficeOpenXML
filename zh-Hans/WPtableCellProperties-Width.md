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

相关的Open Office/ODF讨论  
相关的HTML/CSS讨论

表格单元格属性 - 宽度

单个表格单元格的首选宽度通过<tcPr>元素内的<w:tcW>元素指定。表格中的所有宽度都被视为首选宽度，因为列的宽度可能会冲突，并且表格布局规则可能需要覆盖首选设置。如果省略此元素，则单元格宽度类型为自动。

<w:tcPr>

<w:tcW w:type="pct" w:w="33.3%"/>

</w:tcPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.68。

Word 2007 示例：

下表的首选宽度(<w:tblW>)设置为自动。第一个单元格设置为33.3%，如上面的示例所示。下面的示例显示了单元格内不同内容的效果。

![Table Cell Properties - Width](images\wp-tblCellProperties-Width-1.gif)

---

![Table Cell Properties - Width](images\wp-tblCellProperties-Width-2.gif)

### 属性：

属性如下：

| 属性 | 描述                                                                                                                                                                                                                                                                            |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| w    | 指定单元格首选宽度的值。如果省略，则该值假定为零。![](images/versionConflict3.png)注意：OOXML标准的2006版本规定该值应为小数。当type="pct"时，该值被解释为百分之五，因此4975=99.5%，并且属性中不包含%符号。在2011版本中，该值可以是小数或百分比，因此当type="pct"时应包含%符号。 |
| type | 指定宽度(w)属性的单位。可能的值为：                                                                                                                                                                                                                                             |

- auto \- 指定宽度由整体表格布局算法确定。
- dxa \- 指定值以点的二十分之一（1/1440英寸）为单位。
- nil \- 指定值为零。
- pct \- 指定值作为表格宽度的百分比。

---

# 相关的开放文档格式(ODF)属性：

单元格的宽度通过应用于该单元格所在列的样式的<style:table-column-properties>元素上的style:column-width属性设置。值是一个正数。

还有一个style:rel-column-width属性，它指定列的相对宽度。值是一个后跟\*（U+002A，星号）的数字。

参考：办公应用程序开放文档格式1.2版（2011年5月）§§ 17.16和20.247。

<style:style style:name="Table1.A" style:family="table-column">

<style:table-column-properties style:column-width="0.75in" style:rel-column-width="1080\*"/>

</style:style>

# 相关的HTML/CSS属性：

<table style=" width: auto;">

<tr>

<td style="width:70%;">就是这样…</td>

</tr>

. . .

</table>

CSS 示例：

| 我们自己的过去也是如此。试图重温它是徒劳的：我们智力的所有努力都将证明是徒劳的。 | BBB | CCC |
| -------------------------------------------------------------------------------- | --- | --- |
| DDD                                                                              | EEE | FFF |
| GGG                                                                              | HHH | III |

<table style=" width: auto;">

<tr>

<td style="width:70%;">就是这样…</td>

</tr>

. . .

</table>

| AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA | BBB | CCC |
| ----------------------------------------------------------------------- | --- | --- |
| DDD                                                                     | EEE | FFF |
| GGG                                                                     | HHH | III |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
