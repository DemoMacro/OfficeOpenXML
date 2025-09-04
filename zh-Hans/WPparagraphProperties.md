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
- [文本框架](WPparagraph-textFrames.md)
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

属性

段落属性在<pPr>中指定。每个属性都是<pPr>的子元素。当出现在段落(w:p)元素中而不是样式元素(w:style)中时，它们是直接格式，并在样式/编号/表格属性之后应用。与段落样式比较。

<w:pPr>

<w:pBdr>

<w:bottom w:val="single" w:sz="8" w:space="4" w:color="4F81BD"/>

</w:pBdr>

<w:spacing w:after="300"/>

</w:pPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.26。

最常用的属性如下所示：

### 元素/属性：

| 元素      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |
| framePr   | 将段落定义为文本框架，这是一个类似于文本框的独立段落。参见[文本框架](WPparagraph-textFrames.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.11。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ind       | 定义段落的缩进。参见[段落 - 缩进](WPindentation.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.12。                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| jc        | 指定段落对齐方式。参见[段落 - 对齐](WPalignment.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.13。                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| keepLines | 指定在可能的情况下，段落的所有行都应保持在同一页上。它是一个空元素：<w:keeplines/>。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.14。                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| keepNext  | 指定在可能的情况下，段落（或至少其一部分）应与下一段呈现在同一页上。它是一个空元素：<w:keepNext/>。如果多个段落要保持在同一页但它们超过一页，则这组段落将在新页上开始，并根据需要使用分页符。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.15。                                                                                                                                                                                                                                                                                                                                  |
| numPr     | 指定段落应编号，并继承编号部分中num元素内编号定义指定的属性。特定的编号定义由numPr的numId子元素指定，而编号定义中的特定级别由numPr的ilvl子元素指定。<w:pPr> <w:numPr> <w:ilvl w:val="0"/> <w:numId w:val="1"/> </w:numPr> </w:pPr> numPr具有以下子元素。                                                                                                                                                                                                                                                                                                                                           | 元素 | 描述 |
| ---       | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| numId     | 指定对编号定义实例的引用（对应于<w:num w:numId="1"/>）。该实例将出现在编号部分中，并引用定义编号的<w:abstractNum>元素。numId具有单个属性val。val属性不会具有0值，除非是为了在样式层次结构的特定级别删除编号属性（如直接格式）。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.19。                                                                                                                                                                                                                                                                                                  |
| ilvl      | 指定要用于段落的编号定义的编号级别。它对应于编号部分的<w:abstractNum>元素内的<w:lvl w:ilvl="0">元素。![](images/note.png)注意：当使用直接格式进行编号时（即pPr不在样式内），则编号定义实例和实例内的级别都通过包含numId和ilvl来指定。当作为样式的一部分进行编号时，仅指定numId。要应用的编号定义的级别在编号定义中通过对段落样式的引用来指示。请参见下面的示例。<w:abstractNum w:abstractNumId="1"> . . . <w:lvl w:ilvl="0"> . . . <w:pStyle w:val="TestParagraphStyle"/> <w:pPr> . . . </w:pPr> . . . </w:lvl> </w:abstractNum> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.9.3。 |

有关编号的更多讨论，请参见[编号、级别和列表 - 概述](WPnumbering.md)。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.19。

outlineLvl | 指定与段落关联的大纲级别。它用于构建目录，不影响文本的外观。单个属性val可以具有0到9的值，其中9表示没有大纲级别适用于该段落。因此<w:outlineLvl w:val="0"/>表示该段落是大纲级别1。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.20。  
pBdr | 指定段落的边框。参见[段落 - 边框](WPborders.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.24。  
pStyle | 指定段落样式的样式ID。参见[定义样式 - 段落样式](WPstyleParStyles.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.27。  
rPr | 指定段落标志符号的运行属性，该符号用于表示段落标记的物理位置。当标记被格式化时，rPr出现在pPr内。然后文本相应地格式化，除了可能的直接文本格式。参见[文本 - 格式化](WPtextFormatting.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.29。  
sectPr | 指定节的属性。对于除最后一节之外的所有节，sectPr元素存储为该节中最后一段的子元素。对于最后一节，sectPr存储为body元素的子元素。参见[节](WPsection.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.18。  
shd | 指定段落的底纹。参见[段落 - 底纹](WPshading.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.31。  
spacing | 指定段落之间和段落行之间的间距。参见[段落 - 间距](WPspacing.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.33。  
tabs | 指定自定义制表符。参见[段落 - 制表符](WPtab.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.38。  
textAlignment | 指定当字符大小不同时每行上字符的对齐方式。参见[段落 - 垂直文本对齐](WPtextAlignment.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.39。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
