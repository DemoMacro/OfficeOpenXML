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

Field Definitions

| Field  | Description                                                                                                                                                                                                                                              | Switches                                                            | Examples                   |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------- |
| AUTHOR | Retrieves and optionally sets the document author's name as recorded in the Creator element of the Core File Porperties part. To update the field, add an argument. E.g., AUTHOR "Tony Danza" causes the Creator element to take the value "Tony Danza". | Use a [general field-formatting switch](WPgeneralFieldSwitches.md). | AUTHOR \\\* Caps displays: |

Henry Miller  
CREATEDATE | Retrieves the date and time at which the document was created (using the Gregorian calendar by default), as recorded in the DateCreated element of the Core File Properties part. | Use a [date and time formatting switch](WPdateTimeFieldSwitches.md). | CREATEDATE displays:  
1/4/2006 10:31:00 PM CREATEDATE \@ "dddd, MMMM dd,yyyy HH:mm:ss" displays:  
Wednesday, January 04, 2006 22:31:00  
DATE | Retrieves the current date and time (using the Gregorian calendar by default). | Use a [date and time formatting switch](WPdateTimeFieldSwitches.md). There is also a \l switch which specifies that if no date and time switch is used, then use the date and time formatting switch last used. | DATE displays:  
1/4/2006 10:31:00 PM DATE \@ "dddd, MMMM dd,yyyy HH:mm:ss" displays:  
Wednesday, January 04, 2006 22:31:00  
FILESIZE | Retrieves the size of the WordprocessingML package in bytes. | Use a [numeric formatting switch](WPnumericFieldSwitches.md) or a [general formatting switch](WPgeneralFieldSwitches.md). There is also a \k switch, which rounds to the nearest thousand bytes and a \m switch, which rounds to the nearest million bytes. | FILESIZE \\# #,##0 displays:  
4,660,736 FILESIZE \\#k displays:  
4661 FILESIZE \\#m displays:  
5  
PAGE | Retrieves the number of the current page. | Use the [general formatting switchs](WPgeneralFieldSwitches.md). | PAGE displays:  
19 PAGE \\_ ArabicDash displays:  
-19- PAGE \\# roman displays:  
xix  
SAVEDATE | Retrieves the date and time on which the document was last saved (using the Gregorian calendar by default), as recorded in the DateModified element of the Core File Properties part. For a document that has never been saved, the date and time are 0000-00-00T00:00:00 and each text component is XXX. | Use a [date and time formatting switch](WPdateTimeFieldSwitches.md). | SAVEDATE displays:  
1/6/2006 3:15:00 PM SAVEDATe \@ "dddd, MMMM dd,yyyy HH:mm:ss" displays:  
Wednesday, January 04, 2006 22:31:00 For a document that has not been saved, the same formatting options would display  
0/0/0000 0:00 AM  
and XXX, XXX 00, 0000 00:00:00  
SECTION | Retrieves the number of the current section. | Use the [general formatting switches](WPgeneralFieldSwitches.md). | SECTION displays:  
19 SECTION "My Life, the Fantasy" \\_ Upper sets the value to _My Life, the Fantasy_ and the result is  
MY LIFE THE FANTASY SECTION \\_ ArabicDash displays:  
-19- SECTION \\# roman displays:  
xix  
SEQ *identifier* *field argument* | Sequentially numbers chapters, tables, figures and other user-defined lists of items; it is similar to the LISTNUM field. The identifier is the name assigned to the items to be numbers--e.g., Figure, or Table. The field argument specifies a bookmark name that refers to an item elsewhere in the document. | Uses a [numeric formatting switch](WPnumericFieldSwitches.md) or one of the following: \c repeats the closest preceding number; \h hides the result unless a genera formatting switch is also present; \n insets the next sequence number (the default); \r *field argument* resets the sequence number to the integer specified by the field argument; and \s resets the sequence number to the built-iin heading level specified by the field argument. | SEQ Figure displays:  
Figure 1 SEQ Figure \\_ roman displays:  
Figure ii  
TIME | Retrieves the current date and time. | Use a [date and time formatting switch](WPdateTimeFieldSwitches.md). | TIME displays:  
1:59 PM TIME \@ "dddd, MMMM dd,yyyy HH:mm:ss" displays:  
Wednesday, January 04, 2006 22:31:00  
TITLE | Retrieves and optionally sets the document's title as recorded in the Title element of the Core File Properties part. Set the field by specifying a field argument. | Use a [general formatting switch](WPgeneralFieldSwitches.md). | TITLE displays:  
My Life's Story TITLE "My Life, the Fantasy" \\_ Upper sets the value to *My Life, the Fantasy* and the result is  
MY LIFE THE FANTASY  
TOC | See [Table of Contents](WPtableOfContents.md). | |  
USERNAME | Retrieves the current user's name or the name specified by a field argument. | Use a [general field-formatting switch](WPgeneralFieldSwitches.md). | USERNAME \\_ Lower displays:  
david williams USERNAME "John Jones" displays:  
John Jones USERNAME "Mary Smith" \\\* Upper displays:  
MARY SMITH

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
