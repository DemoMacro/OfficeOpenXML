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

# 文字处理文档

<w:document> 元素是主要内容部分的根元素。

<w:document>

<w:body>

<w:p/>

</w:body>

</w:document>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 §§ 17.2.3。

### 元素：

<w:document> 元素可以包含以下元素。

| 元素       | 描述                                                                                                                                                                          |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |
| background | 指定文档每一页的背景。背景可以是DrawingML对象或纯色。如果是DrawingML对象，则background元素包含一个drawing元素。如果使用纯色，则background是一个空元素，颜色在以下属性中指定。 | 属性 | 描述 |
| ---        | ---                                                                                                                                                                           |
| color      | 指定颜色。可能的值是十六进制编码的RGB值（RRGGBB格式）或auto。例如，<w:background w:color="2C34FF"/>                                                                           |
| themeColor | 指定基本主题颜色（在主题部分中指定）。例如，<w:background w:themeColor="accent5"/>                                                                                            |
| themeShade | 指定应用于主题颜色的阴影值（0-255值的十六进制编码）。例如，<w:background w:themeColor="accent2" w:themeShade="BF"/>                                                           |
| themeTint  | 指定应用于主题颜色的色调值（0-255值的十六进制编码）。例如，<w:background w:themeColor="accent2" w:themeTint="99"/>                                                            |

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.2.1。

body | 指定文档正文的内容。它没有属性。它可以包含多个元素，大多数与跟踪更改和添加客户XML相关。核心元素如下所列。

### 元素：

| 元素   | 描述                                                                                                             |
| ------ | ---------------------------------------------------------------------------------------------------------------- |
| p      | 指定内容段落。参见[段落](WPparagraph.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.22。   |
| sectPr | 指定最后一节的节属性。参见[节](WPsection.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.17。 |
| tbl    | 指定表格。参见[表格](WPtable.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.38。             |

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.2.2。

### 属性：

<w:document> 有一个单一属性：

| 属性        | 描述                                 |
| ----------- | ------------------------------------ |
| conformance | 指定文档符合的一致性类。可能的值是： |

- strict \- 文档符合Office Open XML Strict
- transitional \- 文档符合Office Open XML Transitional。这是默认值。

### 相关HTML元素：

<html>

<head>

...

</head>

<body>

...

</body>

</html>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
