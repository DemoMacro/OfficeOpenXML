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

定义样式 - 常规属性

常规样式属性是可以在样式定义中使用的属性，无论样式类型如何—例如样式名称、别名、ID等。常规属性的示例在下面以蓝色显示。

<w:style w:type="paragraph" w:styleId="Heading1">

<w:name w:val="Heading 1"/>

<w:basedOn w:val="Normal"/>

<w:next w:val="Normal"/>

<w:link w:val="Heading1Char"/>

<w:uiPriority w:val="9"/>

<w:qFormat/>

<w:pPr>

<w:keepNext/>

<w:keepLines/>

<w:numPr>

<w:numId w:val="2"/>

</w:numPr>

<w:spacing w:before="480" w:after="0"/>

<w:outlineLvl w:val="0"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:b/>

<w:color w:val="365F91"/>

<w:sz w:val="28"/>

</w:rPr>

</w:style>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4。

### 作为常规样式属性的<w:style>的子元素：

最重要的属性如下。一些与样式修订和电子邮件相关的属性被省略。

| 元素         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| aliases      | 指定一组样式的替代名称，如果在设置部分中的stylePaneFormatFilter元素中设置了适当的值，则可以在应用程序的用户界面中使用这些替代名称，而不是name元素中指定的名称。它有一个单独的属性val，包含一个或多个名称，用逗号分隔。<w:style w:styleId="TestStyle"> <w:name w:val="GD20Complex"/> <w:aliases w:val="Regional Growth,Complex Growth"/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.1。 |
| autoRedefine | 指定当应用了此样式的整个段落的内容被修改时，应用程序应自动修改样式。如果设置了此项，则对段落的更改将存储在样式中，而不是作为直接格式，并且所有使用该样式的段落将被更改以反映在一个修改段落中的更改。<w:style w:styleId="TestStyle"> . . . <w:autoRedefine/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.2。                                                                             |
| basedOn      | 指定当前样式所基于的样式—即当前样式继承的样式。它是实现样式继承的机制。该元素有一个单独的属性val，指定当前样式所基于的样式的styleId属性的值。请注意，如果当前样式的类型必须与其所基于的样式的类型匹配，否则basedOn元素将被忽略。但是，如果当前样式是编号样式，则basedOn元素将被忽略。<w:style w:styleId="Strong"> <w:basedOn w:val="Underline"/> . . . <w:rPr>                                                               |

<w:b/> </w:rPr> </w:style> <w:style w:styleId="Underline"> <w:basedOn w:val="Emphasis"/> . . . <w:rPr>  
<w:u/> </w:rPr> </w:style> <w:style w:styleId="Emphasis"> . . . <w:rPr>  
<w:i/> </w:rPr> </w:style> 上面示例中的Strong样式继承自Underline样式，而Underline样式继承自Emphasis样式。结果是Strong样式具有粗体、下划线（继承自Underline）和斜体（继承自Emphasis）。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.3。  
hidden | 指定样式应该从所有用户界面中隐藏。结果是该样式可用于格式化内容，但用户无法访问它。<w:style w:styleId="TestStyle"> . . . <w:hidden/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.4。  
link | 指定样式的配对以构成链接样式。链接样式是段落样式与字符样式的组合。每个样式在样式部分中独立存在，但它们根据应用于文本运行还是段落而适当合并和应用，并在应用程序中显示为一个样式。请注意，两个样式必须是段落和字符类型，否则link元素将被忽略。有一个单独的属性val，指定相应的字符或段落样式的ID。<w:style w:type="paragraph" w:styleId="TestParagraphStyle"> <w:link w:val="TestCharacterStyle"/> . . . </w:style> <w:style w:type="character" w:styleId="TestCharacterStyle"> <w:link w:val="TestParagraphStyle"/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.6。  
locked | 指定样式不能应用于其他内容。也就是说，该样式可用于设置引用该样式的现有内容的样式，但不能应用该样式的新实例。<w:style w:styleId="TestStyle"> . . . <w:locked/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.7。  
name | 指定样式的主要名称，可在用户界面中使用。名称存储在val属性中。请注意，如果由aliases元素指定（并且在设置部分中的stylePaneFormatFilter元素中设置了适当的值），则用户界面将使用替代名称。<w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.9。  
next | 指定要自动应用于应用了当前样式的段落之后创建的新段落的样式。它通常应用于只应出现一次的内容，例如后面应有常规文本的标题。这仅适用于段落样式。有一个单独的属性val，指定用于下一段落的段落样式的ID。<w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:next w:val="AnotherParagraphStyle"/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.10。  
semiHidden | 指定加载文档时应从主用户界面中隐藏样式。"主用户界面"的含义未指定。请注意，通过包含如下所示的unhideWhenUsed元素，如果在内容中使用了该样式，则在重新保存文档时会删除semiHidden元素。<w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:semiHidden/> <w:unhideWhenUsed/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.16和§ 17.7.4.20。  
uiPriority | 指定一个数字，当在设置部分中设置了stylePaneSortMethod元素时，该数字可用于在用户界面对样式定义集进行排序。有一个单独的val属性，包含作为数字的优先级。<w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:uiPriority w:val="10"/> . . . </w:style> 参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.7.4.19。

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
