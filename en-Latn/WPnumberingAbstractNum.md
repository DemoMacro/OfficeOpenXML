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

# Wordprocessing Numbering, Levels & Lists

Defining an Overall Numbering Scheme

The core definition of a numbering or leveling scheme is defining in an <w:abstractNum> element within the root <w:numbering> element of the numbering part (numbering.xml).

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="099A081C"/>

<w:multiLevelType w:val="multilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFit w:val="upperRoman"/>

<w:pStyle w:val="Heading1"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="0" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="1">

<w:start w:val="1"/>

<w:numFit w:val="upperLetter"/>

<w:pStyle w:val="Heading2"/>

<w:lvlText w:val="%2."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="2">

<w:start w:val="1"/>

<w:numFit w:val="decimal"/>

<w:pStyle w:val="Heading3"/>

<w:lvlText w:val="%3."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="1440" w:firstLine="0"/>

</w:pPr>

</w:lvl>

. . .

</w:abstractNum>

The above XML defines a leveling scheme with multiple levels (w:lvl) and an outline-like appearance as shown in the example below.

Word 2007 Example:

![abstractNum Numbering Scheme for Outline](images\wp-numbering-2.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.1.

### Attributes:

There is just one attribute:

| Attribute     | Description                                                                                                                                                                                                                                             |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| abstractNumID | Specifies a unique number which will be used as the identifier for the numbering definition. The value is referenced by numbering instances (num) via the num's abstractNumId child element. <w:abstractNum w:abstractNumId="0"> . . . </w:abstractNum> |

<w:num w:numId="1"> <w:abstractNumId w:val="0"/> </w:num>

### Elements:

Below are the child elements, except for <w:tmpl> (related to where the definition can be displayed in the user interface), and nsid (related to tracking numbering definitions when documents are repurposed and changed).

| Element        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| lvl            | Specifies the properties of a particular level within the overall numbering definition. Note that a lvl can appear as part of the abstract definition (when placed within the <w:abstractNum>), or as an exception to the abstract definition (when placed within an <w:lvlOverride> of a <w:num> instance). See [Defining a Particular Level](WPnumberingLvl.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.7. |
| multiLevelType | Specifies the type of numbering defined--single level, multi-level, etc.: <w:multiLevelType w:val="multilevel"/>. This is only used by the word processing application to determine user interface behaviors and does not limit the list in any way. So, for example, a list marked as singleLevel will not be prevented from using levels 2 through 9. It has just one attribute val with the following possible values:                                              |

- singleLevel - specifies a format with only on level
- multiLevel - specifies a list of multiple levels, each of the same kind (bullets or level text)
- hybridMultiLevel - specifies a list of multiple levels, each of a potentially different kind (bullets or level text)

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.13.  
name | Specifies a name for the abstract numbering definition. It is used to provide a user-friendly alias for a definition: <w:name w:val="Example Name"/> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.14.  
numStyleLink | Specifies that the abstract numbering definition does not contain the actual numbering properties, but instead references the properties to be used by pointing to a numbering style in the styles part. A sample from a numbering part is below: <w:abstractNum w:abstractNumId="0"> <w:nsid w:val="099A081C"/> <w:multiLevelType w:val="multilevel"/> <w:numStyleLink w:val="TestNumberingStyle"/> </w:abstractNum> The corresponding style appears in the styles part as shown below: <w:style w:type="numbering" w:styleId="TestNumberingStyle"> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.22.  
styleLink | Specifies that the abstract numbering definition is the base numbering definition for the referenced numbering style in the styles part. (Since styling for the various levels of a numbering definition is specified in the abstract numbering definition via the pPr element, these styles can form the base for a numbering style in the styles part.) <w:numbering> . . . <w:abstractNum w:abstractNumId="5"> . . . <w:styleLink w:val="ExampleNumberingStyle"/> . . . </w:abstractNum> </w:numbering> The referencing style appears in the styles part as shown below: <w:styles> <w:style w:type="numbering" w:styleId="ExampleNumberingStyle"> <w:name w:val="ExampleNumberingStyle"/> . . . <w:pPr> <w:numPr> <w:numId w:val="6"/> </w:numPr> </w:pPr> </w:style> </w:styles> There is a single attribute val. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.28.

### Related HTML/CSS property:

There is no directly comparable HTML counterpart.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
