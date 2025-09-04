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

# 文字处理域

域定义

| 域     | 描述                                                                                                                                                    | 开关                                              | 示例                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ----------------------- |
| AUTHOR | 检索并可选地设置核心文件属性部分的Creator元素中记录的文档作者名称。要更新该域，请添加参数。例如，AUTHOR "Tony Danza"会使Creator元素取值为"Tony Danza"。 | 使用[常规域格式开关](WPgeneralFieldSwitches.md)。 | AUTHOR \\\* Caps 显示： |

Henry Miller  
CREATEDATE | 检索文档创建的日期和时间（默认使用公历），如核心文件属性部分的DateCreated元素中所记录。 | 使用[日期和时间格式开关](WPdateTimeFieldSwitches.md)。 | CREATEDATE 显示：  
1/4/2006 10:31:00 PM CREATEDATE \@ "dddd, MMMM dd,yyyy HH:mm:ss" 显示：  
2006年1月4日星期三 22:31:00  
DATE | 检索当前日期和时间（默认使用公历）。 | 使用[日期和时间格式开关](WPdateTimeFieldSwitches.md)。还有一个\l开关，指定如果未使用日期和时间开关，则使用上次使用的日期和时间格式开关。 | DATE 显示：  
1/4/2006 10:31:00 PM DATE \@ "dddd, MMMM dd,yyyy HH:mm:ss" 显示：  
2006年1月4日星期三 22:31:00  
FILESIZE | 检索WordprocessingML包的大小（以字节为单位）。 | 使用[数字格式开关](WPnumericFieldSwitches.md)或[常规格式开关](WPgeneralFieldSwitches.md)。还有一个\k开关，四舍五入到最接近的千字节，以及一个\m开关，四舍五入到最接近的百万字节。 | FILESIZE \\# #,##0 显示：  
4,660,736 FILESIZE \\#k 显示：  
4661 FILESIZE \\#m 显示：  
5  
PAGE | 检索当前页的页码。 | 使用[常规格式开关](WPgeneralFieldSwitches.md)。 | PAGE 显示：  
19 PAGE \\_ ArabicDash 显示：  
-19- PAGE \\# roman 显示：  
xix  
SAVEDATE | 检索文档上次保存的日期和时间（默认使用公历），如核心文件属性部分的DateModified元素中所记录。对于从未保存过的文档，日期和时间为0000-00-00T00:00:00，每个文本组件为XXX。 | 使用[日期和时间格式开关](WPdateTimeFieldSwitches.md)。 | SAVEDATE 显示：  
1/6/2006 3:15:00 PM SAVEDATe \@ "dddd, MMMM dd,yyyy HH:mm:ss" 显示：  
2006年1月4日星期三 22:31:00 对于未保存的文档，相同的格式选项将显示  
0/0/0000 0:00 AM  
和 XXX, XXX 00, 0000 00:00:00  
SECTION | 检索当前节的编号。 | 使用[常规格式开关](WPgeneralFieldSwitches.md)。 | SECTION 显示：  
19 SECTION "My Life, the Fantasy" \\_ Upper 将值设置为*My Life, the Fantasy*，结果是  
MY LIFE THE FANTASY SECTION \\_ ArabicDash 显示：  
-19- SECTION \\# roman 显示：  
xix  
SEQ *标识符* *域参数* | 对章节、表格、图形和其他用户定义的项目列表进行顺序编号；它类似于LISTNUM域。标识符是分配给要编号的项目的名称—例如，Figure或Table。域参数指定引用文档中其他位置项目的书签名称。 | 使用[数字格式开关](WPnumericFieldSwitches.md)或以下之一：\c重复最接近的前一个编号；\h隐藏结果，除非同时存在常规格式开关；\n插入下一个序列号（默认值）；\r *域参数*将序列号重置为域参数指定的整数；\s将序列号重置为域参数指定的内置标题级别。 | SEQ Figure 显示：  
Figure 1 SEQ Figure \\_ roman 显示：  
Figure ii  
TIME | 检索当前日期和时间。 | 使用[日期和时间格式开关](WPdateTimeFieldSwitches.md)。 | TIME 显示：  
1:59 PM TIME \@ "dddd, MMMM dd,yyyy HH:mm:ss" 显示：  
2006年1月4日星期三 22:31:00  
TITLE | 检索并可选地设置核心文件属性部分的Title元素中记录的文档标题。通过指定域参数来设置该域。 | 使用[常规格式开关](WPgeneralFieldSwitches.md)。 | TITLE 显示：  
My Life's Story TITLE "My Life, the Fantasy" \\_ Upper 将值设置为*My Life, the Fantasy*，结果是  
MY LIFE THE FANTASY  
TOC | 见[目录](WPtableOfContents.md)。 | |  
USERNAME | 检索当前用户的名称或域参数指定的名称。 | 使用[常规域格式开关](WPgeneralFieldSwitches.md)。 | USERNAME \\_ Lower 显示：  
david williams USERNAME "John Jones" 显示：  
John Jones USERNAME "Mary Smith" \\\* Upper 显示：  
MARY SMITH

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
