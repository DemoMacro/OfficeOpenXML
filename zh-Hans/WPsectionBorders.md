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

# 文字处理节

边框

节的每个页面的边框使用<w:pgBorders>元素定义。此元素的子元素指定边框类型—左、右、下和上。

<w:pgBorders w:offsetFrom="page">

<w:top w:val="double" w:sz="4" w:space="24" w:color="C00000"/>

<w:bottom w:val="double" w:sz="4" w:space="24" w:color="C00000"/>

<w:left w:val="single" w:sz="8" w:space="24" w:color="548DD4"/>

<w:right w:val="single" w:sz="8" w:space="24" w:color="548DD4"/>

</w:pgBorders>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.10。

Word 2007 示例：

![Section Page Borders](images\wp-section-pgBorders-1.gif)

---

### 属性

| 元素    | 描述                                   |
| ------- | -------------------------------------- |
| display | 指定在哪些页面上显示边框。可能的值为： |

- allPages
- firstPage
- notFirstPage

offsetFrom | 指定应如何计算边框的相对定位。可能的值为：

- page - 每个边框上的space属性被解释为页面边缘到页面边框之间应保留的距离
- text - 每个边框上的space属性被解释为文本边距到页面边框之间应保留的距离

zOrder | 指定页面边框是位于相交文本和对象的上方还是下方。可能的值为：

- back \- 页面边框将呈现在任何文本下方
- front \- 页面边框将呈现在任何文本上方

### 元素：

| 元素   | 描述                                                                                           |
| ------ | ---------------------------------------------------------------------------------------------- |
| top    | 指定节中每个页面顶部的边框。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.21。 |
| bottom | 指定节中每个页面底部的边框。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.2。  |
| left   | 指定节中每个页面左侧的边框。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.7。  |
| right  | 指定节中每个页面右侧的边框。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.15。 |

### 子元素属性：

最常用的属性如下（省略了与主题相关的属性）：

| 属性   | 描述                                                                                                                                                                                                                                                                                                                                                                                          |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color  | 指定边框的颜色。值以十六进制值（RRGGBB格式）给出。与HTML/CSS中的十六进制值不同，没有#。例如，color="FFFF00"。也允许使用auto值，这将允许使用的文字处理器确定颜色。                                                                                                                                                                                                                             |
| id     | 用于定义客户边框图像。它指定包含边框图像的关系的关系ID。图像包含在包的单独部分中。例如，<w:bottom w:val="custom" r:id="rIdCustomBottomBorder" . . ./>。ID为rIdCustomBottomBorder的关系必须包含图像。请注意，属性所针对的关系必须是http://purl.oclc.org/ooxml/officeDocument/relationships/image类型，否则文档将不符合规范。![](images/versionConflict3.png)注意：标准的早期版本不支持此属性。 |
| shadow | 指定是否应修改边框以创建阴影外观。对于右侧和底部边框，这是通过在正常位置的下方和右侧复制边框来完成的。对于右侧和顶部边框，这是通过将边框向下和向右移动原始位置来完成的。允许的值为true和false。                                                                                                                                                                                               |
| space  | 指定间距偏移。值以磅（1/72英寸）为单位指定。                                                                                                                                                                                                                                                                                                                                                  |
| sz     | 指定边框的宽度。如果边框是线边框，大小以八分之一磅为单位指定，最小值为2（1/4磅），最大值为96（十二磅）。如果边框是艺术边框，宽度以磅为单位给出，最小为1，最大为31。                                                                                                                                                                                                                           |
| val    | 指定边框的样式。页面边框可以是线边框或艺术边框。可能的线边框值为：                                                                                                                                                                                                                                                                                                                            |

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
- threeDEmboss \- 三阶段渐变线，向段落方向逐渐变暗
- threeDEngrave \- 类似三阶段渐变，远离段落方向逐渐变暗
- triple \- 三线
- wave \- 波浪线

有关可能的艺术边框，请参阅ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.18.2中的规范。

### 相关HTML/CSS属性：

HTML没有页面的概念，因此也没有页面边框。请参阅[段落边框](WPborders.md)的讨论。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
