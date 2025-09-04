![SpreadsheetXML.com](ssImages\SpreadsheetMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [电子表格ML文件剖析](anatomyofOOXML-xlsx.md)
- [内容概述](SScontentOverview.md)
- [样式和格式](SSstyles.md)

# 电子表格内容概述

电子表格ML文档是一个包含许多不同部分（主要是XML文件）的包。

![package relationships part](ssImages\rootStructure2.gif)

然而，大多数实际内容位于一个或多个工作表部分（每个工作表一个）和一个共享字符串部分中。对于Microsoft Excel，内容位于xl文件夹内，而工作表则位于worksheet子文件夹内。

![worksheet parts](ssImages\rootStructure5.gif)

工作簿部分不包含实际内容，仅包含电子表格的一些属性，以及对包含数据的单独工作表部分的引用。

<workbook . . .>

. . .

<workbookPr . . ./>

<sheets>

<sheet name="sheet1" r:id="rId1">

<sheet name="sheet2" r:id="rId2">

<sheet name="sheet3" r:id="rId3">

</sheets>

. . .

</workbook>

工作表可以是网格、图表或对话框工作表。

### 网格

单元格网格（或"单元格表格"）是最常见的工作表类型。单元格可以包含文本、布尔值、数字、日期和公式。从一开始就理解大多数文本值不存储在工作表部分中是很重要的。为了最小化值的重复，作为字符串的单元格值单独存储在共享字符串部分中。（然而，这种概括有一个例外。单元格可以是inlineStr类型，在这种情况下，字符串存储在单元格本身的is元素内。）所有其他单元格值—布尔值、数字、日期和公式（以及公式的值）都存储在单元格内。

工作表的一些属性位于根<worksheet>元素的开头。网格的列数和大小在<cols>内定义。然后工作表的核心数据在<sheetData>元素内。工作表数据被划分为行（<row>），每行内是单元格（<c>）。行通过r属性进行编号或索引，从1开始（例如，row r="1"）。行中的每个单元格也有一个引用属性，该属性将行号与列组合以形成引用属性（例如，<c r="D3">）。如果行中的单元格没有内容，则该单元格将从行定义中省略。

<worksheet . . .>

. . .

<cols>

<col min="1" max="1" width="26.140625" customWidth="1"/>

. . .

</cols>

<sheetData>

<row r="1">

<c r="A1" s="1" t="s">

<v>0</v>

. . .

</c>

</row>

. . .

</sheetData>

. . .

<mergeCells count="1">

<mergeCell ref="B12:J16"/>

</mergeCells>

<pageMargins . . ./>

<pageSetup . . ./>

<tableParts ccount="1">

<tableParts count="1">

</tablePart r:id="rId2"/>

</worksheet>

单元格的构成对于理解电子表格内容的整体架构很重要。每个单元格通过t属性指定其类型。可能的值包括：

- b 表示布尔值
- d 表示日期
- e 表示错误
- inlineStr 表示内联字符串（即不存储在共享字符串部分，而是直接存储在单元格中）
- n 表示数字
- s 表示共享字符串（因此存储在共享字符串部分中，而不是在单元格中）
- str 表示公式（表示公式的字符串）

当单元格是数字时，该值存储在<v>元素中，作为<c>（单元格元素）的子元素。

<c r="B2" s="5" t="n">

<v>400</v>

</c>

日期也是一样，只是日期以ISO 8601格式的值存储。对于内联字符串，值位于<is>元素内。但当然，实际文本进一步嵌套在t元素内，因为文本可以格式化。

<c r="C4" s="2" t="inlineStr">

<is>

<t>my string</t>

</is>

</c>

对于公式，公式本身存储在f元素中，作为<c>的子元素。公式后面是<v>元素中的实际计算值。

<c r="B9" s="3" t="str">

<f>SUM(B2:B8)</f>

<v>2105</v>

</c>

当单元格的数据类型是s（共享字符串）时，字符串存储在共享字符串部分中。然而，单元格仍然在<v>元素内包含一个值，该值是存储在共享字符串部分中的字符串的索引（从零开始）。因此，例如，在下面的示例中，实际字符串是共享字符串部分中<si>元素的第9次出现。

<c r="C1" s="4" t="s">

<v>8</v>

</c>

共享字符串部分可能如下所示：

<sst xmls="http://schemas.openmlformats.org/spreadsheetml/2006/main" count="19" uniqueCount="13">

<si><t>费用</t></si>

<si><t>金额</t></si>

<si><t>食物</t></si>

<si><t>总计</t></si>

<si><t>娱乐</t></si>

<si><t>汽车付款</t></si>

<si><t>租金</t></si>

<si><t>水电费</t></si>

<si><t>保险</t></si>

<si><t>付款日期</t></si>

. . .

</sst>

### 表格

工作表上的数据可以组织成表格。表格通过具有清晰标记的列、行和数据区域，帮助为数据提供结构和格式。可以轻松添加行和列，并且通过下拉箭头自动添加筛选和排序功能。

![worksheet table](ssImages\tableExample1.gif)

单元格的实际表格数据通常与其他数据一样存储在工作表部分中，但表格的定义存储在一个单独的表格部分中，该部分从表格出现的工作表中被引用。

<worksheet . . .>

. . .

<sheetData>

. . .

</sheetData>

. . .

<tableParts count="1">

<tableParts count="1">

</tablePart r:id="rId2"/>

</worksheet>

工作表的rels部分包含以下内容：

<Relationship Id="rId2" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/table" Target=".. /tables/table1.xml"/>

表格部分如下所示。

![worksheet table](ssImages\tablePart.gif)

表格部分的内容如下。

<table xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main" id="1" name="Table1" displayName="Table1" ref="A18:C22" totalRowShown="0">

<autoFilter ref="A18:C22"/>

<tableColumns count="3">

tableColumn id="1" name="费用"

tableColumn id="2" name="金额"

tableColumn id="3" name="付款日期"

</tableColumns>

<tableStyleInfo name="TableStyleMedium9" showFirstColumn="0" showLastColumn="0" showRowStripes="1" showColumnStripes="0"/>

</table>

上面红色的ref属性定义了工作表中构成表格的单元格范围。

### 数据透视表

数据透视表用于聚合数据，并以易于理解的布局汇总和显示数据。例如，假设我有一个大型电子表格，记录了四个城市中四种产品的销售情况。我可能有产品、日期、销售数量、城市和州的列。每天都有每个城市每个产品的条目，即每天16个条目。因此，即使在4个城市只有4种产品，一年内我也可以有5840行数据。如果我想确定春季月份哪个城市的销售额最高？哪种产品在改进？哪个城市的红色小工具销售最多？数据透视表有助于汇总数据并快速提供这些问题的答案。

![worksheet table](ssImages\pivotData.gif)

数据透视表有行轴、列轴、值区域和报表筛选区域。每个表还有一个字段列表，用户可以从中选择要包含在数据透视表中的字段。下面是一个按产品汇总销售和收入的数据透视表。

![worksheet data for a pivot table](ssImages\pivotTable2.gif)

数据透视表由以下组件组成。

1. 有数据透视表汇总的基础数据。这些数据可能与数据透视表在同一工作表上，在不同的工作表上，或者可能来自外部源。
2. 该数据的缓存或副本在名为pivotCacheRecords部分的部分中创建；例如，当外部数据源不可用时，需要缓存。
3. 有一个pivotCacheDefinition部分，它定义数据透视表中的每个字段并包含共享项，很像sharedStrings部分包含字符串以消除工作表中的冗余。
4. pivotTable部分定义数据透视表本身的布局，指定哪些字段在行轴、列轴、报表筛选和值区域上。

![pivot table file architecture](ssImages\pivotTable3.gif)

工作簿指向并拥有pivotCacheDefinition部分。工作簿中有对数据透视表数据缓存的引用，跟在对工作表的引用之后：

<pivotCaches>

<pivotCache cacheId="13" r:id="rId4"/>

</pivotCaches>

工作簿的rels部分包含该引用：

<Relationship Id="rId4" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/pivotCacheDefinition" Target="pivotCache/pivotCacheDefinition1.xml"/>

pivotCacheDefinition部分又指向pivotCacheRecords部分。

<pivotCacheDefinition xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main" xmlns:r="http://schemas.openxmlformats.org/spreadsheetml/2006/relationships" r:id="rId1" refreshBy="XXXX" refreshedDate="41059.666109143516" createdVersion="1" refreshedVersion="3" recordCount="32" upgradeOnRefresh="1">

. . .

</pivotCacheDefinition>

pivotCacheDefinition的rels部分包含该引用：

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/pivotCacheRecord" Target="pivotCacheRecords1.xml"/>

pivotCacheDefinition部分还在其<cacheSource>元素中引用源数据：

<cacheSource type="worksheet">

<worksheetSource ref="A1:F33" sheet="Sheet1"/>

</cacheSource>

包含数据透视表的工作表引用pivotTable部分。（可能不止一个，因为一个工作表可以有多个数据透视表。）工作表的rels部分包含该引用：

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/pivotTable" Target="../pivotTables/pivotTable1.xml"/>

pivotTable部分引用pivotCacheDefinitions部分。pivotTable部分的rels部分包含该引用：

<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/pivotCacheDefinition" Target="../pivotCache/pivotCacheDefinition1.xml"/>

#### pivotCacheDefinition

现在让我们简要地看一下这些部分，并尝试理解它们。让我们从pivotCacheDefinition开始。如上所述，它指定源数据的位置。它还定义源数据中的每个字段（如要使用的数据类型和格式），包括那些在数据透视表中未使用的字段。（实际使用哪些字段在数据透视表部分中指定。）它被用作共享字符串的缓存，就像SharedStrings部分用于存储出现在工作表中的字符串一样。

我们示例工作表中六个字段的定义如下。

<pivotCacheDefinition . . .>

<cacheSource type="worksheet">

> worksheetSource ref="A1:F33" sheet="Sheet1"/>

</cacheSource>

<cacheFields count="6">

<cacheField name="Product" numFmtId="0">

<sharedItems count="4">

<s v="Green Widget"/>

<s v="Red Widget"/>

<s v="Grey Widget"/>

<s v="Blue Widget"/>

</sharedItems>

</cacheField>

<cacheField name="Quantity Sold" numFmtId="0">

<sharedItems containsSemiMixedTypes="0" containsString="0" containsNumber="1" containsInteger="1" minValue="1" maxValue="9"/>

</cacheField>

<cacheField name="Date" numFmtId="14">

<sharedItems containsSemiMixedTypes="0" containsNoDate="0" containsDate="1" containsString="0" minDate="2012-03-04T00:00:00" maxDate="2012-03-06T00:00:00 count=2">

<d v="2012-03-04T00:00:00"/>

<d v="2012-03-05T00:00:00"/>

</sharedItems>

</cacheField>

<cacheField name="Revenue" numFmtId="165">

<sharedItems containsSemiMixedTypes="0" containsString="0" containsNumber="1" containsInteger="1" minValue="1" maxValue="9"/>

</cacheField>

<cacheField name="City" numFmtId="0">

<sharedItems count="4">

<s v="Rochester"/>

<s v="Albany"/>

<s v="Pittsburgh"/>

<s v="Philadelphia"/>

</sharedItems>

</cacheField>

<cacheField name="State" numFmtId="0">

<sharedItems count=2">

<s v="NY"/>

<s v="PA"/>

</sharedItems>

</cacheField>

</cacheFields>

</pivotCacheDefinition>

上面定义的第一个字段是产品字段。它由共享字符串值组成。如果字段没有共享字符串值（如上面定义的第二个字段—销售数量字段），则值直接存储在pivotCacheRecords部分中。

#### pivotCacheRecords

让我们看看pivotCacheRecords部分，了解字段定义如何与缓存数据相关。下面是缓存中前两行数据。

<pivotCacheRecords . . .>

<r>

<x v="0"/>

<n v="2"/>

<x v="0"/>

<n v="2"/>

<x v="0"/>

<x v="0"/>

</r>

<r>

<x v="1"/>

<n v="3"/>

<x v="0"/>

<n v="3"/>

<x v="0"/>

<x v="0"/>

</r>

. . .

</pivotCacheRecords>

这对应于下面显示的工作表中的数据。

![sample of record data from the worksheet](ssImages\pivotTable4.gif)

首先注意，缓存数据的每个记录（<r>）具有与pivotCacheDefinition中定义的相同数量的值—在我们的例子中是六个。每个记录内包含以下可能的元素：

- <x> \- 表示引用pivotCacheDefinition中定义的字段项的索引值
- <s> \- 表示字符串值在记录中内联表达
- <n> \- 表示数值在记录中内联表达

查看上面pivotCacheRecords中的两个示例记录，我们从pivotCacheDefinition中知道这六个值依次是产品、数量、日期、收入、城市和州。第一个记录中的产品字段是<x v="0"/>，所以值（0）是产品字段中列出的项的索引。列出的第一个（索引0）是绿色小工具。第二个或数量字段值是<n v="2"/>，所以值（2）是内联表达的数值。第三个或日期字段值是<x v="0"/>，所以值（0）是日期字段中列出的项的索引（2012-03-04T00:00:00或3/4）。等等。

#### pivotTable

现在让我们看看pivotTable部分。根元素是<pivotTableDefinition>元素。其中有几个组件。首先，指定了数据透视表在工作表上的位置。位置很简单。注意，第一个标题和数据列都被指定了。

<pivotTableDefinition . . .>

<location ref="B37:G43 firstHeaderRow="1" firstDataRow="2" firstDataCol="4"/>

</cacheSource>

然后，字段的项顺序和每个字段的其他字段信息由<pivotFields>内的<pivotField>元素指定。

<pivotFields count="6">

<pivotField axis="axisRow" compact="0" outline="0" subtotalTop="0" showAll="0" includeNewItemsFilter="1">

<items count="5">

<item sd="0" x="3"/>

<item sd="0" x="0"/>

<item sd="0" x="2"/>

<item sd="0" x="1"/>

<item t="default"/>

</items>

</pivotField>

<pivotField dataField="1" compact="0" outline="0" subtotalTop="0" showAll="0" includeNewItemsFilter="1"/>

<pivotField axis="axisRow" compact="0" numFmtId="14" outline="0" subtotalTop="0" showAll="0" includeNewItemsFilter="1">

<items count="3">

<item sd="0" x="0"/>

<item sd="0" x="1"/>

<item t="default"/>

</items>

</pivotField>

. . .

</pivotFields count="6">

从pivotCacheDefinition我们知道，上面的第一个<pivotField>是产品。它列出了5个项。第一个是<item sd="0" x="3"/>。sd属性指示该项是否隐藏。值为0表示该项不隐藏。x属性是pivotCacheDefinition中产品的<cacheField>中项的索引。<cacheField>如下所示。注意，索引3处的项的值是蓝色小工具，因此如果产品字段显示，蓝色小工具应该首先出现在数据透视表中。

<cacheField name="Product" numFmtId="0">

<sharedItems count="4">

<s v="Green Widget"/>

<s v="Red Widget"/>

<s v="Grey Widget"/>

<s v="Blue Widget"/>

</sharedItems>

</cacheField>

第二个项的索引是0，即"绿色小工具"，第三个是2或"灰色小工具"，第四个是1或"红色小工具"。注意，<item t="default"/>表示小计或总计。

在<pivotFields>集合之后是<rowFields>集合。此集合指定数据透视表行轴上实际有哪些字段，以及它们的顺序。在我们的示例中，当我们完全展开第一行时，我们看到一行首先由产品组成，然后是城市，接着是州，然后是日期。这些是行字段。

![expanded pivot table row](ssImages\pivotTable5.gif)

按照<pivotFields>集合中的索引顺序，这是0, 4, 5, 2。相应的<rowFields>如下所示。

<rowFields count="4">

<field x="0"/>

<field x="4"/>

<field x="5"/>

<field x="2"/>

</rowFields>

在<rowFields>集合之后是<rowItems>集合。这是行轴上所有值的集合。数据透视表中的每一行都有一个<i>元素。对于每个<i>，有与行中项值一样多的<x>元素。v属性是引用<pivotField>项值的从零开始的索引。如果没有v，则假定值为0。t的grand值表示总计作为最后一个行项值。

<rowItems count="5">

<i>

<x/>

</i>

<i>

<x v="1"/>

</i>

<i>

<x v="2"/>

</i>

<i>

<x v="3"/>

</i>

<i t="grand">

<x/>

</i>

</rowItems>

接下来是<colFields>集合，指示哪些字段在数据透视表的列轴上。这里<x>再次是<pivotField>集合的索引。

<colFields count="1">

<field x="-2"/>

</colFields>

接下来是<colItems>集合，列出了列轴上的所有值。

<colItems count="2">

<i>

<x/>

</i>

<i i="1">

<x v="1"/>

</i>

</colItems>

可能还有一个<pageFields>集合，它描述报表筛选区域中的字段。

最后，有一个<dataFields>集合，它描述数据透视表值区域中的字段。在我们的示例中，值区域中有两个字段—销售数量总和和收入总和。下面是该集合。fld属性是被汇总字段的索引。

<dataFields count="2">

<dataField name="Sum of Quantity Sold" fld="1" baseField="0" baseItem="0"/>

<dataField name="Sum of Revenue" fld="3" baseField="0" baseItem="0"/>

</dataFields>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
