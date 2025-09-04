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

定义样式 - 表格样式

表格样式应用于表格内容，其类型属性值为table。首先是表格属性（在tblPr元素内），应用于整个表格；其次是行级属性（在trPr元素内），应用于表格行；还有单元格级属性（在tcPr元素内），应用于表格单元格。所有这三种属性类型都在style元素内，并且总是被应用（尽管它们可能被其他属性覆盖）。

#### 条件格式

表格样式还可以定义条件属性（在tblStylePr元素内）。这些样式应用于表格的不同区域。这些区域如下所示。

| 左上角单元格 | 标题行   | 右上角单元格 |
| ------------ | -------- | ------------ |
| 第一列       | 表格主体 | 最后一列     |
| 左下角单元格 | 页脚行   | 右下角单元格 |

表格中的行也可以基于交替的行/列进行条件格式设置，以实现带状效果。例如，下面的示例具有带状行和列，奇数行和列应用了格式。

![Table Conditional Formatting](images\wp-tableCondFormatting-1.gif)

---

表格样式通过在内容中的表格属性元素（<w:tblPr>）内包含<w:tblStyle>元素来引用或应用。例如，下面是样式部分中表格样式的定义，它定义了一个由顶部和底部边框组成的非条件格式，以及由表格单元格的粗体和红色底纹组成的条件格式。

<w:style w:type="table" w:styleId="TestTableStyle">

<w:name w:val="Test Table Style"/>

<w:basedOn w:val="TableNormal"/>

<w:tblPr>

<w:tblBorders>

<w:top w:val="single" w:sz="4" w:space="0" w:color="auto"/>

<w:bottom w:val="single" w:sz="4" w:space="0" w:color="auto"/>

</w:tblBorders>

</w:tblPr>

<w:tblStylePr w:type="firstRow">

<w:rPr>

<w:b/>

</w:rPr>

<w:tcPr>

<w:shd w:val="clear" w:color="auto" w:fill="ED1C24"/>

</w:tcPr>

</w:tblStylePr>

</w:style>

上述表格样式随后在内容中应用，如下所示。特别注意<w:tblLook>元素。<w:tblStylePr>中定义的条件格式可以根据引用样式的表格中使用<w:tblLook>元素的指定来应用或不应用。从这个意义上说，格式是"有条件地"依赖于引用表格。例如，在上面的示例中，非条件边框格式必须被应用，除非它被覆盖。然而，第一行的粗体和底纹格式可能会或可能不会被应用，这取决于<w:tblLook>元素的firstRow属性是否包含true值。

<w:tbl>

<w:tblPr>

<w:tblStyle w:val="TestTableStyle"/>

<w:tblW w:w="0" w:type="auto"/>

<w:tblLook w:firstRow="true"/>

</w:tblPr>

</w:tbl>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6。

### 表格样式的子元素（<w:style w:type="table">）：

| 元素       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| tblPr      | 指定一组非条件且总是应用的表格属性（尽管它们可能被条件格式覆盖）。有关详细信息，请参阅[表格 - 属性](WPtableProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.4。                                                                                                                                                                                                                                                                                                                                                                                           |
| tcPr       | 指定一组非条件且总是应用的表格单元格属性（尽管它们可能被条件格式覆盖）。有关详细信息，请参阅[表格 - 单元格属性](WPtableCellProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.9。                                                                                                                                                                                                                                                                                                                                                                           |
| trPr       | 指定一组非条件且总是应用的表格行属性（尽管它们可能被条件格式覆盖）。有关详细信息，请参阅[表格 - 行属性](WPtableRowProperties.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.11。                                                                                                                                                                                                                                                                                                                                                                                   |
| tblStylePr | 指定一组有条件地应用于表格中满足type属性要求的部分的表格属性。有关详细信息，请参阅[样式 - 定义样式 - 表格样式 - 条件属性](WPstyleTableStylesCond.md)。![](images/note.png)注意：此元素可能有多个实例，每个区域一个。<w:style w:type="table" w:styleId="TestTableStyle"> . . . <w:tblStylePr w:type="firstRow"> . . . </w:tblStylePr <w:tblStylePr w:type="lastRow"> . . . </w:tblStylePr </w:style> 在引用该样式的给定表格中，这些条件格式集的实际应用由表格的tblPr中的tblLook元素的属性决定。参见[.](WPtblLook.md) 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.6.11。 |

### 相关HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级。</li>

<li style="list-style-type:upper-alpha; margin-left:2cm;">这是第二级。</li>

<li style="list-style-type:decimal; margin-left:4cm;">这是第三级。</li>

</ol>

HTML/CSS示例：

| 第1列标题 | 第2列标题 | 第3列标题 |
| --------- | --------- | --------- |
| AAA       | BBB       | CCC       |
| DDD       | EEE       | FFF       |
| GGG       | HHH       | III       |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
