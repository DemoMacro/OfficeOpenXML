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

相关Open Office/ODF讨论  
相关HTML/CSS讨论

定义特定级别

编号定义中的特定级别使用<w:lvl>元素指定。请注意，它与在num内的lvlOverride中找到的编号级别覆盖相同。<w:lvl>元素中包含该级别应显示的所有属性。

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="360" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:color w:val="31849B"/>

<w:sz w:val="28"/>

</w:rPr>

</w:lvl>

上述XML定义了编号定义中第一级别的属性。

Word 2007示例：

![lvl Numbering Level Definition](images\wp-numbering-3.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.7。

### 属性：

<w:lvl>具有以下属性（省略了与应用程序界面中显示级别相关的tplc）

| 属性      | 描述                                                                                                                                                                                                                                                                                           |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ilvl      | 指定要在编号定义中定义的级别。级别编号从0（零）开始。此属性值对应于引用编号级别的内容中出现的ilvl元素的val属性值。见下文：<w:p> <w:pPr> <w:pStyle w:val="ListParagraph"/> <w:numPr> <w:ilvl w:val="0"/> <w:numId w:val="1"/> </w:numPr> </w:pPr> <w:r> <w:t>这是第一级别。</w:t> </w:r> </w:p> |
| tentative | 表示编号级别由XML的生产者保存但未在文档中使用，因此可以在不更改文档内容的情况下重新定义。值为true（或1）或false（或0）。                                                                                                                                                                       |

### 元素：

<w:ilv>的子元素如下（省略用于向后兼容的legacy）。

| 元素           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| isLgl          | 指定此级别的编号格式应为十进制格式，无论numFmt元素中指定了什么。参见[编号 - 定义特定级别 - 仅显示为数字](WPnumbering-isLgl.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.4。                                                                                                                                                                                                                                                                                                                                                                                 |
| lvlJc          | 指定编号级别文本（例如项目符号、数字或其他符号）相对于父段落的文本边距的对齐方式。参见[编号 - 定义特定级别 - 对齐方式](WPnumbering-lvlJc.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.16。                                                                                                                                                                                                                                                                                                                                                                  |
| lvlPicBulletId | 指定要用作给定编号级别的编号符号的图片。参见[编号 - 定义特定级别 - 图片或图像作为编号符号](WPnumbering-imagesAsSymbol.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.9。                                                                                                                                                                                                                                                                                                                                                                                      |
| lvlRestart     | 指定编号应在此级别重新开始的时间。参见[编号 - 定义特定级别 - 重新开始编号](WPnumbering-restart.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.11。                                                                                                                                                                                                                                                                                                                                                                                                            |
| lvlText        | 指定要在该级别显示的文本内容。参见[编号 - 定义特定级别 - 编号级别文本](WPnumberingLevelText.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.12。                                                                                                                                                                                                                                                                                                                                                                                                               |
| numFmt         | 指定要在该级别显示的编号格式。参见[编号 - 定义特定级别 - 编号格式](WPnumbering-numFmt.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.18。                                                                                                                                                                                                                                                                                                                                                                                                                     |
| pPr            | 指定要应用于该级别的段落属性。在lvl元素（在编号部分内）中定义的属性可以被段落本身（在文档部分内）中的段落属性覆盖。有关指定段落属性的详细信息，请参见[段落 - 属性](WPparagraphProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.23。                                                                                                                                                                                                                                                                                                                  |
| pStyle         | 指定要应用于该级别的段落样式的名称。它有一个单一属性val，它是在样式部分中定义的段落样式的ID。请注意，pPr可以引用编号定义（numId）和级别（ilvl），如下所示。<w:pPr> <w:numPr> <w:ilvl w:val="0"/> <w:numId w:val="0"/> </w:numPr> </w:pPr> 这将产生冲突，因为编号定义中的lvl将具有属性，而段落的引用段落样式也将具有属性。<w:abstractNum w:abstractNumId="1"> <w:lvl w:ilvl="0"> <w:pPr> . . . <w:pPr> . . . </w:lvl> . . . </w:abstractNum> 在这种情况下，由numPr定义的级别被忽略，编号定义中定义的级别占优势。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.24。 |
| rPr            | 指定要应用于lvlText元素中指定的编号级别文本的运行属性。![](images/note.png)注意：请理解这仅影响级别的数字或符号的文本，而不影响段落运行中的文本。<w:rPr> <w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/> <w:color w:val="C00000"/> <w:sz w:val="28"/> </w:rPr>                                                                                                                                                                                                                                                                                                          |

| ![编号运行属性](images\wp-numbering-rPr.gif)

---

有关指定文本属性的详细信息，请参见[文本 - 属性](WPtextFormatting.md)。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.25。

start | 指定编号的起始值，包括文档启动时和级别编号重新开始时。它有一个属性val，它是一个十进制数。实际输出取决于numFmt元素。例如，对于<w:numFmt w:val="UpperRoman"/>和<w:start w:val="2"/>，此级别第一次出现的编号输出将是II。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.26。  
suff | 指定出现在编号符号和段落文本之间的字符。例如，<w:suff w:val="space"/>。它只有一个属性val，它指定跟随编号符号的字符。以下是可能的值。如果省略该元素，则假定值为制表符。

- 无
- 空格
- 制表符

在下面的示例中，第一级别的suff值为无，第二级别的值为空格，第三级别的值为制表符。| ![编号符号和段落文本之间的编号级别内容](images\wp-numbering-suff.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.29。

---

# 相关开放文档格式(ODF)属性：

在ODF中，特定级别的格式在列表的样式内定义。实际级别由<text:list>元素的嵌套级别确定。例如，<text:list>内的<text:list>是第2级别。列表的样式在<text:list-style>元素内指定。有三种不同的列表样式元素，取决于列表级别是具有包含列表编号、项目符号还是图像的列表标签。

对于具有编号标签的级别，<text:list-style>内特定级别的样式在<text:list-level-style-number>元素内指定。<text:list-style>元素将包含多个<text:list-level-style-number>元素—每个可能的级别一个。

对于具有项目符号标签的级别，特定级别的样式在<text:list-level-style-bullet>元素内指定。对于具有图像标签的级别，特定级别的样式在<text:list-level-style-image>元素内指定。

参考：办公应用程序开放文档格式1.2版（2011年5月）§§16.31（以项目符号为标签的级别）、16.32（以编号为标签的级别）和16.33（以图像为标签的级别）。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L3"/>

<text:list-style style:name="L3">

. . .

<text:list-level-style-number text:level="2" text:style-name="Numbering_20_Symbols" style:num-prefix=" " style:num-suffix="." style:num-format="A">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="0.75in" fo:text-indent="-0.25in" fo:margin-left="0.75in"/>

</style:list-level-properties>

</text:list-level-style-number>

. . .

</text:list-style>

# 相关HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级别。</li>

<li style="list-style-type:upper-alpha; margin-left:2cm;">这是第二级别。</li>

<li style="list-style-type:decimal; margin-left:4cm;">这是第三级别。</li>

</ol>

HTML/CSS示例：

1.这是第一级别。2.这是第二级别。3.这是第三级别。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有©2023。保留所有权利。
