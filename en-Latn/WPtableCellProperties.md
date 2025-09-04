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

Cell Properties

Cell-level properties are specified in <tcPr>. Each property is a child element of <tcPr>, and the cell properties take precedence over table and row properties.

<w:tcPr>

<w:tcMar>

<w:start w:w="1440" w:type="dxa"/>

</w:tcMar>

</w:tcPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.70.

The most commonly used properties are shown below:

### Elements/Properties:

| Element   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| gridSpan  | This element defines the number of logical columns across which the cell spans. It has a single attribute w:val. See the discussion of <w:tblGrid> at [Table Grid/Column Definition](WtableGrid.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.17.                                                                                                                                                                                                                                                                                                     |
| hideMark  | See [Hide End of Table Cell Mark](WPhideMark.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.21.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| noWrap    | This element will prevent text from wrapping in the cell under certain conditions. It is a boolean property. E.g., <w:noWrap/>. ![](images/note.png)Note: This only affects the behavior of the cell when the tblLayout for the row is set to auto. If the cell width is fixed, then noWrap specifies that the cell will not be smaller than that fixed value when other cells in the row are not at their minimum. If the cell width is set to auto or pct, then the content of the cell will not wrap. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.30. |
| shd       | See [Table Cell Properties - Shading](WPtableCellProperties-shading.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.33.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| tcBorders | See [Table Cell Properties - Borders](WPtableCellProperties-borders.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.67.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| tcFitText | Text within a cell can be contracted or expanded to fit the width of the cell using the <w:tcFitText w:val="true"/>. It has a single attribute val with boolean values of true/false. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.68.                                                                                                                                                                                                                                                                                                                    | ![Table Cell Fit Text](images\wp-tableCellFitText-1.gif) |

---

tcMar | See [Table Cell Properties - Margins](WPtableCellProperties-Margins.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.69.  
tcW | See [Table Cell Properties - Width](WPtableCellProperties-Width.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.72.  
vAlign | See [Table Cell Properties - Vertical Alignment](WPtableCellProperties-verticalAlignment.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.84.  
vMerge | This element specifies that the cell is part of a vertically merged set of cells. defines the number of logical columns across which the cell spans. It has a single attribute w:val which specifies how the cell is part of a vertically merged region. The cell can be part of an existing group of merged cells or it can start a new group of merged cells. Possible values are:

- continue \-- the current cell continues a previously existing merge group
- restart \-- the corrent cell starts a new merge group

If omitted, the value is assumed to be continue. See the discussion of <w:tblGrid> at [Table Grid/Column Definition](WtableGrid.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.85.

---

# Related Open Document Format (ODF) Property:

Table cell properties are specified in the <style:table-cell-properties> element.

<style:style style:name="Table1.B2" style:family="table-cell">

<style:table-cell-properties fo:background-color="#00ffff" fo:padding="0.0382in" fo:border-left="0.0007in solid #000000" fo:border-right="none" fo:border-top="none" fo:border-bottom="0.0007in solid #000000">

<style:background-image/>

</style:table-cell-properties>

</style:style>

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 17.18.

The <style:table-cell-properties> element can have the following attributes:

| Attributes                                                                                                                                        | Description                                                                                                                                                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fo:background-color                                                                                                                               | Specifies a color for the background of the cell.                                                                                                                                                                                                                                                     |
| fo:border, fo:border-bottom, fo:border-left, fo:border-right, fo:border-top                                                                       | Specifies a border for the cell.                                                                                                                                                                                                                                                                      |
| fo:padding, fo:padding-bottom, fo:padding-left, fo:padding-right, fo:padding-top                                                                  | Specifies padding for the cell.                                                                                                                                                                                                                                                                       |
| fo:wrap-option                                                                                                                                    | Specifies whether text is to be wrapped. Possible values are no-wrap and wrap.                                                                                                                                                                                                                        |
| style:border-line-width, style:border-line-width-bottom, style:border-line-width-left, style:border-line-width-right, style:border-line-width-top | Specifies the width of borders where the border property is double. The value is a list of three white space-separated lengths. Thie first value specifies the width of the inner line, the second specifies the distance between the two lines, and the third specifies the width of the outer line. |
| style:cell-protect                                                                                                                                | Specifies how a cell is protected. Possible values are hidden-and-protected, none, protected and formula-hidden.                                                                                                                                                                                      |
| style:shadow                                                                                                                                      | Specifies a shadow effect for the cell.                                                                                                                                                                                                                                                               |
| style:vertical-align                                                                                                                              | Specifies the vertical alignment of text. Possible values are automatic, bottom, middle, and top.                                                                                                                                                                                                     |
| style:writing-mode                                                                                                                                | Specifies how the content should be written. Possible values are lr-tb, rl-tb, tb-rl, tb-lr, lr, rl, tb, and page.                                                                                                                                                                                    |

Note that <style:table-cell-properties> can also contain a <style:background-image> element.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
