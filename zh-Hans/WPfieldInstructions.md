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

# 文字处理域

指令

域在XML中以<w:fldSimple>（用于简单域）或一对<w:fldSimple>元素（用于复杂域）的形式放置。但域类型和格式的实际定义由简单域的instr属性或<w:instrText>元素指定。域定义的语法不遵循XML标准，而是通过域名或关键字后跟零个或多个影响结果格式设置的开关来指定域。下面是一个日期域的示例。

DATE \@ "M/d/yyyy h:mm am/pm"

这会产生以下结果示例：2006年1月3日 下午5:28。

### 域类型

OOXML规范将域分为10个功能类别：

- 日期和时间 - [DATE](WPfieldDefinitions.md#date), [CREATEDATE](WPfieldDefinitions.md#createdate), EDITTIME, PRINTDATE, [SAVEDATE](WPfieldDefinitions.md#savedate), [TIME](WPfieldDefinitions.md#time)
- 文档自动化 - COMPARE, DOCVARIABLE, GOTOBUTTON, IF, MACROBUTTON, PRINT
- 文档信息 - [AUTHOR](WPfieldDefinitions.md#author), COMMENTS, DOCPROPERTY, [FILENAME](WPfieldDefinitions.md#filename), [FILESIZE](WPfieldDefinitions.md#filesize), KEYWORDS, LASTSAVEDBY, NUMCHARS, NUMPAGES, NUMWORDS, SUBJECT, TEMPLATE, [TITLE](WPfieldDefinitions.md#title)
- 方程和公式 - _=formula_ , ADVANCE, SYMBOL
- 表单域 - FORMCHECKBOX, FORMDROPDOWN, FORMTEXT
- 索引和表格 - INDEX, RD（标识创建目录、引文表或索引时要包含的文件），TA（引文表条目的文本和页码），TC（目录条目的文本和页码），[TOC](WPtableOfContents.md)（目录），XE（索引条目的文本和页码）
- 链接和引用 - AUTOTEXT, AUTOTEXTLIST, BIBLIOGRAPHY, CITATION, HYPERLINK, INCLUDEPICTURE, INCLUDETEXT, LINK, NOTEREF, PAGEREF, QUOTE, REF, STYLEREF
- 邮件合并 - ADDRESSBLOCK, ASK, COMPARE, DATABASE, FILLIN, GREETINGLINE, IF, MERGEFIELD, MERGEREC, MERGESEQ, NEXT, NEXTIF,SET, SKIPIF
- 编号 - LISTNUM, [PAGE](WPfieldDefinitions.md#page), REVNUM, [SECTION](WPfieldDefinitions.md#section), SECTIONPAGES, [SEQ](WPfieldDefinitions.md#seq)
- 用户信息 - USERADDRESS, USERINITIALS, [USERNAME](WPfieldDefinitions.md#username)

### 域格式

域的格式由域名后放置的开关指定。有三种常规开关类型：

- 日期和时间 \- 适用于与日期和时间相关的域。格式为：

\@ _开关参数_

例如，DATE \@ "yyyy-MM-dd"。有关开关的详细信息，请参阅[日期和时间域格式开关](WPdateTimeFieldSwitches.md)。

- 数字 \- 适用于数字结果。格式为：

\\# _开关参数_

如果没有开关，结果将不带前导空格或尾随小数零进行格式设置。有关详细信息，请参阅[数字域格式开关](WPnumericFieldSwitches.md)。

- 常规格式 \- 适用于各种数字或文本结果。格式为：

\\\* _开关参数_

有关详细信息，请参阅[常规格式域开关](WPgeneralFieldSwitches.md)。

此外，每个域可能都有自己的开关。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.4。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
