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

# Wordprocessing Styles

Defining a Style - Table Styles - Conditional Formatting

Table styles can define conditional formatting which is applied to different regions of the table. Conditional formatting is specified by the <w:tblStylePr> element within the <w:style> element. The regions that can have conditional formatting are shown below.

| Top left cell    | Header row | Top right cell    |
| ---------------- | ---------- | ----------------- |
| First column     | Table body | Last column       |
| Bottom left cell | Footer row | Bottom right cell |

In addition to the regions above, rows within a table can also have conditional formatting on an alternating row/column basis to achive a banded effect. For example, the sample below has banded rows and columns, with the odd rows and columns having formatting applied.

![Table Conditional Formatting](images\wp-tableCondFormatting-1.gif)

---

The actual application of each of these sets of conditional formatting in a given table that references the table style is determined by the attributes of the tblLook element within the tblPr of the table. In this way the properties are "conditional." See [Tables - Conditional Formatting](WPtblLook.md). Below is the definition of a table style within the styles part that defines non-conditional formatting, as well as conditional formatting for the first row that consists of bolding and red shading for table cells and spacing formatting for the last row.

<w:style w:type="table" w:styleId="TestTableStyle">

<w:name w:val="Test Table Style"/>

<w:basedOn w:val="TableNormal"/>

<w:tblPr>

. . .

</w:tblPr>

<w:tblStylePr w:type="firstRow">

<w:rPr>

<w:b/>

</w:rPr>

<w:tcPr>

<w:shd w:val="clear" w:color="auto" w:fill="ED1C24"/>

</w:tcPr>

</w:tblStylePr>

<w:tblStylePr w:type="lastRow">

<w:pPr>

<w:spacing w:before="0" w:after="0" w:line="240" w:lineRule="auto"/>

</w:pPr>

</w:tblStylePr>

</w:style>

![](images/note.png)Note: There may be multiple instances of <w:tblStylePr> within a table style definition - one for each conditionally formatted region.

The above table style is then applied in content as shown below. Note in particular the <w:tblLook> element. The bold and shade formatting for the first row is applied because the <w:tblLook> element contains a value of true for its firstRow attribute. The conditional formatting for the last row is not applied.

<w:tbl>

<w:tblPr>

<w:tblStyle w:val="TestTableStyle"/>

<w:tblW w:w="0" w:type="auto"/>

<w:tblLook w:firstRow="true"/>

</w:tblPr>

</w:tbl>

Note that when multiple conditional formatting sets are applied, there may be conflicts between them. The conditional formats are applied in the following order:

- Whole table
- Banded columns, even column banding
- Banded rows, even row banding
- First row, last row
- First column, last column
- Top left, top right, bottom left, bottom right

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.

### Attributes of <w:tblStylePr>

There is only one attribute, type, which determines the region to which the conditional formatting applies.

| Attribute | Description                        |
| --------- | ---------------------------------- |
| type      | The following possible values are: |

- band1Horz - The formatting applies to odd numbered groupings of rows
- band1Vert - The formatting applies to odd numbered groupings of columns
- band2Horz - The formatting applies to even numbered groupings of rows
- band2Vert - The formatting applies to even numbered groupings of columns
- firstCol - The formatting applies to the first column
- firstRow - The formatting applies to the first row
- lastCol - The formatting applies to the last column
- lastRow - The formatting applies to the last row
- neCell - The formatting applies to the top right cell
- nwCell - The formatting applies to the top left cell
- seCell - The formatting applies to the bottom right cell
- swCell - The formatting applies to the bottom left cell
- wholeTable - The formatting applies to the whole table

### Child Elements of <w:tblStylePr>:

| Element | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| pPr     | Specifies the set of paragraph properties to be applied to paragraphs in a table which match the conditional formatting type. For the details, see [Paragraphs - Properties](WPparagraphProperties.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.1.                                                                                                                                                          |
| rPr     | Specifies the set of run properties to be applied to runs in a table which match the conditional formatting type. For the details, see [Text - Formatting](WPtextFormatting.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.2.                                                                                                                                                                                 |
| tblPr   | Specifies the set of table properties to be applied to all regions of a table which match the conditional formatting type. For the details, see [Tables - Properties](WPtableProperties.md). If the conditional formatting does not consist of one or more full table rows, then table properties which can't be applied to a single cell or column are ignored. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.3. |
| tcPr    | Specifies the set of table cell properties to be applied to cells in a table which match the conditional formatting type. For the details, see [Tables - Cell Properties](WPtableCellProperties.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.8.                                                                                                                                                             |
| trPr    | Specifies the set of table row properties to be applied to rows in a table which match the conditional formatting type. For the details, see [Tables - Row Properties](WPtableRowProperties.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.10.                                                                                                                                                                |

### Related HTML/CSS property:

<ol>

<li style="list-style-type:upper-roman;">This is the first level.</li>

<li style="list-style-type:upper-alpha; margin-left:2cm;">This is the second level.</li>

<li style="list-style-type:decimal; margin-left:4cm;">This is the third level.</li>

</ol>

HTML/CSS Example:

1. This is the first level.
2. This is the second level.
3. This is the third level.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
