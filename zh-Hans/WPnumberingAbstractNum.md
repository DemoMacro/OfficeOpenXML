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

# 文字处理编号、级别和列表

定义整体编号方案

编号或分级方案的核心定义是在编号部分（numbering.xml）的根<w:numbering>元素内的<w:abstractNum>元素中定义的。

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="099A081C"/>

<w:multiLevelType w:val="multilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFit w:val="upperRoman"/>

<w:pStyle w:val="Heading1"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="0" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="1">

<w:start w:val="1"/>

<w:numFit w:val="upperLetter"/>

<w:pStyle w:val="Heading2"/>

<w:lvlText w:val="%2."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="2">

<w:start w:val="1"/>

<w:numFit w:val="decimal"/>

<w:pStyle w:val="Heading3"/>

<w:lvlText w:val="%3."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="1440" w:firstLine="0"/>

</w:pPr>

</w:lvl>

. . .

</w:abstractNum>

上述XML定义了一个具有多个级别（w:lvl）和类似大纲外观的分级方案，如下例所示。

Word 2007 示例：

![abstractNum Numbering Scheme for Outline](images\wp-numbering-2.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.1。

### 属性：

只有一个属性：

| 属性          | 描述                                                                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| abstractNumID | 指定一个唯一数字，将用作编号定义的标识符。该值通过编号实例（num）的abstractNumId子元素引用。<w:abstractNum w:abstractNumId="0"> . . . </w:abstractNum> |

<w:num w:numId="1"> <w:abstractNumId w:val="0"/> </w:num>

### 元素：

以下是子元素，不包括<w:tmpl>（与定义在用户界面中的显示位置相关）和nsid（与文档重新用途和更改时跟踪编号定义相关）。

| 元素           | 描述                                                                                                                                                                                                                                                                             |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| lvl            | 指定整体编号定义中特定级别的属性。请注意，lvl可以作为抽象定义的一部分（当放置在<w:abstractNum>内时），或作为抽象定义的例外（当放置在<w:num>实例的<w:lvlOverride>内时）。参见[定义特定级别](WPnumberingLvl.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.7。 |
| multiLevelType | 指定定义的编号类型—单级、多级等：<w:multiLevelType w:val="multilevel"/>。这仅由文字处理应用程序用于确定用户界面行为，并不以任何方式限制列表。因此，例如，标记为singleLevel的列表不会被阻止使用2到9级。它只有一个属性val，具有以下可能值：                                        |

- singleLevel - 指定只有一级的格式
- multiLevel - 指定多级列表，每级类型相同（项目符号或级别文本）
- hybridMultiLevel - 指定多级列表，每级可能类型不同（项目符号或级别文本）

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.13。  
name | 为抽象编号定义指定名称。它用于为定义提供用户友好的别名：<w:name w:val="示例名称"/> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.14。  
numStyleLink | 指定抽象编号定义不包含实际的编号属性，而是通过指向样式部分中的编号样式来引用要使用的属性。以下是编号部分的示例：<w:abstractNum w:abstractNumId="0"> <w:nsid w:val="099A081C"/> <w:multiLevelType w:val="multilevel"/> <w:numStyleLink w:val="TestNumberingStyle"/> </w:abstractNum> 相应的样式出现在样式部分，如下所示：<w:style w:type="numbering" w:styleId="TestNumberingStyle"> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.22。  
styleLink | 指定抽象编号定义是样式部分中引用的编号样式的基础编号定义。（由于编号定义的各个级别的样式是通过pPr元素在抽象编号定义中指定的，这些样式可以形成样式部分中编号样式的基础。）<w:numbering> . . . <w:abstractNum w:abstractNumId="5"> . . . <w:styleLink w:val="ExampleNumberingStyle"/> . . . </w:abstractNum> </w:numbering> 引用样式出现在样式部分，如下所示：<w:styles> <w:style w:type="numbering" w:styleId="ExampleNumberingStyle"> <w:name w:val="ExampleNumberingStyle"/> . . . <w:pPr> <w:numPr> <w:numId w:val="6"/> </w:numPr> </w:pPr> </w:style> </w:styles> 只有一个属性val。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.28。

### 相关HTML/CSS属性：

没有直接可比的HTML对应项。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
