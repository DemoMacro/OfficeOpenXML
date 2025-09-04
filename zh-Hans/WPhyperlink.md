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

# 文字处理超链接

外部链接

链接使用<w:hyperlink>元素指定。指向文档外部位置的链接和指向文档内部位置的链接根据r:id属性的存在与否进行不同处理。如果链接指向外部目标，则指定r:id属性，该属性是存储在关系部分(document.xml.rels)中的关系的ID。该关系的TargetMode属性值为External。可以使用docLocation属性指定链接目标内的特定位置。请参见下面的属性。

<w:p>

<w:r>

<w:t xml:space="preserve">这是一个外部链接到 </w:t>

</w:r>

<w:hyperlink r:id="rId4">

<w:r>

<w:rPr>

<w:rStyle w:val="Hyperlink"/>

</w:rPr>

<w:t>Google</w:t>

</w:r>

</w:hyperlink>

</w:p>

r:id="rId4"引用文档的关系部分(document.xml.rels)中的以下关系。

<Relationship Id="rId4" Type="http://. . ./hyperlink" Target="http://www.google.com/" TargetMode="External"/>

Word 2007 示例：

![External Hypertext](images\wp-hyperlink-1.gif)

---

内部链接

内部链接通过包含anchor属性来指定，该属性的值为文档中的书签。

<w:p>

<w:r>

<w:t xml:space="preserve">这是一个 </w:t>

</w:r>

<w:hyperlink w:anchor="myAnchor">

<w:r>

<w:rPr>

<w:rStyle w:val="Hyperlink"/>

</w:rPr>

<w:t>内部链接</w:t>

</w:r>

</w:hyperlink>

</w:p>

. . .

<w:p>

<w:r>

<w:t xml:space="preserve">这是带有 </w:t>

</w:r>

<w:bookmarkStart w:id="0" w:name="myAnchor"/>

<w:r>

<w:t>书签</w:t>

</w:r>

<w:bookmarkEnd w:id="0"/>

</w:p>

Word 2007 示例：

![Internal Hypertext](images\wp-bookmark-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.22。

### 属性：

最常用的属性是：

| 属性        | 描述                                                                                                                                               |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| anchor      | 指定文档中书签的名称。请参见[书签](WPbookmark.md)。如果省略该属性，则默认行为是导航到文档的开头。如果指定了r:id属性，则忽略anchor属性。            |
| docLocation | 指定超链接目标中的位置，在链接是外部链接的情况下。 <w:hyperlink r:id="rId9" w:docLocation="table"> <w:r> <w:t>点击此处</w:t> </w:r> </w:hyperlink> |
| history     | 指定是否应将目标添加到已查看链接列表中。可能的值为true和false。                                                                                    |
| id          | 指定外部链接的关系部分中关系的ID。该关系将包含Target属性，该属性是链接的目标。如果指定了id属性，它将取代anchor属性。                               |
| tgtFrame    | 当存在框架集时，指定HTML框架集中目标的框架。如果不存在框架集，则忽略此属性。可能的值是：                                                           |

- \_top - 在当前窗口中打开
- \_self - 在与链接相同的框架中打开
- \_parent - 在当前框架的父框架中打开
- \_blank - 在新的Web浏览器窗口中打开
- 所有其他值 - 在具有指定名称的框架中打开，否则在当前框架中打开

tooltip | 指定可以在用户界面中显示为与超链接关联的字符串。

### 相关HTML属性：

#### 外部链接

<p><a href="http://www.google.com">此链接指向Google.com。</a></p>

HTML 示例：

[此链接指向Google.com。](http://www.google.com)

#### 内部链接

<p><a href="#myAnchor">此链接指向上面的内部链接标题处的锚点。</a></p>

<div><a name="myAnchor">内部链接</a></div>

HTML 示例：

此链接指向上面的内部链接标题处的锚点。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
