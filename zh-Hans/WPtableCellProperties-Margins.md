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

表格单元格属性 - 边距

单个表格单元格的边距使用<tcPr>元素内的<w:tcMar>元素指定。如果存在，这将覆盖[表格级单元格边距](WPtableCellMargins.md)。

<w:tblStyle>

<w:tblCellMar>

<w:top w:w="0" w:type="dxa"/>

<w:start w:w="0" w:type="dxa"/>

<w:bottom w:w="0" w:type="dxa"/>

<w:end w:w="0" w:type="dxa"/>

</w:tblCellMar>

</w:tblStyle>

. . .

<w:tcPr>

<w:tcMar>

<w:top w:w="720" w:type="dxa"/>

<w:start w:w="720" w:type="dxa"/>

<w:bottom w:w="0" w:type="dxa"/>

<w:end w:w="720" w:type="dxa"/>

</w:tcMar>

</w:tcPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.69。

Word 2007示例：

默认表格单元格边距设置为零。下面的B单元格按上述指定设置：

![Table Cell Properties - Margins](images\wp-tblCellProperties-Mar-1.gif)

---

### 元素：

| 元素   | 描述                                                                                                                                                                                                                                          |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| top    | 指定单元格内容顶部与顶部边框之间的空间量。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.78。                                                                                                                                  |
| bottom | 指定单元格内容底部与底部边框之间显示的空间量。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.2。                                                                                                                               |
| start  | 指定从左到右表格中单元格内容左端与左边框之间的空间量（从右到左表格中为右端与右边框之间的空间量）。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素为left。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.36。  |
| end    | 指定从左到右表格中单元格内容右端与右边框之间的空间量（从右到左表格中为左端与左边框之间的空间量）。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素为right。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.10。 |

### 属性：

上述表格单元格边距元素的属性如下：

| 属性 | 描述                                      |
| ---- | ----------------------------------------- |
| w    | 指定边距宽度的值。如果省略，则假定值为0； |
| type | 指定宽度(w)属性的单位。可能的值为：       |

- dxa \- 指定值以点的二十分之一（1/1440英寸）为单位
- nil \- 指定零值

如果省略该属性，则假定其值为dxa。

---

# 相关开放文档格式(ODF)属性：

单元格内的边距可以通过将fo:margin、fo:margin-bottom、fo:margin-left、fo:margin-right和fo:margin-top属性添加到应用于单元格内包含文本的段落的样式的<style:paragraph-properties>元素中来设置。值可以是数字或百分比。因此，边距不是在<style:table-cell-properties>元素中设置，而是在单元格内段落的样式中设置。

参考：办公应用程序开放文档格式版本1.2（2011年5月）§§ 17.6, 20.198 - 20.202。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Table_20_Contents">

<style:paragraph-properties fo:margin-left="0.2in" fo:margin-right="0.2in" fo-text-indent="0in" style:auto-text-indent="false"/>

</style:style>

# 相关HTML/CSS属性：

td {  
padding-bottom:0px;  
padding-top:25px;  
padding-left:15px;  
padding-right:10px;  
}

CSS示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
