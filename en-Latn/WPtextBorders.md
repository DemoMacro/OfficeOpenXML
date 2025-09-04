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

# WordprocessingText

Text Borders

The border for text runs is specified with the <w:bdr> element within the <w:rPr> element. Note that the border is a complete four-sided border. Unlike a paragraph border, there is no way to specify which sides should have borders. Also note that adjacent text runs with identical attributes will be rendered as a single border.

<w:rPr>

<w:bdr w:val="single" w:sz="36" w:space="0" w:color="B8CCE4" />

</w:rPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.2.4.

Word 2007 Example:

![Text Border](images\wp-textBorder-1.gif)

---

### Attributes

The most commonly used attributes are below (theme-related attributes are omitted).

| Attributes | Description                                                                                                                                                                                                                                                                                                                                                             |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| color      | Specifies the color of the border. Values are given as hex values (in RRGGBB format). No #, unlike hex values in HTML/CSS. E.g., color="FFFF00". A value of auto is also permitted and will allow the consuming word processor to determine the color. This attribute will be ignored if a theme color is specified.                                                    |
| frame      | Specifies whether the border should be modified to create a frame effect by reversing the border's appearance from the edge nearest the text to the edge furthest from the text. Permitted values are true and false.                                                                                                                                                   |
| shadow     | Specifies whether the border should be modified to create the appearance of a shadow. For right and bottom borders, this is done by duplicating the border below and right of the normal location. For the right and top borders, this is done by moving the border down and to the right of the original location. Permitted values are true and false.                |
| space      | Specifies the spacing offset. Values are specified in points (1/72nd of an inch).                                                                                                                                                                                                                                                                                       |
| sz         | Specifies the width of the border. Text borders are line borders (see the val attribute below), and so the width is specified in eighths of a point, with a minimum value of two (1/4 of a point) and a maximum value of 96 (twelve points). (Page borders can alternatively be art borders, with the width is given in points and a minimum of 1 and a maximum of 31.) |
| val        | Specifies the style of the border. Text borders can be only line borders. (Page borders can also be art borders.) Possible values are:                                                                                                                                                                                                                                  |

- single \- a single line
- dashDotStroked \- a line with a series of alternating thin and thick strokes
- dashed \- a dashed line
- dashSmallGap \- a dashed line with small gaps
- dotDash \- a line with alternating dots and dashes
- dotDotDash \- a line with a repeating dot - dot - dash sequence
- dotted \- a dotted line
- double \- a double line
- doubleWave \- a double wavy line
- inset \- an inset set of lines
- nil \- no border
- none \- no border
- outset \- an outset set of lines
- thick \- a single line
- thickThinLargeGap \- a thick line contained within a thin line with a large-sized intermediate gap
- thickThinMediumGap \- a thick line contained within a thin line with a medium-sized intermediate gap
- thickThinSmallGap \- a thick line contained within a thin line with a small intermediate gap
- thinThickLargeGap \- a thin line contained within a thick line with a large-sized intermediate gap
- thinThickMediumGap \- a thick line contained within a thin line with a medium-sized intermediate gap
- thinThickSmallGap \- a thick line contained within a thin line with a small intermediate gap
- thinThickThinLargeGap \- a thin-thick-thin line with a large gap
- thinThickThinMediumGap \- a thin-thick-thin line with a medium gap
- thinThickThinSmallGap \- a thin-thick-thin line with a small gap
- threeDEmboss \- a three-staged gradient line, getting darker towards the paragraph
- threeDEngrave \- a three-staged gradient like, getting darker away from the paragraph
- triple \- a triple line
- wave \- a wavy line

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.18.2.

Another Word 2007 Example:

<w:rPr>

<w:bdr w:val="doubleWave" w:sz="16" w:space="36" w:color="FF6600" w:frame="true" />

</w:rPr>

![Text Border](images\wp-textBorder-2.gif)

---

### Related CSS property:

<div>Then they start and tremble, <span style="padding:5px; border-style: double; border-color:#FF6600; border-width: 2px"> they call us by our name</span>, and as soon as we have recognized their voice the spell is broken. We have delivered them.</div>

CSS Example:

Then they start and tremble, they call us by our name, and as soon as we have recognized their voice the spell is broken. We have delivered them.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
