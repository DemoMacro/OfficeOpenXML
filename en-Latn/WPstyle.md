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

Defining a Style

A single style within the style part is specified with the <w:style> element. A style definition can be divided into three components: general style properties, the style type, and the formatting properties of the style.

General style properties are the set of properties which are common to all style types--things like the style name, aliases, id, etc. See [Styles - General Style Properties](WPstyleGenProps.md) for more on these.

A style can be one of four different style types:

- paragraph styles
- character styles
- numbering styles
- table styles

There are also default paragraph and character styles (defined by docDefaults), and linked styles (a grouping of a paragraph style and a character style).

<w:style w:type="paragraph" w:styleId="Heading1">

<w:name w:val="Heading 1"/>

<w:basedOn w:val="Normal"/>

<w:next w:val="Normal"/>

<w:link w:val="Heading1Char"/>

<w:uiPriority w:val="9"/>

<w:qFormat/>

<w:pPr>

<w:keepNext/>

<w:keepLines/>

<w:numPr>

<w:numId w:val="2"/>

</w:numPr>

<w:spacing w:before="480" w:after="0"/>

<w:outlineLvl w:val="0"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:b/>

<w:color w:val="365F91"/>

<w:sz w:val="28"/>

</w:rPr>

</w:style>

The above XML defines a paragraph style; it is also a linked style. The general properties are in blue. The type is in green. And the formatting properties are in orange.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.17.

### Attributes:

<w:style> has the folowing attributes.

| Attribute   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| customStyle | Specifies that the style is user-defined and is not automatically generated by the application. It can be either true (or 1) or false (or 0). If true, then the application cannot automatically change formatting associated with the style. E.g., <w:style w:type="paragraph" w:styleId="MyStyle" w:customStyle="true">.                                                                                                                                                                                                                                                                                                                                                    |
| default     | Indicates that the style is the default for the style type of the style. This style will be used when the content does not reference a style of the type. If this attribute is specified by multiple styles, then the last instance will be used. E.g., <w:style w:type="paragraph" w:default="1" w:styleId="MyStyle">.                                                                                                                                                                                                                                                                                                                                                       |
| styleId     | Specifies a unique identifier for the style. It is used throughout the document to apply styles in content, to link paragraph and character styles, and to reference parent styles for inheritance via the basedOn element. For example, the style <w:style w:type="paragraph" w:styleId="MyStyle"> will be applied to a paragraph in the document content with the following reference: <w:p> <w:pPr> <w:pStyle w:val="MyStyle"/> </w:pPr> </w:p> If multiple styles use the same styleId value, then the first instance keeps its id and all others are reassigned in any way the application chooses. (However, references to the reassigned styles will not be repaired.) |
| type        | Specifies the type of style. Possible values are:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

- character
- numbering
- paragraph
- table

### Elements:

The child elements of <w:style> are either general styple properties or formatting style properties. For details of the general style properties, see [Defining a Style - General Properties](WPstyleGenProps.md).

Formatting style properties are the properties which are not general properties common to all styles but specify the formatting of either paragraphs, characters, tables or numbered paragraphs. For details on each of these style types, see:

- [Defining a Style - Character Properties](WPstyleCharStyles.md)
- [Defining a Style - Paragraph Properties](WPstyleParStyles.md)
- [Defining a Style - Table Properties](WPstyleTableStyles.md)
- [Defining a Style - Numbering Properties](WPstyleNumStyles.md)

### Related HTML/CSS property:

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
