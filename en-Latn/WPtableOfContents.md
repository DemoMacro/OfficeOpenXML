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

# Wordprocessing Table of Contents

A table of contents is built using the TOC field. See [Fields](WPfields.md) and [Field Instructions](WPfieldInstructions.md) for details about fields. Below is a sample of a TOC field instruction, omitting the result of the instruction. Note that the TOC field relies upon TC fields, heading levels, and specified styles to be used within the document.

<w:r>

<w:fldChar w:fldCharType="begin"/>

</w:r>

<w:r>

<w:instrText xml:space="preserve"> TOC \\\* MERGEFORMAT </w:instrText>

</w:r>

<w:r>

<w:fldChar w:fldCharType="separate"/>

</w:r>

<w:r>

. . .

</w:r>

<w:r>

<w:fldChar w:fldCharType="end"/>

</w:r>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.16.5.68.

Word 2007 Example:

![Table of Contents](images\wp-toc-1.gif)

---

### Switches:

The following are the most useful formatting switches for the TOC field.

| Switch              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \b _field argument_ | Includes entries only from a portion of the document marked by the bookmark provided as the field argument.                                                                                                                                                                                                                                                                                                                                  |
| \d _field argument_ | When used with \s, the field argument defines the separator between sequence and page numbers. The default is a hyphen (-).                                                                                                                                                                                                                                                                                                                  |
| \h _field argument_ | Makes the table of contents entries hyperlinks.                                                                                                                                                                                                                                                                                                                                                                                              |
| \n _field argument_ | Without the field argument, this omits page numbers from the table of contents. Page numbers are omitted unless a range of entry levels is specified by the field argument. A range is specified by the following format: _startLevel-endLevel_.                                                                                                                                                                                             |
| \o _field argument_ | Uses paragraphs formatted with all of the specified range of built-in heading styles. Headings in a style range are specified by the field argument using the notation specified as shown in the \n switch above. Each integer corresponds to the style with the style ID of HeadingX. For example, 1 corresponds to Heading1. If no heading range is specified, all heading levels that appear in the document are used. E.g., TOC \o "3-3" |
| \p _field argument_ | The field argument specifies a sequence of characters that separate an entry and its page number. The default is a tab with leader dots.                                                                                                                                                                                                                                                                                                     |
| \s _field argument_ | For entries numbered with a SEQ field, it adds a prefix to the page number; the prefix depends on the type of entry. The argument matches the ID of the SEQ field.                                                                                                                                                                                                                                                                           |
| \t _field argument_ | Uses paragraphs formattted with styles other than the built-in heading styles. In the field argument is a set of comma-separated doublets, each being a comma-separated set of style name and table of content level. E.g., TOC \t "Heading 1,1,Heading 2,2,Appendix 1,1,Appendix 2,2,Unnumbered Heading,1"                                                                                                                                  |
| \z                  | Hides tab leader and page numbers in Web layout view.                                                                                                                                                                                                                                                                                                                                                                                        |

### Related HTML property:

There is no HTML/CSS counterpart.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
