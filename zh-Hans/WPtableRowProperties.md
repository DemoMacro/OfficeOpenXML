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

# 文字处理表格

相关Open Office/ODF讨论  
相关HTML/CSS讨论

行属性

行级属性在<trPr>中指定。每个属性都是<trPr>的子元素，它们影响行中的所有单元格，尽管它们可以被单元格级属性覆盖。

<w:trPr>

<w:trHeight w:val="1440" w:hRule="exact"/>

<w:jc w:val="end"/>

</w:trPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.82。

![](images/note.png)注意：许多可能被视为行属性的属性，如边框、宽度和底纹，并未在<trPr>元素内部定义。例如，表格行<tr>可能在其<trPr>元素内不包含边框定义—只有表格和表格单元格可以指定边框（<tblBorders>和<tcBorders>）。

相反，行可以使用<tblPrEx>元素定义对表格级边框的例外。其他属性在表格单元格级别定义。有关表格和其他行属性（表格属性例外）的信息，请参见[表格属性](WPtableProperties.md)和[表格属性例外](WPtablePropertyExceptions.md)。

Word 2007示例：

![Table Row Properties](images/wp-tableRowProperty-1.gif)

---

最常用的属性如下所示：

### 元素/属性：

| 元素      | 描述                                                                                                                                                                                                            |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cantSplit | 如果存在，它通过将行的开始移动到新页面的开始来防止行的内容跨多个页面断开。如果内容无法容纳在单个页面上，该行将在新页面上开始并流动到多个页面。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.6。 |
| hidden    | 隐藏整行。（但是请注意，应用程序可以有允许显示隐藏内容的设置。）参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.20。                                                                              |
| jc        | 指定行相对于节中文本边距的对齐方式。请注意，只有当表格宽度与文档边距不同时，这才会明显，如上面的示例所示。唯一的属性是val。val的可能值是：                                                                      |

- center
- start ![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是left。
- end ![](images/versionConflict3.png)注意：在标准的先前版本中，此元素是right。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.28。  
tblCellSpacing | 指定行中单元格的默认单元格间距（相邻单元格和表格边缘之间的空间）。例如，<w:tblCellSpacing w:w="144" w:type="dxa"/> | ![表格单元格间距](images/wp-tblCellSpacing-1.gif)

---

属性是：

- w \— 指定间距的宽度。
- type \— 指定上述宽度属性的单位。如果省略，则假定值为dxa（点的二十分之一）。其他可能的值是nil。请注意，您可以指定auto或pct（表格宽度的百分比），但如果这样做，宽度值将被忽略。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.44。

tblHeader | 指定当前行应在显示表格的每个新页面的顶部重复。例如，<w:tblHeader />。这可以为多行指定以生成多行标题。请注意，如果该行不是第一行，则该属性将被忽略。这是一个简单的布尔属性，因此您可以指定val属性为true或false，或者根本不指定值（默认值为true）。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.50。  
trHeight | 指定行的高度。例如，<w:trHeight w:hRule="exact" w: val="2189" />。如果省略，行将自动调整大小以适应内容。属性是：

- hRule \— 指定高度的含义。可能的值是atLeast（高度应至少为指定值）、exact（高度应精确为指定值）或auto（默认值—高度基于内容的高度确定，因此该值被忽略）。
- val \— 指定行的高度，以点的二十分之一为单位。

![](images/note.png)注意：行的高度通常不能减少到单元格结束标记的大小以下。这可以防止表格行在没有内容时消失。但是，这使得无法通过为单元格添加底纹或在单元格中放置图像来将行用作边框。要解决此问题，请在行中每个单元格的<w:tcPr />内使用<w:hideMark />元素。参见[隐藏表格单元格结束标记](WPhideMark.md)参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.4.81。

---

# 相关开放文档格式（ODF）属性：

表格行属性在<style:table-row-properties>元素中指定。

<style:style style:name="Table1.1" style:family="table-row">

<style:table-row-properties style:min-row-height="0.4896in"/>

</style:style>

参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 17.17。

<style:table-row-properties>元素可以具有以下属性：

| 属性                         | 描述                                                     |
| ---------------------------- | -------------------------------------------------------- |
| fo:background-color          | 指定行的背景颜色。                                       |
| fo:break-after               | 指定行后的分隔符。可能的值是auto、column和page。         |
| fo:break-before              | 指定行前的分隔符。可能的值是auto、column和page。         |
| fo:keep-together             | 指定何时应将行与表格保持在一起。可能的值是auto和always。 |
| style:min-row-height         | 指定行的固定最小高度。                                   |
| style:row-height             | 指定固定的行高。                                         |
| style:use-optimal-row-height | 指定如果行中的内容发生变化，应自动重新计算行高。         |

请注意，<style:table-row-properties>还可以包含<style:background-image>元素。

# 相关HTML/CSS属性：

<table cellspacing="20px" style="width: 100%; border-collapse:separate;">

<thead>

<tr>

<th>第一列</th>

<th>第二列</th>

<th>第三列</th>

</tr>

</thead>

<tbody>

<tr> . . .</tr>

<tr style="height:50px; text-align:right;"> . . .</tr>

<tr> . . .</tr>

<tr style="display: none;"> <td>JJJ</td><<td>KKK</td><<td>LLL</td></tr>

</tbody>

</table>

请注意，在HTML中，Cellspacing不能在行级别应用。

CSS示例：

| 第一列 | 第二列 | 第三列 |
| ------ | ------ | ------ |
| AAA    | BBB    | CCC    |
| DDD    | EEE    | FFF    |
| GGG    | HHH    | III    |
| JJJ    | KKK    | LLL    |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
