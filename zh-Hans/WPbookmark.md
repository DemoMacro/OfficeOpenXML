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

# 文字处理超链接

书签

书签是具有唯一名称/ID的文本区域，并作为链接的目标—即超链接所链接到的位置。参见[超链接](WPhyperlink.md)。书签是传统的文字处理功能，早于XML。它们可以在文档内的任何位置开始和结束，因此如果用典型的XML开始和结束标签表示，会违反XML的良好格式性。因此，书签不是在开始和结束标签之间定义的。相反，开始由一个空元素（bookmarkStart）定义，结束由一个空元素（bookmarkEnd）定义。这两个标签通过它们共同的id属性一起定义一个区域。然后，指向书签的链接使用书签的name属性值作为其anchor属性的值。

<w:p>

<w:r>

<w:t xml:space="preserve">这是一个 </w:t>

</w:r>

<w:hyperlink w:anchor="myAnchor">

<w:r>

<w:rPr>

<w:rStyle w:val="Hyperlink"/>

</w:rPr>

<w:t>内部链接</w:t>

</w:r>

</w:hyperlink>

</w:p>

. . .

<w:p>

<w:r>

<w:t xml:space="preserve">这是带有 </w:t>

</w:r>

<w:bookmarkStart w:id="0" w:name="myAnchor"/>

<w:r>

<w:t>书签</w:t>

</w:r>

<w:bookmarkEnd w:id="0"/>

</w:p>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.13.6。

Word 2007 示例：

![Internal Link](images\wp-bookmark-1.gif)

---

### 属性：

bookmarkStart元素具有以下属性。

| 属性     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| id       | 指定书签的唯一标识符。该值必须与bookmarkEnd元素的相应id值匹配。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| name     | 指定书签名称。此属性的值应与hyperlink元素的anchor属性值匹配。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| colFirst | 此属性用于定义表格内的书签。如果出现此属性，则必须也出现colLast属性。表格内的书签可以通过指定作为书签一部分的第一行、作为书签一部分的每行的第一列、作为书签一部分的最后一列和作为书签一部分的最后一行，仅覆盖特定列和行范围内的单元格。第一行通过将开始书签（bookmarkStart）放在该行的第一个单元格中来指定。最后一行通过将结束书签（bookmarkEnd）放在该行的末尾来指定。第一列由此属性指定。最后一列由下面显示的colLast指定。该属性是列的从零开始的索引，因此第一列由w:colFirst="0"表示。例如，一个三行三列的表格可能会将书签应用于前两行的前两个单元格。 | ![表格书签](images\wp-bookmark-2.gif) |

---

上面用蓝色阴影表示的书签将用以下内容指定：

<w:tbl>

<w:tr>

<w:tc

<bookmarkStart w:colFirst="0" w:colLast="1" w:id="0" w:name="tableAnchor"/>

. . .

</w:tc>

</w:tr>

<w:tr>

. . .

</tc>

<bookmarkEnd w:id="0"/>

</w:tr>

<w:tr>

. . .

</w:tr>

</w:tbl>

colLast | 指定作为书签一部分的行中最后一列的从零开始的索引。如果出现此属性，则必须也出现colFirst属性。参见上面的colFirst讨论。

bookmarkEnd元素具有以下属性。

| 属性 | 描述                                                              |
| ---- | ----------------------------------------------------------------- |
| id   | 指定书签的唯一标识符。该值必须与bookmarkStart元素的相应id值匹配。 |

### 相关HTML属性：

<p><a href="#myAnchor">此链接指向上面书签标题处的锚点。</a></p>

<div><a name="myAnchor">书签</a></div>

HTML 示例：

此链接指向上面书签标题处的锚点。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
