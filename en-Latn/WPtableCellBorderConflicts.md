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

Table Border Conflicts

When a table or a table row (table-level exception) specifies a border and individual cells also specify borders, there is a possiblity for conflict. The OOXML specification specifies how such conflicts are to be resolved.

Note first that if [cell spacing](WPtableCellSpacing.md) is non-zero, then both the cell border and the table border can be displayed without conflict.

Word 2007 Example:

![Sample table cell border conflicts](images\wp-tableCellBorderConflicts-1.gif)

---

### Conflicts between cell borders and table and table-level exception borders

If the cell spacing is zero, then there is a conflict. The following rules apply as between cell borders and table and table-level exception (row) borders:

- If there is a cell border, then the cell border is displayed.
- If there is no cell border but there is a table-level exception border on the row, then that table-level exception border is displayed.
- If there is no cell or table-level exception border, then the table border is displayed.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.40.

### Conflicts between adjacent cells

Conflicts between borders of adjacent cells are resolved by first assigning weights to each according to their style; the cell border with the greatest weight prevails. If the weights are equal, then the borders are compared by brightness values; the border with the the smaller brightness value wins. If brightness factors are equal, then the first border in reading order is displayed.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.67.

### Related CSS property:

If borders are not collapsed and there is sufficient spacing between cells, there is no conflict between borders. (Note that HTML rows cannot have borders--only tables and cells.)

<table style="width: 100%; height:50px; border-collapse:separate; border:2px dashed #0000FF; border-spacing:10px; empty-cells:show;">   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">AAA</td>   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">BBB</td>   
. . . </tr>   
. . .   
</table>

CSS Example:

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

<table style="width: 100%; height:50px; border-collapse:collapse; border:2px dashed #0000FF;">   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">AAA</td>   
<tr><td>style="border-bottom:1px double #FF00FF; border-top:1px double #FF00FF; border-left:2px solid #FF0000; border-right:2px solid #FF0000;">BBB</td>   
. . .   
</table>

CSS Example:

| AAA | BBB | CCC |
| --- | --- | --- |
| EEE | FFF | DDD |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
