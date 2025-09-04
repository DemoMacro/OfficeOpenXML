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

# Wordprocessing Fields

Instructions

A field is placed within XML as either a <w:fldSimple> (for a simple field) or within a pair of <w:fldSimple> elements (for a complex field). But the actual definition of the field type and format are specified by the instr attribute of the simple field or the <w:instrText> element or elements. The syntax of the field definitions does not follow XML standards, but instead a field is specified with a field name or key word followed by zero or more switches which affect formatting of the result. Below is a sample of a date field.

DATE \@ "M/d/yyyy h:mm am/pm"

This produces the following result sample: 1/3/2006 5:28 PM.

### Field Types

The OOXML specification divides fields into 10 functional categories:

- date and time - [DATE](WPfieldDefinitions.md#date), [CREATEDATE](WPfieldDefinitions.md#createdate), EDITTIME, PRINTDATE, [SAVEDATE](WPfieldDefinitions.md#savedate), [TIME](WPfieldDefinitions.md#time)
- document automation - COMPARE, DOCVARIABLE, GOTOBUTTON, IF, MACROBUTTON, PRINT
- document information - [AUTHOR](WPfieldDefinitions.md#author), COMMENTS, DOCPROPERTY, [FILENAME](WPfieldDefinitions.md#filename), [FILESIZE](WPfieldDefinitions.md#filesize), KEYWORDS, LASTSAVEDBY, NUMCHARS, NUMPAGES, NUMWORDS, SUBJECT, TEMPLATE, [TITLE](WPfieldDefinitions.md#title)
- equations and formulas - _=formula_ , ADVANCE, SYMBOL
- form fields - FORMCHECKBOX, FORMDROPDOWN, FORMTEXT
- index and tables - INDEX, RD (identifies a file to include when creating a table of contents, table of authorities, or an index), TA (text and page number for a table of authorities entry), TC (text and page number for a table of contents entry), [TOC](WPtableOfContents.md) (table of contents), XE (text and page number for an index entry)
- links and references - AUTOTEXT, AUTOTEXTLIST, BIBLIOGRAPHY, CITATION, HYPERLINK, INCLUDEPICTURE, INCLUDETEXT, LINK, NOTEREF, PAGEREF, QUOTE, REF, STYLEREF
- mail merge - ADDRESSBLOCK, ASK, COMPARE, DATABASE, FILLIN, GREETINGLINE, IF, MERGEFIELD, MERGEREC, MERGESEQ, NEXT, NEXTIF,SET, SKIPIF
- numbering - LISTNUM, [PAGE](WPfieldDefinitions.md#page), REVNUM, [SECTION](WPfieldDefinitions.md#section), SECTIONPAGES, [SEQ](WPfieldDefinitions.md#seq)
- user information - USERADDRESS, USERINITIALS, [USERNAME](WPfieldDefinitions.md#username)

### Field Formatting

The formatting of fields is specified with switches placed after the field name. There are three types of general switch types:

- date and time \- applicable to the fields related to date and time. The format is:

\@ _switch argument_

E.g., DATE \@ "yyyy-MM-dd". See [Date and Time Field Formatting Switches](WPdateTimeFieldSwitches.md) for details on the switches.

- numeric \- applicable to numberic results. The format is:

\\# _switch argument_

If no switch is present, the result is formatted without leading spaces or trailing fractional zeros. See [Numeric Field Formatting Switches](WPnumericFieldSwitches.md) for details.

- general formatting \- applicable to a variety of numeric or text results. The format is:

\\\* _switch argument_

See [General Formatting Field Switches](WPgeneralFieldSwitches.md) for details.

In addition, each field may have its own switches.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.16.4.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
