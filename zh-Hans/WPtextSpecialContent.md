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

换行符、符号和其他特殊内容

换行符、回车符、制表符、特殊字符和其他特殊内容可能作为文本运行（<w:r> </w:r>）内的元素出现，而不是作为文本元素（<t> </t>）内的内容。

### 元素：

| 元素 | 描述                                                                                                                                                                                |
| ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| br   | 参见[分隔符](WPtextSpecialContent-break.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.1。                                                                    |
| cr   | 指定应插入回车符（Unicode字符000D）。它等同于具有空类型和清除属性的分隔符（<w:br/>）。<w:r><w:t>这是另一个</w:t></w:r><w:r><w:br/><w:t xml:space="preserve"> 简单句子。</w:t></w:r> |

| ![回车符](images\wp-carriageReturn.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.4。

sym | 参见[符号](WPtextSpecialContent-symbol.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.30。  
tab | 制表符使用tab元素插入：<w:tab/>。制表符将前进到defaultTabStop元素（在settings.xml中）宽度值的最近倍数，除非前面有自定义制表位，在这种情况下，它将前进到该自定义制表位。自定义制表位使用tabs元素定义。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.32。  
noBreakHyphen | 可以添加不间断连字符，这样行不会在连字符处断开，就像使用连字符减号字符（U+00D2）时可能发生的情况。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.18。<w:r> <w:t>每个公民都有一个唯一的社会保障号码，格式为"999</w:t> </w:r> <w:r> <w:noBreakHyphen/> </w:r> <w:r> <w:t>99</w:t> </w:r> <w:r> <w:noBreakHyphen/> </w:r> <w:r> <w:t>9999。"</w:t> </w:r>  
Word 2007 示例：| ![不间断连字符](images\wp-nobreakHyphen-1.gif)

---

softHyphen | 可以添加一个可选连字符，当需要断行时，它可能显示为常规连字符，但在其他情况下宽度为零。它通常用于标记单词可以连字符分割的位置，而不会导致不必要地显示连字符。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.29。<w:r> <w:t>这个句子需要足够长，以便引起某种换行</w:t> </w:r> <w:r> <w:softHyphen/> </w:r> <w:r> <w:t>ing。</w:t> </w:r>  
Word 2007 示例：| ![软连字符](images\wp-softHyphen-1.gif)

---

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
