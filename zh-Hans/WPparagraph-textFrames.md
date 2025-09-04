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

# 文字处理ML \- 文本框

文本框是文档中位于单独区域的文本段落，具有特定的大小和相对于非框架段落的位置。文本框类似于文本框。两者都是可以在页面上定位和调整大小的文本容器。文本框在格式设置方面具有更大的灵活性。文本框是drawingML规范的一部分，并在[此处](http://www.officeopenxml.com/drwSp-textbox.md)进行了更详细的讨论。文本框是wordprocessingML的一部分，并且不那么复杂。

文本框段落只是一个包含<w:framePr>作为<w:pPr>子元素的段落。<w:framePr>元素是一个空元素，具有多个可能的属性来指定框架的特性。相邻的段落都可以是文本框段落。如果两个相邻段落上的<w:framePr>属性集相同，则它们被视为同一文本框的一部分。每个属性都必须相同，否则它们将被视为单独的文本框。文本框的位置是相对于文档中下一个非文本框段落计算的。

下面是一个示例文本框。

<w:p>

<w:pPr>

<w:framePr w:w="3500" w:h="3500" w:wrap="auto" w:vAnchor="page" w:hAnchor="page" w:xAlign="right" w:yAlign="top"/>

<w:pBdr>

<w:left w:val="single" w:sz="12" w:space="1" w:color="auto"/>

<w:bottom w:val="single" w:sz="12" w:space="1" w:color="auto"/>

</w:pBdr>

<w:rPr>

<w:sz w:val="24"/>

<w:szCs w:val="24"/>

</w:rPr>

</w:pPr>

<w:r>

<w:rPr>

<w:sz w:val="24"/>

<w:szCs w:val="24"/>

</w:rPr>

<w:t>这是文本框段落。</w:t>

</w:r>

</w:p>

下面是文本框的外观 — 在页面的右上角。

![WordprocessingML - Text Frames](images\WPtextFrame1.gif)

下面是定义文本框特性的<w:framePr>属性。

| 属性       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| anchorLock | 指定框架应相对于非框架段落保持在相同的逻辑位置。值为布尔值。当值为true且文本框具有锁定锚点时，即使视觉位置更改，文本框段落位置在xml中也相对于其他非框架段落保持不变。                                                                                                                                                                                                                                                                                                                               |
| dropCap    | 首字下沉是通过增大段落第一个字母或字母的大小来开始段落的一种方式。首字下沉实现为文本框。也就是说，大字母放在文本框中，而段落的其余部分（正常大小）放在后面的非文本框中。此属性指定大字母相对于非文本框段落中的正常大小文本的位置。可能的值有margin（框架位于文本边距外）、drop（框架位于文本边距内）和none（文本框不是首字下沉框）。下面是一个值设置为drop的首字下沉示例：<w:framePr w:dropCap="drop" . . . />。有关首字下沉的高度，请参见下面的行。![文字处理ML - 文本框](images\WPtextFrame2.gif) |
| h          | 以缇或点的二十分之一指定框架的高度。此属性与hRule属性一起使用。如果hRule的值为auto，则忽略高度值，高度基于内容的高度。如果值为atLeast，则框架的高度应至少为h属性中指定的值。如果值为exact，则框架的高度应完全为h属性中指定的值。                                                                                                                                                                                                                                                                    |
| hAnchor    | 指定框架应水平锚定的对象。水平定位（由x属性指定）是从此对象确定的。可能的值有margin（水平定位应相对于文本边距计算）、page（水平定位应相对于页面边缘计算）和text（水平定位应相对于文本边缘计算，包括文本缩进）。下面首先是一个hAnchor和vAnchor设置为page的文本框。![文字处理ML - 文本框](images\WPtextFrame3.gif) 下面是上面显示的示例文本框，但hAnchor设置为margin，vAnchor设置为text。![文字处理ML - 文本框](images\WPtextFrame4.gif)                                                              |
| hRule      | 请参阅上面关于h属性的讨论。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| hSpace     | 指定当前文本框与环绕的任何非框架文本之间应保持的最小距离。值以点的二十分之一为单位。下面是上面的文本框，但hSpace值为1440或1英寸。![文字处理ML - 文本框](images\WPtextFrame5.gif)                                                                                                                                                                                                                                                                                                                    |
| lines      | 以行指定首字下沉的高度。默认值为1。                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| vAnchor    | 指定框架应垂直锚定的对象。垂直定位（由y属性指定）是从此对象确定的。可能的值有margin（垂直定位应相对于顶部水平文本边距计算）、page（垂直定位应相对于页面边缘计算）和text（垂直定位应相对于文本的顶部水平边缘计算）。请参见上面关于hAnchor讨论中的示例。                                                                                                                                                                                                                                              |
| vSpace     | 指定当前文本框与上方或下方的任何非框架文本之间应垂直保持的最小距离。值以点的二十分之一为单位。                                                                                                                                                                                                                                                                                                                                                                                                      |
| w          | 以缇或点的二十分之一指定框架的宽度。当省略该属性时，宽度由框架的内容确定。                                                                                                                                                                                                                                                                                                                                                                                                                          |
| wrap       | 指定文本框周围的文本环绕样式。可能的值有：                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

- around \- 文本应环绕每行文本
- auto \- 由应用程序确定
- none \- 无环绕
- notBeside \- 文本不应环绕文本框的其余行；文本放置在不与框架相交的文本框之后的下一行
- through \- 文本应环绕文本框周围每行的剩余空间
- tight \- 文本应紧密环绕文本框周围每行的剩余空间

下面是一个wrap设置为none的示例。![文字处理ML - 文本框](images\WPtextFrame6.gif) 下面是一个wrap设置为through的示例。![文字处理ML - 文本框](images\WPtextFrame7.gif)  
x | 指定文本框的绝对水平位置。它是相对于hAnchor属性指定的水平锚点指定的。值以点的二十分之一为单位。如果值为正，则文本框定位在锚点对象之后。如果值为负，则定位在锚点对象之前。如果还指定了xAlign属性，则忽略此值。如果省略，则假定值为0。  
xAlign | 指定文本框的相对水平位置 - 相对于hAnchor属性指定的锚点。如果省略，则使用x属性指定的值来确定绝对水平定位。可能的值有：

- center \- 水平居中
- inside \- 父对象应位于锚点对象内部，例如水平位于文本边距内部
- left \- 父对象应相对于锚点左对齐
- outside \- 父对象应位于锚点对象外部，例如水平位于文本边距外部
- right \- 父对象应相对于锚点右对齐

下面是一个hAnchor属性设置为margin，xAlign设置为left，vAnchor属性设置为text，yAlign设置为center的示例。![文字处理ML - 文本框](images\WPtextFrame8.gif)  
y | 指定文本框的绝对垂直位置。它是相对于vAnchor属性指定的垂直锚点指定的。值以点的二十分之一为单位。如果值为正，则文本框定位在锚点对象之后。如果值为负，则定位在锚点对象之前。如果还指定了xAlign属性，则忽略此值。如果省略，则假定值为0。  
yAlign | 指定文本框的相对垂直位置 - 相对于vAnchor属性指定的锚点。如果省略，则使用y属性指定的值来确定绝对垂直定位。可能的值有：

- bottom \- 父对象应垂直对齐到锚点的底部边缘
- center \- 垂直居中
- inline \- 父对象应与周围文本垂直对齐 — 即，文本不环绕它
- inside \- 父对象应垂直对齐到锚点的边缘并位于锚点对象内部
- outside \- 父对象应垂直对齐到锚点的边缘并位于锚点对象外部
- top \- 父对象应垂直对齐到锚点的顶部边缘

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
