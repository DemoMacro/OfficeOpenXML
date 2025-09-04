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

# 文字处理样式

定义样式 - 表格样式 - 条件格式

表格样式可以定义应用于表格不同区域的条件格式。条件格式由<w:style>元素内的<w:tblStylePr>元素指定。可以具有条件格式的区域如下所示。

| 左上角单元格 | 标题行   | 右上角单元格 |
| ------------ | -------- | ------------ |
| 第一列       | 表格主体 | 最后一列     |
| 左下角单元格 | 页脚行   | 右下角单元格 |

除了上述区域外，表格中的行还可以基于交替的行/列具有条件格式，以实现条纹效果。例如，下面的示例具有条纹行和列，其中奇数行和列应用了格式。

![Table Conditional Formatting](images\wp-tableCondFormatting-1.gif)

---

在引用表格样式的给定表格中，每组条件格式的实际应用由表格的tblPr中tblLook元素的属性确定。通过这种方式，这些属性是"有条件的"。请参阅[表格 - 条件格式](WPtblLook.md)。下面是样式部分中表格样式的定义，该定义定义了非条件格式，以及第一行的条件格式，包括表格单元格的加粗和红色底纹，以及最后一行的间距格式。

<w:style w:type="table" w:styleId="TestTableStyle">

<w:name w:val="Test Table Style"/>

<w:basedOn w:val="TableNormal"/>

<w:tblPr>

. . .

</w:tblPr>

<w:tblStylePr w:type="firstRow">

<w:rPr>

<w:b/>

</w:rPr>

<w:tcPr>

<w:shd w:val="clear" w:color="auto" w:fill="ED1C24"/>

</w:tcPr>

</w:tblStylePr>

<w:tblStylePr w:type="lastRow">

<w:pPr>

<w:spacing w:before="0" w:after="0" w:line="240" w:lineRule="auto"/>

</w:pPr>

</w:tblStylePr>

</w:style>

![](images/note.png)注意：表格样式定义中可能有多个<w:tblStylePr>实例 - 每个条件格式区域一个。

然后，上述表格样式在内容中的应用如下所示。特别注意<w:tblLook>元素。第一行的加粗和底纹格式被应用，因为<w:tblLook>元素的firstRow属性值为true。最后一行的条件格式未被应用。

<w:tbl>

<w:tblPr>

<w:tblStyle w:val="TestTableStyle"/>

<w:tblW w:w="0" w:type="auto"/>

<w:tblLook w:firstRow="true"/>

</w:tblPr>

</w:tbl>

请注意，当应用多个条件格式集时，它们之间可能存在冲突。条件格式按以下顺序应用：

- 整个表格
- 条纹列，偶数列条纹
- 条纹行，偶数行条纹
- 第一行，最后一行
- 第一列，最后一列
- 左上，右上，左下，右下

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6。

### <w:tblStylePr>的属性

只有一个属性type，它确定条件格式应用的区域。

| 属性 | 描述           |
| ---- | -------------- |
| type | 可能的值如下： |

- band1Horz - 格式应用于奇数编号的行组
- band1Vert - 格式应用于奇数编号的列组
- band2Horz - 格式应用于偶数编号的行组
- band2Vert - 格式应用于偶数编号的列组
- firstCol - 格式应用于第一列
- firstRow - 格式应用于第一行
- lastCol - 格式应用于最后一列
- lastRow - 格式应用于最后一行
- neCell - 格式应用于右上角单元格
- nwCell - 格式应用于左上角单元格
- seCell - 格式应用于右下角单元格
- swCell - 格式应用于左下角单元格
- wholeTable - 格式应用于整个表格

### <w:tblStylePr>的子元素：

| 元素  | 描述                                                                                                                                                                                                                                                                           |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| pPr   | 指定应用于表格中与条件格式类型匹配的段落的段落属性集。有关详细信息，请参阅[段落 - 属性](WPparagraphProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.1。                                                                                         |
| rPr   | 指定应用于表格中与条件格式类型匹配的文本运行的运行属性集。有关详细信息，请参阅[文本 - 格式](WPtextFormatting.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.2。                                                                                          |
| tblPr | 指定应用于表格中与条件格式类型匹配的所有区域的表格属性集。有关详细信息，请参阅[表格 - 属性](WPtableProperties.md)。如果条件格式不由一个或多个完整表格行组成，则无法应用于单个单元格或列的表格属性将被忽略。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.3。 |
| tcPr  | 指定应用于表格中与条件格式类型匹配的单元格的表格单元格属性集。有关详细信息，请参阅[表格 - 单元格属性](WPtableCellProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.8。                                                                           |
| trPr  | 指定应用于表格中与条件格式类型匹配的行的表格行属性集。有关详细信息，请参阅[表格 - 行属性](WPtableRowProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.10。                                                                                       |

### 相关的HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级。</li>

<li style="list-style-type:upper-alpha; margin-left:2cm;">这是第二级。</li>

<li style="list-style-type:decimal; margin-left:4cm;">这是第三级。</li>

</ol>

HTML/CSS示例：

1. 这是第一级。
2. 这是第二级。
3. 这是第三级。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
