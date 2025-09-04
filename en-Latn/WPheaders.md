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

# Wordprocessing Headers

Related Open Office/ODF Discussion

Overview

Headers can be specified for sections. See [Sections](WPsection.md). Each section can have a different header for the first page, odd pages, and even pages. Each header is specified in a Header part within the package. Each Header part is the target of an explicit relationship in the part-relationship item (document.xml.rels) for the main document part. That is, each header will be contained in a separate file within the package and the files will be referenced in document.xml.rels. The glossary can also have headers, and so the glossary may have explicit relationships for headers too.

Below are relationships in document.xml.rels for a first page header and a default header for all other pages in the section.

<Relationships xmls="...">

<Relationship Id="rId6" Type="http://.../footer" Target="header1.xml"/>

<Relationship Id="rId8" Type="http://.../footer" Target="header2.xml"/>

</Relationships>

The document references the headers with a headerReference element within the sectPr element of the section. See [Sections](WPsection.md) and [Sections - Headers](WPsectionHeaderReference.md).

<w:sectPr>

. . .

<w:headerReference r:id="rId8" w:type="first"/>

<w:headerReference r:id="rId6" w:type="default"/>

. . .

</w:sectPr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 11.3.9.

The Header part has a hdr root element which specifies the content for any header that references the Header part. The content of the hdr element is similar to that of the body element and contains block-level markup which can exist as a sibling element to paragraphs. Below is a sample header for the first page header of a section.

Below is the content of the header1.xml Header part.

<w:hdr xmlns:ve= ... >

<w:p>

<w:pPr>

<w:pStyle w:val="Header"/>

</w:pPr>

<w:r&gt

<w:t>Default Header</w:t>

</w:r&gt

</w:p>

</w:hdr>

Below is the content of the header2.xml Header part.

<w:hdr xmlns:ve= ... >

<w:p>

<w:pPr>

<w:pStyle w:val="Header"/>

</w:pPr>

<w:r&gt

<w:t>First Page Header</w:t>

</w:r&gt

</w:p>

</w:hdr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.4.

Word 2007 Example:

![Footers](images\wp-footers-1.gif)

---

### Elements:

Below are the most important of the child elements of ftr.

| Element | Description                                                                                                                                                                |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| p       | Specifies a paragraph of content. See [Paragraphs](WPparagraph.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.3.1.22. |
| tbl     | Specifies the contents of a table. See [Tables](WPtable.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.4.38.          |

---

---

# Related Open Document Format (ODF) Property:

A header in the ODF format is defined with a <style:header> element within a <style:master-page> element of the styles part. A <style:header> can contain a <table:table>, a <text:h>, a <text:list>, a <text:p>, a <text:section>, or a <text:table-of-content>, among other elements. Note that there is also a <style:header-left> element that can also be within a <style:master-page> if content for the header for the left page is different from the right.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 16.10.

<office:master-styles>

<style:master-page style:name="Standard" style:page-layout-name="Mpm1">

<style:header>

<text:p text:style-name="Header">My sample document header</text:p>

</style:header>

<style:footer>

<text:p text:style-name="Footer">My sample document footer</text:p>

</style:footer>

</style:master-page>

</office:master-styles>

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
