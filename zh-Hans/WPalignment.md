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
    - [将图片或图像作为编号符号](WPnumbering-imagesAsSymbol.md)
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

相关Open Office/ODF讨论  
相关HTML/CSS讨论

对齐/两端对齐

应用于段落的对齐或两端对齐由<w:jc>元素指定。

<w:pPr>

<w:jc w:val="end"/>

</w:pPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.13。

Word 2007示例：

<w:pPr>

<w:jc w:val="left"/>

</w:pPr>

<w:pPr>

<w:jc w:val="right"/>

</w:pPr>

<w:pPr>

<w:jc w:val="both"/>

</w:pPr>

![Sample paragraph alignment](images\wp-jc-1.gif)

---

### 属性：

最常用的属性值如下：

| 属性 | 描述                           |
| ---- | ------------------------------ |
| val  | 指定段落对齐的值。可能的值有： |

- start \- 对于从左到右的文档，向左页边距对齐。![](images/versionConflict3.png)注意：在2003版标准中，此值为left。
- end \- 对于从左到右的文档，向右页边距对齐。![](images/versionConflict3.png)注意：在2003版标准中，此值为right。
- center \- 文本居中。
- both \- 在两个页边距之间均匀对齐文本，但字符间距不受影响。
- distribute \- 在两个页边距之间均匀对齐文本，并且字间和字符间距都会受到影响。

---

# 相关开放文档格式(ODF)属性：

段落的对齐方式是通过在应用于段落的样式中的<style:paragraph-properties>元素上设置fo:text-align属性来指定的。可能的值有start、end、left、right、center和justify。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 20.216

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard">

<style:paragraph-properties fo:text-align="end"/>

</style:style>

---

# 相关HTML/CSS属性：

text-align: right;  
text-align: center;  
text-align: justify;

CSS示例：

我觉得凯尔特人的信仰很有道理，他们认为我们失去的人的灵魂被囚禁在某些低等生物中，在动物中，在植物中，在某些无生命的物体中，因此实际上对我们来说是失去了，直到有一天（对许多人来说这一天永远不会到来）我们偶然经过那棵树或获得构成他们监狱的物体。

然后他们开始颤抖，他们呼唤我们的名字，一旦我们认出他们的声音，咒语就被打破了。我们已经解救了他们：他们已经战胜了死亡，回来分享我们的生活。我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都必定是徒劳的。

过去隐藏在领域之外的某个地方，超出智力的范围，在我们不怀疑的某个物质对象中（在该物质对象将给我们的感觉中）。至于那个物体，在我们自己必须死去之前，我们是否会遇到它，这取决于偶然。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
