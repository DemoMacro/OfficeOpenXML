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

文本间距和字距调整

有一些文本属性会影响文本间距。每个属性都是通过<rPr>元素内的子元素应用的。其他文本格式，如粗体、大小、底纹和边框，在单独的页面中介绍。

![](images/note.png) 注意：XML中的空白不总是保留的。与任何XML一样，要在OOXML中保留空格，必须将space属性设置为preserve：<w:t xml:space="preserve">。

### 元素：

| 元素    | 描述                                                                                                                                                                                                  |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| spacing | 指定要在每个字符后添加或移除的字符间距量。<spacing w:val="200"/>。单个属性是val。它指定以点的二十分之一（相当于1/1440英寸）为单位的正或负测量值。将spacing与w属性进行比较，后者会拉伸或扩展每个字符。 | ![spacing (字符间距调整)](images\wp-text-spacing-1.gif) |

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.35。

w | 指定拉伸或压缩每个字符的量。<w w:val="200%"/>。单个属性是val。注意最小值为1%，最大值为600%。将w与spacing属性进行比较，后者通过添加额外的字符间距来扩展/压缩文本，但不改变字符的宽度。 | ![字符扩展或压缩)](images\wp-w-1.gif)

---

![](images/versionConflict3.png) 注意：2006版本指定val的值不带百分号（%）[<w w:val="200"/>]，但2011版本添加了百分号（%）[<w w:val="200%"/>]。包含百分号会在Microsoft Word 2007中导致错误。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.43。

kern | 指定是否应将字体字距调整应用于文本。字距调整是调整比例字体中字符间距的过程。它使字母更靠近在一起。它使用<w:kern>元素指定。<w:rPr> <w:kern w:val="22"/> <w:sz w:val="28"/> </w:rPr> 单个属性是val。它指定将自动进行字距调整的最小字体大小。如果sz元素指定的字体大小小于val属性指定的值，则不会应用字距调整。属性值以半点（1/144英寸）为单位指定。 | ![文本字距调整](images\wp-text-kerning-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.19。

fitText | 指定内容将被调整大小以适应val属性指定的宽度，而不是根据内容的宽度自动显示。扩展或收缩是通过增加或减小每个字符的大小来执行的。<fitText w:id="50" w:val="1440"/>。 | ![fitText](images\wp-fitText-1.gif)

---

| 属性 | 描述                                                                                                                                   |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------- |
| id   | 指定用于链接包含fitText元素的多个运行的id。这使多个连续运行可以因格式差异而分开，同时保留其fitText属性。如果运行不连续，则忽略该属性。 |
| val  | 指定运行必须适应的宽度，以点的二十分之一为单位。                                                                                       |

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.14。

### 相关CSS属性：

<div style="letter-spacing: 10px;">Then they start and tremble,</div>   
<div style="word-spacing: 10px;"> they call us by our name, and as soon as we have recognized their voice the spell</div>   
<div> 已破碎。我们已经拯救了他们；</div>   
<div style="max-width:50px">they have overcome death and return to share our life.</div>

CSS示例：

然后他们开始颤抖，

他们呼唤我们的名字，一旦我们认出他们的声音，咒语

就被打破。我们已经拯救了他们；

他们已经战胜死亡，回来分享我们的生活。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
