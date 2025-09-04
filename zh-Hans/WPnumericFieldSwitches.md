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

# 文字处理域

数字域格式

数字域格式开关具有以下格式：

\\# _开关参数_

数字域开关参数由一系列"图片项"组成。以下是最常用的。（注意，[常规格式开关](WPgeneralFieldSwitches.md)也有适用于数字域的格式。）

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.4.2。

### 数字域开关图片项：

| 图片项 | 描述                                                                      | 示例                               |
| ------ | ------------------------------------------------------------------------- | ---------------------------------- |
| 0      | 指定要显示的数字位置。                                                    | =4+5 \\# 00.00 显示"09.00"。       |
| #      | 指定要显示的数字位置，如果结果在该位置不包含数字，则显示空格。            | =9+6 \\# $###  显示"$ 15"。        |
| x      | 舍弃x占位符左侧的数字。如果占位符在小数点右侧，则结果会四舍五入到该位置。 | =111053+111439 \\# x## 显示"492"。 |

=1/8 \\# 0.00x 显示"0.125"。  
=3/4 \\# .x 显示".8"。  
. | 表示美式英语中的小数点。| =95.4 \\# $###.00  显示"$ 95.40"。  
, | 分隔三位数字组。| =2456800 \\# $#,###,###  显示"$ 2,456,800"。

- | 在负结果前添加减号，如果结果为正或0，则添加空格。| =80-90 \\# -## 显示"-10"。  
  =90-80 \\# -## 显示"10"。

* | 在正结果前添加加号，在负结果前添加减号，如果结果为0，则添加空格。| =90-80 \\# +## 显示"+10"。  
  =80-90 \\# +## 显示"-10"。  
  其他字符 | 在该位置包含指定字符。| =33 \\# ##% 显示"33%"。  
  'text' | 在结果中包含文本。| =Price\*15% \\# "$##0.00 'is the sale tax' 可能显示"$ 3.98 is the sales tax"。  
  'numbered item' | 以阿拉伯数字包含作为标题编号的前一项的编号。| =SUM(A1:D4) \\# "##.00 'is the total of Table' 'table'" 显示"456.34 is the total of Table 2"。  
  _正结果_ ; _负结果; 零结果_ | 为正结果和负结果指定不同格式。要为零结果也指定格式，请添加另一个以分号分隔的图片。| =Sales95 \\# "$#,##0.00; -$#,##.00; $0 显示，例如，正值为$5,320.00，负值为-$5,320.00，零值为$0。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
