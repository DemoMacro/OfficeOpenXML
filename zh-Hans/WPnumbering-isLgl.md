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

定义特定级别 - 仅显示为数字

通过在级别定义中包含<w:isLgl>元素，可以将给定级别的编号格式设置为阿拉伯数字。<w:isLgl>元素指定此级别的编号格式应为十进制格式，无论<numFmt>元素中指定了什么。例如，以下是编号定义中第四级别的定义。

<w:lvl w:ilvl="3">

<w:start w:val="1"/>

<w:numFmt w:val="lowerLetter"/>

<w:lvlText w:val="%4."/>

<w:lvlJc w:val="start"/>

<w:pStyle w:val="Heading4"/>

<w:pPr>

<w:ind w:start="2160" w:firstLine="0"/>

</w:pPr>

</w:lvl>

Word 2007 示例：

以下是上面定义的级别（没有isLgl）的外观：

![isLgl Numbering Scheme for Outline](images\wp-numberingLvl-1.gif)

---

通过添加isLgl，我们得到以下内容：

<w:lvl w:ilvl="3">

<w:start w:val="1"/>

<w:numFmt w:val="lowerLetter"/>

<w:isLgl/>

<w:lvlText w:val="%4."/>

<w:lvlJc w:val="start"/>

<w:pStyle w:val="Heading4"/>

<w:pPr>

<w:ind w:start="2160" w:firstLine="0"/>

</w:pPr>

</w:lvl>

Word 2007 示例：

![abstractNum Numbering Scheme for Outline](images\wp-numberingLvl-2.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.9.4。

---

# 相关开放文档格式(ODF)属性：

列表中给定级别的编号格式由应用于列表的<text:list-style>内定义的级别的<text:list-level-style-number>元素中的style:num-format属性指定。

参考：办公应用程序开放文档格式1.2版（2011年5月）§16.32和§19.500。

以下示例将列表的第4级格式定义为阿拉伯数字。

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

style:num-format的可能属性值为：1表示阿拉伯数字序列，a表示小写拉丁字母字符，A表示大写拉丁字母字符，i表示小写罗马数字，I表示大写罗马数字，字符串，或空字符串（不显示数字序列）。

# 相关HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级。

<ol>

<li style="list-style-type:upper-alpha;">这是第二级。

<ol>

<li style="list-style-type:decimal;">这是第三级。

<ol>

<li style="list-style-type:decimal;">这是第四级。</li>

</ol>

</li>

</ol>

</li>

</ol>

</li>

<li style="list-style-type:upper-roman;">这也是第一级。</li>

</ol>

HTML/CSS 示例：

1. 这是第一级。
1. 这是第二级。
1. 这是第三级。
1. 这是第四级。
1. 这也是第一级。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
