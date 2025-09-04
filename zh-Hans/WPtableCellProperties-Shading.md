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

单元格属性 - 底纹

单元格底纹由<w:tcPr/>内的span class="featuredItem"><shd>元素指定。底纹应用于单元格边框。底纹由背景色、可选图案和可选图案颜色组成。

<w:tcPr>

<w:shd w:val="clear" w:color="auto" w:fill="FF0000">

</w:tcPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.33。

Word 2007 示例：

<w:tcPr>

<w:shd w:val="pct45" w:color="FFFF00" w:fill="B2A1C7">

</w:tcPr>

![Sample table cell shading](images\wp-tableCellShading-1.gif)

---

### 属性：

最常用的属性值如下。还有几个特定于主题的属性，如themeColor、themeFill、themeFillShade等。

| 属性  | 描述                                                                                                                                                                                                 |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fill  | 指定用于背景的颜色。值以十六进制值给出（即RRGGBB格式）。与HTML/CSS中的十六进制值不同，不包含#。例如，fill="FFFF00"。可以使用auto值，使消费软件能够确定该值。可以使用auto值，使消费软件能够确定该值。 |
| color | 指定用于val属性指定的任何前景图案的颜色。值以十六进制值给出（RRGGBB格式）。与HTML/CSS中的十六进制值不同，不包含#。例如，fill="FFFF00"。可以使用auto值，使消费软件能够确定该值。                      |
| val   | 指定用于将图案颜色覆盖在背景色上的图案。例如，w:val="pct10"表示边框样式是10%的前景填充蒙版。                                                                                                         |

可能的值有：clear（无图案）、pct10、pct12、pct15…、diagCross、diagStripe、horzCross、horzStripe、nil、thinDiagCross、solid等。完整列表请参见ECMA-376，第3版，§ 17.18.78。

---

# 相关开放文档格式(ODF)属性：

单元格内的底纹可以通过将fo:background-color属性添加到应用于单元格的样式的<style:table-cell-properties>元素中来设置。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 17.18和§ 20.175。

<style:style style:name="Table1.A1" style:family="table-cell">

<style:table-cell-properties fo:background-color="#9999FF" fo:padding="0.382in" fo:border-left="0.007in solid #000000" fo-border-right="none" fo-border-top="0.007in solid #000000" fo-border-bottom="0.007in solid #000000">

<style:background-image/>

</style:table-cell-properties>

</style:style>

# 相关HTML/CSS属性：

<td style="background-color:#FF0000;">

CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
