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

制表符

单个自定义制表符使用<w:tab>元素定义，而<w:tab>元素包含在父级<w:tabs>元素中。对于从左到右的段落，制表位位置是相对于左边缘测量的。将制表符与悬挂缩进（由ind元素指定）进行比较，悬挂缩进会隐式创建一个制表位。

<w:pPr>

<w:tabs>

<w:tab w:val="start" pos="2160"/>

</w:tabs>

</w:pPr>

可以在<w:tabs>元素内指定一系列自定义制表符：

<w:pPr>

<w:tabs>

<w:tab w:val="start" pos="2160"/>

<w:tab w:val="start" pos="5040"/>

</w:tabs>

</w:pPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.1.37 和 § 17.3.1.38。

Word 2007 示例：

</w:pPr>

<w:tab w:val="left" w:leader="dot" w:pos="1440"/>  
. . .<w:r><w:tab/></w:r>...

</w:pPr>

. . .

<w:pPr>

<w:tabs>

<w:tab w:val="left" w:pos="2160"/>

<w:tab w:val="left" w:leader="dot" w:pos="5040"/>  
. . .<w:r><w:tab/></w:r><w:r><w:tab/></w:r>...

</w:tabs>

</w:pPr>

![Sample tabs](images\wp-tabs-1.gif)

---

### 属性：

制表符具有以下属性。

| 属性   | 描述                                                                                 |
| ------ | ------------------------------------------------------------------------------------ |
| leader | 指定用于填充制表符所创建空间的字符。该字符根据需要重复以填充制表符空间。可能的值有： |

- dot \- 一个点
- heavy \- 一条粗实线或下划线
- hyphen \- 一个连字符或破折号
- middleDot \- 一个居中的点
- none \- 无前导字符
- underscore \- 一个下划线

pos | 指定制表位的位置。值以缇为单位（1440缇 = 一英寸）。允许使用负值，并将页边距移动指定的量。  
val | 指定制表符的样式。可能的值有：

- bar \- 条形制表符不会在父段落中产生制表位，而是在该位置绘制一条垂直条。
- center \- 下一个制表符之后和之前的所有文本都应围绕该制表符居中。
- clear \- 清除当前制表位并应将其删除。
- decimal \- 所有后续文本围绕后续文本中的第一个小数字符对齐。
- end \- 所有后续和之前的文本都相对于尾边缘对齐。
- num \- 列表制表符或编号与内容之间的制表符。这是为了向后兼容，应避免使用，而应使用段落缩进。
- start \- 所有后续和之前的文本都相对于前导边缘对齐。

### 相关CSS属性：

没有直接对应的CSS元素，但有关CSS的text-indent的使用，请参见[段落缩进](WPindentation.md)。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
