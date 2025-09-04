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

# Wordprocessing Hyperlinks

Bookmarks

A bookmark is a region of text that has a unique name/id and acts as a target for a link--that is, the location to which the hyperlink links. See [Hyperlinks](WPhyperlink.md). Bookmarks are a legacy word processing function and pre-date XML. They can begin and end at any location within a document and would therefore violate XML well-formedness if represented with typical XML begin and end tags. For this reason, a bookmark is not defined between begin and end tags. Instead, the beginning is defined by an empty element (bookmarkStart) and the ending is defined by an empty element (bookmarkEnd). The two tags together define a region through their common id attribute. A link to the bookmark then uses the value of the bookmark's name attribute as the value of its anchor attribute.

<w:p>

<w:r>

<w:t xml:space="preserve">This is an </w:t>

</w:r>

<w:hyperlink w:anchor="myAnchor">

<w:r>

<w:rPr>

<w:rStyle w:val="Hyperlink"/>

</w:rPr>

<w:t>internal link</w:t>

</w:r>

</w:hyperlink>

</w:p>

. . .

<w:p>

<w:r>

<w:t xml:space="preserve">This is text with a </w:t>

</w:r>

<w:bookmarkStart w:id="0" w:name="myAnchor"/>

<w:r>

<w:t>bookmark</w:t>

</w:r>

<w:bookmarkEnd w:id="0"/>

</w:p>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.13.6.

Word 2007 Example:

![Internal Link](images\wp-bookmark-1.gif)

---

### Attributes:

The bookmarkStart element has the following attributes.

| Attribute | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| id        | Specifies a unique identifier for the bookmark. The value must match the value of the corresponding id for the bookmarkEnd element.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| name      | Specifies the bookmark name. The value of this attribute should match the value of the anchor attribute for the hyperlink element.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| colFirst  | This attribute is used to define a bookmark that is within a table. If it appears, so must the colLast attribute. It is possible for a bookmark within a table to only cover cells within a certain column and row range by specifying the first row that is part of the bookmark, the first column of each row that is part of the bookmark, the last column that is part of the bookmark, and the last row that is part of the bookmark. The first row is specified by placing the beginning bookmark (bookmarkStart) in the first cell of the row. The last row is specified by placing the ending bookmark (bookmarkEnd) at the end of the row. The first column is specified with this attribute. And the last column is specified with the colLast, shown below. The attribute is a zero-based index of the columns, so the first column is represented by w:colFirst="0". For example, a table of three rows and three columns might have a bookmark applied to the first two cells in the first two rows. | ![Table Bookmark](images\wp-bookmark-2.gif) |

---

The bookmark indicated by blue shading above would be specified with the following:

<w:tbl>

<w:tr>

<w:tc

<bookmarkStart w:colFirst="0" w:colLast="1" w:id="0" w:name="tableAnchor"/>

. . .

</w:tc>

</w:tr>

<w:tr>

. . .

</tc>

<bookmarkEnd w:id="0"/>

</w:tr>

<w:tr>

. . .

</w:tr>

</w:tbl>

colLast | Specifies the zero-based index of the last column in the row which is part of the bookmark. If this attribute appears, so must the colFirst attribute. See the colFirst discussion, above.

The bookmarkEnd element has the following attributes.

| Attribute | Description                                                                                                                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| id        | Specifies a unique identifier for the bookmark. The value must match the value of the corresponding id for the bookmarkStart element. |

### Related HTML property:

<p><a href="#myAnchor">This link goes to the anchor at the Bookmarks heading above.</a></p>   
  
<div><a name="myAnchor">Bookmarks</a></div>

HTML Example:

This link goes to the anchor at the Bookmarks heading above.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
