![OfficeOpenXML.com](images/banner1.png)

[主页](index.md) | [字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

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

# 字处理段落

相关Open Office/ODF讨论  
相关HTML/CSS讨论

结构

段落是ooxml文档中内容的主要块级容器。（表格也可以包含与段落同级的内容。）段落通过<w:p>元素指定。段落可以包含段落的丰富格式属性（包含在<w:pPr>中）。段落内的文本进一步包含在一个或多个运行（<w:r>）中。段落还可能包含书签、超链接、域、注释等。

<w:p>

<w:pPr>

<w:pStyle> w:val="NormalWeb"/>

<w:spacing w:before="120" w:after="120"/>

</w:pPr>

<w:r>

<w:t xml"space="preserve">我觉得凯尔特人的信仰很有道理，他们认为我们失去的人的灵魂被囚禁在某些低等生物中…</w:t>

</w:r>

</w:p>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 §§ 17.3.1 和 17.3.1.22。

Word 2007 示例：

![Paragraph](images\wp-paragraph-1.gif)

---

### 元素：

<w:p>元素可以包含多个元素，大多与跟踪修订和添加自定义XML有关。核心元素如下所示。

| 元素          | 描述                                                                                                                               |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| bookmarkStart | 指定文档中书签的开始。参见[书签](WPbookmark.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.13.6.2。              |
| bookmarkEnd   | 指定文档中书签的结束。参见[书签](WPbookmark.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.13.6.1。              |
| r             | 指定段落内的内容运行。参见[文本](WPtext.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.25。                  |
| pPr           | 指定段落的一组属性。参见[段落属性](WPparagraphProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.26。 |
| fldSimple     | 指定一个简单域。参见[域 - 概述](Wpfields.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.19。                  |
| hyperlink     | 指定该位置存在超链接。参见[超链接](WPhyperlink.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.22。            |

---

# 相关开放文档格式（ODF）属性：

ODF中的段落通过<text:p>元素指定。它是ODF文档中文本的基本单位，具有混合内容。最常见的情况是它具有text:style-name属性，并位于<office:text>元素内。

参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 5.1.3。

# 相关HTML/CSS属性：

<table style="width:100%;">

<tr>

<td>AAA</td>

<td>BBB</td>

<td>CCC</td>

</tr>

. . .

</table>

HTML/CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
