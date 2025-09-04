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

# 文字处理表格

相关Open Office/ODF讨论  
相关HTML/CSS讨论

网格/列定义

表格的列由<w:tblGrid>元素定义。<w:tblGrid>包含表格中每个可能的单元格大小（有时称为逻辑列）的<w:gridCol>元素。表格的<w:tblGrid>所需的<w:gridCol>元素数量是通过延伸每个单元格的垂直边框并计算线条定义的列总数来确定的。例如，下面的表格有三列，需要在其<w:tblGrid>中有3个<w:gridCol>元素。

Word 2007示例：

![Table Grid](images\wp-tableGrid-3.gif)

---

此表格的<w:tblGrid>如下：

<w:tblGrid>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2880"/>

</w:tblGrid>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.49。

当单元格在行与行之间的长度不相等时，情况变得更加复杂。例如，下面的表格有五列，因此在其<w:tblGrid>元素中需要5个<w:gridCol>元素。

Word 2007示例：

![Table Grid](images\wp-tableGrid-1.gif)

---

此表格的<w:tblGrid>如下：

<w:tblGrid>

</w:gridCol w:w="1638"/>

</w:gridCol w:w="1242"/>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2178"/>

</w:gridCol w:w="702"/>

</w:tblGrid>

![](images/note.png)注意：每个单元格的宽度(<w:tcW>)将等于其中一个<w:gridCol>元素值，或者当表格不是自动调整大小时，将是两个或多个值的总和。

考虑上面表格中的第一行。它看起来像这样：

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>AAA</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="5058" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>BBB</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="702" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>CCC</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

### 元素：

<w:tblGrid>元素包含一个或多个<w:gridCol>元素。（用于跟踪修订的<w:tblGridChange>元素已被省略。）

| 元素    | 描述                               |
| ------- | ---------------------------------- |
| gridCol | 指定单个网格列的详细信息。属性为： |

- <w:w> \— 以点的二十分之一指定列的宽度。然而，仅此一项并不能确定实际宽度。当表格显示时，它可能会被表格布局算法或作为列一部分的特定单元格的首选宽度所覆盖。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.16。

### 单元格跨越

内容为"AAA"的第一个单元格跨越前两个逻辑列，因此宽度是第一个和第二个<w:gridCol>元素值的总和（1638 + 1242 = 2880）。请注意，<w:gridSpan>值为2，表示该单元格跨越两个逻辑列。内容为"BBB"的第二个单元格跨越第三和第四个逻辑列，因此宽度是第三和第四个<w:gridCol>元素值的总和（2880 + 2178 = 5058）。<w:gridSpan>值也是2。

<w:gridSpan>表示一个单元格水平跨越多个逻辑单元格（由<w:tblGrid>定义，类似于放置在单元格上的HTML colspan属性。单元格也可以使用<w:tcPr>元素中的<w:vMerge>元素/属性垂直跨越。

Word 2007示例：

![Table Grid](images\wp-tableGrid-5.gif)

---

最后两行如下所示。

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="1638" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>DDD</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="4122" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>EEE</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:vMerge w:val="restart"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>FFF</w:t>

</w:r>

</w:p>

<w:p>

<w:r>

<w:t>III</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>GGG</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>HHH</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

<w:vMerge/>

</w:tcPr>

<w:p/>

</w:tc>

</w:tr>

---

# 相关开放文档格式(ODF)属性：

表格网格使用<table:table-column>元素指定—表格中出现的每个单元格大小对应一个。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 9.1.6。

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A"/>

<table:table-column table:style-name="Table1.B"/>

<table:table-column table:style-name="Table1.C"/>

. . .

</table:table>

如果相邻列具有相同的样式，则可以设置table:number-columns-repeated属性，而不是列出三个单独的<table:table-column>元素：

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A" table:number-columns-repeated="3"/>

. . .

</table:table>

### 属性：

最常用的属性如下。

| 属性                          | 描述                                               |
| ----------------------------- | -------------------------------------------------- |
| table:default-cell-style-name | 指定当table:style-name没有值时要使用的单元格样式。 |
| table:style-name              | 为表格指定表格样式。                               |
| table:number-columns-repeated | 指定具有相同样式的列数。参见上面的注释。           |
| xml:id                        | 指定唯一ID，并由W3C（xml-id）标准化。              |
| table:visibility              | 指定列是否可见。                                   |

# 相关HTML/CSS属性：

单元格宽度可以使用width css属性设置。单元格可以分别使用单元格上的rowspan和colspan属性跨越行或列。请注意，尽管HTML中也有colgroup和col元素，但它们用于按样式相似性对单元格进行分组，并不像OOXML tblGrid那样暗示结构分组。

<table style="width:100%;">

<tr>

<td style="width:10%">AAA</td>

<td rowspan="2" style="width:20%">BBB</td>

<td style="width:70%">CCC</td>

</tr>

<tr>

<td>DDD</td>

<td>FFF</td>

</tr>

<tr>

<td>GGG</td>

<td colspan="2">HHH</td>

</tr>

</table>

HTML/CSS示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | FFF |
| GGG | HHH |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
