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

Text Spacing and Kerning

There are a handful of text properties which affect text spacing. Each is applied with child elements within the <rPr> element. Other text formatting, such as bold, size, shading, and borders, is covered in separate pages.

![](images/note.png) Note: Whitespace in XML is not always preserved. As with any XML, to preserve spaces in OOXML, the space attribute must be set to preserve: <w:t xml:space="preserve">.

### Elements:

| Element | Description                                                                                                                                                                                                                                                                                                                              |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| spacing | Specifies the amount of character pitch to be added or removed after each character. <spacing w:val="200"/>. The single attribute is val. It specifies a positive or negative measurement in twentieths of a point (equivalent to 1/1440th of an inch). Compare spacing with the w property, which stretches or expanded each character. | ![spacing (character spacing adjustment)](images\wp-text-spacing-1.gif) |

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.2.35.

w | Specifies the amount to stretch or compress each character. <w w:val="200%"/>. The single attribute is val. Note the minimum value is 1% and the maximum is 600%. Compare w with the spacing property, which expands/compresses the text by adding additional character pitch but not changing the width of the characters. | ![character expansion or compression)](images\wp-w-1.gif)

---

![](images/versionConflict3.png) Note: The 2006 version specifies that the value of the val without a percent sign (%) [<w w:val="200"/>], but the 2011 version added the percent sign (%) [<w w:val="200%"/>]. Including the percent sign causes an error in Microsoft Word 2007.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.2.43.

kern | Specifies whether font kerning should be applied to the text. Kerning is the process of adjusting the spacing between characters in a proportional font. It moves the letters closer together. It is specified with the <w:kern> element. <w:rPr> <w:kern w:val="22"/> <w:sz w:val="28"/> </w:rPr> The single attribute is val. It specifies the smallest font size which will have kerning automatically adjusted. If the font size as specified by the sz element is smaller than the value specified by the val attribute, then no kerning will be applied. The attribute value is specified in half-points (1/144 of an inch). | ![text kerning](images\wp-text-kerning-1.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.2.19.

fitText | Specifies that the content is to be resized to fit the width specified by the val attribute rather than automatically displayed based on the width of the content. The expansion or contraction is performed by increasing or decreasing the size of each character. <fitText w:id="50" w:val="1440"/>. | ![fitText](images\wp-fitText-1.gif)

---

| Attribute | Description                                                                                                                                                                                                                                                                 |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id        | Specifies an id to be used to link multiple runs containing fitText elements. This enables multiple contiguous runs to be broken apart for differences in formatting while retaining their fitText property. If the runs are not contiguous, then the attribute is ignored. |
| val       | Specifies the width that the run must fit into, in twentieths of a point.                                                                                                                                                                                                   |

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.2.14.

### Related CSS property:

<div style="letter-spacing: 10px;">Then they start and tremble,</div>   
<div style="word-spacing: 10px;"> they call us by our name, and as soon as we have recognized their voice the spell</div>   
<div> is broken. We have delivered them;</div>   
<div style="max-width:50px">they have overcome death and return to share our life.</div>

CSS Example:

Then they start and tremble,

they call us by our name, and as soon as we have recognized their voice the spell

is broken. We have delivered them;

they have overcome death and return to share our life.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
