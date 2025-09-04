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

# WordprocessingNumbering

Overriding a Numbering Definition

A leveling or numbering scehme is referenced within content through the numPr element, which itself refers to the num within the numbering part. The num is actually an instance of the abstract numbering scheme. This referencing of instances of abstract numbering schemes allows re-use of an abstract scheme so that variants of a single scheme can be defined without repeating the entirety of the scheme. This is the function of an overrride--it defines a variant of an already-defined scheme by simply overriding the particular properties of one or more levels of the scheme that are different. An override is specified with the <w:lvlOverride> element within the definition of a numbering instance (num) in the numbering part.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.9.

Below is the definition of an abstract numbering scheme, followed by an instance of the scheme with id=1, wich does not contain any overides. Following that instance is another instance which references the same abstract scheme but also specifies an override of the abstract definition for the first level by adding a top border to the level. Either instance could be referenced in a paragraph of content by simply referring to the desired num.

<w:numbering>

<w:abstractNum w:abstractNumId="1">

<w:nsid w:val="26152095"/>

<w:multiLevelType w:val="hybridMultilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFit w:val="decimal"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:hanging="360"/>

</w:pPr>

</w:lvl

. . .

</w:abstractNum>

<w:num w:numId="1">

<w:abstractNumId w:val="1"/>

<w:num>

<w:num w:numId="2">

<w:abstractNumId w:val="1"/>

<w:lvlOverride w:ilvl="0">

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numfit w:val="decimal"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:pBdr>

<w:top w:val="single" w:sz="24" w:space="1" w:color="FF0000"/>

</w:pBdr>

<w:ind w:start="0" w:firstLine="0"/>

</w:pPr>

</w:lvl>

</w:lvlOverride>

</w:num>

</w:numbering>

Word 2007 Example:

![Overriding a numbering definition](images\wp-numOverride-1.gif)

---

### Attributes:

There is just one attribute:

| Attribute | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| ilvl      | Specifies the numbering level of the abstract numbering scheme to be overridden. |

### Elements:

There are two element:

| Element       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| lvl           | Specifies the appearance of the numbering level definition that is being overridden. See [Defining a Particular Level](WPnumberingLvl.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.6.                                                                                                                                                                                                            |
| startOverride | Specifies the number with which the level to be overridden should begin. It is used when the level starts or restarts. It has a single attribute val, which is the number. Note that the actual format will depend on the format specified by the numFmt element. See [Numbering Format](WPnumbering-numFmt.md). E.g., <w:startOverride w:val="2"/>. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.27. |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
