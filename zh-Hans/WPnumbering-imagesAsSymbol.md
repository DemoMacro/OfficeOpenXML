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

# 文字处理编号

相关Open Office/ODF讨论  
相关HTML/CSS讨论

图片或图像作为编号符号

在编号定义中，图片/绘图作为编号符号的外观由编号部分中根编号元素内的<w:numPicBullet>元素指定。该图片通过其numPicBulletId属性被抽象编号定义中的lvlPicBulletId元素引用。

以下是在编号部分中找到的示例xml：

<w:numPicBullet w:numPicBulletId="0">

<w:drawing>

. . .

</w:drawing>

</w:numPicBullet>

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="007A7BC1"/>

<w:multiLevelType w:val="hybridMultilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="bullet"/>

<w:lvlText w:val=" "/>

<w:lvlPicBulletId w:val="0"/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Symbol" w:hAnsi="Symbol"/>

<w:color w:val="auto"/>

</w:rPr>

</w:lvl>

. . .

</w:abstractNum>

<w:num w:numId="1">

<w:abstractNumId w:val="0"/>

</w:num>

文档内容中的XML不直接引用该绘图—只引用num，即编号部分中abstractNum的实例。

<w:p>

<w:pPr>

<w:pStyle w:val="ListParagraph"/>

<w:numPr>

<w:ilvl w:val="0"/>

<w:numID w:val="1"/>

</w:numPr>

</w:pPr>

<w:r>

<w:t>这是第一个…

</w:r>

</w:p>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 17.9.21和§ 17.9.10。

Word 2007示例：

![Picture or Image as bullet](images\wp-numbering-numPicBullet-1.gif)

---

### numPicBullet的属性：

只有一个属性：

| 属性           | 描述                   |
| -------------- | ---------------------- |
| numPicBulletId | 指定图片定义的唯一ID。 |

### numPicBullet的子元素：

只有一个元素：

| 元素    | 描述                                                                                            |
| ------- | ----------------------------------------------------------------------------------------------- |
| drawing | 指定一个DrawingML对象。![](images/versionConflict3.png)注意：在标准的2003版本中，此元素是pict。 |

### lvlPicBulletId的属性：

只有一个属性：

| 属性 | 描述                                         |
| ---- | -------------------------------------------- |
| val  | 指定numPicBulletId中指定的图片定义的唯一ID。 |

---

# 相关开放文档格式（ODF）属性：

列表项的图像使用<text:list-level-style-image>元素为适当的级别指定，如应用于列表的<text:list-style>中指定的那样。

参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 16.33。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L1"/>

<text:list-style style:name="L1">

<text:list-level-style-image text:level="1" xlink:href="Pictures/100002000000000C0000000CDA3C0BB5.gif" xlink:type="simple" xlink:show="embed" xlink:actuate="onLoad">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment" style:vertical-pos="middle" style:vertical-rel="line" fo:width="0.1252in" fo:height="0.1252in">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="0.5in" fo:text-indent="-0.25in" fo:margin-left="0.5in"/ >

</style:list-level-properties>

</text:list-level-style-image>

. . .

</text:list-style>

# 相关HTML/CSS属性：

<ul style="list-style-image: url(images/bulletImage.gif)">

CSS示例：

- 这是第一个无序列表项。
- 这是第二个无序列表项。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
