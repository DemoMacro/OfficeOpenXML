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

Alignment/Justification

The alignment or justification to be applied to a paragraph is specified with the <w:jc> element.

<w:pPr>

<w:jc w:val="end"/>

</w:pPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.1.13.

Word 2007 Example:

<w:pPr>

<w:jc w:val="left"/>

</w:pPr>

<w:pPr>

<w:jc w:val="right"/>

</w:pPr>

<w:pPr>

<w:jc w:val="both"/>

</w:pPr>

![Sample paragraph alignment](images\wp-jc-1.gif)

---

### Attributes:

The most commonly used attribute values are below:

| Attribute | Description                                                               |
| --------- | ------------------------------------------------------------------------- |
| val       | Specifies the value for the paragraph justification. Possible values are: |

- start \- justification to the left margin for left-to-right documents. ![](images/versionConflict3.png)Note: In the 2003 version of the standard, this value was left.
- end \- justification to the right margin for left-to-right documents. ![](images/versionConflict3.png)Note: In the 2003 version of the standard, this value was right.
- center \- center the text.
- both \- justify text between both margins equally, but inter-character spacing is not affected.
- distribute \- justify text between both margins equally, and both inter-word and inter-character spacing are affected.

---

# Related Open Document Format (ODF) Property:

The alignment of a paragraph is specified by setting the fo:text-align attribute on the <style:paragraph-properties> element within the style applied to the paragraph. Possible values are start, end, left, right, center, and justify.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 20.216

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard">

<style:paragraph-properties fo:text-align="end"/>

</style:style>

---

# Related HTML/CSS Property:

text-align: right;  
text-align: center;  
text-align: justify;

CSS Example:

I feel that there is much to be said for the Celtic belief that the souls of those whom we have lost are held captive in some inferior being, in an animal, in a plant, in some inanimate object, and so effectively lost to us until the day (which to many never comes) when we happen to pass by the tree or to obtain possession of the object which forms their prison.

Then they start and tremble, they call us by our name, and as soon as we have recognized their voice the spell is broken. We have delivered them: they have overcome death and return to share our life. And so it is with our own past. It is a labor in vain to attempt to recapture it: all the efforts of our intellect must prove futile.

The past is hidden somewhere outside the realm, beyond the reach of intellect, in some material object (in the sensation which that material object will give us) which we do not suspect. And as for that object, it depends on chance whether we come upon it or not before we ourselves must die

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
