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

概述

域是一种将可变数据插入文档的方法—这些数据如日期、页码、表格或图表的数量。它们本质上是可变数据的占位符，它们指示处理应用程序自动将文本、图形、页码和其他材料插入文档中。插入的文本、图形或其他内容被称为域结果。域结果的默认值是空字符串。执行域指令的行为被称为域更新。

域在XML中可以使用<w:fldSimple>元素表示为简单域，或者使用一组涉及<w:fldChar>和<w:instrText>元素的运行(<w:r>)表示为复杂域。每个简单域都可以实现为复杂域，但并非每个复杂域都可以实现为简单域。如果域中的某些字符具有与其他字符不同的运行属性，则该域必须使用多个运行实现，这需要一个复杂域。

### 简单域

简单域使用<w:fldSimple>元素放置在文档中，通常在段落<w:p>元素内。域插入的数据类型（即域功能）和格式由<w:instr>属性指定。<w:fldSimple>元素将包含一个运行，其中包含上次更新域时的域值的缓存版本。当更新简单域时，其子元素将被替换为适当的WordProcessingML形式的更新值。以下是文档作者姓名的简单域示例。

<w:fldSimple w:instr="AUTHOR">

<w:r>

<w:t>马塞尔·普鲁斯特</w:t>

</w:r>

</w:fldSimple>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.19。

### <w:fldSimple>的子元素：

最常用的子元素如下。

| 元素          | 描述                                                                                                                                            |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| bookmarkEnd   | 指定书签的开始。参见[书签](WPbookmark.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.13.6.1。                                 |
| bookmarkStart | 指定书签的结束。参见[书签](WPbookmark.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.13.6.2。                                 |
| fldSimple     | 简单域可以嵌套在其他简单域内—例如，当使用IF语句时，它包含另一个域功能。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.19。      |
| hyperlink     | 指定内部或外部链接。参见[超链接](WPhyperlink.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.22。                           |
| r             | 指定文本运行。这将包含上次更新域时的域值的缓存版本。参见[文本](WPtext.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.25。 |

### <w:fldSimple>的属性：

| 属性    | 描述                                                                                                                   |
| ------- | ---------------------------------------------------------------------------------------------------------------------- |
| dirty   | 指定应用程序已将该域标记为不是最新的，并且该域需要在再次显示之前更新。它可以是true或false，如果不存在，则假定为false。 |
| fldLock | 指定不应更新该域。它可以是true或false，如果不存在，则假定为false。                                                     |
| instr   | 指定将生成动态数据的简单域的域代码。参见[域指令](WPfieldInstructions.md)。                                             |

### 复杂域

当由于格式差异而需要多个运行时，使用复杂域。它们可以跨越多个段落或运行。目录是复杂域的一个很好的例子，因为它由多个具有不同格式的段落组成。

复杂域由一系列运行组成，这些运行共同包含以下元素，顺序如下所述。

- 一个属性fldCharType值为begin的<w:fldChar>元素。
- 一个或多个<w:instrText>元素，它们共同包含一个完整的域。
- 可选地，一个属性fldCharType值为separate的<w:fldChar>元素，它将域与其域结果分开。
- 任意数量的包含最近更新的域结果的运行和段落。
- 一个属性fldCharType值为end的<w:fldChar>。

以下是DATE域的复杂域实现。

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> DATE </w:instrText>

</w:r>

<w:r>

<w:fldChar w:fldCharType="separate"/>

</w:r>

<w:r>

<w:t>2005/12/31</w:t>

</w:r>

<w:r>

<w:fldChar w:fldCharType="end"/>

</w:r>

### 复杂域的组成元素

| 元素    | 描述                                                                                                                    |
| ------- | ----------------------------------------------------------------------------------------------------------------------- |
| fldChar | 指定复杂域的开始或结束，或将域功能或代码与结果分开。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.18。 |

### <w:fldChar>的属性：

| 属性        | 描述                                                                                                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| dirty       | 指定应用程序已将该域标记为不是最新的，并且该域需要在再次显示之前更新。它可以是true或false，如果不存在，则假定为false。如果fldCharType属性的值不是start，则忽略此属性。 |
| fldCharType | 指定复杂域字符的类型。可能的值是                                                                                                                                       |

- begin - 标记复杂域的开始
- end - 标记复杂域的结束
- separate - 指定该字符是分隔符字符，它定义域代码或功能的结束和域结果的开始。

fldLock | 指定不应更新该域。它可以是true或false，如果不存在，则假定为false。  
instrText | 指定运行包含域代码。有关指定域代码的详细信息，请参见[域指令](WPfieldInstructions.md)。请注意，如果此元素位于不属于复杂域代码的运行中，则它及其内容将被视为常规文本。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.23。

### 相关CSS属性：

HTML/CSS中没有域的概念。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
