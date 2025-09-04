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

Table Cell Properties - Margins

Margins for a single table cell are specified with the <w:tcMar> element within the <tcPr> element. This overrides the [table-level cell margins](WPtableCellMargins.md), if present.

<w:tblStyle>

<w:tblCellMar>

<w:top w:w="0" w:type="dxa"/>

<w:start w:w="0" w:type="dxa"/>

<w:bottom w:w="0" w:type="dxa"/>

<w:end w:w="0" w:type="dxa"/>

</w:tblCellMar>

</w:tblStyle>

. . .

<w:tcPr>

<w:tcMar>

<w:top w:w="720" w:type="dxa"/>

<w:start w:w="720" w:type="dxa"/>

<w:bottom w:w="0" w:type="dxa"/>

<w:end w:w="720" w:type="dxa"/>

</w:tcMar>

</w:tcPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.69.

Word 2007 Example:

Default table cell margins are set to zero. The B cell below is set as specified above:

![Table Cell Properties - Margins](images\wp-tblCellProperties-Mar-1.gif)

---

### Elements:

| Element | Description                                                                                                                                                                                                                                                                                                                                                                                     |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| top     | Specifies the amount of space between the top of the cell contents and the top border. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.78.                                                                                                                                                                                                     |
| bottom  | Specifies the amount of space displayed between the bottom of the cell content and the bottom border. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.2.                                                                                                                                                                                       |
| start   | Specifies the amount of space between the left end of the cell contents and left border for left-to-right tables (between the right end and right border for right-to-left tables). ![](images/versionConflict3.png)Note: In the previous version of the standard, this element was left. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.36.  |
| end     | Specifies the amount of space between the right end of the cell contents and right border for left-to-right tables (between the left end and left border for right-to-left tables). ![](images/versionConflict3.png)Note: In the previous version of the standard, this element was right. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.10. |

### Attributes:

The attributes for the above table cell margin elements are:

| Attribute | Description                                                                               |
| --------- | ----------------------------------------------------------------------------------------- |
| w         | Specifies the value of the width of the margin. If omitted, the value is assumed to be 0; |
| type      | Specifies the units of the width (w) property. Possible values are:                       |

- dxa \- Specifies that the value is in twentieths of a point (1/1440 of an inch)
- nil \- Specifies a value of zero

If the attribute is omitted, its value is assumed to be dxa.

---

# Related Open Document Format (ODF) Property:

Margins within a cell can be set by adding the fo:margin, fo:margin-bottom, fo:margin-left, fo:margin-right, and fo:margin-top attributes to the <style:paragraph-properties> element for the style applied to the paragraph that contains the text within the cell. Values are either a number or a percent. So margins are not set in the <style:table-cell-properties> element, but on the style for the paragraph within the cell.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) §§ 17.6, 20.198 - 20.202.

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Table_20_Contents">

<style:paragraph-properties fo:margin-left="0.2in" fo:margin-right="0.2in" fo-text-indent="0in" style:auto-text-indent="false"/>

</style:style>

# Related HTML/CSS Property:

td {  
padding-bottom:0px;  
padding-top:25px;  
padding-left:15px;  
padding-right:10px;  
}

CSS Example:

| AAA | BBB | CCC |
| --- | --- | --- |
| DDD | EEE | FFF |
| GGG | HHH | III |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
