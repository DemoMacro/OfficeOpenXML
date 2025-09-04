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

External Links

Links are specified with the <w:hyperlink> element. Links to locations external to the document and links to locations within the document are handled differently based upon the presence or not of the r:id attribute. If the link is to an external target, then the r:id attribute is specified, which is the ID of a relationship stored in the relationship part (document.xml.rels). That relationship has a value of External for the TargetMode attribute. A specific location within the target for the link can be specified with the docLocation attribute. See attributes below.

<w:p>

<w:r>

<w:t xml:space="preserve">This is an external link to </w:t>

</w:r>

<w:hyperlink r:id="rId4">

<w:r>

<w:rPr>

<w:rStyle w:val="Hyperlink"/>

</w:rPr>

<w:t>Google</w:t>

</w:r>

</w:hyperlink>

</w:p>

The r:id="rId4" references the following relationship within the relationships part for the document (document.xml.rels).

<Relationship Id="rId4" Type="http://. . ./hyperlink" Target="http://www.google.com/" TargetMode="External"/>

Word 2007 Example:

![External Hypertext](images\wp-hyperlink-1.gif)

---

Internal Links

An internal link is specified by including the anchor attribute with the value of a bookmark within the document.

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

Word 2007 Example:

![Internal Hypertext](images\wp-bookmark-1.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.16.22.

### Attributes:

The most commonly used attributes are:

| Attribute   | Description                                                                                                                                                                                                                                                        |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| anchor      | Specifies the name of a bookmark within the document. See [Bookmark](WPbookmark.md). If the attribute is omitted, then the default behavior is to navigate to the start of the document. If the r:id attribute is specified, then the anchor attribute is ignored. |
| docLocation | Specifies a location in the target of the hyperlink, in the case in which the link is an external link. <w:hyperlink r:id="rId9" w:docLocation="table"> <w:r> <w:t>Click Here</w:t> </w:r> </w:hyperlink>                                                          |
| history     | Specifies whether the target should be added to the list of viewed links. Possible values are true and false.                                                                                                                                                      |
| id          | Specifies the ID of the relationship in the relationships part for an external link. The relationship will contain a Target attribute which is the target of the link. If the id attribute is specified, it supersedes the anchor attribute.                       |
| tgtFrame    | Specifies a frame within the HTML frameset for the target when a frameset exists. If no frameset exists, then this attribute is ignored. Possbile values are:                                                                                                      |

- \_top - opens in the current window
- \_self - opens in the same frame as the link
- \_parent - opens in the parent of the current frame
- \_blank - opens in a new web browser window
- all other values - opens in the frame with the specified name, otherwise opens in the current frame

tooltip | Specifies a string that can be displayed as associated with the hyperlink in the user interface.

### Related HTML property:

#### External link

<p><a href="http://www.google.com">This link goes to Google.com.</a></p>

HTML Example:

[This link goes to Google.com.](http://www.google.com)

#### Internal link

<p><a href="#myAnchor">This link goes to the anchor at the Internal Links heading above.</a></p>   
  
<div><a name="myAnchor">Internal Links</a></div>

HTML Example:

This link goes to the anchor at the Internal Links heading above.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
