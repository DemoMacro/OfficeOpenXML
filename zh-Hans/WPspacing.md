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

间距

段落之间和段落内行之间的间距使用<w:spacing>元素定义。

<w:pPr>

<w:spacing w:before="120" w:after="120" w:beforeAutospacing="0" w:afterAutospacing="0"/>

</w:pPr>

<w:pPr>

<w:spacing w:before="360" w:after="120" w:line="480" w:lineRule="auto" w:beforeAutospacing="0" w:afterAutospacing="0"/>

</w:pPr>

<w:pPr>

<w:spacing w:before="120" w:after="120" w:beforeAutospacing="0" w:afterAutospacing="0"/>

</w:pPr>

值以点的二十分之一为单位。正常的单倍行距段落的w:line值为240，即12磅。要以行的百分之一为单位指定单位，请使用'afterLines'/'beforeLines'属性。

相邻段落之间的间距将是每个段落的'line'间距、第一段之后的间距和第二段之前的间距中的较大值。因此，如果第一段指定240之后的间距，第二段指定80之前的间距，并且它们都是单倍行距（'line'值为240），那么段落之间的间距将为240。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.3.1.33。

Word 2007 示例：

![sample line spacing](images\wp-spacing-1.gif)

---

### 属性：

最常用的属性是：

| 属性              | 描述                                                                                                                                                                                               |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| after             | 指定应在段落的最后一行之后添加的间距（以绝对单位）。                                                                                                                                               |
| before            | 指定应在段落的第一行之前添加的间距（以绝对单位）。                                                                                                                                                 |
| line              | 指定段落内文本行之间的垂直间距量。![](images/note.png)注意：如果lineRule属性的值为atLeast或exactly，则line属性的值被解释为点的1/240。如果lineRule的值为auto，则line的值被解释为行的1/240。         |
| lineRule          | 指定如何计算line属性中指定的行之间的间距。![](images/note.png)注意：如果lineRule属性的值为atLeast或exactly，则line属性的值被解释为点的1/240。如果lineRule的值为auto，则line的值被解释为行的1/240。 |
| beforeAutospacing | 指定段落之前的间距是否应由使用者/文字处理器确定。![](images/note.png)注意：如果此设置为true（即='1'或='true'），则before或beforeLines的任何值都将被忽略。                                          |
| afterAutospacing  | 指定段落之后的间距是否应由使用者/文字处理器确定。![](images/note.png)注意：如果此设置为true（即='1'或='true'），则after或afterLines的任何值都将被忽略。                                            |

### 相关CSS属性：

margin-top:2em;  
line-height:2;

CSS 示例：

我觉得凯尔特人的信仰有很多值得称道的地方，他们认为我们失去的人的灵魂被囚禁在某些低等生物中，在动物中，在植物中，在某些无生命的物体中，因此实际上对我们来说是失去了，直到有一天（对许多人来说这一天永远不会到来）我们偶然经过那棵树或获得构成他们监狱的物体的所有权。

然后他们惊醒并颤抖，他们呼唤我们的名字，一旦我们认出他们的声音，咒语就被打破了。我们已经解救了他们：他们已经战胜了死亡并回来分享我们的生活。我们自己的过去也是如此。试图重新捕捉它是徒劳的：我们智力的所有努力都将证明是徒劳的。

过去隐藏在领域之外的某个地方，超出智力的范围，在我们不怀疑的某个物质对象中（在该物质对象将给我们的感觉中）。至于那个物体，在我们自己必须死亡之前，我们是否偶然遇到它取决于机会。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
