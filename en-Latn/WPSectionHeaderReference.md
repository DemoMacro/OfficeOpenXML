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

# Wordprocessing Sections

Headers

The header for a section is specified with the <w:headerReference> element. The header is referenced via the id attribute. Below is a sample reference to a header for a section.

<w:sectPr>

. . .

<w:headerReference r:id="rId3" w:type="first"/>

<w:headerReference r:id="rId5" w:type="default"/>

<w:headerReference r:id="rId2" w:type="even"/>

. . .

</w:sectPr>

These references point to relationships in the document.xml.rels, which in turn point to the headers:

<Relationships xmlns="http://schemas.openxmlformats.org/package/2006/relationships">

<Relationship Id="rId2" type="http://purl.oclc.org/ooxml/officeDocument/relationships/header" target="header1.xml"/>

<Relationship Id="rId3" type="http://purl.oclc.org/ooxml/officeDocument/relationships/header" target="header2.xml"/>

<Relationship Id="rId5" type="http://purl.oclc.org/ooxml/officeDocument/relationships/header" target="header3.xml"/>

</Relationships>

For each section there can be up to three types of headers: first page header, odd page header, and even page header. The type is specified via the type attribute.

### Attributes

| Attribute | Description                                                   |
| --------- | ------------------------------------------------------------- |
| id        | Specifies the relationship ID to the appropriate header part. |
| type      | Specifies the type of header. Possible values are:            |

- default - the header should be applied to every page of the section that is not overridden by a first or even type.
- even - the header should be applied to every even page of the section (counting from the first page, not the section numbering). The actual appearance is dependent upon the setting of the evenAndOddHeaders element in settings.
- first - the header should be applied to the first page of the section. The actual appearance is dependent upon the setting of the titlePg element in sectPr.

If any of the above three types of headers is omitted, then the following rules apply.

- If no first page header is specified, but thetitlePg element is specified in sectPr, then the first page header will inherit from the previous section. If this is the first section, then a blank header is created. If thetitlePg element is not specified, then the odd page header will be applied.
- If no header for the even pages is specified and the evenAndOddHeaders element in settings is specified, then the even page header will inherit from the previous section. If this is the first section, then a blank header is created. If theevenAndOddHeaders element is not specified, then the odd page header will be applied.
- If no header for the odd pages is specified, then the even page header will be inherited from the previous section. If this is the first section, then a blank header will be created.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.5.

### Related HTML/CSS property:

HTML has no notion of pages, and so no page headers.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
