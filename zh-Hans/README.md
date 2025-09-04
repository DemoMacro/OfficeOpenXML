![OfficeOpenXML.com](images/ooxmlBanner.png)

[文字处理ML (docx) ](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

# 什么是OOXML？

Office Open XML，也称为OpenXML或OOXML，是一种基于XML的办公文档格式，包括文字处理文档、电子表格、演示文稿，以及图表、图示、形状和其他图形材料。该规范由微软开发，并于2006年被ECMA国际采纳为[ECMA-376](http://www.ecma-international.org/publications/standards/Ecma-376.htm)。第二个版本于2008年12月发布，标准的第三个版本于2011年6月发布。该规范已被ISO和IEC采纳为ISO/IEC 29500。

重要的是要记住，OOXML与Open Office XML或支撑[OpenOffice.org](http://www.openoffice.org/)和其他开源办公软件的[开放文档格式(ODF)](http://www.oasis-open.org/standards)并不相同。Office Open XML和Open Office XML或ODF在某种意义上是办公文档的竞争性XML标准。

尽管微软继续支持较旧的二进制格式（.doc、.xls和.ppt），但OOXML现在是所有Microsoft Office文档（.docx、.xlsx和.pptx）的默认格式。

## OOXML规定了什么？

### 标记规范

ECMA-376为三种主要办公文档类型分别包含了三种不同的规范—用于文字处理文档的WordprocessingML，用于电子表格文档的SpreadsheetML，以及用于演示文稿文档的PresentationML。它还包括一些支持性标记语言，最重要的是用于绘图、形状和图表的DrawingML。

该规范包括XML架构和书面形式的约束。任何符合标准的文档都必须符合XML架构，并采用UTF-8或UTF-16编码。该规范确实包含一些可扩展性机制，允许将自定义XML与OOXML标记一起存储。

### 文件打包规范

除了标记语言规范外，ECMA-376的第2部分规定了开放打包约定（OPC）。OPC是一种利用常见ZIP格式将文件组合成一个通用包的容器文件技术。因此，OOXML文件是包含各种XML文件（部件）并组织成单个包的ZIP存档。这种将数据分解或分块的方式使访问数据更容易、更快速，并减少了数据损坏的可能性。部件可以包含任何类型的数据；为了在不依赖文件扩展名的情况下跟踪每个部件的数据类型，每个部件的类型在包内一个名为[Content_Types].xml的文件中指定。部件与包的关系以及任何部件可能具有的关系被从部件中抽象出来，并单独存储在关系文件中—一个用于整个包，一个用于每个具有关系的包。通过这种方式，引用只存储一次，因此在必要时可以轻松更改。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
