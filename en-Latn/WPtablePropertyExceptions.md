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

Table Property Exceptions

Some row properties are specified as exceptions to the table-level properties using the <tblPrEx> element. The <tblPrEx> element contains all table-level properties which are being overridden for the row. This is typically used in legacy documents or where two existing independent tables are merged, in order to prevent the appearance of the second table from being superseded by the first table.

<w:tr>

<w:tblPrEx>

<w:tblBorders>

<w:top w:val="single" w:sz="12" w:space="0" w:color="FF0000" />

<w:start w:val="single" w:sz="24" w:space="0" w:color="00FF00" />

<w:bottom w:val="single" w:sz="12" w:space="0" w:color="0000FF" />

<w:end w:val="single" w:sz="24" w:space="0" w:color="000000" />

<w:insideH w:val="single" w:sz="24" w:space="0" w:color="FFFF00" />

<w:insideV w:val="single" w:sz="24" w:space="0" w:color="FF00FF" />

</w:tblBorders>

</w:tblPrEx>

</w:tr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference §§ 17.4.61 and 17.4.82.

Word 2007 Example:

![Table Row Borders](images\wp-tblPrEx-1.gif)

---

Note that the yellow (FFFF00) <insideH> element causes the top and bottom borders of the row to be yellow rather than the red (FF0000) and blue (0000FF) of the top and bottom.

### Elements:

The most commonly used table exceptions are below:

| Element | Description                                                                                                                                                                                            |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------- |
| jc      | Specifies the alignment of the row when a table does not have the same width as the document margins: <w:jc w:val="right">. See <jc> within [table row property](WPtableRowProperties.md) for details. | ![Table Row Justification](images\wp-tblPrEx-2.gif) |

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.27.

shd | Specifies the shading for the row up to the table borders, and unlike cell shading, it includes any cell padding: <w:shd w:val="clear" w:color="auto" w:fill="EEECE1"/>. The shading consists of three components: the background color, an optional pattern, and an optional pattern color. The attributes include (theme-related attributes omitted):

- color \-- The foreground pattern color. Values are given as hex values (i.e., in RRGGBB format). No #, unlike hex values in HTML/CSS. E.g., fill="FFFF00". auto can be specified and is the default. Note that if the val specifies no shading format or is omitted, of if a theme is specified, this value is superseded.
- fill \-- The background color. Values are given as hex values (i.e., in RRGGBB format). No #, unlike hex values in HTML/CSS. E.g., fill="FFFF00". auto can be specified and is the default.
- val \-- Specifies the pattern to be used to lay the pattern color over the background color. For example, w:val="pct10" indicates that the shading style is a 10 percent foreground fill mask.

Possible values are: clear (no pattern), pct10, pct12, pct15 . . ., diagCross, diagStripe, horzCross, horzStripe, nil, thinDiagCross, solid, etc. See ECMA-376, 3rd, § 17.18.78 for a complete listing.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.31.  
tblBorders | Specifies the borders for the row. Note that if the cell spacing is non-zero, there is no border conflict and the row exception border is applied. If the cell spacing is zero, then there is a conflict. Otherwise the cell border is applied. See [Table Borders](WPtableBorders.md) for details of this element. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.4.  
tblCellMar | Specifies the cell margins for cells in the row. See [Table Cell Margins](WPtableCellMargins.md) for details of this element. | ![Table Row Cell Margins](images\wp-tblPrEx-cellMar-1.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.42.

tblCellSpacing | Specifies cell spacing for all cells in the row. It specifies the minimum amount of space after including the width of the table borders. This is superseded by the row cell spacing tblCellSpacing value. See [Table Row Properties](WPtableRowProperties.md) for details. Note that table-level cell spacing is added outside of the text margins. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.45.  
tblInd | Specifies the indentation to be added before the leading edge of the row (left edge in left-to-right tables): <w:tblInd w:w="2160" w:type="dxa"/>. The attributes are: | Attribute | Description  
---|---  
w | Specifies the value of the width of the indentation. The row will shift into the text margin by the specified amount. ![](images/versionConflict3.png)Note: The 2006 version of the OOXML standard specified val instead of w.  
type | Specifies the units of the width (w) property. Possible values are:

- dxa \- Specifies that the value is in twentieths of a point (1/1440 of an inch)
- nil \- Specifies a value of zero

If pct or auto is specified, the value is ignored.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.52.

tblLayout | Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.54.  
tblLook | Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.55.  
tblW | Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.65.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
