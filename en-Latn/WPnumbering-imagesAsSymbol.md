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

Picture or Image as Numbering Symbol

The appearance of a picture/drawing as the numbering symbol within a numbering definition is specified by the <w:numPicBullet> element within the root numbering element of the numbering part. The picture is referenced through its numPicBulletId attribute by the lvlPicBulletId element within the abstract numbering definition.

Below is sample xml found within the numbering part:

<w:numPicBullet w:numPicBulletId="0">

<w:drawing>

. . .

</w:drawing>

</w:numPicBullet>

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="007A7BC1"/>

<w:multiLevelType w:val="hybridMultilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="bullet"/>

<w:lvlText w:val=" "/>

<w:lvlPicBulletId w:val="0"/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="720" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Symbol" w:hAnsi="Symbol"/>

<w:color w:val="auto"/>

</w:rPr>

</w:lvl>

. . .

</w:abstractNum>

<w:num w:numId="1">

<w:abstractNumId w:val="0"/>

</w:num>

The XML in the document content does not directly reference the drawing--only the num, i.e., the instance of the abstractNum within the numbering part.

<w:p>

<w:pPr>

<w:pStyle w:val="ListParagraph"/>

<w:numPr>

<w:ilvl w:val="0"/>

<w:numID w:val="1"/>

</w:numPr>

</w:pPr>

<w:r>

<w:t>This is the first . . .

</w:r>

</w:p>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.21 and § 17.9.10.

Word 2007 Example:

![Picture or Image as bullet](images\wp-numbering-numPicBullet-1.gif)

---

### Attributes for numPicBullet:

There is just one attribute:

| Attribute      | Description                                         |
| -------------- | --------------------------------------------------- |
| numPicBulletId | Specifies the unique ID for the picture definition. |

### Child Elements of numPicBullet:

There is just element:

| Element | Description                                                                                                                     |
| ------- | ------------------------------------------------------------------------------------------------------------------------------- |
| drawing | Specifies a DrawingML object. ![](images/versionConflict3.png)Note: In the 2003 version of the standard, this element was pict. |

### Attributes for lvlPicBulletId:

There is just one attribute:

| Attribute | Description                                                                            |
| --------- | -------------------------------------------------------------------------------------- |
| val       | Specifies the unique ID for the picture definition as specified in the numPicBulletId. |

---

# Related Open Document Format (ODF) Property:

The image for a list item is specified with the <text:list-level-style-image> element for the appropriate level, as specified within the <text:list-style> applied to the list.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 16.33.

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard" style:list-style-name="L1"/>

<text:list-style style:name="L1">

<text:list-level-style-image text:level="1" xlink:href="Pictures/100002000000000C0000000CDA3C0BB5.gif" xlink:type="simple" xlink:show="embed" xlink:actuate="onLoad">

<style:list-level-properties text:list-level-position-and-space-mode="label-alignment" style:vertical-pos="middle" style:vertical-rel="line" fo:width="0.1252in" fo:height="0.1252in">

<style:list-level-label-alignment text:label-followed-by="listtab" text:list-tab-stop-position="0.5in" fo:text-indent="-0.25in" fo:margin-left="0.5in"/ >

</style:list-level-properties>

</text:list-level-style-image>

. . .

</text:list-style>

# Related HTML/CSS Property:

<ul style="list-style-image: url(images/bulletImage.gif)">

CSS Example:

- This is the first unordered list item.
- This is the second unordered list item.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
