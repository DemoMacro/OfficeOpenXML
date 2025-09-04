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

WordProcessingML文件剖析

# 包结构

WordprocessingML或docx文件是一个包含多个"部件"的zip文件（一个包）—通常是UTF-8或UTF-16编码的XML文件，尽管严格定义，部件是字节流。该包还可能包含其他媒体文件，如图像和视频。该结构根据[开放打包约定](whatIsOOXML.md)组织。

您可以通过简单地将任何docx文件重命名为zip文件并解压该文件来查看文件结构和文件。![WordprocessingML文件结构](images\zipFile1.gif)

# 内容类型

每个包必须在包的根目录中有一个[Content_Types].xml文件。该文件包含包中所有部件的内容类型列表。每个部件及其类型必须在[Content_Types].xml中列出。以下是主文档部件的内容类型：

<Override PartName="/word/document.xml" ContentType="application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>

向包中添加新部件时，记住这一点很重要。

# 关系

每个包都包含一个关系部件，该部件定义其他部件之间的关系以及与包外部资源的关系。这将关系与内容分离，使得在不更改引用目标的源的情况下更改关系变得容易。

![package relationships part](images\zipFile2.gif)

对于OOXML包，\_rels文件夹中总有一个关系部件（.rels），用于标识包的起始部件或包关系。例如，以下定义了内容的起始部件的身份：

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target="word/document.xml"/>.

通常，.rels中还有app.xml和core.xml的关系。

除了包的关系部件外，作为一个或多个关系源的每个部件都将有自己的关系部件。每个这样的关系部件位于部件的\_rels子文件夹中，并通过在部件名称后附加'.rels'来命名。通常，主要内容部件（document.xml）有自己的关系部件。它将包含与内容其他部件的关系，如styles.xml、themes.xml和footer.xml，以及外部链接的URI。

![document relationships part](images\zipFile3.gif)

关系可以是显式的或隐式的。对于显式关系，使用<Relationship>元素的Id属性引用资源。也就是说，源中的Id直接映射到关系项的Id，并明确引用目标。

例如，文档可能包含如下超链接：

<w:hyperlink r:id="rId4">

r:id="rId4"引用文档的关系部件（document.xml.rels）中的以下关系。

<Relationship Id="rId4" Type="http://. . ./hyperlink" Target="http://www.google.com/" TargetMode="External"/>

对于隐式关系，没有对<Relationship> Id的直接引用。相反，引用是隐含的。例如，文档可能包含对脚注的引用，如下所示。

<w:footnoteReference r:id="2">

在这种情况下，对w:id="2"的脚注的引用被理解为存在于存在脚注时的脚注部件中。在脚注部件中，我们将看到以下内容。

<w:footnote w:id="2">

# WordprocessingML文档特有的部件

以下是WordprocessingML包中可能存在的、特定于WordprocessingML文档的部件列表。请记住，文档可能只有其中几个部件。例如，如果文档没有脚注，则包中将不包含脚注部件。

| 部件     | 描述                                                                                                                                                                                                                                              |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 注释     | 包含文档中的注释。主文档可能有一个注释部件，如果有词汇表，则词汇表也可能有一个注释部件。                                                                                                                                                          |
| 文档设置 | 指定文档的设置，包括是否隐藏拼写和语法错误、跟踪修订、写保护等。主文档可能有一个文档设置部件，如果有词汇表，则词汇表也可能有一个文档设置部件。                                                                                                    |
| 尾注     | 包含文档的尾注。主文档可能有一个尾注部件，如果有词汇表，则词汇表也可能有一个尾注部件。                                                                                                                                                            |
| 字体表   | 指定有关文档中使用的字体的信息。应用程序将使用该部件中的信息来确定当系统上没有指定字体时使用哪些字体来显示文档。主文档可能有一个字体表，如果有词汇表，则词汇表也可能有一个字体表。                                                                |
| 页脚     | 包含[页脚](WPfooters.md)的信息。请注意，文档的每个[节](WPsection.md)可能包含首页、奇数页和偶数页的页脚。因此，可能有多个页脚部件，具体取决于文档中有多少节以及这些节的页脚类型。                                                                  |
| 脚注     | 包含文档的脚注。主文档可能有一个脚注部件，如果有词汇表，则词汇表也可能有一个脚注部件。                                                                                                                                                            |
| 词汇表   | 这是一个辅助文档存储位置，可能包含随文档携带但从主文档内容中不可见的内容。它旨在存储可选的文档片段。只允许有一个。                                                                                                                                |
| 页眉     | 包含[页眉](WPheaders.md)的信息。请注意，文档的每个[节](WPsection.md)可能包含首页、奇数页和偶数页的页眉。因此，可能有多个页眉部件，具体取决于文档中有多少节以及这些节的页眉类型。                                                                  |
| 主文档   | 包含文档的正文。                                                                                                                                                                                                                                  |
| 编号定义 | 包含文档中[每个编号定义的结构](WPnumbering.md)的定义。主文档可能有一个编号定义部件，如果有词汇表，则词汇表也可能有一个编号定义部件。                                                                                                              |
| 样式定义 | 包含文档使用的一组[样式](WPstyles.md)的定义。主文档可能有一个样式定义部件，如果有词汇表，则词汇表也可能有一个样式定义部件。                                                                                                                       |
| Web设置  | 包含文档使用的Web特定设置的定义。这些设置指定两个类别：可在WordprocessingML文档中使用的与HTML文档相关的设置（即框架集定义），以及影响文档另存为HTML时如何处理的设置。主文档可能有一个Web设置部件，如果有词汇表，则词汇表也可能有一个Web设置部件。 |

# 其他OOXML文档共享的部件

有许多部件类型可能出现在任何OOXML包中。以下是一些与WordprocessingML文档更相关的部件。

| 部件                                     | 描述                                                                                                                                                                                     |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 嵌入式包                                 | 包含一个完整的包，该包可以在引用包的内部或外部。例如，WordprocessingML文档可能包含电子表格或演示文稿文档。                                                                               |
| 扩展文件属性（通常位于docProps/app.xml） | 包含特定于OOXML文档的属性—例如使用的模板、页数和字数、应用程序名称和版本等属性。                                                                                                         |
| 文件属性，核心                           | 核心文件属性使用户能够发现和设置包中的常见属性—例如创建者名称、创建日期、标题等属性。尽可能使用[Dublin Core](http://dublincore.org/)属性（一组用于描述资源的元数据术语）。               |
| 字体                                     | 包含直接嵌入到文档中的字体。字体可以存储为位图字体（其中每个字形存储为光栅图像），也可以存储为符合ISO/IEC 14496-22:2007的格式。                                                          |
| 图像                                     | 文档通常包含图像。图像可以作为zip项存储在包中。该项必须通过图像部件关系和适当的内容类型来标识。                                                                                          |
| 主题                                     | DrawingML是OOXML文档类型之间的一种共享语言。它包含一个主题部件，当文档使用主题时，该部件包含在WordprocessingML文档中。主题部件包含有关文档主题的信息，即配色方案、字体和格式方案等信息。 |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
