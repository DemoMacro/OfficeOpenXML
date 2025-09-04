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

# Wordprocessing Numbering, Levels & Lists

Related Open Office/ODF Discussion  
Related HTML/CSS Discussion

Overview

Numbering or leveling refers to ways of labeling individual paragraphs with numbers, letters, and/or symbols, such as might be used in an outline format or with a simple group of bulleted items. Numbering in OOXML wordprocessing is implemented by first defining a set of rules for how a particular number scheme is to work. For example, a traditional outline format might look something like this:

I. This is the first level

A. This is the second level

1\. This is the third level.

These set of rules which will be used in the document is defined using the <w:abstractNum> element within the root numbering element of the numbering part (numbering.xml). This set of definitions is "abstract," however, and is not directly referenced in the document. Instead, instances of the abstract numbering definition are created using <w:num> elements, also within the numbering part. Those instances may follow the abstract definition exactly or may define overrides or exceptions to the abstract definition. Finally, those instances are referenced in the document content. Below is an abstract numbering definition, followed by an instance of that definition. Both appear within the numbering part.

<w:numbering>

<w:abstractNum w:abstractNumId="0">

<w:nsid w:val="099A081C"/>

<w:multiLevelType w:val="hybridMultilevel"/>

<w:lvl w:ilvl="0">

<w:start w:val="1"/>

<w:numFmt w:val="upperLetter"/>

<w:lvlText w:val="%1."/>

<w:lvlJc w:val="start"/>

<w:pPr>

<w:ind w:start="360" w:hanging="360"/>

</w:pPr>

<w:rPr>

<w:rFonts w:ascii="Arial Black" w:hAnsi="Arial Black"/>

<w:color w:val="C00000"/>

<w:sz w:val="28"/>

</w:rPr>

</w:lvl>

</w:abstractNum>

<w:num w:numId="1">

<w:abstractNumId w:val="0"/>

</w:num>

</w:numbering>

The above XML defines a leveling scheme with just one level (w:lvl w:ilvl="0"). It also creates an instance numbered 1 (w:num w:NumId="1") referencing the abstractNum without any changes or exceptions. Within the document content this instance may be referenced for a given paragraph, such as shown in the example below.

<w:p>

<w:pPr>

<w:pStyle w:val="ListParagraph"/>

<w:numPr>

<w:ilvl w:val="0"/>

<w:numId w:val="1"/>

</w:numPr>

</w:pPr>

<w:r>

<w:t>This is the first numbered paragraph.</w:t>

</w:r>

</w:p>

Note that the numbering reference within the document content in the sample above contains a direct reference to the level to be applied because the <w:numPr> contains both the reference to the numbering definition (numId) and a reference to the level (ilvl). See [Paragraph Properties](WPparagraphProperties.md) for more on <w:numPr>. The other possible way to reference a level in content is through the referenced paragraph style. That is, in the <w:abstractNum> the appropriate subsidiary level (lvl) could contain a pStyle with a value of ListParagraph. In that case, the content contains only a reference to the numbering definition instance (numId), but it also references the paragraph style. The same style will be found in the numbering definition referenced and that level will be used for the paragraph.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9 and § 17.9.1.

Word 2007 Example:

![Numbering/Levels](images/wp-numbering-1.gif)

---

### Numbering Definitions Part Elements:

The Numbering Definitions part has a root element <w:numbering>. See ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 11.3.11. The part contains the definition of each set of numbering rules used in the document, even if a particular level of a given set of rules is not actually used in the document. Note that a package can contain no more than two Numbering Definitions parts--one for the main document and one for the glossary.

The child elements of <w:numbering> are below (omitting numIdMacAtLeanup used in tracking changes).

| Element     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------- |
| abstractNum | Specifies a set of properties called an abstract numbering definition. It defines how numbered paragraphs which reference this definition through a num instance will appear (unless the num contains overrides to the abstract definition). See [Defining the Overall Numbering Scheme](WPnumberingAbstractNum.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.2.                                                                                                                                                                                                                                                                                                                                              |
| num         | Specifies a unique instance of a numbering definition (<w:abstractNum>) that can be referenced by paragraphs within the document content. Each instance references a <w:abstractNum> via its child element <w:abstractNumId>, thereby inheriting the properties of the referenced <w:abstractNum>. These inherited properties can be overridden for the instance, thereby essentially creating a new variant of the numbering definition, by including <w:lvlOverride> child elements, which override the properties of a given level in the numbering definition. See [Overriding a Numbering Definition](WPnumberingOverride.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.16. There is just one attribute: | Attribute | Description |
| ---         | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| numId       | Specifies a unique ID which any numbered paragraph in the content may reference (with the numId within a numPr within a pPr for the paragraph) if it wants to inherit the properties defined by the <w:abstractNum>.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

There are two elements:

| Element       | Description                                                                                                                                                                                                                                                                                                                                                                        |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| abstractNumId | Specifies the abstract numbering definition from which the instance will inherit its properties. It has just one attribute, val, which must have a value equal to the value of an abstractNumId attribute of an abstractNum. (See the numbers in red in the XML sample above.) Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.2. |
| lvlOverride   | Specifies an override to be applied to zero or more levels from the abstract numbering definition referenced in the abstractNumId. See [Overriding a Numbering Definition](WPnumberingOverride.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.9.                                                                            |
| numPicBullet  | Specifies the appearance of a picture to be used as a numbering symbol in a numbering definition. See [Numbering - Images as Bullets](WPnumbering-imagesAsBullets.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 17.9.21.                                                                                                        |

---

# Related Open Document Format (ODF) Property:

Bullets, lists, levels, numbered paragraphs, etc. are specified with the <text:list> element. The <text:list> element can contain a header (<text:list-header>) and one or more items (<text:list-item>). The lists may be numbered independently beginning with any number or may continue from other lists. The numbering format is determined by the list style applied to the list. As in HTML, lists may be nested, and the nesting determines the level of the list. For example, if a list is nested within another list, then the nested list is at level 2.

Reference: Open Document Format for Office Applications Version 1.2 (May, 2011) § 5.3.

<text:list xml:id="list36339527" text:style-name="L2">

<text:list-item>

<text:p text:style-name="P2">This is the top level</text:p>

<text:list

<text:list-item>

<text:p text:style-name="P2">This is the second level</text:p>

</text:list-item>

</text:list>

</text:list>

### Attributes:

| Attributes              | Description                                                                                                    |
| ----------------------- | -------------------------------------------------------------------------------------------------------------- |
| text:continue-list      | Specifies the xml:id value of a list that is to be continued.                                                  |
| text:continue-numbering | Specifies whether the numbering of the preceding list is continued or not. Possible values are true and false. |
| text:style-name         | Specifies a unique id for the list.                                                                            |
| xml:id                  | Specifies a unique id for the list.                                                                            |

### Elements:

| Element            | Description                                                                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| <text:list-header> | Specifies a header for the list, i.e., one or more paragraphs that are displayed before the list and do not have a preceding number or bullet. |
| <text:list-item>   | Specifies a nested list.                                                                                                                       |

# Related HTML/CSS Property:

<ol>

<li style="list-style-type:upper-roman;">This is the first level.

<ol>

<li style="list-style-type:upper-alpha;">This is the second level.

<ol>

<li style="list-style-type:decimal;">This is the third level.</li>

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
1. This is also the first level.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
