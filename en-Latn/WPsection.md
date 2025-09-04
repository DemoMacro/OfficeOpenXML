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

# Wordprocessing Sections

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Overview

OOXML does not define pages--only paragraphs and text. However, it does enable the storing of certain information important to page composition, such as page size, page orientation, borders and margins. It does this through the use of the section. A section is a grouping of paragraphs that have a specific set of properties used to define the pages on which the text will appear.

A section's properties are stored in a sectPr element. For all sections except the last section, the sectPr element is stored as a child element of the last paragraph in the section. For the last section, the sectPr is stored as a child element of the body element. The following sample shows two sections--the first in portrait orientation and the second in landscape.

<w:body>

<w:p>

. . .

</w:p>

<w:p>

<w:pPr>

<w:sectPr>

<w:pgSz w:w="12240" w:h="15840"/>

</w:sectPr>

</w:pPr>

</w:p>

<w:p>

. . .

</w:p>

<w:sectPr>

<w:pgSz w:w="15840" w:h="12240" w:orient="landscape"/>

</w:sectPr>

</w:body>

### Elements:

| Element         | Description                                                                                                                                                                                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| cols            | Specifies the set of columns for the section. See [Sections - Columns](WPsectionCols.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.4.                                                                                                                             |
| footerReference | Specifies a footer to be associated with the section. The footer is referenced via the id attribute. See [Sections - Footers](WPsectionFooterReference.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.2.                                                          |
| formProt        | Specifies that the content of the section cannot be edited by a user except for text contained in a form field. Note that enforcement is determined by the documentProtection element within the settings part. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.6.       |
| headerReference | Specifies a header to be associated with the section. The header is referenced via the id attribute. See [Sections - Headers](WPsectionHeaderReference.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.5.                                                          |
| lnNumType       | Specifies line numbering to be displayed before each column of text in the section -- e.g., <w:lnNumType w:countBy="3" w:start="1" w:restart="newSection"/>. See [Sections - Line Numbers](WPsectionLineNumering.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.8. |
| paperSrc        | Specifies printer-specific settings for the printer trays to be used for the first and later pages. E.g., <w:paperSrc w:first="1" w:other="1"/>. There are two attributes:                                                                                                                                                |

- first \- specifies a code that uniquely identifies the printer tray to be used for the first page. The default value of 1 indicates that the printer shall automatically select the tray.
- other \- specifies a code that uniquely identifies the printer tray to be used for all subsequent pages. The default value of 1 indicates that the printer shall automatically select the tray.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.9.  
pgBorders | Specifies the page borders for each page in the section. See [Sections - Page Borders](WPsectionBorders.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.10.  
pgMar | Specifies the page margins for each page in the section. See [Sections - Page Margins](WPsectionPgMar.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.11.  
pgNumType | Specifies the page numbering for the pages in the section. See [Sections - Page Numbers](WPSectionPgNumType.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.12.  
pgSz | Specifies the properties (size and orientation) for all pages in the section. E.g., <w:pgSz w:h="12240" w:w="15840" w:orient="landscape"/>. The important attributes are below. | Attribute | Description  
---|---  
h | Specifies the page height in twentieths of a point.  
w | Specifies the page width in twentieths of a point.  
orient | Specifies the page orientation. Possible values are landscape and portrait.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.6.13.

titlePg | Specifies whether the section should have a different header and footer for its first page. If the element is set to true (e.g., <w:titlePg/>), then the section will use a first page header; if it is false (e.g., <w:titlePg w:val="false"/>) (the default value), then the first page uses the odd page header. If the element is set to true but the first page header type is omitted, then a blank header is created. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.6.  
type | Specifies the section type. It determines how the contents of the section will be placed relative to the previous section. E.g., <w:type w:val="nextPage"/> There are five different types, corresponding to the five possible values of the val attribute.

- continuous - Begins the section on the next paragraph. Certain page-level section properties cannot be specified, as they are inherited from the previous section. If a footnote occurs of the same page as a section of this kind, the new section begins on the following page.
- evenPage - The section begins on the next even-numbered page, leaving the next odd page blank if necessary.
- nextColumn - The section begins on the following column on the page.
- nextPage - The section begins on the following page.
- oddPage - The section begins on the next odd-numbered page, leaving the next even page blank if necessary.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.22.  
vAlign | Specifies the vertical alignment for text in the section, relative to the top and bottom margins. E.g., <w:vAlign w:val="center"/>. There is a single attribute val with the following possible values:

- both - the text is vertically justified between the top and bottom margins by adding additional space to each paragraph as required
- bottom - the text is vertically aligned to the bottom margin
- center - the text is vertically aligned to the center
- top - the text is vertically aligned to the top margin

Below is an example of <w:vAlign w:val="both"/>. | ![Section Valign](images\wp-sectionValign-1.gif)

---

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.10.23.

---

---

# Related Open Document Format (ODF) Property:

A section in the ODF format is defined with the <text:section> element. It represents a named region of content in a document. A section is used to assign certain formatting to the region or to group text that is acquired from an external data source. So a section can contain regular text content or the text can be stored in another file and linked to the section. Such a link to an external source can be through either a resource identified by an XLink (<text:section-source>) or a Dynamic Data Exchange (DDE)(<text:dde-source>). Sections can also be write-protected or hidden.

Sections start and end on paragraph boundaries.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 5.4.

<text:section text:style-name="Sect1" text:name="Section2">

<text:p text:style-name="Standard"/>

</text:section>

### Attributes:

The most commonly used attributes are below.

| Attributes      | Description                                                                                                                                           |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| text:name       | Specifies a unique name.                                                                                                                              |
| text:style-name | Specifies a section family style for the section.                                                                                                     |
| xml:id          | Specifies a unique ID and is standardized by the W3C (xml-id).                                                                                        |
| text:protected  | Specifies whether the section is protected so the user cannot edit it. Values are true and false.                                                     |
| text:display    | Specifies whether the section is hidden. Values are true, none, and condition. If condition, then the condition is supplied in a condition attribute. |

### Elements:

The most commonly used elements are below.

| Element                 | Description                     |
| ----------------------- | ------------------------------- |
| table:table             | Specifies a table.              |
| text:h                  | Specifies a heading.            |
| text:list               | Specifies a list.               |
| text:numbered-paragraph | Specifies a numbered paragraph. |
| text:p                  | Specifies a paragraph.          |
| text:section            | Specifies a section.            |
| text:table-of-content   | Specifies a table of contents.  |

---

# Related HTML/CSS Property:

There is no corresponding HTML property.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
