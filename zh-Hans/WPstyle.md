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

# 文字处理样式

定义样式

样式部分中的单个样式使用<w:style>元素指定。样式定义可以分为三个组成部分：常规样式属性、样式类型和样式的格式属性。

常规样式属性是所有样式类型共有的属性集合—如样式名称、别名、ID等。有关这些属性的更多信息，请参见[样式 - 常规样式属性](WPstyleGenProps.md)。

样式可以是四种不同样式类型之一：

- 段落样式
- 字符样式
- 编号样式
- 表格样式

还有默认段落和字符样式（由docDefaults定义），以及链接样式（段落样式和字符样式的组合）。

<w:style w:type="paragraph" w:styleId="Heading1">

<w:name w:val="标题 1"/>

<w:basedOn w:val="正文"/>

<w:next w:val="正文"/>

<w:link w:val="标题1字符"/>

<w:uiPriority w:val="9"/>

<w:qFormat/>

<w:pPr>

<w:keepNext/>

<w:keepLines/>

<w:numPr>

<w:numId w:val="2"/>

</w:numPr>

<w:spacing w:before="480" w:after="0"/>

<w:outlineLvl w:val="0"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:b/>

<w:color w:val="365F91"/>

<w:sz w:val="28"/>

</w:rPr>

</w:style>

上述XML定义了一个段落样式；它也是一个链接样式。常规属性以蓝色显示。类型以绿色显示。格式属性以橙色显示。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.17。

### 属性：

<w:style>具有以下属性。

| 属性        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| customStyle | 指定样式是用户定义的，不是由应用程序自动生成的。它可以是true（或1）或false（或0）。如果为true，则应用程序不能自动更改与样式关联的格式。例如，<w:style w:type="paragraph" w:styleId="MyStyle" w:customStyle="true">。                                                                                                                                                                                                                 |
| default     | 指示样式是该样式类型的默认样式。当内容未引用该类型的样式时，将使用此样式。如果多个样式指定了此属性，则将使用最后一个实例。例如，<w:style w:type="paragraph" w:default="1" w:styleId="MyStyle">。                                                                                                                                                                                                                                     |
| styleId     | 指定样式的唯一标识符。它在整个文档中用于在内容中应用样式，链接段落和字符样式，以及通过basedOn元素引用父样式进行继承。例如，样式<w:style w:type="paragraph" w:styleId="MyStyle">将通过以下引用应用于文档内容中的段落：<w:p> <w:pPr> <w:pStyle w:val="MyStyle"/> </w:pPr> </w:p> 如果多个样式使用相同的styleId值，则第一个实例保留其ID，所有其他实例将以应用程序选择的任何方式重新分配。（但是，对重新分配的样式的引用将不会被修复。） |
| type        | 指定样式的类型。可能的值有：                                                                                                                                                                                                                                                                                                                                                                                                         |

- 字符
- 编号
- 段落
- 表格

### 元素：

<w:style>的子元素可以是常规样式属性或格式样式属性。有关常规样式属性的详细信息，请参见[定义样式 - 常规属性](WPstyleGenProps.md)。

格式样式属性不是所有样式共有的常规属性，而是指定段落、字符、表格或编号段落的格式。有关这些样式类型的详细信息，请参见：

- [定义样式 - 字符属性](WPstyleCharStyles.md)
- [定义样式 - 段落属性](WPstyleParStyles.md)
- [定义样式 - 表格属性](WPstyleTableStyles.md)
- [定义样式 - 编号属性](WPstyleNumStyles.md)

### 相关HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级。</li>

<li style="list-style-type:upper-alpha; margin-left:2cm;">这是第二级。</li>

<li style="list-style-type:decimal; margin-left:4cm;">这是第三级。</li>

</ol>

HTML/CSS示例：

1. 这是第一级。
2. 这是第二级。
3. 这是第三级。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
