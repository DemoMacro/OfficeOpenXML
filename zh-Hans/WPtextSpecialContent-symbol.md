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

符号

符号使用w:r元素内的w:sym元素指定。符号是一种特殊字符，不使用rFonts或样式层次结构中指定的任何运行字体。该字符是通过从font属性指定的字体中提取char属性指定的十六进制值来确定的。

<w:r>

<w:rPr>

<w:fonts w:ascii="Courier New" w:hAnsi="Courier New"/>

<w:rPr>

<w:t xml:space="preserve">这是Courier New文本。>/w:t>

</w:r>

<w:r>

<w:rPr>

<w:fonts w:ascii="Courier New" w:hAnsi="Courier New"/>

<w:rPr>

<w:t xml:space="preserve">这是一个Wingdings字符>/w:t>

<w:sym w:font="Wingdings" w:char="F034"/>

</w:r>

Word 2007 示例：

![Text - Symbols](images\wp-symbols-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.3.30。

### 属性：

| 属性 | 描述                                                                |
| ---- | ------------------------------------------------------------------- |
| char | 指定符号的Unicode字符值的十六进制代码。该值可以以下列任一格式存储： |

- 直接以其字体字形中的Unicode字符值
- 在通过向字符值添加F000创建的Unicode字符值中，从而将值移入Unicode私有使用区域。这样做是为了与旧版文字处理格式实现互操作性。因此，在上面的示例中，char属性的值是F034，因此我们将通过从F034中移除F000来获取字符值，以获得Wingdings字体中十六进制值0x34处的字符（或十进制值52）。

font | 指定用于格式化符号的字体。

### 相关HTML/CSS属性：

符号可以在HTML中作为字符实体使用短名称（例如，&copy;）引用。请参阅[W3关于字符引用的建议](http://www.w3.org/TR/html4/sgml/entities.md)。符号也可以使用数字字符引用形式&#number（十进制形式）或&#xnumber（十六进制形式）引用。[请参阅W3建议](http://www.w3.org/TR/html4/charset.html#h-5.3.1)。

HTML中仅正式支持Unicode字符，并且只应使用这些字符，因为并非所有浏览器都会有Wingdings等字体。但是，可以在CSS中指定字体，并对所需字体中的所需字符进行数字字符引用。

<div>这是一个Wingdings字符<span style="font-family:Wingdings;">&#52;</span>。只有您的机器上安装了Wingdings才能看到此字符。</div>   
<div>这是使用其短名称引用的版权符号：&copy;</div>   
<div>这是使用数字字符引用的商标符号：&#8482;。</div>

CSS 示例：

这是一个Wingdings字符4。只有您的机器上安装了Wingdings才能看到此字符。

这是使用其短名称引用的版权符号：©

这是使用数字字符引用的商标符号：™。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
