![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

[Home](index.md) | [WordprocessingML (docx)](anatomyofOOXML.md) | [SpreadsheetML (xlsx)](anatomyofOOXML-xlsx.md) | [PresentationML (pptx)](anatomyofOOXML-pptx.md) | [DrawingML](drwOverview.md)

- [Overview](drwOverview.md)
- Pictures
  - [Overview](drwPic.md)
  - Image Properties
    - [Image Data](drwPic-ImageData.md)
    - [Tile or Stretch Image to Fill](drwPic-tile.md)
    - [Effects](drwPic-effects.md)
  - [Non-Visual Properties](drwPic-nvPicPr.md)
  - [Shape Properties](drwSp-SpPr.md)
- Shapes
  - [Overview](drwShape.md)
  - [Non-Visual Properties](drwSp-nvSpPr.md)
  - [Visual Properties](drwSp-SpPr.md)
    - [Size of Bounding Box](drwSp-size.md)
    - [Location of Bounding Box](drwSp-location.md)
    - Geometry
      - [Preset](drwSp-prstGeom.md)
      - [Custom](drwSp-custGeom.md)
    - [Shape Fill](drwSp-shapeFill.md)
      - [Solid Fill](drwSp-SolidFill.md)
      - [Picture Fill](drwSp-PictFill.md)
      - [Gradient Fill](drwSp-GradFill.md)
      - [Pattern Fill](drwSp-PattFill.md)
      - [Group Fill](drwSp-grpFill.md)
    - [Effects](drwSp-effects.md)
    - [Outline Style](drwSp-outline.md)
    - [2D Transforms](drwSp-rotate.md)
    - 3-D
      - [Shape Properties](drwSp-3dProps.md)
      - [Scene Properties](drwSp-3dScene.md)
  - [Styles](drwSp-styles.md)
  - [Text](drwSp-text.md)
    - [Text Body Properties](drwSp-text-bodyPr.md)
      - [Positioning and Insets](drwSp-text-bodyPr-inset.md)
      - [Fit, Wrap, Warp and 3D](drwSp-text-bodyPr-fit.md)
      - [Columns, Vertical Text and Rotation](drwSp-text-bodyPr-columns.md)
    - [Paragraphs](drwSp-text-paragraph.md)
      - [Paragraph Properties](drwSp-text-paraProps.md)
        - [Bullets and Numbering](drwSp-text-paraProps-numbering.md)
        - [Spacing, Indent and Margins](drwSp-text-paraProps-margins.md)
        - [Alignment, Tabs, Other](drwSp-text-paraProps-align.md)
      - [Run Properties](drwSp-text-runProps.md)
    - [List Properties](drwSp-text-lstPr.md)
- [Connectors](drwCxnSp.md)
  - [Non-Visual Properties](drwSp-nvCxnSpPr.md)
- [Text](drwSp-textbox.md)
- Charts
- Diagrams
- [Tables](drwTable.md)
  - [Defining Structure](drwTableGrid.md)
  - [Rows, Cells, Cell Content](drwTableRowAndCell.md)
  - Cell Properties
    - [Alignment, Margins, Direction](drwTableCellProperties-alignment.md)
    - [Borders and Fill](drwTableCellProperties-bordersFills.md)
  - [Table Styles and Properties](drwTableStyles.md)
- Placement within Docs
  - [Overview](drwPicInWord.md)
  - [Inline Objects](drwPicInline.md)
  - [Floating Objects](drwPicFloating.md)
    - [Positioning](drwPicFloating-position.md)
    - [Text Wrapping](drwPicFloating-textWrap.md)
- Placement within Spreadsheets
  - [Overview](drwPicInSpread.md)
  - [Absolute Anchoring](drwPicInSpread-absolute.md)
  - [One Cell Anchoring](drwPicInSpread-oneCell.md)
  - [Two Cell Anchoring](drwPicInSpread-twoCell.md)
- [Placement within Presentations](drwPicInPresentation.md)

# DrawingML Shapes

Text - Content

The text content of a shape is contained within one or more <a:p> elements. The content model for text in a shape is similar but not identical to that of content within a wordprocessingML document. Below are the permitted elements of a <a:p>.

### Elements:

| Element    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| br         | Specifies a line break. Note that within a wordprocessingML document, breaks are contained within runs (<a:r>). However, within shapes breaks are contained directly within the paragraph element. Breaks within shapes can have run properties specified by a <a:rPr> element. If text is later inserted where the break is, a new run can be generated with the specified formatting. See [Shapes - Text - Run Properties](drwSp-text-runProps.md) for more on the <a:rPr> element. |
| endParaRPr | Specifies the text run properties that are to be used if another run is inserted after the last run. If it is not specified, then the application can determine the properties to apply. See [Shapes - Text - Run Properties](drwSp-text-runProps.md) for the details.                                                                                                                                                                                                                |
| r          | Specifies a run of content within the paragraph. It is the lowest level of text separator that can have properties. If no properties are specified, then the properties specified in the default run properties element (<a:defRPr>) are used. A run can have run properties and text elements (<a:t>). See [Shapes - Text - Run Properties](drwSp-text-runProps.md) for details on run properties.                                                                                   |
| pPr        | Specifies a set of properties for the paragraph. See [Shapes - Text - Paragraph Properties](drwSp-text-paraProps.md). Note that if no properties are specified, then the default properties specified in the <a:defPPr> element are used. See Shapes - Text - List Styles for more on default paragraph properties.                                                                                                                                                                   |
| fld        | Specifies a text field which contains generated text that the application updates periodically. The types of text are limited to dates and times or slide numbers. An id attribute for the fld element is generated by the application. A type attribute specifies the type of text. The reserved values are:                                                                                                                                                                         |

- slidenum
- datetime (the default date time format for the application)
- datetime1 (MM/DD/YYYY)
- datetime2 (Day, Month DD YYYY)
- datetime3 (MM/DD/YYYY)
- datetime4 (MM/DD/YYYY)
- datetime5 (MM/DD/YYYY)
- datetime6 (MM/DD/YYYY)
- datetime7 (MM/DD/YYYY)
- datetime8 (MM/DD/YYYY)
- datetime9 (MM/DD/YYYY)
- datetime10 (MM/DD/YYYY)
- datetime11 (MM/DD/YYYY)
- datetime12 (MM/DD/YYYY)
- datetime13 (MM/DD/YYYY)

The <a:fld> element can contain text (<a:t>) as well as paragraph and run property elements. See [Shapes - Text - Paragraph Properties](drwSp-text-paraProps.md) and [Shapes - Text - Run Properties](drwSp-text-runProps.md) for details. Below is a sample shape with a date field. <p:txBody> <a:bodyPr rtlCol="0" anchor="ctr"/> <a:lstStyle/> <a:p> <a:pPr algn="ctr"/> <a:r> <a:rPr . . . > . . . </a:rPr> <a:t>The time is </a:t> </a:r> <a:fld id="8DE09930-A1F0-4970-A755-490F150ACA4" type="datetime4"> <a:rPr lang="en-US" smtClean="0"> . . . </a:rPr> <a:t> October 26, 2012 </a:t> </a:fld <a:endParaRPr . . .> . . . </a:endParaRPr> </a:p> </p:txBody> ![Shape with text - rotation](drwImages\drwSp-text-field.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
