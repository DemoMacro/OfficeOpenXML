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

# Wordprocessing Numbering

Defining a Particular Level - Numbering Format

The format of the number to be used at the level is specified with the <w:numFmt w:val=" "/> element. All text in the val attribute is treated as literal text to appear in each instance, except for any use of the percent symbol (%) followed by a number. That percent-number combination represents the index of the level whose number is to be used. The index is one-based (begins with 1). So, for example, %2 indicates that the symbol/number/letter used at the second level (w:lvl w:ilvl="1") should be used.

In the example below, the first level uses Roman numerals as the numbering symbol, the second uses upper-case letters, and the third incorporates text, the previous level symbols, as well as hyphens and the symbol specified for the level (decimal number).

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperRoman"/>

<w:pStyle w:val="Heading1"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="0" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="1">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:pStyle w:val="Heading2"/>

<w:lvlText w:val="%2."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:firstLine="0"/>

</w:pPr>

</w:lvl>

<w:lvl w:ilvl="2">

<w:start w:val="1"/>

<w:numFmt w:val="decimal"/>

<w:pStyle w:val="Heading3"/>

<w:lvlText w:val="Sub %1-%2-%3. "/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="1440" w:firstLine="0"/>

</w:pPr>

</w:lvl>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.12.

Word 2007 Example:

![Numbering Level Text](images\wp-numbering-lvlText-1.gif)

---

### Attributes:

| Attribute | Description                                                     |
| --------- | --------------------------------------------------------------- |
| val       | Specifies the number format. The most commonly used values are: |

- bullet
- cardinalText - the cardinal text of the run language. (In English, One, Two, Three, etc.)
- chicago - Set of symbols from the Chicago Manual of Style. (e.g., \*, †, ‡, §)
- decimal - decimal numbering (1, 2, 3, 4, etc.)
- decimalEnclosedCircle - decimal number enclosed in a circle
- decimalEnclosedFullstop - decimal number followed by a period
- decimalEnclosedParen - decimal number enclosed in parentheses
- decimalZero - decimal number but with a zero added to numbers 1 through 9
- lowerLetter - based on the run language (e.g., a, b, c, etc.). Letters repeat for values greater than the size of the alphabet
- lowerRoman - lowercase Roman numerals (i, ii, iii, iv, etc.)
- none
- ordinalText - ordinal text of the run laguage. (In English, First, Second, Third, etc.)
- upperLetter - based on the run language (e.g., A, B, C, etc.). Letters repeat for values greater than the size of the alphabet
- upperRoman - uppercase Roman numerals (I, II, III, IV, etc.)

format | Specifies a custom format using the XSLT format attribute. For example, a value of &#x30A2 indicates that Katakana numbering should be used. ![](images/versionConflict3.png)Note: In the 2006 version of the standard, this attribute was not supported.

### Related HTML/CSS property:

There is no direct counterpart which enables the building of a level or numbering symbol from text and upper-level symbols. Each level is independent of all others.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
