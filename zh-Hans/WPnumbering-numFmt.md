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

# 文字处理编号

定义特定级别 - 编号格式

级别上使用的编号格式通过<w:numFmt w:val=" "/>元素指定。val属性中的所有文本都被视为要在每个实例中出现的字面文本，除了任何百分号(%)后跟数字的使用。该百分号-数字组合表示要使用其编号的级别的索引。索引是基于1的（从1开始）。因此，例如，%2表示应使用第二级别(w:lvl w:ilvl="1")上使用的符号/数字/字母。

在下面的示例中，第一级别使用罗马数字作为编号符号，第二级别使用大写字母，第三级别则结合了文本、前一级别的符号，以及连字符和为该级别指定的符号（十进制数字）。

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperRoman"/>

<w:pStyle w:val="Heading1"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="0" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="1">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:pStyle w:val="Heading2"/>

<w:lvlText w:val="%2."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="2">

<w:start w:val="1"/>

<w:numFmt w:val="decimal"/>

<w:pStyle w:val="Heading3"/>

<w:lvlText w:val="Sub %1-%2-%3. "/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="1440" w:firstLine="0"/>

</w:pPr>

</w:lvl>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.12。

Word 2007 示例：

![Numbering Level Text](images\wp-numbering-lvlText-1.gif)

---

### 属性：

| 属性 | 描述                         |
| ---- | ---------------------------- |
| val  | 指定编号格式。最常用的值是： |

- 项目符号
- cardinalText - 运行语言的基本数词文本。（在英语中，One、Two、Three等）
- chicago - 来自芝加哥手册的符号集。（例如，\*、†、‡、§）
- decimal - 十进制编号（1、2、3、4等）
- decimalEnclosedCircle - 圆圈包围的十进制数字
- decimalEnclosedFullstop - 后跟句点的十进制数字
- decimalEnclosedParen - 括号包围的十进制数字
- decimalZero - 十进制数字，但在1到9的数字前加零
- lowerLetter - 基于运行语言（例如，a、b、c等）。对于大于字母表大小的值，字母会重复
- lowerRoman - 小写罗马数字（i、ii、iii、iv等）
- 无
- ordinalText - 运行语言的序数文本。（在英语中，First、Second、Third等）
- upperLetter - 基于运行语言（例如，A、B、C等）。对于大于字母表大小的值，字母会重复
- upperRoman - 大写罗马数字（I、II、III、IV等）

format | 使用XSLT格式属性指定自定义格式。例如，值&#x30A2表示应使用片假名编号。![](images/versionConflict3.png)注意：在2006版本的标准中，不支持此属性。

### 相关HTML/CSS属性：

没有直接的对应属性可以从文本和上级符号构建级别或编号符号。每个级别都独立于所有其他级别。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
