![OfficeOpenXML.com](images/banner1.png)

[Home](index.md) | [WordprocessingML (docx)](anatomyofOOXML.md) | [SpreadsheetML (xlsx)](anatomyofOOXML-xlsx.md) | [PresentationML (pptx)](anatomyofOOXML-pptx.md) | [DrawingML](drwOverview.md)

- [Content Overview](WPcontentOverview.md)
- [Sample Docx View](WPsampleDoc.md)
- [Document](WPdocument.md)
- Paragraphs
  - [Overview](WPparagraph.md)
  - [Properties](WPparagraphProperties.md)
    - [Horizontal Alignment](WPalignment.md)
    - [Borders](WPborders.md)
    - [Breaks](WPtextSpecialContent-break.md)
    - [Indentation](WPindentation.md)
    - [Shading and Background](WPshading.md)
    - [Spacing](WPspacing.md)
    - [Styles](WPstyleParStyles.md)
    - [Tabs](WPtab.md)
    - [Vertical Alignment](WPborders.md)
- [Text Frames](WPparagraph-textFrames.md)
- Text
  - [Overview](WPtext.md)
  - [Properties](WPtextFormatting.md)
    - [Borders](WPtextBorders.md)
    - [Fonts](WPtextFonts.md)
    - [Shading](WPtextShading.md)
    - [Spacing](WPtextSpacing.md)
    - [Special Content](WPtextSpecialContent.md)
      - [Breaks](WPtextSpecialContent-break.md)
      - [Symbols](WPtextSpecialContent-symbol.md)
    - [Styles](WPstyleCharStyles.md)
- Tables
  - Structure
    - [Overview](WPtable.md)
    - [Defining Columns or Table Grid](WPtableGrid.md)
    - [Rows](WPtableRow.md)
    - [Cells](WPtableCell.md)
  - [Table Properties](WPtableProperties.md)
    - [Alignment](WPtableAlignment.md)
    - [Borders](WPtableBorders.md)
    - [Border Conflicts](WPtableCellBorderConflicts.md)
    - [Captions](WPtableCaption.md)
    - [Indentation](WPtableIndent.md)
    - [Shading](WPtableShading.md)
    - [Width](WPtableWidth.md)
    - [Styles](WPstyleTableStyles.md)
    - [Cell Margins](WPtableCellMargins.md)
    - [Cell Spacing](WPtableCellSpacing.md)
    - [Autofit/Width Layout](WPtableLayout.md)
    - [Absolute Positioning or Floating Tables](WPfloatingTables.md)
    - [Conditional Formatting](WPtblLook.md)
  - [Table Property Exceptions](WPtablePropertyExceptions.md)
  - [Row Properties](WPtableRowProperties.md)
  - [Cell Properties](WPtableCellProperties.md)
    - [Borders](WPtableCellProperties-Borders.md)
    - [Cell Border Conflicts](WPtableCellBorderConflicts.md)
    - [Margins](WPtableCellProperties-Margins.md)
    - [Shading](WPtableCellProperties-Shading.md)
    - [Vertical Alignment](WPtableCellProperties-verticalAlignment.md)
    - [Width](WPtableCellProperties-Width.md)
    - [Hide End of Cell Mark](WPhideMark.md)
- Numbering, Levels and Lists
  - [Overview](WPnumbering.md)
  - [Defining a Numbering Scheme](WPnumberingAbstractNum.md)
  - [Defining a Particular Level](WPnumberingLvl.md)
    - [Numbering Level Text](WPnumberingLevelText.md)
    - [Numbering Format](WPnumbering-numFmt.md)
    - [Displaying as Numerals Only](WPnumbering-isLgl.md)
    - [Restart Numbering](WPnumbering-restart.md)
    - [Picture or Image as Numbering Symbol](WPnumbering-imagesAsSymbol.md)
    - [Justification](WPnumbering-lvlJc.md)
  - [Overriding a Numbering Definition](WPnumberingOverride.md)
- Sections
  - [Overview](WPsection.md)
  - [Columns](WPsectionCols.md)
  - [Footers](WPsectionFooterReference.md)
  - [Headers](WPsectionHeaderReference.md)
  - [Borders](WPsectionBorders.md)
  - [Page Margins](WPsectionPgMar.md)
  - [Page Numbers](WPSectionPgNumType.md)
  - [Line Numbers](WPsectionLineNumbering.md)
- Styles
  - [Overview](WPstyles.md)
  - [Defining Default Formats](WPstyleDefaults.md)
  - [Defining a Style](WPstyle.md)
    - [General Style Properties](WPstyleGenProps.md)
    - [Character Styles](WPstyleCharStyles.md)
    - [Paragraph Styles](WPstyleParStyles.md)
    - [Table Styles](WPstyleTableStyles.md)
      - [Conditional Formatting](WPstyleTableStylesCond.md)
    - [Numbering Styles](WPstyleNumStyles.md)
- [Fonts](WPfonts.md)
- [Headers](WPheaders.md)
- [Footers](WPfooters.md)
- [Page Numbers](WPSectionPgNumType.md)
- Links
  - [Overview](WPhyperlink.md)
  - [Bookmarks](WPbookmark.md)
- Fields
  - [Overview](WPfields.md)
  - [Field Instructions](WPfieldInstructions.md)
  - [Field Definitions](WPfieldDefinitions.md)
  - [General Field Formatting](WPgeneralFieldSwitches.md)
  - [Date and Time Field Formatting](WPdateTimeFieldSwitches.md)
  - [Numeric Field Formatting](WPnumericFieldSwitches.md)
