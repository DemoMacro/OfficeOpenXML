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

单元格属性

单元格级别的属性在<tcPr>中指定。每个属性都是<tcPr>的子元素，单元格属性优先于表格和行属性。

<w:tcPr>

<w:tcMar>

<w:start w:w="1440" w:type="dxa"/>

</w:tcMar>

</w:tcPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.70。

最常用的属性如下所示：

### 元素/属性：

| 元素      | 描述                                                                                                                                                                                                                                                                                                                                                                                      |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| gridSpan  | 此元素定义单元格跨越的逻辑列数。它具有单个属性w:val。参见[表格网格/列定义](WtableGrid.md)中关于<w:tblGrid>的讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.17。                                                                                                                                                                                                      |
| hideMark  | 参见[隐藏表格单元格结束标记](WPhideMark.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.21。                                                                                                                                                                                                                                                                           |
| noWrap    | 此元素将在某些条件下防止单元格中的文本换行。它是一个布尔属性。例如，<w:noWrap/>。![](images/note.png)注意：这仅影响当行的tblLayout设置为auto时单元格的行为。如果单元格宽度是固定的，那么noWrap指定当行中的其他单元格未达到其最小值时，单元格不会小于该固定值。如果单元格宽度设置为auto或pct，则单元格的内容将不会换行。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.30。 |
| shd       | 参见[表格单元格属性 - 底纹](WPtableCellProperties-shading.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.33。                                                                                                                                                                                                                                                         |
| tcBorders | 参见[表格单元格属性 - 边框](WPtableCellProperties-borders.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.67。                                                                                                                                                                                                                                                         |
| tcFitText | 使用<w:tcFitText w:val="true"/>可以收缩或扩展单元格内的文本以适应单元格的宽度。它具有单个属性val，布尔值为true/false。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.68。                                                                                                                                                                                                  | ![表格单元格适应文本](images\wp-tableCellFitText-1.gif) |

---

tcMar | 参见[表格单元格属性 - 边距](WPtableCellProperties-Margins.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.69。  
tcW | 参见[表格单元格属性 - 宽度](WPtableCellProperties-Width.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.72。  
vAlign | 参见[表格单元格属性 - 垂直对齐](WPtableCellProperties-verticalAlignment.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.84。  
vMerge | 此元素指定单元格是垂直合并单元格集合的一部分。定义单元格跨越的逻辑列数。它具有单个属性w:val，该属性指定单元格如何成为垂直合并区域的一部分。单元格可以是现有合并单元格组的一部分，也可以开始一个新的合并单元格组。可能的值有：

- continue \— 当前单元格继续先前存在的合并组
- restart \— 当前单元格开始一个新的合并组

如果省略，则假定值为continue。参见[表格网格/列定义](WtableGrid.md)中关于<w:tblGrid>的讨论。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.85。

---

# 相关开放文档格式(ODF)属性：

表格单元格属性在<style:table-cell-properties>元素中指定。

<style:style style:name="Table1.B2" style:family="table-cell">

<style:table-cell-properties fo:background-color="#00ffff" fo:padding="0.0382in" fo:border-left="0.0007in solid #000000" fo:border-right="none" fo:border-top="none" fo:border-bottom="0.0007in solid #000000">

<style:background-image/>

</style:table-cell-properties>

</style:style>

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 17.18。

<style:table-cell-properties>元素可以具有以下属性：

| 属性                                                                                                                                              | 描述                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| fo:background-color                                                                                                                               | 指定单元格背景的颜色。                                                                                                                               |
| fo:border, fo:border-bottom, fo:border-left, fo:border-right, fo:border-top                                                                       | 指定单元格的边框。                                                                                                                                   |
| fo:padding, fo:padding-bottom, fo:padding-left, fo:padding-right, fo:padding-top                                                                  | 指定单元格的内边距。                                                                                                                                 |
| fo:wrap-option                                                                                                                                    | 指定文本是否换行。可能的值为no-wrap和wrap。                                                                                                          |
| style:border-line-width, style:border-line-width-bottom, style:border-line-width-left, style:border-line-width-right, style:border-line-width-top | 指定边框属性为双线时的边框宽度。该值是由三个空格分隔的长度组成的列表。第一个值指定内线的宽度，第二个值指定两条线之间的距离，第三个值指定外线的宽度。 |
| style:cell-protect                                                                                                                                | 指定单元格的保护方式。可能的值为hidden-and-protected、none、protected和formula-hidden。                                                              |
| style:shadow                                                                                                                                      | 指定单元格的阴影效果。                                                                                                                               |
| style:vertical-align                                                                                                                              | 指定文本的垂直对齐方式。可能的值为automatic、bottom、middle和top。                                                                                   |
| style:writing-mode                                                                                                                                | 指定内容应该如何书写。可能的值为lr-tb、rl-tb、tb-rl、tb-lr、lr、rl、tb和page。                                                                       |

注意<style:table-cell-properties>还可以包含<style:background-image>元素。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
