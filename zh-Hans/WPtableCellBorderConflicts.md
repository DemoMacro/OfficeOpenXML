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

表格边框冲突

当表格或表格行（表格级例外）指定了边框，而单个单元格也指定了边框时，可能会发生冲突。OOXML规范规定了如何解决此类冲突。

首先注意，如果[单元格间距](WPtableCellSpacing.md)不为零，则单元格边框和表格边框都可以无冲突地显示。

Word 2007 示例：

![Sample table cell border conflicts](images\wp-tableCellBorderConflicts-1.gif)

---

### 单元格边框与表格和表格级例外边框之间的冲突

如果单元格间距为零，则存在冲突。以下规则适用于单元格边框与表格和表格级例外（行）边框之间：

- 如果存在单元格边框，则显示单元格边框。
- 如果没有单元格边框但行上有表格级例外边框，则显示该表格级例外边框。
- 如果没有单元格或表格级例外边框，则显示表格边框。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.40。

### 相邻单元格之间的冲突

相邻单元格边框之间的冲突通过首先根据样式为每个边框分配权重来解决；权重最大的单元格边框占优。如果权重相等，则通过亮度值比较边框；亮度值较小的边框获胜。如果亮度因子相等，则显示阅读顺序中的第一个边框。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.67。

### 相关CSS属性：

如果边框不折叠且单元格之间有足够的间距，则边框之间没有冲突。（注意HTML行不能有边框—只有表格和单元格可以。）

<table style="width: 100%; height:50px; border-collapse:separate; border:2px dashed #0000FF; border-spacing:10px; empty-cells:show;">   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">AAA</td>   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">BBB</td>   
. . . </tr>   
. . .   
</table>

CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

<table style="width: 100%; height:50px; border-collapse:collapse; border:2px dashed #0000FF;">   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">AAA</td>   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">BBB</td>   
. . .   
</table>

CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
