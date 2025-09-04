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

# 文字处理编号、级别和列表

相关Open Office/ODF讨论  
相关HTML/CSS讨论

概述

编号或分级是指使用数字、字母和/或符号标记单个段落的方法，如在大纲格式或简单的项目符号组中可能使用的方法。OOXML文字处理中的编号是通过首先定义一组规则来实现的，这些规则规定了特定编号方案的工作方式。例如，传统的大纲格式可能如下所示：

I. 这是第一级

A. 这是第二级

1\. 这是第三级。

将在文档中使用的这组规则是使用编号部分(numbering.xml)的根编号元素中的<w:abstractNum>元素定义的。然而，这组定义是"抽象的"，并不在文档中直接引用。相反，抽象编号定义的实例是使用<w:num>元素创建的，这些元素也在编号部分内。这些实例可以完全遵循抽象定义，也可以定义对抽象定义的覆盖或例外。最后，这些实例在文档内容中被引用。下面是一个抽象编号定义，后跟该定义的一个实例。两者都出现在编号部分内。

<w:numbering>

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="099A081C"/>

<w:multiLevelType w:val="hybridMultilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="360" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:color w:val="C00000"/>

<w:sz w:val="28"/>

</w:rPr>

</w:lvl>

</w:abstractNum>

<w:num w:numId="1">

<w:abstractNumId w:val="0"/>

</w:num>

</w:numbering>

上面的XML定义了一个只有一个级别(w:lvl w:ilvl="0")的分级方案。它还创建了一个编号为1的实例(w:num w:NumId="1")，该实例引用了abstractNum，没有任何更改或例外。在文档内容中，此实例可以被引用用于特定段落，如下面的示例所示。

<w:p>

<w:pPr>

<w:pStyle w:val="ListParagraph"/>

<w:numPr>

<w:ilvl w:val="0"/>

<w:numId w:val="1"/>

</w:numPr>

</w:pPr>

<w:r>

<w:t>这是第一个编号段落。</w:t>

</w:r>

</w:p>

请注意，上面示例中文档内容内的编号引用包含对要应用的级别的直接引用，因为<w:numPr>包含对编号定义(numId)的引用和对级别(ilvl)的引用。有关<w:numPr>的更多信息，请参见[段落属性](WPparagraphProperties.md)。在内容中引用级别的另一种可能方式是通过引用的段落样式。也就是说，在<w:abstractNum>中，适当的子级别(lvl)可以包含值为ListParagraph的pStyle。在这种情况下，内容仅包含对编号定义实例(numId)的引用，但它也引用段落样式。相同的样式将在引用的编号定义中找到，并且该级别将用于段落。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9和§ 17.9.1。

Word 2007示例：

![Numbering/Levels](images/wp-numbering-1.gif)

---

### 编号定义部分元素：

编号定义部分有一个根元素<w:numbering>。参见ECMA-376，第3版（2011年6月），基础和标记语言参考§ 11.3.11。该部分包含文档中使用的每组编号规则的定义，即使给定规则集的特定级别实际上并未在文档中使用。请注意，一个包最多可以包含两个编号定义部分—一个用于主文档，一个用于词汇表。

<w:numbering>的子元素如下（省略了用于跟踪更改的numIdMacAtLeanup）。

| 元素        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- | ---- |
| abstractNum | 指定一组称为抽象编号定义的属性。它定义了通过num实例引用此定义的编号段落将如何显示（除非num包含对抽象定义的覆盖）。参见[定义整体编号方案](WPnumberingAbstractNum.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.2。                                                                                                                                                                                                    |
| num         | 指定编号定义(<w:abstractNum>)的唯一实例，该实例可由文档内容中的段落引用。每个实例通过其子元素<w:abstractNumId>引用<w:abstractNum>，从而继承引用的<w:abstractNum>的属性。这些继承的属性可以通过包含<w:lvlOverride>子元素来为实例覆盖，从而实质上创建编号定义的新变体，这些子元素覆盖编号定义中给定级别的属性。参见[覆盖编号定义](WPnumberingOverride.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.16。只有一个属性： | 属性 | 描述 |
| ---         | ---                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| numId       | 指定一个唯一ID，内容中的任何编号段落如果要继承由<w:abstractNum>定义的属性，都可以引用该ID（通过段落的pPr中的numPr内的numId）。                                                                                                                                                                                                                                                                                                           |

有两个元素：

| 元素          | 描述                                                                                                                                                                                                         |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| abstractNumId | 指定实例将从中继承其属性的抽象编号定义。它只有一个属性val，该值必须等于abstractNum的abstractNumId属性的值。（参见上面XML示例中红色的数字。）参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.2。 |
| lvlOverride   | 指定要应用于abstractNumId中引用的抽象编号定义的零个或多个级别的覆盖。参见[覆盖编号定义](WPnumberingOverride.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.9。                            |
| numPicBullet  | 指定在编号定义中用作编号符号的图片的外观。参见[编号 - 图像作为项目符号](WPnumbering-imagesAsBullets.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.21。                                   |

---

# 相关开放文档格式(ODF)属性：

项目符号、列表、级别、编号段落等使用<text:list>元素指定。<text:list>元素可以包含标题(<text:list-header>)和一个或多个项目(<text:list-item>)。列表可以独立编号，从任何数字开始，也可以从其他列表继续。编号格式由应用于列表的列表样式决定。与HTML一样，列表可以嵌套，嵌套决定列表的级别。例如，如果一个列表嵌套在另一个列表内，则嵌套列表位于第2级。

参考：办公应用程序开放文档格式1.2版（2011年5月）§ 5.3。

<text:list xml:id="list36339527" text:style-name="L2">

<text:list-item>

<text:p text:style-name="P2">这是顶层</text:p>

<text:list

<text:list-item>

<text:p text:style-name="P2">这是第二级</text:p>

</text:list-item>

</text:list>

</text:list>

### 属性：

| 属性                    | 描述                                                |
| ----------------------- | --------------------------------------------------- |
| text:continue-list      | 指定要继续的列表的xml:id值。                        |
| text:continue-numbering | 指定是否继续前面列表的编号。可能的值为true和false。 |
| text:style-name         | 指定列表的唯一id。                                  |
| xml:id                  | 指定列表的唯一id。                                  |

### 元素：

| 元素               | 描述                                                                       |
| ------------------ | -------------------------------------------------------------------------- |
| <text:list-header> | 指定列表的标题，即显示在列表之前且没有前面数字或项目符号的一个或多个段落。 |
| <text:list-item>   | 指定嵌套列表。                                                             |

# 相关HTML/CSS属性：

<ol>

<li style="list-style-type:upper-roman;">这是第一级。

<ol>

<li style="list-style-type:upper-alpha;">这是第二级。

<ol>

<li style="list-style-type:decimal;">这是第三级。</li>

</ol>

</li>

</ol>

</li>

<li style="list-style-type:upper-roman;">这也是第一级。</li>

</ol>

HTML/CSS示例：

1. 这是第一级。
1. 这是第二级。
1. 这是第三级。
1. 这也是第一级。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
