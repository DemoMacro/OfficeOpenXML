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

# 文字处理域

常规域格式

常规格式开关指定数字或文本结果的多种格式。常规域格式开关具有以下格式：

\\\* _开关参数_

开关参数由一系列"图片项"组成。以下是美国英语中最常用于数值的开关参数。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.4.3。

### 常规格式 - 数值：

| 开关参数   | 描述                                                                                                                   | 示例                                                                              |
| ---------- | ---------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Arabic     | 使用阿拉伯基数数字格式化数值结果                                                                                       | PAGE \\\* Arabic 可能显示"123"。                                                  |
| CardText   | 将数值结果格式化为小写基数文本                                                                                         | PAGE \\\* CardText 可能显示"one hundred twenty-three"。                           |
| DollarText | 将数值结果格式化为以下形式：*整数部分作为基数文本*和*nn/100*。小数部分四舍五入到两位小数，并使用阿拉伯基数数字格式化。 | =1234.567 \\\* DollarText 显示"one thousand two hundred thirty-four and 57/100"。 |
| Ordinal    | 将数值结果格式化为小写序数阿拉伯数字                                                                                   | =32 \\\* Ordinal 显示"32nd"。                                                     |
| OrdText    | 将数值结果格式化为小写序数文本。请注意，小数部分仅用于四舍五入。                                                       | =1234.567 \\\* OrdText 显示"one thousand two hundred thirty-fifth"。              |
| Roman      | 使用大写罗马数字格式化数值结果                                                                                         | =PAGE \\\* Roman 可能显示"CXXIII"。                                               |
| roman      | 使用小写罗马数字格式化数值结果                                                                                         | =PAGE \\\* roman 可能显示"cxxiii"。                                               |

以下是美国英语中最常用于字符串值的开关参数。

### 常规格式 - 文本值：

| 开关参数 | 描述                     | 示例                                                   |
| -------- | ------------------------ | ------------------------------------------------------ |
| Caps     | 将每个单词的首字母大写   | USERNAME "mary smith" \\\* Caps 显示"Mary Smith"。     |
| FirstCap | 将第一个单词的首字母大写 | USERNAME "mary smith" \\\* FirstCap 显示"Mary smith"。 |
| Lower    | 所有字母均为小写         | USERNAME "mary smith" \\\* Lower 显示"mary smith"。    |
| Upper    | 所有字母均为大写         | USERNAME "mary smith" \\\* Upper 显示"MARY SMITH"。    |

### 常规格式 - 所有值：

以下开关参数适用于任何域结果：MERGEFORMAT 和 CHARFORMAT。

使用 MERGEFORMAT 保留应用于结果的任何直接格式，以便在后续域更新时保持这些格式。

例如，下面是一个示例，其中直接格式应用于为秒添加下划线。域的后续更新将使用相同的结构，仅更改时间值。

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> TIME \@ "HH:mm:ss" \\\* MERGEFORMAT</w:instrText>

</w:r>

<w:r>

<w:fldChar w:fldCharType="separate"/>

</w:r>

<w:r>

. . .

<w:t>17:02:</w:t>

</w:r>

<w:r>

. . .

<w:rPr>

<w:u w:val="single"/>

</w:rPr>

<w:t>32</w:t>

</w:r>

<w:r>

<w:fldChar w:fldCharType="end"/>

</w:r>

如果省略 MERGEFORMAT 开关，则后续域更新可能会导致单个新运行，如下所示。

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> TIME \@ "HH:mm:ss"</w:instrText>

</w:r>

<w:r>

<w:fldChar w:fldCharType="separate"/>

</w:r>

<w:r>

<w:t>12:22:27</w:t>

</w:r>

<w:r>

<w:fldChar w:fldCharType="end"/>

</w:r>

使用 CHARFORMAT 强制域使用应用于 begin fldChar 后的第一个 instrText 的格式来格式化整个域。例如，考虑下面的示例，其中域指令的第一个运行应用了粗体、下划线和红色。

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> </w:instrText>

</w:r>

<w:r>

. . .

<w:rPr>

<w:b/>

<w:color w:val="ED1C24"/>

<w:u w:val="single"/>

</w:rPr>

<w:instrText>D</w:instrText>

</w:r>

<w:r>

<w:instrText xml:space="preserve">ATE </w:instrText>

</w:r>

<w:r>

<w:fldChar fldCharType="separate"/>

</w:r>

<w:r>

. . .

<w:t>1/4/2006</w:t>

</w:r>

<w:r>

<w:fldChar fldCharType="end"/>

</w:r>

如果应用了 CHARFORMAT，则应用于第一个运行的格式将延续到域中的所有运行。

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> </w:instrText>

</w:r>

<w:r>

. . .

<w:rPr>

<w:b/>

<w:color w:val="ED1C24"/>

<w:u w:val="single"/>

</w:rPr>

<w:instrText>D</w:instrText>

</w:r>

<w:r>

<w:instrText xml:space="preserve">ATE /\* CHARFORMAT</w:instrText>

</w:r>

<w:r>

<w:fldChar fldCharType="separate"/>

</w:r>

<w:r>

. . .

<w:rPr>

<w:b/>

<w:color w:val="ED1C24"/>

<w:u w:val="single"/>

</w:rPr>

<w:instrText>1/4/2006</w:instrText>

</w:r>

<w:r>

<w:fldChar fldCharType="end"/>

</w:r>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
