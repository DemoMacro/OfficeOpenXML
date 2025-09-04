![SpreadsheetXML.com](ssImages\SpreadsheetMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [电子表格ML文件剖析](anatomyofOOXML-xlsx.md)
- [内容概述](SScontentOverview.md)
- [样式和格式](SSstyles.md)

# 电子表格样式

电子表格可以使用样式、主题和直接格式进行样式设置。有单元格样式、表格样式和数据透视表样式。然而，与文字处理ML不同，样式XML永远不会与工作表中的内容一起出现。格式始终单独存储在工作簿的单个样式部分中。整个工作表还有一个单独的主题部分。

单元格样式可以指定数字格式、单元格对齐方式、字体信息、单元格边框和背景/前景填充。表格样式指定表格区域的格式，例如，标题为粗体或应将灰色填充应用于交替行。数据透视表样式指定数据透视表区域的格式，例如总计或行轴的颜色。主题定义一组颜色、字体信息和形状效果。样式或格式元素可以通过引用主题来定义颜色、字体或效果，但当然，如果主题更改，该格式可能会更改。

## 文本级格式

然而，在讨论应用于工作表的样式之前，让我们先介绍文本级格式，即不是应用于整个单元格的格式，而是可能从单词到单词变化的格式，例如不同的颜色或效果。例如，请看下面的单元格A13，第一个单词为蓝色，第二个单词有橙色下划线。显然，这无法通过单元格样式实现。这种格式是在存储单元格文本的共享字符串部分中完成的。

![formatting within a cell](ssImages\SSstyles1.gif)

让我们看看工作表部分中第13行第一个单元格的XML。从单元格的类型属性t="s"我们知道文本存储在共享字符串部分中，从<v="25"/>我们知道该字符串是第26个字符串或<si>。（请记住，这是从零开始的索引。）

<row r="13">

<c r="A13" t="s">

<v>25</v>

</c>

. . .

</row>

该字符串的XML如下。请注意，格式直接应用于字符串项内，就像直接格式应用于文字处理ML（docx）文档中使用运行属性（<rPr>）的文本运行（<r>）一样。

<si>

<r>

<rPr>

<sz val="11"/>

<color theme="4"/>

<rFont val="Calibri"/>

<family val="2"/>

<scheme val="minor"/>

</rPr>

<t>蓝色</t>

</r>

<r>

<rPr>

<sz val="11"/>

<color theme="1"/>

<rFont val="Calibri"/>

<family val="2"/>

<scheme val="minor"/>

</rPr>

<t xml:space="preserve"> </t>

</r>

<r>

<rPr>

<u/>

<sz val="11"/>

<color theme="9"/>

<rFont val="Calibri"/>

<family val="2"/>

<scheme val="minor"/>

</rPr>

<t>小部件</t>

</r>

</si>

## 单元格级格式

现在让我们回到单元格样式。电子表格ML中的样式实现是为了最小化重复，这是通过集合完成的。在样式部分中有如下所示的集合。

<stylesheet xmls="http://schemas.openxmlformats.org/spreadsheetml/2006/main">

<numFmts/>

<fonts/>

<fills/>

<borders/>

<cellStyleXfs/>

<cellXfs/>

<cellStyles/>

<dxfs/>

<tableStyles/>

</stylesheet>

上面的大多数集合（除了<dxfs>和<tableStyles>）都与单元格相关。前四个集合—numFmts、fonts、fills和borders—包含工作簿中每个单元格的所有可能特征。每个集合可能有许多元素，每个元素定义具有相同特征的一组单元格的特征。例如，下面是工作簿的<fills>示例。工作簿中的每个单元格都将使用这些填充定义之一。

<fills count="5">

<fill>

<patternFill patternType="none"/>

</fill>

<fill>

<patternFill patternType="gray125"/>

</fill>

<fill>

<patternFill patternType="solid">

<fgColor rgb="FFFFEB9C"/>

</patternFill/>

</fill>

<fill>

<patternFill patternType="solid">

<fgColor theme="5" tint="0.39997558519241921"/>

<bgColor indexed="65"/>

</patternFill/>

</fill>

<fill>

<patternFill patternType="solid">

<fgColor rgb="FFC6EFCE"/>

</patternFill/>

</fill>

</fills>

特定单元格的<fill>是通过从零开始的索引指定到上述fills集合中的。单元格的字体、数字格式和边框也是如此。因此，单元格的格式可以通过指向这四个集合的索引列表或集合来指定。实际上，这就是<cellXfs>的作用。它包含索引组的集合，每个组对应于工作簿中找到的每种单元格格式特征组合。下面是这样一个分组。

<cellXfs count="14">

<xf numFmtId="0" fontId="0" fillId="0" borderId="0" xfId="0"/>

. . .

</cellXfs>

每个单元格都将引用<cellXfs>集合中的一个<xf>。这是单元格的直接格式。要将样式应用于单元格，<xf>使用xfId属性引用样式。xfId属性是<cellStyleXFs>集合的索引，该集合收集用户可用的单元格样式。<cellStyleXFs>为每个样式包含一个<xf>。每个这样的<xf>通过来自<cellStyles>集合的索引（在其xfId属性中）与其名称关联。

让我们通过查看一个示例来尝试将所有内容联系在一起。考虑下面示例中的第10行。

![formatting within a cell](ssImages\SSstyles2.gif)

第一个单元格A10应用了单元格样式。工作表中该单元格的XML如下。

<row r="10">

<c r="A10" s="12" t="s">

<v>6</v>

</c>

. . .

</row>

从属性s="12"我们知道单元格的格式存储在样式部分的<cellXfs>集合中的第13个（从零开始的索引）<xf>中。第13个<xf>如下。

<xf numFmtId="0" fontId="8" fillId="4" borderId="0" xfId="3"/>

因此，对于此单元格，数字格式是<numFmts>集合中的第一个（索引值为0）。单元格使用<fonts>集合中第9个<font>中的字体格式，<fills>集合中的第5个<fill>（引用绿色的主题），以及<borders>集合中的第一个<border>。此单元格还应用了一个样式（xfId="3"）—<cellStyleXfs>集合中的第4个<xf>。该样式如下所示。

<xf numFmtId="0" fontId="8" fillId="4" borderId="0" applyNumberFormat="0" applyBorder="0" applyAlignment="0" applyProtection="0"/>

样式的格式与直接格式相同，属性applyNumberFormat、applyBorder、applyAlignment和applyProtection的值均为0，告诉我们不要应用样式的相应值，而是应用直接格式的值。在这种情况下它们是相同的，所以无论如何都没有区别。

## 表格级格式

表格通过在表格部分的表格定义中指定<tableStyleInfo>元素来应用表格样式。例如，以下示例表格定义指定了TableStyleMedium9样式。请注意，它是通过名称指定的。还要注意，不仅指定了样式，该规范还告诉我们样式的哪些方面被打开（例如，showRowStripes="1"），哪些方面被关闭（例如，showLastColumn="0"）。每个表格样式由格式定义集合组成，每个定义对应于表格的特定区域—例如，整个表格、第一列条纹、第一行条纹、第一列、标题列、第一个标题单元格等。这些格式定义中的每一个都可以打开或关闭。

<table xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main" id="1" name="Table1" displayName="Table1" ref="A18:C22" totalRowShown="0">

<autoFilter ref="A18:C22"/>

<tableColumns count="3">

tableColumn id="1" name="费用"

tableColumn id="2" name="金额"

tableColumn id="3" name="支付日期"

</tableColumns>

<tableStyleInfo name="TableStyleMedium9" showFirstColumn="0" showLastColumn="0" showRowStripes="1" showColumnStripes="0"/>

</table>

ECMA-376第3版（2011年6月）OOXML规范的附件G定义了单元格、表格和数据透视表的内置样式，样式TableStyleMedium9是内置表格样式之一。内置表格和数据透视表样式不存储在样式部分中—只有自定义样式才存储。

下面是在样式部分中定义的自定义样式，基于TableStyleMedium9样式。

<tableStyles count="1" defaultTableStyle="TableStyleMedium9" defaultPivotStyle="PivotStyleLight16">

<tableStyle name="My Custom Table Style" pivot="0" count="3">

<tableStyleElement type="wholeTable" dxfId="2">

<tableStyleElement type="headerRow" dxfId="1">

<tableStyleElement type="firstColumn" dxfId="0">

</tableStyle>

</tableStyles>

该样式如下所示：

![custom table style](ssImages\SSstyles3.gif)

上面的样式定义使用差异格式记录（从dxfId属性引用的<dxf>元素），这使得可以指定格式子集而不是指定所有格式。查看上面的示例，我们看到默认样式是TableStyleMedium9样式。从中我们正在更改三个方面—wholeTable、headerRow和firstColumn。这些元素中的每一个都引用（再次使用从零开始的索引）样式部分中的<dxfs>集合。例如，<headerRow>元素引用第二个<dxf>（dxfId="1"）。它将粗体和填充背景颜色应用于默认表格样式defaultTableStyle="TableStyleMedium9"。

<dxfs count="3">

<dxf>

<font>

<b val="0"/>

<i/>

<strike/>

</font>

<fill>

<patternFill>

<bgColor theme="2" tint="-0.2499465926081701"/>

</patternFill>

</fill>

</dxf>

<dxf>

<font>

<b/>

<i val="0"/>

<strike val="0"/>

</font>

<fill>

<patternFill>

<bgColor theme="8" tint="0.59996337778862885"/>

</patternFill>

</fill>

</dxf>

<dxf>

<fill>

<patternFill>

<bgColor theme="5" tint="0.59996337778862885"/>

</patternFill>

</fill>

<border>

<left style="hair">

<color auto="1"/>

</left>

<right style="hair">

<color auto="1"/>

</right>

<top style="hair">

<color auto="1"/>

</top>

<bottom style="hair">

<color auto="1"/>

</bottom>

<vertical style="hair">

<color auto="1"/>

</vertical>

<horizontal style="hair">

<color auto="1"/>

</horizontal>

</border>

</dxf>

</dxfs>

## 条件格式

条件格式是一种格式，如单元格底纹或字体颜色，如果指定条件为真，电子表格可以自动将其应用于单元格。例如，您可以指定如果单元格中的值高于50，则单元格填充颜色应为红色。它可以是一个非常有效的工具，用于视觉上突出显示工作表中数据的重要方面。

条件格式规则存储在工作表部分中，位于<sheetData>元素之后的<conditionalFormatting>元素内。格式应用的单元格范围由sqref属性指定。每个条件都在<cfRule>元素内。可以设置多个规则，每个规则具有不同的优先级。有几种不同类型的规则来指定不同的条件。例如，type="cellIs"将根据单元格值是大于还是小于指定值，或介于两个值之间来确定单元格格式。type="dataBar"将根据单元格中的值在单元格内显示一个长度可变的条形。这些类型通过<cfRule>上的type属性设置。type="iconSet"将根据单元格中的值在单元格中显示一个图标。下面是一个示例表格，它对单元格B2:B7应用两个条件—一个条件是如果单元格值大于500则应用粉红色填充，另一个条件是如果值小于300则应用绿色填充。

![conditional formatting](ssImages\SSstyles4.gif)

条件的XML如下。

<conditionalFormatting sqref="B2:B7">

<cfRule type="cellIs" dxfId="0" priority="2" operator="greaterThan">

<formula>500</formula>

</cfRule>

<cfRule type="cellIs" dxfId="1" priority="1" operator="lessThan">

<formula>300</formula>

</cfRule>

</conditionalFormatting>

页脚
