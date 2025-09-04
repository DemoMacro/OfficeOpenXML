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

# Wordprocessing Text

Line Breaks, Symbols, and Other Special Content

Line breaks, carriage returns, tabs, special characters and other special content may appear as elements within text runs (<w:r> </w:r>) rather than within text elements (<t> </t>).

### Elements:

| Element | Description                                                                                                                                                                                                                                                       |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| br      | See [Breaks](WPtextSpecialContent-break.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.1.                                                                                                                |
| cr      | Specifies that a carriage return (Unicode character 000D) should be inserted. It is equivalent to a break with null type and clear attributes (<w:br/>). <w:r><w:t>This is another</w:t></w:r><w:r><w:br/><w:t xml:space="preserve"> simple sentence.</w:t></w:r> |

| ![Carriage Return](images\wp-carriageReturn.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.4.

sym | See [Symbols](WPtextSpecialContent-symbol.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.30.  
tab | A tab character is inserted with the tab element: <w:tab/>. The tab will advance to the nearest multiple of the defaultTabStop element (within settings.xml) width value unless there is a custom tab stop further along, in which case it will advance to that custom tab. Custom tab stops are defined using the tabs element. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.32.  
noBreakHyphen | A non-breaking hyphen may be added so that the line will not break at the hyphen as it might if a hyphen-minus character (U+00D2) were used. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.18. <w:r> <w:t>Each citizen has a unique social security number of the form "999</w:t> </w:r> <w:r> <w:noBreakHyphen/> </w:r> <w:r> <w:t>99</w:t> </w:r> <w:r> <w:noBreakHyphen/> </w:r> <w:r> <w:t>9999."</w:t> </w:r>  
Word 2007 Example: | ![No break hyphen](images\wp-nobreakHyphen-1.gif)

---

softHyphen | An optional hyphen character may be added which may appear as a regular hyphen when needed to break the line, but which otherwise has a width of zero. It is typically used to mark locations where a word can be hyphenated without causing the hyphen to be displayed unnecessarily. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.29. <w:r> <w:t>This sentence needs to be just long enough so as to cause some sort of line break</w:t> </w:r> <w:r> <w:softHyphen/> </w:r> <w:r> <w:t>ing.</w:t> </w:r>  
Word 2007 Example: | ![soft hyphen](images\wp-softHyphen-1.gif)

---

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
