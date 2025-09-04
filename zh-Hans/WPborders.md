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

# 文字处理段落

边框

段落边框使用<w:pBdr>元素定义。该元素的子元素指定边框类型—左、右、下、上和之间。

<w:pPr>

<w:pBdr>

<w:top w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:bottom w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:left w:val="single" w:sz="24 w:space="1" w:color="0000FF" />

<w:right w:val="single" w:sz="24 w:space="1" w:color="0000FF" />

</w:pBdr>

</w:pPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.24。

Word 2007 示例：

![Simple Indent](images\wp-pBrd-1.gif)

---

### 元素：

| 元素    | 描述                                                                                                                                                                                                                                                                      |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| top     | 指定显示在具有相同段落边框设置的一组段落上方的边框。请注意，如果相邻段落具有相同的边框设置并且指定了之间边框，则将使用单个之间边框，而不是第一个段落的底部边框和第二个段落的顶部边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.42。               |
| bottom  | 指定显示在具有相同段落边框设置的一组段落下方的边框。请注意，如果相邻段落具有相同的边框设置并且指定了之间边框，则将使用单个之间边框，而不是第一个段落的底部边框和第二个段落的顶部边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.7。                |
| left    | 指定显示在段落周围页面左侧的边框，无论段落方向如何。边框跨越顶部或之间边框在顶部的长度以及底部或之间边框在底部的长度。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.17。                                                                               |
| right   | 指定显示在段落周围页面右侧的边框，无论段落方向如何。边框跨越顶部或之间边框在顶部的长度以及底部或之间边框在底部的长度。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.28。                                                                               |
| between | 指定具有相同段落边框设置的一组段落中每个段落之间的边框。因此，如果相邻段落具有相同的边框设置，则它们之间将有一个由between元素指定的边框。否则，第一个段落将使用其底部边框，后续段落将使用其顶部边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.5。 |

### 子元素的属性：

最常用的属性是：

| 属性   | 描述                                                                                                                                                                                                        |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color  | 指定边框的颜色。值以十六进制值（RRGGBB格式）给出。没有#，与HTML/CSS中的十六进制值不同。例如，color="FFFF00"。也允许使用auto值，这将允许使用的文字处理器确定颜色。                                           |
| shadow | 指定是否应修改边框以创建阴影外观。对于右侧和底部边框，这是通过在正常位置的下方和右侧复制边框来完成的。对于右侧和顶部边框，这是通过将边框向下和向右移动原始位置来完成的。允许的值是true和false。             |
| space  | 指定间距偏移量。值以磅（1/72英寸）为单位指定。                                                                                                                                                              |
| sz     | 指定边框的宽度。段落边框是线边框（请参见下面的val属性），因此宽度以磅的八分之一为单位指定，最小值为二（1/4磅），最大值为96（十二磅）。（页面边框也可以是艺术边框，宽度以磅为单位给出，最小为1，最大为31。） |
| val    | 指定边框的样式。段落边框只能是线边框。（页面边框也可以是艺术边框。）可能的值是：                                                                                                                            |

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
- thickThinLargeGap \- 包含在细线内的粗线，中间有大间隙
- thickThinMediumGap \- 包含在细线内的粗线，中间有中等间隙
- thickThinSmallGap \- 包含在细线内的粗线，中间有小间隙
- thinThickLargeGap \- 包含在粗线内的细线，中间有大间隙
- thinThickMediumGap \- 包含在细线内的粗线，中间有中等间隙
- thinThickSmallGap \- 包含在细线内的粗线，中间有小间隙
- thinThickThinLargeGap \- 细-粗-细线，中间有大间隙
- thinThickThinMediumGap \- 细-粗-细线，中间有中等间隙
- thinThickThinSmallGap \- 细-粗-细线，中间有小间隙
- threeDEmboss \- 三阶段渐变线，朝向段落变暗
- threeDEngrave \- 三阶段渐变线，远离段落变暗
- triple \- 三线
- wave \- 波浪线

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.18.2。

Word 2007 示例：

<w:pPr>

<w:pBdr>

<w:top w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:bottom w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:between w:val="single" w:sz="24" w:space="1" w:color="0000FF" />

</w:pBdr>

</w:pPr>

<w:pPr>

<w:pBdr>

<w:top w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:bottom w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:between w:val="single" w:sz="24" w:space="1" w:color="0000FF" />

</w:pBdr>

</w:pPr>

![Simple Indent](images\wp-pBrd-2.gif)

---

另一个 Word 2007 示例：

<w:pPr>

<w:pBdr>

<w:top w:val="double" w:sz="16" w:space="1" w:color="FF00FF" />

<w:bottom w:val="dotDotDash" w:sz="8" w:space="1" w:color="00FF00" />

</w:pBdr>

</w:pPr>

![Simple Indent](images\wp-pBrd-3.gif)

---

### 相关CSS属性：

border-top-width: 5px;  
border-top-style: solid;  
border-top-color: #0000FF;  
border-left-width: 10px;  
border-left-color: #000000;  
border-left-style: double;

CSS 示例：

声音，咒语已被打破。我们已经交付了他们：他们已经战胜死亡，回来分享我们的生活。

我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。

过去隐藏在领域之外的某个地方，超出智力的范围，在某些物质中

相关Open Office (ODF)属性：

<w:pPr>

<w:pBdr>

<w:top w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:bottom w:val="single" w:sz="24" w:space="1" w:color="FF0000" />

<w:between w:val="single" w:sz="24" w:space="1" w:color="0000FF" />

</w:pBdr>

</w:pPr>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
