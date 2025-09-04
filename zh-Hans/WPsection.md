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

相关的Open Office/ODF讨论  
相关的HTML/CSS讨论

概述

OOXML不定义页面—只定义段落和文本。但是，它确实允许存储对页面构成重要的某些信息，如页面大小、页面方向、边框和边距。它通过使用节来实现这一点。节是具有一组特定属性的段落分组，这些属性用于定义文本将出现的页面。

节的属性存储在sectPr元素中。对于除最后一节之外的所有节，sectPr元素作为该节中最后一个段落的子元素存储。对于最后一节，sectPr作为body元素的子元素存储。以下示例显示两个节—第一个是纵向方向，第二个是横向方向。

<w:body>

<w:p>

. . .

</w:p>

<w:p>

<w:pPr>

<w:sectPr>

<w:pgSz w:w="12240" w:h="15840"/>

</w:sectPr>

</w:pPr>

</w:p>

<w:p>

. . .

</w:p>

<w:sectPr>

<w:pgSz w:w="15840" w:h="12240" w:orient="landscape"/>

</w:sectPr>

</w:body>

### 元素：

| 元素            | 描述                                                                                                                                                                                                                     |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| cols            | 指定节的列集。请参阅[节 - 列](WPsectionCols.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.4。                                                                                                       |
| footerReference | 指定要与节关联的页脚。页脚通过id属性引用。请参阅[节 - 页脚](WPsectionFooterReference.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.2。                                                             |
| formProt        | 指定节的内容不能由用户编辑，表单字段中包含的文本除外。请注意，执行由设置部分中的documentProtection元素确定。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.6。                                            |
| headerReference | 指定要与节关联的页眉。页眉通过id属性引用。请参阅[节 - 页眉](WPsectionHeaderReference.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.5。                                                             |
| lnNumType       | 指定要在节中每列文本前显示的行号 — 例如，<w:lnNumType w:countBy="3" w:start="1" w:restart="newSection"/>。请参阅[节 - 行号](WPsectionLineNumering.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.8。 |
| paperSrc        | 指定用于首页和后续页面的打印机托盘的打印机特定设置。例如，<w:paperSrc w:first="1" w:other="1"/>。有两个属性：                                                                                                            |

- first \- 指定唯一标识用于首页的打印机托盘的代码。默认值1表示打印机应自动选择托盘。
- other \- 指定唯一标识用于所有后续页面的打印机托盘的代码。默认值1表示打印机应自动选择托盘。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.9。  
pgBorders | 指定节中每页的页面边框。请参阅[节 - 页面边框](WPsectionBorders.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.10。  
pgMar | 指定节中每页的页边距。请参阅[节 - 页边距](WPsectionPgMar.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.11。  
pgNumType | 指定节中页面的页码编号。请参阅[节 - 页码](WPSectionPgNumType.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.12。  
pgSz | 指定节中所有页面的属性（大小和方向）。例如，<w:pgSz w:h="12240" w:w="15840" w:orient="landscape"/>。重要属性如下。 | 属性 | 描述  
---|---  
h | 以点的二十分之一指定页面高度。  
w | 以点的二十分之一指定页面宽度。  
orient | 指定页面方向。可能的值为landscape（横向）和portrait（纵向）。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.6.13。

titlePg | 指定节是否应为其首页使用不同的页眉和页脚。如果元素设置为true（例如，<w:titlePg/>），则节将使用首页页眉；如果为false（例如，<w:titlePg w:val="false"/>）（默认值），则首页使用奇数页页眉。如果元素设置为true但省略了首页页眉类型，则会创建空白页眉。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.6。  
type | 指定节类型。它确定节的内容将如何相对于前一节放置。例如，<w:type w:val="nextPage"/>。有五种不同的类型，对应于val属性的五个可能值。

- continuous - 在下一段落开始节。某些页面级别的节属性不能指定，因为它们是从前一节继承的。如果脚注出现在与此类节相同的页面上，则新节从下一页开始。
- evenPage - 节从下一个偶数页开始，必要时留空下一个奇数页。
- nextColumn - 节从页面上的下一列开始。
- nextPage - 节从下一页开始。
- oddPage - 节从下一个奇数页开始，必要时留空下一个偶数页。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.22。  
vAlign | 指定节中文本的垂直对齐方式，相对于上下边距。例如，<w:vAlign w:val="center"/>。有一个属性val，具有以下可能值：

- both - 通过根据需要向每个段落添加额外空间，使文本在上下边距之间垂直对齐
- bottom - 文本垂直对齐到底边距
- center - 文本垂直对齐到中心
- top - 文本垂直对齐到上边距

下面是<w:vAlign w:val="both"/>的示例。 | ![节垂直对齐](images\wp-sectionValign-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.10.23。

---

---

# 相关开放文档格式(ODF)属性：

ODF格式中的节使用<text:section>元素定义。它表示文档中命名的内容区域。节用于为区域分配某些格式或对从外部数据源获取的文本进行分组。因此，节可以包含常规文本内容，或者文本可以存储在另一个文件中并链接到节。这种到外部源的链接可以通过XLink标识的资源（<text:section-source>）或动态数据交换(DDE)（<text:dde-source>）实现。节也可以写保护或隐藏。

节在段落边界处开始和结束。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 5.4。

<text:section text:style-name="Sect1" text:name="Section2">

<text:p text:style-name="Standard"/>

</text:section>

### 属性：

最常用的属性如下。

| 属性            | 描述                                                                                      |
| --------------- | ----------------------------------------------------------------------------------------- |
| text:name       | 指定唯一名称。                                                                            |
| text:style-name | 指定节的节系列样式。                                                                      |
| xml:id          | 指定唯一ID，并由W3C（xml-id）标准化。                                                     |
| text:protected  | 指定节是否受保护，以便用户无法编辑它。值为true和false。                                   |
| text:display    | 指定节是否隐藏。值为true、none和condition。如果是condition，则在condition属性中提供条件。 |

### 元素：

最常用的元素如下。

| 元素                    | 描述           |
| ----------------------- | -------------- |
| table:table             | 指定表格。     |
| text:h                  | 指定标题。     |
| text:list               | 指定列表。     |
| text:numbered-paragraph | 指定编号段落。 |
| text:p                  | 指定段落。     |
| text:section            | 指定节。       |
| text:table-of-content   | 指定目录。     |

---

# 相关HTML/CSS属性：

没有对应的HTML属性。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
