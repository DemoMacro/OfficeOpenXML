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

# Wordprocessing Paragraphs

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Indentation

Indentation is defined with the <w:ind> element.

<w:pPr>

<w:ind w:left="1440" w:right="1440" />

</w:pPr>

Values are in twentieths of a point: 1440 twips = 1 inch; 567 twips = 1 centimeter. To specify units in hundreths of a character, use attributes leftChars/endChars, rightChars/endChars, etc. Negative values are possible. See attributes below.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.1.12.

Word 2007 Example:

![Simple Indent](images\wp-ind-simpleIndent.gif)

---

### Attributes:

The most commonly used attributes are:

| Attribute  | Description                                                                                                                                                                                                                                                                      |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| left/start | Specifies the indentation to be placed at the left (for paragraphs going left to right). ![](images/versionConflict3.png)Note: The 2006 version of the OOXML standard specified left but the 2011 version specifies start. Microsoft Word 2007 does not seem to recognize start. |
| right/end  | Specifies the indentation to be placed at the right (for paragraphs going left to right). ![](images/versionConflict3.png)Note: The 2006 version of the OOXML standard specified right but the 2011 version specifies end. Microsoft Word 2007 does not recognize end.           |
| hanging    | Specifies indentation to be removed from the first line. This attribute and firstLine are mutually exclusive. This attribute controls when both are specified.                                                                                                                   |
| firstLine  | Specifies additional indentation to be applied to the first line. This attribute and hanging are mutually exclusive. This attribute is ignored if hanging is specified.                                                                                                          |

Word 2007 Example:

<w:pPr>

<w:ind w:left="1440" w:right="1440" w:hanging="1080" />

</w:pPr>

![Simple Indent](images\wp-ind-hangingIndent.gif)

---

---

# Related Open Document Format (ODF) Property:

There are two related ODF properties. First, indentation of a paragraph can be specified by setting the fo:margin, fo:margin-left, or fo:margin-right attribute on the <style:paragraph-properties> element within the style applied to the paragraph. Values can be either a length or percentage referring to the margin of the parent style.

Second, the indentation for the first line of a paragraph is specified by setting the fo:text-indent attribute on the <style:paragraph-properties> element. Values are either lengths or, if the attribute is contained in a common style, the value may be a percent that refers to the text indent of the parent style.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) §§20.198, 20.200, 20.201, and 20.218.

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard">

<style:paragraph-properties fo:margin-left="0.5in" fo:margin-right="0in" fo:text-indent="0.2402in" style:auto-text-indent="false"/>

</style:style>

---

# Related HTML/CSS Property:

margin-left: 35px;  
margin-right: 35px;  
text-indent: 15px;

CSS Example:

voice the spell is broken. We have delivered them: they have overcome death and return to share our life.

And so it is with our own past. It is a labour in vain to attempt to recapture it: all the efforts of our intellect must prove futile.

The past is hidden somewhere outside the realm, beyond the reach of intellect, in some material

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
