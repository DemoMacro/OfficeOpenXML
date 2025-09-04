![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 放映
  - [切换效果](prSlide-transitions.md)
  - 动画和计时
  - 自定义放映
- 演示文稿属性
- 视图属性
- 幻灯片
  - [Overview](prSlide.md)
  - [内容（通用幻灯片数据）](prCommonSlideData.md)
    - [形状](prSlide-shapeTree.md)
    - [Tables](drwTable.md)
    - [音频和视频](prSlide-multiMedia.md)
  - [幻灯片母版](prSlideMaster.md)
  - [幻灯片版式](prSlideLayout.md)
  - [Slide](prPresentationSlide.md)
  - [备注母版](prNotesMaster.md)
  - [备注幻灯片](prNotesSlide.md)
    讲义母版
    幻灯片属性
    [大小](prSlide-size.md)
    [背景](prSlide-background.md)
    [页眉和页脚](prSlide-footer.md)
    样式和格式
    [填充、字体、轮廓、效果](prSlide-styles-themes.md)
    [文本样式](prSlide-styles-textStyles.md)
    [配色方案](prSlide-color.md)
    幻灯片编号

# 包结构

PresentationML 或 .pptx 文件是一个包含多个"部件"（通常为 UTF-8 或 UTF-16 编码）或 XML 文件的 zip 文件（包）。该包还可能包含其他媒体文件，如图像。其结构按照 OOXML 标准 ECMA-376 第 2 部分中概述的开放打包约定进行组织。

您只需解压缩 .pptx 文件，即可查看构成 PresentationML 文件的文件结构和文件。![PresentationML 文件结构](pptxImages\presentationMLStructure1.gif)

部件的数量和类型将根据演示文稿中的内容而有所不同，但始终会有一个 [Content_Types].xml、一个或多个关系（.rels）部件，以及一个演示文稿部件（presentation.xml），该部件位于 Microsoft Powerpoint 文件的 ppt 文件夹内。通常还会有至少一个幻灯片部件，以及一个母版幻灯片和一个版式幻灯片，幻灯片就是由这些形成的。

# 内容类型

每个包必须有一个 [Content_Types].xml，位于包的根目录。此文件包含包中所有部件的内容类型列表。每个部件及其类型必须在 [Content_Types].xml 中列出。以下是幻灯片部件的内容类型：

<Override PartName="/ppt/slides/slide1.xml" ContentType="application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>

向包中添加新部件时，重要的是要记住，不仅必须添加新部件并更新 .rels 文件中的任何关系，还必须更新 Content_Types.xml 文件。

# 关系

每个包都包含一个关系部件，该部件定义其他部件之间的关系以及与包外资源的关系。这将关系与内容分离开来，使得在不更改引用目标的源的情况下更改关系变得容易。

![package relationships part](pptxImages\rootStructure3.gif)

对于 OOXML 包，\_rels 文件夹中总有一个关系部件（.rels），用于标识包的起始部件或包关系。例如，以下内容定义了演示文稿内容的起始部件的身份：

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target="ppt/presentation.xml"/>.

通常，.rels 中也存在与 app.xml 和 core.xml 的关系。

除了包的关系部件外，作为了一个或多个关系源的每个部件都将有自己的关系部件。每个这样的关系部件位于该部件的 \_rels 子文件夹中，并通过在部件名称后附加 '.rels' 来命名。

通常，主要内容部件（presentation.xml）有自己的关系部件（presentation.xml.rels）。它将包含与内容其他部件的关系，如 slideMaster1.xml、notesMaster1.xml、handoutMaster1.xml、slide1.xml、presProps.xml、tableStyles.xml、theme1.xml，以及外部链接的 URI。

![document relationships part](pptxImages\rootStructure4.gif)

关系可以是显式的或隐式的。对于显式关系，使用 <Relationship> 元素的 Id 属性引用资源。也就是说，源中的 Id 直接映射到关系项的 Id，并显式引用目标。

例如，幻灯片可能包含如下超链接：

<a:hlinkClick r:id="rId2">

r:id="rId2" 引用幻灯片的关系部件（slide1.xml.rels）中的以下关系。

<Relationship Id="rId2" Type="http://. . ./hyperlink" Target="http://www.google.com/" TargetMode="External"/>

对于隐式关系，没有对 <Relationship> Id 的直接引用。相反，引用是隐含的。

# PresentationML 文档特有的部件

以下是 PresentationML 包中可能存在的、特定于 PresentationML 演示文稿的部件列表。请记住，演示文稿可能只包含其中几个部件。例如，如果演示文稿没有备注，则包中将不包含备注母版部件。

| 部件           | 描述                                                                                                                 |
| -------------- | -------------------------------------------------------------------------------------------------------------------- |
| 评论作者       | 包含有关向演示文稿添加评论的每个作者的信息。                                                                         |
| 评论           | 包含单个幻灯片的评论。                                                                                               |
| 讲义母版       | 包含演示文稿讲义上幻灯片、备注、页眉和页脚文本、日期或页码的外观、位置和大小。只能有一个这样的部件。                 |
| 备注母版       | 包含有关所有备注页的内容和格式的信息。只能有一个这样的部件。                                                         |
| 备注幻灯片     | 包含单个幻灯片的备注。                                                                                               |
| 演示文稿       | 包含幻灯片演示文稿的定义。必须有且仅有一个这样的部件。请参阅[演示文稿](PrPresentation.md)。                          |
| 演示文稿属性   | 包含演示文稿的所有属性。必须有且仅有一个这样的部件。                                                                 |
| 幻灯片         | 包含单个幻灯片的内容。                                                                                               |
| 幻灯片版式     | 包含幻灯片模板的定义。它定义幻灯片上绘图对象的默认外观和位置。必须有一个或多个这样的部件。                           |
| 幻灯片母版     | 包含格式、文本和对象的母版定义，这些内容出现在演示文稿中从幻灯片母版派生的每个幻灯片上。必须有一个或多个这样的部件。 |
| 幻灯片同步数据 | 包含指定幻灯片当前状态的属性，该幻灯片正在与存储在中央服务器上的幻灯片版本进行同步。                                 |
| 用户定义的标记 | 包含演示文稿中对象的一组用户定义属性。可以有零个或多个这样的部件。                                                   |
| 视图属性       | 包含演示文稿的显示属性。                                                                                             |

# 其他 OOXML 文档共享的部件

有多种部件类型可能出现在任何 OOXML 包中。以下是一些与 PresentationML 文档更相关的部件。

| 部件                                      | 描述                                                                                                                                                                                     |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 音频                                      | 包含与讲义母版、备注幻灯片、幻灯片、幻灯片版式或幻灯片母版关联的音频文件。                                                                                                               |
| 嵌入式控件                                | 包含有关嵌入式控件的信息。                                                                                                                                                               |
| 嵌入式对象                                | 包含有关幻灯片上嵌入式对象的信息。例如，幻灯片可能包含嵌入式视频或音频对象。                                                                                                             |
| 嵌入式包                                  | 包含一个完整的包，该包可能在引用包的内部或外部。例如，PresentationML 文档可能包含 SpreadsheetML 文档。                                                                                   |
| 扩展文件属性（通常位于 docProps/app.xml） | 包含特定于 OOXML 文档的属性—例如使用的模板、幻灯片和单词数量、应用程序名称和版本等属性。                                                                                                 |
| 文件属性，核心                            | 核心文件属性使用户能够发现和设置包中的常见属性—如创建者名称、创建日期、标题等属性。尽可能使用 [Dublin Core](http://dublincore.org/) 属性（用于描述资源的一组元数据术语）。               |
| 图像                                      | 演示文稿通常包含图像。图像可以作为 zip 项存储在包中。该项必须通过图像部件关系和适当的内容类型来标识。                                                                                    |
| 主题                                      | DrawingML 是跨 OOXML 文档类型的共享语言。它包含一个主题部件，当电子表格使用主题时，该部件包含在 SpreadsheetML 文档中。主题部件包含有关文档主题的信息，即配色方案、字体和格式方案等信息。 |
| 视频                                      | 包含与讲义母版、备注幻灯片、幻灯片、幻灯片版式或幻灯片母版关联的视频文件。                                                                                                               |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