- [Table of Contents](WPtableOfContents.md)

# Wordprocessing Tables

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Row Properties

Row-level properties are specified in <trPr>. Each property is a child element of <trPr>, and they affect all cells in the row, though they can be overridden by cell-level properties.

<w:trPr>

<w:trHeight w:val="1440" w:hRule="exact"/>

<w:jc w:val="end"/>

</w:trPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.82.

![](images/note.png)Note: Many properties which one might regard as row properties, such as borders, width, and shading, are not defined inside of the <trPr> element. For example, a table row <tr> may not contain a border definition inside its <trPr> element--only tables and tables cells may specify borders (<tblBorders> and <tcBorders>).

Instead, a row may define an exception to the table-level borders using the <tblPrEx> element. Other properties are defined at the table cell level. See [Table Properties](WPtableProperties.md) and [Table Property Exceptions](WPtablePropertyExceptions.md) for table and other row properties (table property exceptions).

Word 2007 Example:

![Table Row Properties](images/wp-tableRowProperty-1.gif)

---

The most commonly used properties are shown below:

### Elements/Properties:

| Element   | Description                                                                                                                                                                                                                                                                                                                                                    |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cantSplit | If present, it prevents the contents of the row from breaking across multiple pages by moving the start of the row to the start of a new page. If the contents cannot fit on a single page, the row will start on a new page and flow onto multiple pages. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.6. |
| hidden    | Hides the entire row. (Note, however, that applications can have settings that allow hidden content to be displayed.) Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.20.                                                                                                                                     |
| jc        | Specifies the alignment of the row with respect to the text margins in the section. Note that this will only be apparent if the table does not have the same width as the document margins, as in the example above. The only attribute is val. The possible values for val are:                                                                               |

- center
- start ![](images/versionConflict3.png)Note: In the previous version of the standard, this element was left.
- end ![](images/versionConflict3.png)Note: In the previous version of the standard, this element was right.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.28.  
tblCellSpacing | Specifies the default cell spacing (space between adjacent cells and the edges of the table) for cells in the row. E.g., <w:tblCellSpacing w:w="144" w:type="dxa"/> | ![Table Cell Spacing](images/wp-tblCellSpacing-1.gif)

---

The attributes are:

- w \-- Specifies the width of the spacing.
- type \-- Specifies the units of the width attribute above. If omitted, the value is assumed to be dxa (twentieths of a point). Other possible values are nil. Note that you can specify auto or pct (width in percent of table width), but if you do, the width value will be ignored.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.44.

tblHeader | Specifies that the current row should be repeated at the top each new page on which the table is displayed. E.g, <w:tblHeader />. This can be specified for multiple rows to generate a multi-row header. Note that if the row is not the first row, then the property will be ignored. This is a simple boolean property, so you can specify a val attribute of true or false, or no value at all (defalut value is true). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.50.  
trHeight | Specifies the height of the row. E.g, <w:trHeight w:hRule="exact" w: val="2189" />. If omitted, the row is automatically resized to fit the content. The attributes are:

- hRule \-- Specifies the meaning of the height. Possible values are atLeast (height should be at leasat the value specified), exact (height should be exactly the value specified), or auto (default value--height is determined based on the height of the contents, so the value is ignored).
- val \-- Specifies the row's height, in twentieths of a point.

![](images/note.png)Note: The height of a row typically cannot be reduced below the size of the end of the cell marker. This prevents table rows from disappearing when they have no content. However, this makes it impossible to use a row as a border by shading its cells or putting an image in the cells. To overcome this problem, use the <w:hideMark /> element within the <w:tcPr /> of each cell in the row. See [Hide End of Table Cell Mark](WPhideMark.md) Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.81.

---

# Related Open Document Format (ODF) Property:

Table row properties are specified in the <style:table-row-properties> element.

<style:style style:name="Table1.1" style:family="table-row">

<style:table-row-properties style:min-row-height="0.4896in"/>

</style:style>

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 17.17.

The <style:table-row-properties> element can have the following attributes:

| Attributes                   | Description                                                                                     |
| ---------------------------- | ----------------------------------------------------------------------------------------------- |
| fo:background-color          | Specifies a color for the background of the row.                                                |
| fo:break-after               | Specifies a break after the row. Possible values are auto, column, and page.                    |
| fo:break-before              | Specifies a break before the row. Possible values are auto, column, and page.                   |
| fo:keep-together             | Specifies when the row should be kept with the table. Possible values are auto and always.      |
| style:min-row-height         | Specifies a fixed minimum height for the row.                                                   |
| style:row-height             | Specifies a fixed row height.                                                                   |
| style:use-optimal-row-height | Specifies that a row height should be recalculated automatically if content in the row changes. |

Note that <style:table-row-properties> can also contain a <style:background-image> element.

# Related HTML/CSS Property:

<table cellspacing="20px" style="width: 100%; border-collapse:separate;">

<thead>

<tr>

<th>First column</th>

<th>Second Column</th>

<th>Third Colum</th>

</tr>

</thead>

<tbody>

<tr> . . .</tr>

<tr style="height:50px; text-align:right;"> . . .</tr>

<tr> . . .</tr>

<tr style="display: none;"> <td>JJJ</td><<td>KKK</td><<td>LLL</td></tr>

</tbody>

</table>

Note that Cellspacing cannot be applied at the row level in HTML.

CSS Example:

| First column | Second column | Third column |
| ------------ | ------------- | ------------ |
| AAA          | BBB           | CCC          |
| DDD          | EEE           | FFF          |
| GGG          | HHH           | III          |
| JJJ          | KKK           | LLL          |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
