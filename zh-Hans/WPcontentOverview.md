![OfficeOpenXML.com](images/banner1.png)

[主页](index.md) | [Docx文件解剖](anatomyofOOXML.md) | [示例Docx视图](WPsampleDoc.md)

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

# WordprocessingML内容概述

WordprocessingML文档是一个包含许多不同部分（主要是XML文件）的包。然而，大多数实际内容位于主文档部分中。该内容主要由段落和表格组成。

### 段落

段落（<w:p>）是块级内容的基本单位。也就是说，它是在新行开始的内容划分。它通常有两部分。首先声明段落的格式（或属性），然后是内容。

格式可以直接声明（"此段落应居中"），也可以通过引用样式间接声明（"此段落应使用X样式，该样式使段落居中"）。或者它可以两者结合使用。段落格式在<w:pPr>内。

段落的内容包含在一个或多个运行（<w:r>）中。运行是非块级内容；它们定义不一定在新行开始的文本区域。与段落一样，它们由格式/属性定义组成，后跟内容。格式在<w:rPr>中指定，可以是直接格式，通过样式引用的间接格式，或两者兼有。

一个运行可以分成更小的运行，或者如果它们具有相同的属性，则可以合并运行。因此，例如，如果一个句子包含一个粗体单词，那么该句子必须分成多个运行，以考虑句子的粗体和非粗体部分。

运行的内容主要由文本元素（<w:t>）组成，这些元素本身包含构成读取内容的实际字符数据。运行还可能包含分隔符、制表符、符号、图像和域。下面是一个非常简单的段落示例。

<w:p>

<w:pPr>

<w:jc w:val="center">

<w:pPr>

<w:r>

<w:rPr>

<w:b/>

</w:rPr>

<w:t>这是文本。</w:t>

</w:r>

</w:p>

从上面的示例以及您将在此站点上看到的几乎所有示例XML中省略的是可用于跟踪编辑会话的可选信息。此类信息通常以属性形式存在，会使您在查看Word文档底层XML时看到的XML变得杂乱。为清晰起见，此处省略了这些信息。示例如下所示。

<w:p w:rsidR="00D57EDE" w:rsidRDefault="00D57EDE">

. . .

</w:p>

### 表格

表格是另一种类型的块级内容。表格由行和列组成。表格（<w:tbl>）的规范可以分为三部分。与段落和运行一样，首先是属性，对于表格，它们在<w:tblPr>中定义。

然而，与段落和运行不同，表格将内容分成行，并且不需要任何两行具有相同数量的列。这为表格的定义增加了一层复杂性。WordprocessingML通过在<w:tblGrid>中为表格定义"网格"来解决这一挑战。此表格网格定义是表格定义的第二部分。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
