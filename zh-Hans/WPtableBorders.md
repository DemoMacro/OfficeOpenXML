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

边框

表格边框使用<w:tblBorders>元素定义。该元素的子元素指定边框类型—底部、结束（标准前一版本中的"右侧"）、内部水平、内部垂直、开始（标准前一版本中的"左侧"）和顶部。

<w:tblPr>

<w:tblBorders>

<w:top w:val="single" w:sz="12" w:space="0" w:color="FF0000" />

<w:start w:val="single" w:sz="24" w:space="0" w:color="00FF00" />

<w:bottom w:val="single" w:sz="12" w:space="0" w:color="0000FF" />

<w:end w:val="single" w:sz="24" w:space="0" w:color="000000" />

<w:insideH w:val="single" w:sz="24" w:space="0" w:color="CC0000" />

<w:insideV w:val="single" w:sz="24" w:space="0" w:color="666666" />

</w:tblBorders>

</w:tblPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.39。

Word 2007 示例：

![Table Borders](images\wp-tblBorders-1.gif)

---

### 元素：

| 元素    | 描述                                                                                                                                                                                               |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| top     | 指定表格顶部显示的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.77。                                                                                                        |
| bottom  | 指定表格底部显示的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.4。                                                                                                         |
| start   | 指定从左到右表格的左侧和从右到左表格的右侧显示的边框。![](images/versionConflict3.png)注意：在标准的前一版本中，此元素是left。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.37。  |
| end     | 指定从左到右表格的右侧和从右到左表格的左侧显示的边框。![](images/versionConflict3.png)注意：在标准的前一版本中，此元素是right。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.13。 |
| insideH | 指定所有内部水平表格单元格边框上显示的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.23。                                                                                    |
| insideV | 指定所有内部垂直表格单元格边框上显示的边框。 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.25。                                                                                    |

表格边框的显示受制于与表格行和单元格边框定义的冲突解决。请参阅[表格边框冲突](WPtableCellBorderConflicts.md)和[tcBorders](WPtcBorders.md)。

### 子元素的属性：

最常用的属性如下。（已省略与主题和框架相关的属性。）

| 属性   | 描述                                                                                                                                                                                                                |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color  | 指定边框的颜色。值以十六进制值（RRGGBB格式）给出。与HTML/CSS中的十六进制值不同，没有#。例如，color="FFFF00"。还允许使用auto值，这将允许使用的文字处理器确定颜色。                                                   |
| shadow | 指定是否应修改边框以创建阴影外观。对于右侧和底部边框，这是通过在正常位置的下方和右侧复制边框来完成的。对于右侧和顶部边框，这是通过将边框向下并向右移动原始位置来完成的。允许的值为true和false。                     |
| space  | 指定间距偏移量。值以磅（1/72英寸）为单位指定。                                                                                                                                                                      |
| sz     | 指定边框的宽度。表格边框是线边框（请参见下面的val属性），因此宽度以磅的八分之一为单位指定，最小值为2（四分之一磅），最大值为96（十二磅）。（页面边框也可以是艺术边框，宽度以磅为单位给出，最小值为1，最大值为31。） |
| val    | 指定边框的样式。表格边框只能是线边框。（页面边框也可以是艺术边框。）可能的值有：                                                                                                                                    |

- single \- 单线
- dashDotStroked \- 具有一系列交替细线和粗线的线条
- dashed \- 虚线
- dashSmallGap \- 带有小间隙的虚线
- dotDash \- 具有交替点和短划线的线条
- dotDotDash \- 具有重复点-点-短划线序列的线条
- dotted \- 点线
- double \- 双线
- doubleWave \- 双波浪线
- inset \- 内嵌线组
- nil \- 无边框
- none \- 无边框
- outset \- 外嵌线组
- thick \- 单线
- thickThinLargeGap \- 包含在细线中的粗线，具有大尺寸中间间隙
- thickThinMediumGap \- 包含在细线中的粗线，具有中等尺寸中间间隙
- thickThinSmallGap \- 包含在细线中的粗线，具有小尺寸中间间隙
- thinThickLargeGap \- 包含在粗线中的细线，具有大尺寸中间间隙
- thinThickMediumGap \- 包含在细线中的粗线，具有中等尺寸中间间隙
- thinThickSmallGap \- 包含在细线中的粗线，具有小尺寸中间间隙
- thinThickThinLargeGap \- 具有大间隙的细-粗-细线
- thinThickThinMediumGap \- 具有中等间隙的细-粗-细线
- thinThickThinSmallGap \- 具有小间隙的细-粗-细线
- threeDEmboss \- 三级渐变线，向段落方向变暗
- threeDEngrave \- 类似三级渐变，远离段落方向变暗
- triple \- 三线
- wave \- 波浪线

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.18.2。

### 相关CSS属性：

border-collapse:collapse;  
border-bottom:4px dashed #0000FF;  
border-top:6px double #FF0000;  
border-left:5px solid #00FF00;  
border-right:5px solid #666666;

CSS 示例：

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
