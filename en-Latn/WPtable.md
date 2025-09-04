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

Structure

A table consists of rows and cells and is structured much like an HTML table. It is defined with the <w:tbl> element.

<w:tbl>

<w:tblPr>

<w:tblStyle w:val="TableGrid"/>

<w:tblW w:w="5000" w:type="pct"/>

</w:tblPr>

<w:tblGrid>

<w:gridCol w:w="2880"/>

<w:gridCol w:w="2880"/>

<w:gridCol w:w="2880"/>

</w:tblGrid>

<w:tr>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>AAA</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>BBB</w:t>

</w:r>

</w:p>

</w:tc>

<w:tc>

<w:tcPr>

<w:tcW w:w="2880" w:type="dxa"/>

</w:tcPr>

<w:p>

<w:r>

<w:t>CCC</w:t>

</w:r>

</w:p>

</w:tc>

</w:tr>

. . .

</w:tbl>

![](images/note.png)Note: When two adjacent tables having the same style are present together without any intervening <w:p> elements, the tables are treated as a single table.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.38.

Word 2007 Example:

![Table](images\wp-table-1.gif)

---

### Elements:

The <w:tbl> element can contain a whole host of elements, mostly related to tracking revisions and adding custom XML. The core elements are shown below.

| Element | Description                                                                                                                                                                                                                                                                                                         |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| tblGrid | Specifies the columns for the table. See Table [Table Columns](WPtableGrid.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.49.                                                                                                                                |
| tblPr   | Specifies the table-wide properties for the table. These properties can be overridden by individual table level exception, row, and cell-level properties. See Table [Table properties](WPtableProperties.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.60. |
| tr      | Specifies a table row. See Table [Table Row](WPtableRow.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.79.                                                                                                                                                   |

---

# Related Open Document Format (ODF) Property:

A table in the ODF format is specified with <table:table> element. A table consists of rows and columns. Rows are divided into cells, and columns are implied by taking all cells with the same position within the rows. A table can appear within a <office:text>, within a section, within a table cell, a header, or a footer, among others.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 9.1.2.

<table:table table:name="Table1" table:style-name="Table1">

<table:table-column table:style-name="Table1.A" table:number-columns-repeated="3"/>

<table:row>

<table:table-cell table:style-name="Table1.A1" office:value="string">

<text:p text:style-name="Table_20_Contents">AAA</text:p>

</table:table-cell>

<table:table-cell table:style-name="Table1.A1" office:value="string">

<text:p text:style-name="Table_20_Contents">BBB</text:p>

</table:table-cell>

<table:table-cell table:style-name="Table1.C1" office:value="string">

<text:p text:style-name="Table_20_Contents">CCC</text:p>

</table:table-cell>

<table:row>

. . .

</table:table>

### Attributes:

The most commonly used attributes are below.

| Attributes       | Description                                                                                     |
| ---------------- | ----------------------------------------------------------------------------------------------- |
| table:name       | Specifies a unique name.                                                                        |
| table:style-name | Specifies a table style for the table.                                                          |
| xml:id           | Specifies a unique ID and is standardized by the W3C (xml-id).                                  |
| table:protected  | Specifies whether the table is protected so the user cannot edit it. Values are true and false. |

### Elements:

The most commonly used elements are below.

| Element                      | Description                                                                                  |
| ---------------------------- | -------------------------------------------------------------------------------------------- |
| <table:table-column>         | Specifies properties for one or more adjacent columns.                                       |
| <table:table-column-group>   | Groups adjacent columns                                                                      |
| <table:table-columns>        | Contains groups of <table:table-column> elements that don't repeat when a table spans pages. |
| <table:table-header-columns> | Represents column headers.                                                                   |
| <table:table-header-rows>    | Represents row headers.                                                                      |
| <table:table-row>            | Represents a row.                                                                            |
| <table:table-row-group>      | Groups adjacent rows that do not appear as table headers.                                    |
| <table:table-rows>           | Contains groups of <table:table-row> elements that don't repeat when a table spans pages.    |
| <table:title>                | Specifies a title for the table.                                                             |

# Related HTML/CSS Property:

<table style="width:100%;">

<tr>

<td>AAA</td>

<td>BBB</td>

<td>CCC</td>

</tr>

. . .

</table>

HTML/CSS Example:

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
