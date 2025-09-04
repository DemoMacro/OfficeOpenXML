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

单元格属性 - 边框

单元格边框通过<w:tcPr/>内的<tcBorders>元素指定。可以指定八种不同的边框作为子元素。

![](images/note.png)注意：单元格边框的实际外观取决于表格的单元格间距等因素。如果[tblCellSpacing](WPtableCellSpacing.md)值非零，则单元格边框将始终显示。否则，边框的显示受冲突解决算法的影响。请参阅[表格边框冲突](WPtableCellBorderConflicts.md)。

<w:tcPr>

<w:tcBorders>

<w:top w:val="double" w:sz="24" w:space="0" w:color="FF0000">

<w:start w:val="double" w:sz="24" w:space="0" w:color="FF0000">

<w:bottom w:val="double" w:sz="24" w:space="0" w:color="FF0000">

<w:end w:val="double" w:sz="24" w:space="0" w:color="FF0000">

<w:tl2br w:val="double" w:sz="24" w:space="0" w:color="FF0000">

</w:tcBorders>

<w:tcPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.67。

![Sample table cell borders](images\wp-tableCellBorders-1.gif)

---

### 元素：

| 元素    | 描述                                                                                                                                                                                                                                                                                                 |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| top     | 指定显示在单元格顶部的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.75。                                                                                                                                                                                                       |
| bottom  | 指定显示在单元格底部的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.3。                                                                                                                                                                                                        |
| start   | 指定显示在单元格前缘的边框（从左到右的表格为左侧，从右到左的表格为右侧）。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是left。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.34。                                                                                  |
| end     | 指定显示在单元格后缘的边框（从左到右的表格为右侧，从右到左的表格为左侧）。![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是right。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.12。                                                                                 |
| insideH | 指定显示在单元格所有内部水平边缘的边框。请注意，对于单个单元格，这基本无用，因为单个单元格没有内部边缘的概念。但是，它用于确定应用于特定单元格组的单元格边框，作为表格样式中表格条件格式的一部分，例如第一列中单元格集的内部边缘。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.24。 |
| insideV | 指定显示在单元格所有内部垂直边缘的边框。请注意，对于单个单元格，这基本无用，因为单个单元格没有内部边缘的概念。但是，它用于确定应用于特定单元格组的单元格边框，作为表格样式中表格条件格式的一部分，例如第一列中单元格集的内部边缘。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.26。 |
| tl2br   | 指定显示在单元格内从左上到右下对角线的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.74。                                                                                                                                                                                       | ![示例表格单元格对角线边框](images\wp-tableCellBorders-2.gif) |

---

tr2bl | 指定显示在单元格内从右上到左下对角线的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.4.80。

### 子元素的属性：

以下是最常用的属性。（已省略与主题和框架相关的属性。）

| 属性   | 描述                                                                                                                                                                                                      |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color  | 指定边框的颜色。值以十六进制值（RRGGBB格式）给出。与HTML/CSS中的十六进制值不同，没有#。例如，color="FFFF00"。也允许使用auto值，这将允许使用的文字处理器确定颜色。                                         |
| shadow | 指定是否应修改边框以创建阴影外观。对于右侧和底部边框，这是通过在正常位置的下方和右侧复制边框来完成的。对于右侧和顶部边框，这是通过将边框向下和向右移动原始位置来完成的。允许的值为true和false。           |
| space  | 指定间距偏移量。值以磅（1/72英寸）为单位指定。                                                                                                                                                            |
| sz     | 指定边框的宽度。表格边框是线边框（请参见下面的val属性），因此宽度以八分之一磅为单位指定，最小值为二（1/4磅），最大值为96（十二磅）。（页面边框也可以是艺术边框，宽度以磅为单位给出，最小为1，最大为31。） |
| val    | 指定边框的样式。表格边框只能是线边框。（页面边框也可以是艺术边框。）可能的值有：                                                                                                                          |

- single \- 单线
- dashDotStroked \- 一系列交替的细线和粗线
- dashed \- 虚线
- dashSmallGap \- 带有小间隙的虚线
- dotDash \- 点和虚线交替的线
- dotDotDash \- 重复点-点-虚线序列的线
- dotted \- 点线
- double \- 双线
- doubleWave \- 双波浪线
- inset \- 内嵌线组
- nil \- 无边框
- none \- 无边框
- outset \- 外嵌线组
- thick \- 单线
- thickThinLargeGap \- 包含在细线内的粗线，中间有大尺寸间隙
- thickThinMediumGap \- 包含在细线内的粗线，中间有中等尺寸间隙
- thickThinSmallGap \- 包含在细线内的粗线，中间有小间隙
- thinThickLargeGap \- 包含在粗线内的细线，中间有大尺寸间隙
- thinThickMediumGap \- 包含在细线内的粗线，中间有中等尺寸间隙
- thinThickSmallGap \- 包含在细线内的粗线，中间有小间隙
- thinThickThinLargeGap \- 细-粗-细线，中间有大间隙
- thinThickThinMediumGap \- 细-粗-细线，中间有中等间隙
- thinThickThinSmallGap \- 细-粗-细线，中间有小间隙
- threeDEmboss \- 三阶段渐变线，向段落方向变暗
- threeDEngrave \- 类似三阶段渐变，远离段落方向变暗
- triple \- 三线
- wave \- 波浪线

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.18.2。

---

# 相关开放文档格式(ODF)属性：

可以通过将fo:border、fo:border-bottom、fo:border-left、fo:border-right和fo:border-top属性添加到应用于单元格的样式的<style:table-cell-properties>元素来设置单元格边框。请注意，对于双线边框，<style:table-cell-properties>有其他属性，如style:border-line-width-bottom等，这些属性允许设置内外线的宽度以及它们之间的间距。

参考：办公应用程序开放文档格式1.2版（2011年5月）§§ 17.18, 20.176.2 - 20.176.6。

<style:style style:name="Table1.A1" style:family="table-cell">

<style:table-cell-properties fo:border-left="0.12in solid #6666FF" fo:border-right="0.12in solid #6666FF" fo:border-top="none" fo:border-bottom="none"/>

<style:background-image/>

</style:table-cell-properties>

</style:style>

# 相关HTML/CSS属性：

请注意，HTML行不能有边框—只有表格和单元格可以。

<table style="width: 100%; height:50px; border-collapse:separate; border-spacing:10px; empty-cells:show;">

<tr>

<td>style="border-bottom:1px double #FF00FF; border-top:1px dashed #FFFF00; border-left:2px solid #FF0000; border-right:2px groove #CCCC00;">AAA</td>

<td>style="border-bottom:3px dotted #00FF66; border-top:3px double #FF00FF; border-left:2px solid #FF0000; border-right:2px outset #9933FF;">BBB</td>

. . .

</tr>

. . .

</table>

CSS示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
