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

相关Open Office/ODF讨论  
相关HTML/CSS讨论

定义特定级别 - 编号级别文本

在级别上显示的文本由<w:lvlText w:val=" "/>元素指定。val属性中的所有文本都被视为要在每个实例中出现的字面文本，除了任何使用百分号(%)后跟数字的情况。该百分号-数字组合表示要使用其编号的级别的索引。索引是从1开始的（以1开始）。因此，例如，%2表示应使用第二级别(w:lvl w:ilvl="1")上使用的符号/数字/字母。

在下面的示例中，第一级别使用罗马数字作为编号符号，第二级别使用大写字母，第三级别包含文本、前一级别符号以及连字符和为该级别指定的符号（十进制数字）。

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

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.12。

Word 2007示例：

![Numbering Level Text](images\wp-numbering-lvlText-1.gif)

---

### 属性：

| 属性 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| null | 指定应将空字符用作编号符号：<w:lvlText w:null="1"/>。可能的值为true（或1）或false（或0）。请注意，将其设置为true将意味着使用空字符，而不是空字符串。                                                                                                                                                                                                                                                                                                                                                                          |
| val  | 指定在内容中引用时要用于编号级别的文本。如果未指定值，则使用空字符串。可以使用百分号-数字组合（例如，%2）来包含更高级别的编号。在这种情况下，数字表示要使用其编号符号的级别的索引。索引是从1开始的（以1开始）。因此，%2将包含第二级别的符号。请注意，正在定义的级别（例如级别x）通常会以某种方式使用%x包含其自己的级别编号。这将根据为该级别的numFmt格式指定的内容以及自该级别重新开始编号以来出现的次数输出适当的数字。因此，如果级别x指定%x且numFmt为upperLetter，并且它是内容中该级别的第五次出现，则该级别的输出将为"E"。 |

---

# 相关开放文档格式(ODF)属性：

在编号或项目符号列表项中或在大纲标题中使用的文本由应用于列表的<text:list-style>中定义的级别或应用于标题的大纲样式的<text:list-level-style-number>、<text:list-level-style-bullet>或<text:outline-level-style>元素中的style:num-prefix、style:num-suffix和style:num-format属性指定。

参考：办公应用程序开放文档格式1.2版（2011年5月）§§19.502（前缀）、19.503（后缀）和19.500（数字格式）。

以下示例将列表的第4级别的文本定义为阿拉伯数字后跟右括号—例如，1)、2)等。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L3"/>

<text:list-style style:name="L3">

. . .

<text:list-level-style-number text:level="4" style:num-suffix=")" style:num-format="1">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="1.25in" fo:text-indent="-0.25in" fo:margin-left="1.25in"/>

</style:list-level-properties>

</text:list-level-style-number>

. . .

</text:list-style>

实际可变数字或项目符号字符的格式分别由style:num-format或style:bullet-char属性指定。有关style:num-format属性的更多信息，请参见[定义特定级别 - 仅显示为数字](WPnumbering-isLgl.md)中的ODF讨论。数字或项目符号字符的前缀和后缀使用style:num-prefix和style:num-suffix值的字面文本指定。

# 相关HTML/CSS属性：

没有直接的对应项可以从文本和更高级别符号构建级别或编号符号。每个级别都独立于所有其他级别。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有©2023。保留所有权利。
