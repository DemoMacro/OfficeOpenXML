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

缩进

要在表格前缘（从左到右表格中的左边缘）之前添加的缩进是通过<w:tblPr>元素内的<w:tblInd>元素指定的。

![](images/note.png)注意：此属性不影响表格单元格内文本的缩进。但是，对齐方式(<w:jc>)确实会影响表格缩进。例如，任何右对齐的行都会导致表格忽略任何指定的缩进。

<w:tblPr>

<w:jc w:val="start"/>

<w:tblInd w:w="2160" w:type="dxa"/>

</w:tblPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.4.51。

Word 2007示例：

![Table Indent](images/wp-tableIndent-1.gif)

---

### 属性：

属性如下：

| 属性 | 描述                                                                                                                            |
| ---- | ------------------------------------------------------------------------------------------------------------------------------- |
| w    | 指定缩进宽度的值。表格将按指定量向文本边距内移动。![](images/versionConflict3.png)注意：2006版本的OOXML标准指定的是val而不是w。 |
| type | 指定宽度(w)属性的单位。可能的值有：                                                                                             |

- dxa \- 指定值以点的二十分之一（1/1440英寸）为单位
- nil \- 指定值为零

如果指定了pct或auto，该值将被忽略。

---

# 相关开放文档格式(ODF)属性：

表格的缩进可以通过几种不同的方式指定。当然，可以将表格宽度设置为小于页面的完整宽度，然后根据缩进应该在左侧还是右侧，将表格对齐方式设置为左对齐或右对齐。例如，要在7英寸的页面上实现左侧2英寸的边距，可以将表格宽度设置为5英寸，并将表格对齐方式设置为右对齐。

<style:style style:name="Table1" style:family="table">

<style:table-properties style:width="5in" table:align="right"/>

</style:style>

或者，可以使用应用于表格的样式的<style:table-properties>元素上的fo:margin-left属性来设置表格边距属性。可以设置以下表格边距：fo:margin、fo:margin-left、fo:margin-right、fo:margin-top、fo:margin-bottom。请注意，左对齐或居中对齐的表格会忽略右边距，而右对齐或居中对齐的表格会忽略左边距。可以设置百分比，这将引用父样式的相应边距。

<style:style style:name="Table1" style:family="table">

<style:table-properties style:width="5in" table:align="left" fo:margin-left="2in"/>

</style:style>

参考：办公应用程序开放文档格式1.2版（2011年5月）§§17.15和20.198-20:202。

# 相关HTML/CSS属性：

<table style="width: 100%; margin-left:50px;">

. . .

</table>

CSS示例：

我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。过去隐藏在领域之外的某个地方，超出智力的范围，在我们不怀疑的某个物质对象（在该物质对象将给我们的感觉中）中。

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |

至于那个物体，在我们自己必须死去之前，我们是否会偶然发现它，这取决于机会。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有©2023。保留所有权利。
