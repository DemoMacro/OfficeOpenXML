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

# 文字处理文本

文本底纹和高亮

有几个与文本底纹和高亮相关的文本属性。每个属性都是通过<rPr>元素内的子元素应用的。

### 元素：

| 元素 | 描述                                                                                                                                                                                                |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| shd  | 指定文本运行的底纹：<w:shd w:val="pct10" w:fill="00FFFF" w:color="FF0000"/>。底纹由三个组件组成：背景色、可选的图案和可选的图案颜色。生成的底纹是通过先设置背景色，然后应用图案和图案颜色来应用的。 | ![文本运行底纹](images\wp-textShade-1.gif) |

---

最常用的属性值如下。还有几个特定于主题的属性，如themeColor、themeFill、themeFillShade等。

| 属性  | 描述                                                                                                                                  |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------- |
| fill  | 指定用于背景的颜色。值以十六进制值给出（即RRGGBB格式）。没有#，与HTML/CSS中的十六进制值不同。例如，fill="FFFF00"。                    |
| color | 指定用于val属性指定的任何前景图案的颜色。值以十六进制值给出（RRGGBB格式）。没有#，与HTML/CSS中的十六进制值不同。例如，fill="FFFF00"。 |
| val   | 指定用于将图案颜色覆盖在背景色上的图案。例如，w:val="pct10"表示边框样式是10%的前景填充蒙版。                                          |

可能的值有：clear（无图案）、pct10、pct12、pct15…、diagCross、diagStripe、horzCross、horzStripe、nil、thinDiagCross、solid等。完整列表请参见ECMA-376，第3版，§ 17.18.78。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.3.2.32。

highlight | 指定要用作内容背景的高亮颜色：<w:highlight w:val="red"/> 此元素将取代shd中指定的任何背景底纹。 | ![文本高亮](images\wp-text-highlight-1.gif)

---

单个属性val指定文本高亮的颜色。可能的值有：black、blue、cyan、darkBlue、darkCyan、darkGray、darkGreen、darkMagenta、darkRed、darkYellow、green、lightGray、magenta、none、red、white、yellow

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.3.2.15。

### 相关CSS属性：

<div>然后他们开始颤抖，<span style="background-color:#FFFF00"> 他们呼唤我们的名字</span>，一旦我们认出他们的声音，咒语就被打破了。我们已经拯救了他们。</div>

CSS示例：

然后他们开始颤抖，他们呼唤我们的名字，一旦我们认出他们的声音，咒语就被打破了。我们已经拯救了他们。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
