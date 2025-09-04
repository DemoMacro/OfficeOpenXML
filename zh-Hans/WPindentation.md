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

# 文字处理段落

相关的Open Office/ODF讨论  
相关的HTML/CSS讨论

缩进

缩进使用<w:ind>元素定义。

<w:pPr>

<w:ind w:left="1440" w:right="1440" />

</w:pPr>

值以点的二十分之一为单位：1440 twips = 1英寸；567 twips = 1厘米。要以字符的百分之一指定单位，请使用leftChars/endChars、rightChars/endChars等属性。可以使用负值。请参见下面的属性。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.3.1.12。

Word 2007示例：

![Simple Indent](images\wp-ind-simpleIndent.gif)

---

### 属性：

最常用的属性是：

| 属性       | 描述                                                                                                                                                                             |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| left/start | 指定要放置在左侧的缩进（对于从左到右的段落）。![](images/versionConflict3.png)注意：OOXML标准的2006版本指定了left，但2011版本指定了start。Microsoft Word 2007似乎无法识别start。 |
| right/end  | 指定要放置在右侧的缩进（对于从左到右的段落）。![](images/versionConflict3.png)注意：OOXML标准的2006版本指定了right，但2011版本指定了end。Microsoft Word 2007无法识别end。        |
| hanging    | 指定要从第一行移除的缩进。此属性和firstLine互斥。当两者都指定时，此属性起控制作用。                                                                                              |
| firstLine  | 指定要应用于第一行的额外缩进。此属性和hanging互斥。如果指定了hanging，则忽略此属性。                                                                                             |

Word 2007示例：

<w:pPr>

<w:ind w:left="1440" w:right="1440" w:hanging="1080" />

</w:pPr>

![Simple Indent](images\wp-ind-hangingIndent.gif)

---

---

# 相关的开放文档格式(ODF)属性：

有两个相关的ODF属性。首先，可以通过在应用于段落的样式中的<style:paragraph-properties>元素上设置fo:margin、fo:margin-left或fo:margin-right属性来指定段落的缩进。值可以是长度或百分比，指的是父样式的边距。

其次，段落第一行的缩进是通过在<style:paragraph-properties>元素上设置fo:text-indent属性来指定的。值可以是长度，或者如果属性包含在通用样式中，则值可以是百分比，指的是父样式的文本缩进。

参考：办公应用程序的开放文档格式版本1.2（2011年5月）§§20.198、20.200、20.201和20.218。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard">

<style:paragraph-properties fo:margin-left="0.5in" fo:margin-right="0in" fo:text-indent="0.2402in" style:auto-text-indent="false"/>

</style:style>

---

# 相关的HTML/CSS属性：

margin-left: 35px;  
margin-right: 35px;  
text-indent: 15px;

CSS示例：

声音咒语被打破了。我们已经解救了他们：他们已经战胜死亡并回来分享我们的生活。

我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。

过去隐藏在领域之外的某个地方，超出智力的范围，在某些物质中

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
