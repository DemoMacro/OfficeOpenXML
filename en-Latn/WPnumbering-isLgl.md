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

# Wordprocessing Numbering

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Defining a Particular Level - Displaying as Numerals Only

The format of the numbering at a given level can be set to Arabic numerals by including a <w:isLgl> element in the level definition. The <w:isLgl> element specifies that the format for the numbering at this level should be in the decimal format, regardless of what is specified in the <numFmt> element. For example, below is the definition of the fourth level in a numbering definition.

<w:lvl w:ilvl="3">

<w:start w:val="1"/>

<w:numFmt w:val="lowerLetter"/>

<w:lvlText w:val="%4."/>

<w:lvlJc w:val="start"/>

<w:pStyle w:val="Heading4"/>

<w:pPr>

<w:ind w:start="2160" w:firstLine="0"/>

</w:pPr>

</w:lvl>

Word 2007 Example:

Below is how the level defined above appears (without the isLgl):

![isLgl Numbering Scheme for Outline](images\wp-numberingLvl-1.gif)

---

By adding the isLgl, we get the following:

<w:lvl w:ilvl="3">

<w:start w:val="1"/>

<w:numFmt w:val="lowerLetter"/>

<w:isLgl/>

<w:lvlText w:val="%4."/>

<w:lvlJc w:val="start"/>

<w:pStyle w:val="Heading4"/>

<w:pPr>

<w:ind w:start="2160" w:firstLine="0"/>

</w:pPr>

</w:lvl>

Word 2007 Example:

![abstractNum Numbering Scheme for Outline](images\wp-numberingLvl-2.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.4.

---

# Related Open Document Format (ODF) Property:

The format of the numbering at a given level of a list is specified by the style:num-format attribute within the <text:list-level-style-number> element for the level defined within the <text:list-style> applied to the list.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 16.32 and § 19.500.

The following sample defines the format for level 4 of the list as an Arabic number.

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L3"/>

<text:list-style style:name="L3">

. . .

<text:list-level-style-number text:level="4" style:num-suffix=")" style:num-format="1">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="1.25in" fo:text-indent="-0.25in" fo:margin-left="1.25in"/>

</style:list-level-properties>

</text:list-level-style-number>

. . .

</text:list-style>

The possible attribute values for style:num-format are 1 for Arabic number sequences, a for lowercase Latin alphabet characters, A for uppercase Latin alphabet characters, i for lowercase Roman numerals, I for uppercase Roman numerals, a string, or the empty string so that no number sequence is displayed.

# Related HTML/CSS Property:

<ol>

<li style="list-style-type:upper-roman;">This is the first level.

<ol>

<li style="list-style-type:upper-alpha;">This is the second level.

<ol>

<li style="list-style-type:decimal;">This is the third level.

<ol>

<li style="list-style-type:decimal;">This is the fourth level.</li>

</ol>

</li>

</ol>

</li>

</ol>

</li>

<li style="list-style-type:upper-roman;">This is also the first level.</li>

</ol>

HTML/CSS Example:

1. This is the first level.
1. This is the second level.
1. This is the third level.
1. This is the fourth level.
1. This is also the first level.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
