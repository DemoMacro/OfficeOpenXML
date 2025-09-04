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

属性

表格范围的属性在<tblPr>中指定。每个属性都是<tblPr>的子元素，它们影响表格中的所有行和单元格，尽管它们可以被[表格级例外](WPtablePropertyExceptions.md)、[行级属性](WPtableRowProperties.md)和[单元格级属性](WPtableCellProperties.md)覆盖。

<w:tblPr>

<w:tblW w:w="0" w:type="auto"/>

<w:jc w:val="end"/>

</w:tblPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.60。

最常用的属性如下所示：

### 元素/属性：

| 元素                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| jc                  | 参见[表格对齐](WPtableAlignment.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.29。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| shd                 | 参见[表格底纹](WPtableShading.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.32。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| tblBorders          | 参见[表格边框](WPtableBorders.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.39。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| tblCaption          | 参见[表格标题](WPtableCaption.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.41。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| tblCellMar          | 参见[表格单元格边距](WPtableCellMargins.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.43。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| tblCellSpacing      | 参见[表格单元格间距](WPtableCellSpacing.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.46。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| tblInd              | 参见[表格缩进](WPtableIndent.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.51。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| tblLayout           | 参见[表格布局](WPtableLayout.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.53。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| tblLook             | 参见[表格条件格式](WPtblLook.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.56。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| tblOverlap          | 参见[浮动表格 - 重叠表格](WPfloatingTables.md#overlappingTables)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.57。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| tblpPr              | 参见[浮动表格](WPfloatingTables.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.58。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| tblStyle            | 指定表格样式的样式ID（如果要使用表格样式来格式化表格）。参见[定义样式 - 表格样式](WPstyleTableStyles.md)。表格样式在文档默认样式之后应用，因此它们会覆盖默认值，但所有其他样式类型在表格样式之后应用，因此它们会覆盖表格样式。在下面的示例中，引用了一个表格样式，但同时也应用了表格对齐的直接格式。<w:tblPr> <w:tblStyle w:val="TestTableStyle"/> <w:jc w:val="center"/> </w:tblPr> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.63。                                                                                                                                                                                                                                         |
| tblStyleColBandSize | 此元素适用于表格样式中的<tblPr>。表格样式可以有条件格式，通过为交替的列或行应用不同的格式，使列和/或行能够"分条显示"。通常，每隔一列的格式相同。因此，例如，奇数列可能有灰色底纹，偶数列可能有绿色底纹。此元素可用于对列进行分组，以便交替的列组以相同的方式格式化，而不是每隔一列。例如，通过将val属性的值设置为3，前三个列将以相同方式格式化，第二组三个列将以相同方式格式化，之后的每组三个列将交替其格式。参见[表格样式 - 条件格式](WPstyleTableStylesCond.md)。<w:style w:type="table" w:styleId="myTableStyle"> <w:tblPr> <w:tblStyleColBandSize w:val="3"/> <w:tblStyleRowBandSize w:val="2"/> </w:tblPr> </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.5。 |
| tblStyleRowBandSize | 此元素适用于表格样式中的<tblPr>。表格样式可以有条件格式，通过为交替的列或行应用不同的格式，使列和/或行能够"分条显示"。通常，每隔一行的格式相同。因此，例如，奇数行可能有灰色底纹，偶数行可能有绿色底纹。此元素可用于对行进行分组，以便交替的行组以相同的方式格式化，而不是每隔一行。例如，通过将val属性的值设置为3，前三行将以相同方式格式化，第二组三行将以相同方式格式化，之后的每组三行将交替其格式。参见[表格样式 - 条件格式](WPstyleTableStylesCond.md)。<w:style w:type="table" w:styleId="myTableStyle"> <w:tblPr> <w:tblStyleColBandSize w:val="3"/> <w:tblStyleRowBandSize w:val="2"/> </w:tblPr> </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.7。       |
| tblW                | 参见[表格宽度](WPtableWidth.md)。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.64。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |

---

# 相关开放文档格式(ODF)属性：

表格行属性在<style:table-properties>元素中指定。

<style:style style:name="Table1" style:family="table">

<style:table-properties style:width="4.7in" table:align="right" fo:background-color="#e6e6e6" style:shadow="none" fo:keep-with-next="always"/>

</style:style>

参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 17.15。

<style:table-properties>元素可以具有以下属性：

| 属性                                                                            | 描述                                                                                                               |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| fo:background-color                                                             | 指定表格背景的颜色。                                                                                               |
| fo:break-after                                                                  | 指定表格后的分隔符。可能的值为auto、column和page。                                                                 |
| fo:break-before                                                                 | 指定表格前的分隔符。可能的值为auto、column和page。                                                                 |
| fo:keep-with-next                                                               | 指定何时应将行与表格保持在一起。可能的值为auto和always。                                                           |
| fo:margin, fo:margin-bottom, fo:margin-left, fo:margin-right, and fo:margin-top | 指定表格的边距。可能的值为非负数或百分比。                                                                         |
| style:may-break-between pages                                                   | 指定表格内可能发生分页。可能的值为true和false。                                                                    |
| style:page-number                                                               | 指定当表格样式指定主页时，新页面应使用的页码。可能的值为auto和正数。                                               |
| style:rel-width                                                                 | 指定表格相对于其所在区域宽度的宽度。可能的值为百分比。                                                             |
| style:width                                                                     | 指定表格的固定宽度。                                                                                               |
| style:shadow                                                                    | 指定表格的阴影效果。                                                                                               |
| style:writing-mode                                                              | 指定内容应该如何书写。可能的值为lr-tb、rl-tb、tb-rl、tb-lr、lr、rl、tb和page。                                     |
| table:align                                                                     | 指定水平对齐方式。可能的值为center、left、margins和right。                                                         |
| table:border-model                                                              | 指定边框模型。可能的值为collapsing（当相邻单元格具有不同边框时，显示较宽的边框）和separating（边框出现在单元格内） |
| table:display                                                                   | 指定是否应显示表格。可能的值为true和false。                                                                        |

注意，<style:table-properties>还可以包含<style:background-image>元素。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
