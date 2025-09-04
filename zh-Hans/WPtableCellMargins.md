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
    - [对齐](WPnumbering-lvlJc.md)
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

单元格边距默认值

默认表格单元格边距（即单元格内容与单元格边框之间的距离）由<w:tblCellMar>元素指定。与[tblCellSpacing](WPtableCellSpacing.md)比较。此设置可以在单元格级别使用单元格属性中的tcMar元素进行覆盖。

<w:tblPr>

<w:tblCellMar>

<w:top w:w="720" w:type="dxa"/>

<w:start w:w="432" w:type="dxa"/>

<w:bottom w:w="0" w:type="dxa"/>

<w:end w:w="144" w:type="dxa"/>

</w:tblCellMar>

</w:tblPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.43。

Word 2007示例：

![Table Cell Margin Default](images\wp-tblCellMar-1.gif)

---

### 元素：

| 元素   | 描述                                                                                                                                                                                                                                                                                     |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| top    | 指定单元格内容顶部与所有单元格顶部边框之间保留的空间量。如果省略，表格将没有顶部填充，除非单元格覆盖默认值。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.76。                                                                                                          |
| bottom | 指定单元格内容底部与所有单元格边框之间保留的空间量。如果省略，表格将没有底部填充，除非单元格覆盖默认值。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.5。                                                                                                               |
| start  | 指定从左到右表格左侧显示的空间量和从右到左表格右侧显示的空间量。如果省略，表格将有115二十分之一点（0.08英寸）的左填充，除非单元格覆盖默认值。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是left。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.35。  |
| end    | 指定从左到右表格右侧显示的空间量和从右到左表格左侧显示的空间量。如果省略，表格将有115二十分之一点（0.08英寸）的右填充，除非单元格覆盖默认值。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是right。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.11。 |

### 属性：

上述表格单元格边距元素的属性如下：

| 属性 | 描述                                      |
| ---- | ----------------------------------------- |
| w    | 指定边框宽度的值。如果省略，则假定值为0； |
| type | 指定宽度（w）属性的单位。可能的值为：     |

- dxa \- 指定值以二十分之一点（1/1440英寸）为单位。
- nil \- 指定零值

如果省略该属性，则假定其值为dxa。

---

# 相关开放文档格式（ODF）属性：

单元格边距不在<style:table-cell-properties>元素中设置，而是在单元格内段落的样式中设置。有关更多详细信息，请参见[表格单元格属性 - 边距](WPtableCellProperties-Margins.md)。

# 相关HTML/CSS属性：

padding属性在单元格级别应用：  
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
版权 © 2023。保留所有权利。
