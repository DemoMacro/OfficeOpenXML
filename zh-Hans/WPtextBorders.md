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
    - [通用样式属性](WPstyleGenProps.md)
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
  - [通用域格式](WPgeneralFieldSwitches.md)
  - [日期和时间域格式](WPdateTimeFieldSwitches.md)
  - [数字域格式](WPnumericFieldSwitches.md)
- [目录](WPtableOfContents.md)

# 文字处理文本

文本边框

文本运行的边框通过<w:rPr>元素内的<w:bdr>元素指定。请注意，边框是一个完整的四边边框。与段落边框不同，无法指定哪些边应该有边框。还要注意，具有相同属性的相邻文本运行将呈现为单个边框。

<w:rPr>

<w:bdr w:val="single" w:sz="36" w:space="0" w:color="B8CCE4" />

</w:rPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.4。

Word 2007 示例：

![Text Border](images\wp-textBorder-1.gif)

---

### 属性

最常用的属性如下（省略了与主题相关的属性）。

| 属性   | 描述                                                                                                                                                                                                           |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color  | 指定边框的颜色。值以十六进制值（RRGGBB格式）给出。与HTML/CSS中的十六进制值不同，没有#。例如，color="FFFF00"。也允许使用auto值，这将允许使用的文字处理器确定颜色。如果指定了主题颜色，则此属性将被忽略。        |
| frame  | 指定是否应该通过将边框外观从最接近文本的边缘反转到距离文本最远的边缘来修改边框以创建框架效果。允许的值为true和false。                                                                                          |
| shadow | 指定是否应该修改边框以创建阴影外观。对于右侧和底部边框，这是通过在正常位置的下方和右侧复制边框来完成的。对于右侧和顶部边框，这是通过将边框向下和向右移动到原始位置来完成的。允许的值为true和false。            |
| space  | 指定间距偏移量。值以磅（1/72英寸）为单位指定。                                                                                                                                                                 |
| sz     | 指定边框的宽度。文本边框是线边框（请参见下面的val属性），因此宽度以磅的八分之一为单位指定，最小值为2（1/4磅），最大值为96（十二磅）。（页面边框也可以是艺术边框，宽度以磅为单位给出，最小值为1，最大值为31。） |
| val    | 指定边框的样式。文本边框只能是线边框。（页面边框也可以是艺术边框。）可能的值为：                                                                                                                               |

- single \- 单线
- dashDotStroked \- 一条由一系列交替的细线和粗线组成的线
- dashed \- 虚线
- dashSmallGap \- 带有小间隙的虚线
- dotDash \- 点和虚线交替的线
- dotDotDash \- 具有重复点-点-虚线序列的线
- dotted \- 点线
- double \- 双线
- doubleWave \- 双波浪线
- inset \- 一组内嵌线
- nil \- 无边框
- none \- 无边框
- outset \- 一组外嵌线
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
- threeDEmboss \- 三阶段渐变线，向段落方向变暗
- threeDEngrave \- 类似三阶段渐变，远离段落方向变暗
- triple \- 三线
- wave \- 波浪线

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.18.2。

另一个Word 2007示例：

<w:rPr>

<w:bdr w:val="doubleWave" w:sz="16" w:space="36" w:color="FF6600" w:frame="true" />

</w:rPr>

![Text Border](images\wp-textBorder-2.gif)

---

### 相关CSS属性：

<div>然后他们开始颤抖，<span style="padding:5px; border-style: double; border-color:#FF6600; border-width: 2px"> 他们呼唤我们的名字</span>，一旦我们认出他们的声音，咒语就被打破了。我们已经拯救了他们。</div>

CSS示例：

然后他们开始颤抖，他们呼唤我们的名字，一旦我们认出他们的声音，咒语就被打破了。我们已经拯救了他们。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
