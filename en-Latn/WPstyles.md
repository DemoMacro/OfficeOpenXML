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

# Wordprocessing Styles

Overview

Styles are predefined sets of paragraph, character, table and numbering properties which can be applied to text. They are stored separately from the document content, which enable them to be managed independently and to be changed in a single location, as opposed to direct formatting which might appear with the content within a document. Each style requires a <w:style> definition within the styles part.

Note the difference between the use of styles and the use of direct formatting within a document. Styles are stored separately within the styles part and are referenced using a style's Id. Direct formatting appears inline with the document content. Often content will contain both a reference to a style and direct formatting intended to fill in omissions in the style or to overwrite properties of the style. The sample below contains a reference to a paragraph style, as well as direct formatting to center justify the paragraph. Both are contained with in the <w:pPr> element.

<w:p>

<w:pPr>

<w:pStyle w:val="MyStyle"/>

<w:jc w:val="center"/>

</w:pPr>

</w:p>

The referenced style may appear in the styles part as shown below. The paragraph style defines only a run property of bold for the paragraph.

<w:style w:type="paragraph" w:styleId="MyStyle">

<w:name w:val="My Paragraph Style"/>

<w:rPr>

<w:b/>

</w:rPr>

</w:style>

#### Inheritance

Styles can be built or layered upon each other, with styles inheriting properties of the styles upon which they are based. This layering is achieved by including a <w:basedOn w:val=""/> element within a style's definition and specifying a style ID for the val attribute. For example, assume we have a style with ID of Base. This style may define a font of Arial and bold. We can then create a new style called Green by including the following within the defintion for Green: <w:basedOn w:val="Base"/>. In this new style we can specify a color of green. Text with the Green style will then be in Arial, bold and green, as the style inherits the properties of the style upon which is is based. Conversely, properties of a lower level (that is, properties of styles upon which other styles are based) can be overridden by redeining the property. So the Green style might set the font to Times New Roman, thereby overriding the lower style's Arial font property.

#### Hierarchy

Styles are applied in the following order.

- Document defaults are applied first. Document defaults are defined with the <w:docDefaults> element, which is a child of <w:styles>. That is, it is at the same level as style definitions.
- Next, table styles are applied.
- Next, numbering styles are applied.
- Next, paragraph and run styles are applied as defined in paragraph styles. (A <w:pPr> can contain an <w:rPr>)
- Next, run properties are applied.
- Finally, direct formatting is applied.

#### Toggle Properties

There are a handful of properties which are considered toggle properties, including bold, display all characters as capital letters, embossing, italics, imprinting, display character outline, shadow, small caps, single strike through, and hidden text. Toggle properties are either true or false. For non-toggle properties, the property that is used is the last one to be applied. For toggle properties, things are more complicated.

If a toggle property is explicitly set in direct formatting (i.e., is not applied by referencing a style), then that value is used. If multiple instances of the toggle property appear at the same level (that is, inheritance is used and the property is applied in multiple styles in the <w:basedOn/> hierarchy), then the first value encountered is used, starting at the current style and then going back the chain of styles specified in <w:basedOn/> elements. If the toggle property appears at mulitple levels, the property is true if the value in the document defaults is true; otherwise, the value is true if the property is true for an odd number of levels.

### Style Definitions Part Elements:

The Styles Definitions part has a root element <w:styles>. See ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.18. The part contains the definition of each style (<w:style>) which can be applied to content within the document. It may also contain a definition of document defaults (<w:docDefaults>). And finally, it may define properties of styles known to the application but which are not included in the document (<w:latentStyles>).

The child elements of <w:styles> are below.

| Element      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| docDefaults  | Specifies the default set of properties which are inherited by every paragraph and run within the document. These will define the formatting unless they are overridden by other styles or by direct formatting. Note that if the docDefaults is not specified, then the application can define defaults. See [Styles - Defining Default Formatting](WPstyleDefaults.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.5.                                                                                                                                                                                                                                                               |
| style        | Specifies a set of properties which can be applied to a region of a document. See [Styles - Defining a Style](WPstyle.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.17.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| latentStyles | Latent styles refer to style definitions known to an application which have not been included in the current document. The latentStyles element provides a mechanism for storing information regarding certain behaviors of such styles without storing the actual formatting properties of the styles. Such behaviors include such things as how many latent styles must be initialized to their defaults when the document is opened, whether latent styles should be locked so that instances of the styles cannot be created, what the uiPriority should be for latent styles, etc. Latent styles are not covered in detail here. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.5. |

### Related HTML/CSS property:

Below is a style definition for a paragraph that might appear in an external stylesheet.

.myParagraphStyle {

margin:5px 5px;

border-color:#000000;

background-color:#FF6699

padding: 10px;

border-style:dotted;

border-width:2px;

}

The style is then applied as shown below.

<div class="myparagraphStyle">This is a styled paragraph.</div>

HTML/CSS Example:

This is a styled paragraph.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
