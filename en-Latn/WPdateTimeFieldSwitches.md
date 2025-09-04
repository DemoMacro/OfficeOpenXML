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

Date and Time Field Formatting

Date and time field formatting switches have the following format:

\@ _switch argument_

A date and time field switch argument is made up of a series of "picture items." The most commonly used are below.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.16.4.1.

### Date and Time Field Switch Picture Items:

| Picture Item    | Description                                                                                                                                               |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| d               | Formats the day of the week or day of the month as a number without a leading zero for single-digit days.                                                 |
| dd              | Formats the day of the month as a two-digit number with a leading zero for single-digit days.                                                             |
| ddd             | Formats the day of the week in its abbreviated form according to the language specified by the lang element on the run containing the field instructions. |
| dddd            | Formats the day of the week as its full name according to the language specified by the lang element on the run containing the field instructions.        |
| M               | Formats the month as a number without a leading zero for single-digit months.                                                                             |
| MM              | Formats the month as a number with a leading zero for single-digit months.                                                                                |
| MMM             | Formats the month in its abbreviated form according to the language specified by the lang element on the run containing the field instructions.           |
| MMMM            | Formats the month as its full name according to the language specified by the lang element on the run containing the field instructions.                  |
| W               | Formats the day of the week in an abbreviated form according to the language specified by the lang element on the run containing the field instructions.  |
| yy              | Formats the year as a 2-digit number.                                                                                                                     |
| yyyy            | Formats the year as a 4-digit number.                                                                                                                     |
| hor H           | Formats the hour on a 12-hour clock without a leading zero for single-digit hours.                                                                        |
| hh              | Formats the hour on a 12-hour clock with a leading zero for single-digit hours.                                                                           |
| H               | Formats the hour on a 24-hour clock without a leading zero for single-digit hours.                                                                        |
| HH              | Formats the hour on a 24-hour clock with a leading zero for single-digit hours.                                                                           |
| m               | Formats the minutes without a leading zero for single-digit minutes.                                                                                      |
| mm              | Formats the minutes with a leading zero for single-digit minutes.                                                                                         |
| s               | Formats the seconds without a leading zero for single-digit minutes.                                                                                      |
| ss              | Formats the minutes as a two-digit number with a leading zero for single-digit seconds.                                                                   |
| am/pm or AM/PM  | Formats the uppercase 12-hour clock indicators according to the language specified by the lang element on the run containing the field instructions.      |
| Other character | Includes the specified character in the result at that position. E.g., colon (:), hyphen (-), slash (/), and space.                                       |
| 'text'          | Includes _text_ in the result.                                                                                                                            |

Below are some examples of date and time for US-English.

### Date and Time Switch Examples:

| Switch                           | Result                    |
| -------------------------------- | ------------------------- |
| DATE \@ "M/d/yyyy"               | 1/3/2006                  |
| DATE \@ "dddd, MMMM dd, yyyy"    | Tuesday, January 03, 2006 |
| DATE \@ "MMMM d, yyyy"           | January 3, 2006           |
| DATE \@ "M/d/yy"                 | 1/3/06                    |
| DATE \@ "yyyy-MM-dd"             | 2006-01-03                |
| DATE \@ "d-MMM-yy"               | 3-Jan-06                  |
| DATE \@ "M.d.yyyy"               | 1.3.2006                  |
| DATE \@ "MMM. d, yy"             | Jan. 3, 06                |
| DATE \@ "d MMMM yyyy"            | 3 January 2006            |
| DATE \@ "MMMM yy"                | January 06                |
| DATE \@ "M/d/yyyy h:mm am/pm"    | 1/3/2006 5:28 PM          |
| DATE \@ "M/d/yyyy h:mm:ss am/pm" | 1/3/2006 5:28:34 PM       |
| DATE \@ "h:mm am/pm"             | 5:28 PM                   |
| DATE \@ "h:mm am/pm"             | 5:28:34 PM                |
| DATE \@ "HH:mm"                  | 17:28                     |
| DATE \@ "'Today is 'HH:mm:ss"    | Today is 17:28:34         |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
