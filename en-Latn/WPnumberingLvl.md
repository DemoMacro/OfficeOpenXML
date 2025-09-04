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

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Defining a Particular Level

A particular level within a numbering definition is specified using the <w:lvl> element. Note that it is identical to a numbering level override found within an lvlOverride, within a num. Within the <w:lvl> element are all of the properties that the level should display.

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="360" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:color w:val="31849B"/>

<w:sz w:val="28"/>

</w:rPr>

</w:lvl>

The above XML defines the properties of the first level in a numbering definition.

Word 2007 Example:

![lvl Numbering Level Definition](images\wp-numbering-3.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.7.

### Attributes:

<w:lvl> has the folowing attributes (omitting tplc, related to displaying the level in the application interface)

| Attribute | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ilvl      | Specifies the level within the numbering definition to be defined. Level numbering begins at 0 (zero). This attribute value corresponds to the value of the val attribute of the ilvl element that appears in the content that references the numbering level. See below: <w:p> <w:pPr> <w:pStyle w:val="ListParagraph"/> <w:numPr> <w:ilvl w:val="0"/> <w:numId w:val="1"/> </w:numPr> </w:pPr> <w:r> <w:t>This is the first level.</w:t> </w:r> </w:p> |
| tentative | Indicates that a numbering level was saved by the producer of the XML but was not used in the document, and so it can be redefined without changing the content of the document. Values are either true (or 1) or false (or 0).                                                                                                                                                                                                                          |

### Elements:

The child elements of <w:ilv> are below (omitting legacy used for backward compatibility).

| Element        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| isLgl          | Specifies that the format for the numbering at this level should be in the decimal format, regardless of what is specified in the numFmt element. See [Numbering - Defining a Particular Level - Displaying as Numerals Only](WPnumbering-isLgl.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.4.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| lvlJc          | Specifies justification for the numbering level's text (e.g., the bullet, number, or other symbol) relative to the text margin of the parent paragraph. See [Numbering - Defining a Particular Level - Justification](WPnumbering-lvlJc.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.16.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| lvlPicBulletId | Specifies a picture to be used as a numbering symbol for a given numbering level. See [Numbering - Defining a Particular Level - Picture or Image as Numbering Symbol](WPnumbering-imagesAsSymbol.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.9.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| lvlRestart     | Specifies when numbering should restart at this level. See [Numbering - Defining a Particular Level - Restart Numbering](WPnumbering-restart.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.11.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| lvlText        | Specifies the text content to be displayed at the level. See [Numbering - Defining a Particular Level - Numbering Level Text](WPnumberingLevelText.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.12.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| numFmt         | Specifies the numbering format to be displayed at the level. See [Numbering - Defining a Particular Level - Numbering Format](WPnumbering-numFmt.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.18.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| pPr            | Specifies the paragraph properties to be applied to the level. The properties defined within the lvl element (within the numbering part) can be overridden by paragraph properties within the paragraph itself (within the document part). See [Paragraphs - Properties](WPparagraphProperties.md) for the details of specifying paragraph properties. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.23.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| pStyle         | Specifies the name of a paragraph style to be applied to the level. It has a single attribute val which is the ID of the paragraph style defined in the styles part. Note that a pPr could reference both a numbering definition (numId) and a level (ilvl), as shown below. <w:pPr> <w:numPr> <w:ilvl w:val="0"/> <w:numId w:val="0"/> </w:numPr> </w:pPr> This would present a conflict, as the lvl in the numbering definition will have properties and the referenced paragraph style for the paragraph will have properties. <w:abstractNum w:abstractNumId="1"> <w:lvl w:ilvl="0"> <w:pPr> . . . <w:pPr> . . . </w:lvl> . . . </w:abstractNum> In this case, the level defined by the numPr is ignored, and the level as defined in the numbering definition prevails. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.24. |
| rPr            | Specifies the run properties to be applied to the numbering level's text specified in the lvlText element. ![](images/note.png)Note: Understand that this affects only the text of the number or symbol of the level and not the text within runs of the paragraph. <w:rPr> <w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/> <w:color w:val="C00000"/> <w:sz w:val="28"/> </w:rPr>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |

| ![Numbering Run Properties](images\wp-numbering-rPr.gif)

---

See [Text - Properties](WPtextFormatting.md) for the details of specifying text properties.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.25.

start | Specifies the starting value for the numbering, both for when a document starts and when numbering at the level restarts. It has one attribute val which is a decimal. The actual output depends upon the numFmt element. For example, for <w:numFmt w:val="UpperRoman"/> and <w:start w:val="2"/>, the output for the number of the first occurence of this level would be II. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.26.  
suff | Specifies the character to appear between the numbering symbol and the text of the paragraph. E.g., <w:suff w:val="space"/>. It has just one attribute val which specifies the character to follow the numbering symbol. The following values are possible. If the element is omitted, the value is assumed to be tab.

- nothing
- space
- tab

In the example below, the first level has a suff value of nothing, the second level has a value of space, and the third has a value of tab. | ![Numbering Level Content Between Numbering Symbol and Paragraph Text](images\wp-numbering-suff.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.29.

---

# Related Open Document Format (ODF) Property:

In ODF the formatting for a particular level is defined within the style for the list. The actual level is determined by the level of nesting of <text:list> elements. A <text:list> within a <text:list> is level 2, for example. The style for the list is specified within a <text:list-style> element. There are three different list style elements, depending on whether a list level is to have a list label containing the list numbering, a bullet, or an image.

For levels that have numbering labels, the style for a particular level within the <text:list-style> is specified within a <text:list-level-style-number> element. A <text:list-style> element will contain multiple <text:list-level-style-number> elements--one for each possible level.

For levels that have bullet labels, the style for a particular level is specified within a <text:list-level-style-bullet> element. For levels that have image labels, the style for a particular level is specified within a <text:list-level-style-image> element.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) §§ 16.31 (levels with bullets as labels), 16.32 (levels with numbering labels), and 16.33 (levels with image labels).

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L3"/>

<text:list-style style:name="L3">

. . .

<text:list-level-style-number text:level="2" text:style-name="Numbering_20_Symbols" style:num-prefix=" " style:num-suffix="." style:num-format="A">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="0.75in" fo:text-indent="-0.25in" fo:margin-left="0.75in"/>

</style:list-level-properties>

</text:list-level-style-number>

. . .

</text:list-style>

# Related HTML/CSS Property:

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
