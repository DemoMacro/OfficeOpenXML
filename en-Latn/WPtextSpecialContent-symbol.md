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

Symbols

Symbols are specified with the w:sym element within the w:r element. A symbol is a special character that does not use any of the run fonts specified in rFonts or in the style hierarchy. The character is determined by pulling the hexadecimal value specified in the char attribute from the font specified in the font attribute.

<w:r>

<w:rPr>

<w:fonts w:ascii="Courier New" w:hAnsi="Courier New"/>

<w:rPr>

<w:t xml:space="preserve">This is Courier New text. >/w:t>

</w:r>

<w:r>

<w:rPr>

<w:fonts w:ascii="Courier New" w:hAnsi="Courier New"/>

<w:rPr>

<w:t xml:space="preserve">This is a Wingdings character >/w:t>

<w:sym w:font="Wingdings" w:char="F034"/>

</w:r>

Word 2007 Example:

![Text - Symbols](images\wp-symbols-1.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.3.30.

### Attributes:

| Attribute | Description                                                                                                                               |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| char      | Specifies the hexadecimal code for the Unicode character value of the symbol. The value can be stored in either of the following formats: |

- directly in its Unicode character value from the font glyph
- In a Unicode character value created by adding F000 to the character value, thereby shifting the value into the Unicode private use area. This is done to allow interoperability with legacy word processing formats. So, in the example above, the value of the char attribute is F034, and so we would obtain the character value by removing F000 from F034 to obtain the character at the hexadecimal value 0x34 in the Wingdings font (or 52 as a decimal value).

font | Specifies the font to be used to to format the symbol.

### Related HTML/CSS property:

Symbols may be referenced in HTML as character entities using short names (e.g., &copy;). See the [W3 recommendation regarding character references](http://www.w3.org/TR/html4/sgml/entities.md). Symbols may also be referenced with numeric character references in the form &#number (decimal form) or &#xnumber (hexadecimal form). [See the W3 recommendation](http://www.w3.org/TR/html4/charset.html#h-5.3.1).

Only Unicode characters are officially supported in HTML and only those should be used, as not all browsers will have fonts such as Wingdings. However, fonts may be specified in CSS and numeric character references made to the desired character in the desired font.

<div>This is a Wingdings character <span style="font-family:Wingdings;">&#52;</span>. You will only see this if your machine has Wingdings.</div>   
<div>This is a copyright symbol referenced using its short name: &copy;</div>   
<div>This is a trademark symbol referenced using a numeric character reference: &#8482;.</div>

CSS Example:

This is a Wingdings character 4. You will only see this if your machine has Wingdings.

This is a copyright symbol referenced using its short name: ©

This is a trademark symbol referenced using a numeric character reference: ™.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
