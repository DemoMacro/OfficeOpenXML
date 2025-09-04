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

相关Open Office/ODF讨论  
相关HTML/CSS讨论

结构

文本运行定义了具有一组共同属性的非块文本区域。它使用<w:r>元素指定。文本运行的属性使用<w:rPr>元素指定，该元素是<w:r>的第一个元素。文本运行最常包含文本元素<w:t>（包含段落的实际字面文本），但它们也可能包含特殊内容，如符号、制表符、连字符、回车符、绘图、分隔符和脚注引用。参见[特殊内容](WPtextSpecialContent.md)。

<w:r>

<w:rPr>

<w:b/>

<w:i/>

</w:rPr>

<w:t>我觉得凯尔特人的信仰很有道理，他们认为我们失去的人的灵魂被囚禁在某些低等生物中…</w:t>

</w:r>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 §§ 17.3.2, 17.3.3 和 17.3.2.25。

Word 2007 示例：

![Paragraph](images\wp-paragraph-1.gif)

---

### 元素：

<w:r>元素可以包含大量元素。最常用的元素如下所示。

| 元素          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| br            | 指定分隔符。参见[文本 - 特殊内容](WPtextSpecialContent.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.1。                                                                                                                                                                                                                                                                                                                                 |
| cr            | 指定回车符。参见[文本 - 特殊内容](WPtextSpecialContent.md)。<w:r><w:t>这是另一个</w:t&gt <w:cr/><w:t xml:space="preserve"> 简单句子。</w:t></w:r> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.4。                                                                                                                                                                                                                                           |
| drawing       | 指定绘图对象（即图形DrawingML对象，如图表、图形或图片）位于文本运行中。DrawingML对象在文档中的布局（即其在页面上的位置）使用WordProcessingL绘图语法指定。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.9。                                                                                                                                                                                                                                    |
| noBreakHyphen | 指定不间断连字符。参见[文本 - 特殊内容](WPtextSpecialContent.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.18。                                                                                                                                                                                                                                                                                                                          |
| rPr           | 指定文本运行的属性。参见[样式 - 字符样式](WPstyleCharStyles.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.28。                                                                                                                                                                                                                                                                                                                           |
| softHyphen    | 指定软连字符。参见[文本 - 特殊内容](WPtextSpecialContent.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.29。                                                                                                                                                                                                                                                                                                                              |
| sym           | 指定特殊字符或符号。参见[文本 - 符号](WPtextSpecialContent-symbol.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.30。                                                                                                                                                                                                                                                                                                                     |
| t             | 指定将在文本运行中显示的字面文本。文档中几乎所有文本都包含在t元素中，域代码中的文本除外。XML命名空间中有一个可能的属性（xml:space），可用于指定如何处理t元素中的空格。可能的值是preserve和default。如果需要保留文本运行中的空白，则必须将此属性设置为preserve。请参见XML 1.0规范 § 2.10。<w:r> <w:t>这是另一个</w:t> </w:r> <w:r><w:br/><w:t xml:space="preserve"> 简单句子。</w:t> </w:r> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.31。 |
| tab           | 指定制表符。参见[文本 - 特殊内容](WPtextSpecialContent.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.32。                                                                                                                                                                                                                                                                                                                                |

---

# 相关开放文档格式(ODF)属性：

ODF中文本的内容模型与HTML非常相似。字符数据位于段落内，不像在OOXML中那样进一步嵌套在文本运行和文本元素中。当需要对段落内的文本进行格式化时，使用<text:span>元素。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 5.1.3。

<text:p>这个句子的最后一个词是

<text:span text:style-name="emphasis">强调</text:span>。

</text:p>

---

# 相关HTML/CSS属性：

没有对应的HTML属性。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
