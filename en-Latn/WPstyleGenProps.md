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

Defining a Style - General Properties

General style properties are the properties which can be used in a style definition regardless of the style type--things like the style name, aliases, id, etc. An example of general properties are shown in blue below.

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

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.

### Child Elements of <w:style> that Are General Style Properties:

The mosr important properties are below. Some related to revision of styles and email are omitted.

| Element      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| aliases      | Specifies a set of alternate names for the style that can be used in the application's user interface, instead of the name specified in the name element, if the appropriate value is set in the stylePaneFormatFilter element within the settings part. It has a single attribute val that contains one or more names, separated by commas. <w:style w:styleId="TestStyle"> <w:name w:val="GD20Complex"/> <w:aliases w:val="Regional Growth,Complex Growth"/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.1.                                                    |
| autoRedefine | Specifies that the application should automatically modify the style when the contents of an entire paragraph with this style applied are modified. If this is set, then changes to the paragraph are stored in the style rather than as direct formatting, and all paragraphs with the style will be changed to reflect the change in the one modified paragraph. <w:style w:styleId="TestStyle"> . . . <w:autoRedefine/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.2.                                                                                        |
| basedOn      | Specifies the style upon which the current style is based--that is, the style from which the current style inherits. It is the mechanism for implementing style inheritance. The element has a single attribute val that designates the value of the styleId attribute of the style upon which the current style is based. Note that if the type of the current style must match the type of the style upon which it is based or the basedOn element will be ignored. However, if the current style is a numbering style, then the basedOn element is ignored. <w:style w:styleId="Strong"> <w:basedOn w:val="Underline"/> . . . <w:rPr> |

<w:b/> </w:rPr> </w:style> <w:style w:styleId="Underline"> <w:basedOn w:val="Emphasis"/> . . . <w:rPr>  
<w:u/> </w:rPr> </w:style> <w:style w:styleId="Emphasis"> . . . <w:rPr>  
<w:i/> </w:rPr> </w:style> The Strong style in the sample above inherits from the Underline style, which inherits from the Emphasis style. The result is that the Strong style has bold, underline (inherited from Underline), and italics (inherited from Emphasis). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.3.  
hidden | Specifies that the style should be hidden from all user interfaces. The result is that the style can be used to format content but the user cannot access it. <w:style w:styleId="TestStyle"> . . . <w:hidden/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.4.  
link | Specifies the pairing of styles to comprise a linked style. A linked style is a grouping of a paragaph style with a character style. Each style exists independently in the styles part but they are merged and applied appropriately based on whether they are applied to a run or a paragraph, and they appear as one style in the application. Note that the two must be of type paragaph and character, or the link element is ignored. There is a single attribute val which specifies the id of the corresponding character or paragraph style. <w:style w:type="paragraph" w:styleId="TestParagraphStyle"> <w:link w:val="TestCharacterStyle"/> . . . </w:style> <w:style w:type="character" w:styleId="TestCharacterStyle"> <w:link w:val="TestParagraphStyle"/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.6.  
locked | Specifies that the style cannot be applied to additional content. That is, the style can be used to style existing content that references the style, but new instances of the style cannot be applied. <w:style w:styleId="TestStyle"> . . . <w:locked/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.7.  
name | Specifies the primary name for the style, which can be used in the user interface. The name is stored in the val attribute. Note that alternate names will be used by the user interface if specified by the aliases element (and if the appropriate value is set in the stylePaneFormatFilter element within the settings part). <w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.9.  
next | Specifies the style to be automatically applied to a new paragraph created following a paragraph with the current style applied. It is typically applied to content that should appear only once, such as a heading that should have regular text following it. This only applies to paragraph styles. There is a single attribute val which specifies the id of the paragraph style to be used for the next paragraph. <w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:next w:val="AnotherParagraphStyle"/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.10.  
semiHidden | Specifies that the style should be hidden from the main user interface when the document is loaded. The meaning of "main user interface" is not specified. Note that by including the unhideWhenUsed element as shown below, the semiHidden element is removed when the document is resaved, if the style is used in the content. <w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:semiHidden/> <w:unhideWhenUsed/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.16 and § 17.7.4.20.  
uiPriority | Specifies a number which can be used to sort the set of style definitions in a user interface when the stylePaneSortMethod element is set in the settings part. There is a single val attribute which contains the priority as a numeral. <w:style w:styleId="TestStyle"> <w:name w:val="My Test Style"/> <w:uiPriority w:val="10"/> . . . </w:style> Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.7.4.19.

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
