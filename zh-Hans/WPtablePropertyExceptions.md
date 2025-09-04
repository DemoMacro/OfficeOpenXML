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

表格属性例外

某些行属性使用<tblPrEx>元素指定为表格级属性的例外。<tblPrEx>元素包含正在为该行覆盖的所有表格级属性。这通常用于旧文档或合并两个现有独立表格时，以防止第二个表格的外观被第一个表格所取代。

<w:tr>

<w:tblPrEx>

<w:tblBorders>

<w:top w:val="single" w:sz="12" w:space="0" w:color="FF0000" />

<w:start w:val="single" w:sz="24" w:space="0" w:color="00FF00" />

<w:bottom w:val="single" w:sz="12" w:space="0" w:color="0000FF" />

<w:end w:val="single" w:sz="24" w:space="0" w:color="000000" />

<w:insideH w:val="single" w:sz="24" w:space="0" w:color="FFFF00" />

<w:insideV w:val="single" w:sz="24" w:space="0" w:color="FF00FF" />

</w:tblBorders>

</w:tblPrEx>

</w:tr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 §§ 17.4.61 和 17.4.82。

Word 2007 示例：

![Table Row Borders](images\wp-tblPrEx-1.gif)

---

请注意，黄色（FFFF00）的<insideH>元素使行的顶部和底部边框变为黄色，而不是顶部和底部的红色（FF0000）和蓝色（0000FF）。

### 元素：

最常用的表格例外如下：

| 元素 | 描述                                                                                                                                  |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| jc   | 指定当表格宽度与文档边距不同时行的对齐方式：<w:jc w:val="right">。有关详细信息，请参见[表格行属性](WPtableRowProperties.md)中的<jc>。 | ![表格行对齐](images\wp-tblPrEx-2.gif) |

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.27。

shd | 指定行的底纹直到表格边框，与单元格底纹不同，它包括任何单元格内边距：<w:shd w:val="clear" w:color="auto" w:fill="EEECE1"/>。底纹由三个组件组成：背景色、可选的图案和可选的图案颜色。属性包括（省略主题相关属性）：

- color \— 前景图案颜色。值以十六进制值给出（即RRGGBB格式）。没有#，与HTML/CSS中的十六进制值不同。例如，fill="FFFF00"。可以指定auto，这是默认值。请注意，如果val指定没有底纹格式或被省略，或者指定了主题，则此值将被取代。
- fill \— 背景颜色。值以十六进制值给出（即RRGGBB格式）。没有#，与HTML/CSS中的十六进制值不同。例如，fill="FFFF00"。可以指定auto，这是默认值。
- val \— 指定用于将图案颜色覆盖在背景颜色上的图案。例如，w:val="pct10"表示底纹样式是10%的前景填充蒙版。

可能的值有：clear（无图案）、pct10、pct12、pct15…、diagCross、diagStripe、horzCross、horzStripe、nil、thinDiagCross、solid等。完整列表请参见ECMA-376，第3版，§ 17.18.78。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.31。  
tblBorders | 指定行的边框。请注意，如果单元格间距不为零，则没有边框冲突，并且应用行例外边框。如果单元格间距为零，则存在冲突。否则应用单元格边框。有关此元素的详细信息，请参见[表格边框](WPtableBorders.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.4。  
tblCellMar | 指定行中单元格的单元格边距。有关此元素的详细信息，请参见[表格单元格边距](WPtableCellMargins.md)。| ![表格行单元格边距](images\wp-tblPrEx-cellMar-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.42。

tblCellSpacing | 指定行中所有单元格的单元格间距。它指定包含表格边框宽度后的最小空间量。这被行单元格间距tblCellSpacing值取代。有关详细信息，请参见[表格行属性](WPtableRowProperties.md)。请注意，表格级单元格间距添加在文本边距之外。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.45。  
tblInd | 指定要在行的前导边缘（从左到右表格中的左边缘）之前添加的缩进：<w:tblInd w:w="2160" w:type="dxa"/>。属性为：| 属性 | 描述  
---|---  
w | 指定缩进宽度的值。行将按指定量向文本边距内移动。![](images/versionConflict3.png)注意：OOXML标准的2006版本指定的是val而不是w。  
type | 指定宽度（w）属性的单位。可能的值有：

- dxa \- 指定值以点的二十分之一（1/1440英寸）为单位
- nil \- 指定值为零

如果指定了pct或auto，则该值将被忽略。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.52。

tblLayout | 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.54。  
tblLook | 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.55。  
tblW | 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.65。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
