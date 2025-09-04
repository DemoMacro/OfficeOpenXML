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

# 文字处理页眉

相关Open Office/ODF讨论

概述

可以为节指定页眉。参见[节](WPsection.md)。每个节可以为首页、奇数页和偶数页设置不同的页眉。每个页眉在包内的Header部分中指定。每个Header部分是主文档部分的部件关系项(document.xml.rels)中显式关系的目标。也就是说，每个页眉将包含在包内的单独文件中，这些文件将在document.xml.rels中被引用。词汇表也可以有页眉，因此词汇表也可能有页眉的显式关系。

以下是document.xml.rels中节的第一页页眉和所有其他页的默认页眉的关系。

<Relationships xmls="...">

<Relationship Id="rId6" Type="http://.../footer" Target="header1.xml"/>

<Relationship Id="rId8" Type="http://.../footer" Target="header2.xml"/>

</Relationships>

文档通过节的sectPr元素内的headerReference元素引用页眉。参见[节](WPsection.md)和[节 - 页眉](WPsectionHeaderReference.md)。

<w:sectPr>

. . .

<w:headerReference r:id="rId8" w:type="first"/>

<w:headerReference r:id="rId6" w:type="default"/>

. . .

</w:sectPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 11.3.9。

Header部分有一个hdr根元素，它指定引用该Header部分的任何页眉的内容。hdr元素的内容类似于body元素的内容，并包含可以作为段落的同级元素存在的块级标记。以下是节的第一页页眉的示例页眉。

以下是header1.xml Header部分的内容。

<w:hdr xmlns:ve= … >

<w:p>

<w:pPr>

<w:pStyle w:val="Header"/>

</w:pPr>

<w:r&gt

<w:t>默认页眉</w:t>

</w:r&gt

</w:p>

</w:hdr>

以下是header2.xml Header部分的内容。

<w:hdr xmlns:ve= … >

<w:p>

<w:pPr>

<w:pStyle w:val="Header"/>

</w:pPr>

<w:r&gt

<w:t>首页页眉</w:t>

</w:r&gt

</w:p>

</w:hdr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.4。

Word 2007 示例：

![Footers](images\wp-footers-1.gif)

---

### 元素：

以下是ftr的最重要的子元素。

| 元素 | 描述                                                                                                           |
| ---- | -------------------------------------------------------------------------------------------------------------- |
| p    | 指定内容段落。参见[段落](WPparagraph.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.22。 |
| tbl  | 指定表格的内容。参见[表格](WPtable.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.38。     |

---

---

# 相关开放文档格式(ODF)属性：

ODF格式中的页眉是通过样式部分的<style:master-page>元素内的<style:header>元素定义的。<style:header>可以包含<table:table>、<text:h>、<text:list>、<text:p>、<text:section>或<text:table-of-content>等元素。请注意，如果左页的页眉内容与右页不同，则还有一个<style:header-left>元素也可以位于<style:master-page>内。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 16.10。

<office:master-styles>

<style:master-page style:name="Standard" style:page-layout-name="Mpm1">

<style:header>

<text:p text:style-name="Header">我的示例文档页眉</text:p>

</style:header>

<style:footer>

<text:p text:style-name="Footer">我的示例文档页脚</text:p>

</style:footer>

</style:master-page>

</office:master-styles>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
