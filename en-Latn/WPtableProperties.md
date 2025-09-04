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

Properties

Table-wide properties are specified in <tblPr>. Each property is a child element of <tblPr>, and they affect all rows and cells in the table, though they can be overridden by [table-level exception](WPtablePropertyExceptions.md), [row-level](WPtableRowProperties.md), and [cell-level properties](WPtableCellProperties.md).

<w:tblPr>

<w:tblW w:w="0" w:type="auto"/>

<w:jc w:val="end"/>

</w:tblPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.60.

The most commonly used properties are shown below:

### Elements/Properties:

| Element             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| jc                  | See [Table Alignment](WPtableAlignment.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.29.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| shd                 | See [Table Shading](WPtableShading.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.32.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| tblBorders          | See [Table Borders](WPtableBorders.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.39.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| tblCaption          | See [Table Captions](WPtableCaption.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.41.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| tblCellMar          | See [Table Cell Margins](WPtableCellMargins.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.43.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| tblCellSpacing      | See [Table Cell Spacing](WPtableCellSpacing.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.46.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| tblInd              | See [Table Indent](WPtableIndent.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.51.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| tblLayout           | See [Table Layout](WPtableLayout.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.53.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| tblLook             | See [Table Conditional Formatting](WPtblLook.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.56.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| tblOverlap          | See [Floating Tables - Overlapping Tables](WPfloatingTables.md#overlappingTables). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.57.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| tblpPr              | See [Floating Tables](WPfloatingTables.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.58.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| tblStyle            | Specifies the style ID of the table style if a table style is to be used to format the table. See [Defining a Style - Table Styles](WPstyleTableStyles.md). Table styles are applied after document default styles, so they override the defaults, but all other style types are applied after the table styles, so they override the table style. In the sample below, a table style is referenced, but there is also direct formatting applied for the table justification. <w:tblPr> <w:tblStyle w:val="TestTableStyle"/> <w:jc w:val="center"/> </w:tblPr> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.63.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| tblStyleColBandSize | This element is applicable to a <tblPr> within a table style. Tables styles can have conditional formatting which enables columns and/or rows to be "banded" by applying different formatting to alternating columns or rows. Typically every other column is formatted the same. So, for example, odd columns may have gray shading and even columns may have green shading. This element can be used to group columns so that alternating groups of columns are formatted the same way rather than every other column. For example, by setting the value of the val attribute to 3, the first three columns will be formatted the same, and the second group of three will be formatted the same, and each group of three thereafter will alternate their formatting. See [Table Styles - Conditional Formatting](WPstyleTableStylesCond.md). <w:style w:type="table" w:styleId="myTableStyle"> <w:tblPr> <w:tblStyleColBandSize w:val="3"/> <w:tblStyleRowBandSize w:val="2"/> </w:tblPr> </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.5. |
| tblStyleRowBandSize | This element is applicable to a <tblPr> within a table style. Tables styles can have conditional formatting which enables columns and/or rows to be "banded" by applying different formatting to alternating columns or rows. Typically every other row is formatted the same. So, for example, odd rows may have gray shading and even rows may have green shading. This element can be used to group rows so that alternating groups of rows are formatted the same way rather than every other row. For example, by setting the value of the val attribute to 3, the first three rows will be formatted the same, and the second group of three will be formatted the same, and each group of three thereafter will alternate their formatting. See [Table Styles - Conditional Formatting](WPstyleTableStylesCond.md). <w:style w:type="table" w:styleId="myTableStyle"> <w:tblPr> <w:tblStyleColBandSize w:val="3"/> <w:tblStyleRowBandSize w:val="2"/> </w:tblPr> </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.6.7.                      |
| tblW                | See [Table Width](WPtableWidth.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.64.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

---

# Related Open Document Format (ODF) Property:

Table row properties are specified in the <style:table-properties> element.

<style:style style:name="Table1" style:family="table">

<style:table-properties style:width="4.7in" table:align="right" fo:background-color="#e6e6e6" style:shadow="none" fo:keep-with-next="always"/>

</style:style>

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 17.15.

The <style:table-properties> element can have the following attributes:

| Attributes                                                                      | Description                                                                                                                                                                       |
| ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fo:background-color                                                             | Specifies a color for the background of the table.                                                                                                                                |
| fo:break-after                                                                  | Specifies a break after the table. Possible values are auto, column, and page.                                                                                                    |
| fo:break-before                                                                 | Specifies a break before the table. Possible values are auto, column, and page.                                                                                                   |
| fo:keep-with-next                                                               | Specifies when the row should be kept with the table. Possible values are auto and always.                                                                                        |
| fo:margin, fo:margin-bottom, fo:margin-left, fo:margin-right, and fo:margin-top | Specify a margins for the table. Possible values are a non-negative number or a percent.                                                                                          |
| style:may-break-between pages                                                   | Specifies that page break may occur inside the table. Possible values are true and false.                                                                                         |
| style:page-number                                                               | Specifies the page number that should be used for a new page when the table style specifies a master page. Possible values are auto and a positive number.                        |
| style:rel-width                                                                 | Specifies the width of the table relative to the width of the area that the table is in. Possible value is a percent.                                                             |
| style:width                                                                     | Specifies the fixed width of the table.                                                                                                                                           |
| style:shadow                                                                    | Specifies a shadow effect for the table.                                                                                                                                          |
| style:writing-mode                                                              | Specifies how the content should be written. Possible values are lr-tb, rl-tb, tb-rl, tb-lr, lr, rl, tb, and page.                                                                |
| table:align                                                                     | Specifies the horizontal alignment. Possible values are center, left, margins, and right.                                                                                         |
| table:border-model                                                              | Specifies the border model. Possible values are collapsing (when adjacent cells have different borders, the wider border appears) and separating (borders appear within the cell) |
| table:display                                                                   | Specifies whether the table should be displayed. Possible values are true and false.                                                                                              |

Note that <style:table-properties> can also contain a <style:background-image> element.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
