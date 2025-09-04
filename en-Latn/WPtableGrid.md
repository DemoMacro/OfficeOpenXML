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

Grid/Column Definition

The columns of a table are defined by the <w:tblGrid> element. The <w:tblGrid> contains an element <w:gridCol> for each possible cell size (sometimes called logical columns) in the table. The number of <w:gridCol> elements needed for the table's <w:tblGrid> is determined by extending each cell's vertical borders and counting the total number of columns defined by the lines. For example, the table below has three columns and needs 3 <w:gridCol> elements in its <w:tblGrid>.

Word 2007 Example:

![Table Grid](images\wp-tableGrid-3.gif)

---

The <w:tblGrid> for this table is below:

<w:tblGrid>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2880"/>

</w:tblGrid>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.49.

Things become more complicated when cells are not of equal length from row to row. For example, the table below has five columns and so needs 5 <w:gridCol> elements in its <w:tblGrid> element.

Word 2007 Example:

![Table Grid](images\wp-tableGrid-1.gif)

---

The <w:tblGrid> for this table is below:

<w:tblGrid>

</w:gridCol w:w="1638"/>

</w:gridCol w:w="1242"/>

</w:gridCol w:w="2880"/>

</w:gridCol w:w="2178"/>

</w:gridCol w:w="702"/>

</w:tblGrid>

![](images/note.png)Note: The width of each cell (<w:tcW>) will equal one of the <w:gridCol> element values, or will be the sum of two or more when the table is not sized automatically.

Consider the first row in the table directly above. It looks like this:

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>AAA</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="5058" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>BBB</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="702" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>CCC</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

### Elements:

The <w:tblGrid> element contains one or more <w:gridCol> elements. (The <w:tblGridChange> element for tracking revisions has been omitted.)

| Element | Description                                                           |
| ------- | --------------------------------------------------------------------- |
| gridCol | Specifies the details about a single grid column. The attributes are: |

- <w:w> \-- specifies the width of the column in twentieths of a point. This alone does not determine the actual width, however. It can be overridden when the table is displayed by the table layout algorithm or by the preferred widths of particular cells that are a part of the column.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.16.

### Cell Spanning

The first cell with contents "AAA" spans the first two logical columns, so the width is the sum of the first and second <w:gridCol> element values (1638 + 1242 = 2880). Note that the <w:gridSpan> value is 2, meaning the cell spans two logical columns. The second cell with contents "BBB" spans the third and fourth logical columns, so the width is the sum of the third and fourth <w:gridCol> element values (2880 + 2178 = 5058). The <w:gridSpan> value is also 2.

The <w:gridSpan> indicates a cell horizontally spanning multiple logical cells (as defined by the <w:tblGrid>, much like the HTML colspan attribute placed on a cell. Cells can also span vertically using the <w:vMerge> element/property in a <w:tcPr> element.

Word 2007 Example:

![Table Grid](images\wp-tableGrid-5.gif)

---

The last two rows are shown below.

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="1638" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>DDD</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="4122" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>EEE</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:vMerge w:val="restart"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>FFF</w:t>

</w:r>

</w:p>

<w:p>

<w:r>

<w:t>III</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>GGG</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>HHH</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

<w:gridSpan w:val="2"/>

<w:vMerge/>

</w:tcPr>

<w:p/>

</w:tc>

</w:tr>

---

# Related Open Document Format (ODF) Property:

A table grid is specified with <table:table-column> elements--one for each cell size appearing in the table.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 9.1.6.

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A"/>

<table:table-column table:style-name="Table1.B"/>

<table:table-column table:style-name="Table1.C"/>

. . .

</table:table>

If adjoining columns have the same style, then the table:number-columns-repeated attribute can be set instead of listing three separate <table:table-column> elements:

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A" table:number-columns-repeated="3"/>

. . .

</table:table>

### Attributes:

The most commonly used attributes are below.

| Attributes                    | Description                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------ |
| table:default-cell-style-name | Specifies the cell style to be used if there is no value for table:style-name. |
| table:style-name              | Specifies a table style for the table.                                         |
| table:number-columns-repeated | Specifies the number of columns with the same style. See comments above.       |
| xml:id                        | Specifies a unique ID and is standardized by the W3C (xml-id).                 |
| table:visibility              | Specifies whether the column is visible.                                       |

# Related HTML/CSS Property:

Cell widths can be set with the width css property. Cells can span rows or columns with the rowspan and colspan attributes on a cell, respectively. Note that although there are also colgroup and col elements in HTML, they are used for grouping cells for sytlistic similarities and do not imply structural groupings like the OOXML tblGrid.

<table style="width:100%;">

<tr>

<td style="width:10%">AAA</td>

<td rowspan="2" style="width:20%">BBB</td>

<td style="width:70%">CCC</td>

</tr>

<tr>

<td>DDD</td>

<td>FFF</td>

</tr>

<tr>

<td>GGG</td>

<td colspan="2">HHH</td>

</tr>

</table>

HTML/CSS Example:

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | FFF |
| GGG | HHH |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
