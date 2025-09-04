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

概述

样式是可应用于文本的预定义段落、字符、表格和编号属性集合。它们与文档内容分开存储，使它们能够独立管理并在单个位置进行更改，而不是直接格式化，后者可能与文档中的内容一起出现。每个样式都需要在样式部分中有一个<w:style>定义。

注意文档中使用样式和使用直接格式之间的区别。样式单独存储在样式部分中，并使用样式的ID进行引用。直接格式与文档内容一起内联显示。通常内容将包含对样式的引用以及旨在填补样式中的遗漏或覆盖样式属性的直接格式。下面的示例包含对段落样式的引用，以及使段落居中对齐的直接格式。两者都包含在<w:pPr>元素中。

<w:p>

<w:pPr>

<w:pStyle w:val="MyStyle"/>

<w:jc w:val="center"/>

</w:pPr>

</w:p>

引用的样式可能出现在样式部分中，如下所示。段落样式仅为段落定义了一个粗体运行属性。

<w:style w:type="paragraph" w:styleId="MyStyle">

<w:name w:val="My Paragraph Style"/>

<w:rPr>

<w:b/>

</w:rPr>

</w:style>

#### 继承

样式可以相互构建或分层，样式继承其所基于的样式的属性。这种分层是通过在样式定义中包含<w:basedOn w:val=""/>元素并为val属性指定样式ID来实现的。例如，假设我们有一个ID为Base的样式。此样式可能定义Arial字体和粗体。然后我们可以通过在Green的定义中包含以下内容来创建一个名为Green的新样式：<w:basedOn w:val="Base"/>。在这个新样式中，我们可以指定绿色。使用Green样式的文本将是Arial、粗体和绿色，因为样式继承了其所基于的样式的属性。相反，较低级别的属性（即其他样式所基于的样式的属性）可以通过重新定义属性来覆盖。因此，Green样式可能会将字体设置为Times New Roman，从而覆盖较低级别的Arial字体属性。

#### 层次结构

样式按以下顺序应用。

- 首先应用文档默认值。文档默认值使用<w:docDefaults>元素定义，该元素是<w:styles>的子元素。也就是说，它与样式定义处于同一级别。
- 接下来，应用表格样式。
- 接下来，应用编号样式。
- 接下来，应用段落样式中定义的段落和运行样式。（<w:pPr>可以包含<w:rPr>）
- 接下来，应用运行属性。
- 最后，应用直接格式。

#### 切换属性

有一些属性被认为是切换属性，包括粗体、将所有字符显示为大写字母、浮雕、斜体、压印、显示字符轮廓、阴影、小型大写字母、单删除线和隐藏文本。切换属性要么为true，要么为false。对于非切换属性，使用的属性是最后应用的属性。对于切换属性，情况更为复杂。

如果切换属性在直接格式中显式设置（即不是通过引用样式应用），则使用该值。如果切换属性的多个实例出现在同一级别（即使用继承，并且属性在<w:basedOn/>层次结构中的多个样式中应用），则使用遇到的第一个值，从当前样式开始，然后返回<w:basedOn/>元素中指定的样式链。如果切换属性出现在多个级别，如果文档默认值中的值为true，则该属性为true；否则，如果属性在奇数个级别中为true，则该值为true。

### 样式定义部分元素：

样式定义部分有一个根元素<w:styles>。参见ECMA-376，第3版（2011年6月），基础和标记语言参考§17.7.4.18。该部分包含可应用于文档内内容的每个样式（<w:style>）的定义。它还可能包含文档默认值（<w:docDefaults>）的定义。最后，它可能定义应用程序已知但未包含在文档中的样式属性（<w:latentStyles>）。

<w:styles>的子元素如下。

| 元素         | 描述                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| docDefaults  | 指定文档中每个段落和运行继承的默认属性集。这些将定义格式，除非它们被其他样式或直接格式覆盖。请注意，如果未指定docDefaults，则应用程序可以定义默认值。参见[样式 - 定义默认格式](WPstyleDefaults.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.7.5。                                                                                                                             |
| style        | 指定可应用于文档区域的一组属性。参见[样式 - 定义样式](WPstyle.md)。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.7.4.17。                                                                                                                                                                                                                                                           |
| latentStyles | 潜在样式指的是应用程序已知但未包含在当前文档中的样式定义。latentStyles元素提供了一种机制，用于存储有关此类样式的某些行为的信息，而不存储样式的实际格式属性。此类行为包括诸如打开文档时必须将多少潜在样式初始化为其默认值，是否应锁定潜在样式以便无法创建样式的实例，潜在样式的uiPriority应该是什么等。此处不详细讨论潜在样式。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§17.7.4.5。 |

### 相关HTML/CSS属性：

以下是可能出现在外部样式表中的段落样式定义。

.myParagraphStyle {

margin:5px 5px;

border-color:#000000;

background-color:#FF6699

padding: 10px;

border-style:dotted;

border-width:2px;

}

然后应用样式，如下所示。

<div class="myparagraphStyle">This is a styled paragraph.</div>

HTML/CSS示例：

这是一个样式化的段落。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
