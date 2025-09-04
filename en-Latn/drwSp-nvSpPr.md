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

Non-Visual Properties

The <nvSpPr> element within the <sp> element specifies the non-visual properties of a shape. The actual properties are within child elements - <cNvPr> (for Id, name, title, and description and hidden) and <cNvSpPr> (locking properties and text box). Presentations also have a third child element <nvPr> (for multimedia associated with a shape and for placeholders within slide layouts and slide masters).

Note that the non-visual properties are in different namespaces, depending on the document type. The examples show the spreadsheet drawingML namespace with prefix 'xdr'. For presentations the non-visual properties are in the main presentationML namespace with prefix 'p'.

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="2" name="Rounded Rectangle 1"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

. . .

</xdr:sp>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 19.3.1.34 (presentations) and § 20.5.2.23 (spreadsheets).

## Id, Name, Title and Description

An id, name, title and description for a picture can be specified with attributes on the <cNvPr> element: <cNvPr id="222" name="Rounded Rectangle 1" title="My Shape" descr="This is the description"/>. The id is an integer and specifies a unique identifier. The name is a string. The title is a string that specifies the caption. The descr is alternative text used for assistive technologies which do not display the object. Finally, note that <cNvPr> can have child elements <hlinkClick> and <hlinkhover> for links that are not covered here.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 19.3.1.12 (presentations) and § 20.5.2.8 (spreadsheets).

## Hidden

A shape can be hidden by specifying the hidden attribute on the <cNvPr> element: <cNvPr hidden="true">. However, note that an application can have settings that allow the object to be displayed.

## Shape Resizing, Cropping, Rotating, Changing Aspect Ratio, Moving, Selecting

The locking properties of a shape are specified with the <spLocks> element within the <cNvSpPr> element. Various aspects of a shape's size can be specified with attributes on <spLocks>. If the attributes are not specified, then it is assumed that the properties can be changed. For example, to disallow changing the aspect ratio, specify the noChangeAspect attribute as true.

The following are the most useful attributes:

- noAdjustHandles (the application should not show adjust handles)
- noChangeArrowHandles (the application should not allow arrowhead changes)
- noChangeAspect
- noChangeShapeType
- noEditPoints (the application should not allow shape point changes)
- noGrp (disallow shape grouping)
- noMove
- noResize
- noRot (no rotation)
- noSelect
- noTextEdit

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 19.3.1.13 (presentations) and § 20.5.2.9 (spreadsheets).

## Text Boxes

The <cNvSpPr> element has a txBox attribute which specifies that the shape is a text box. The value is a boolean. However, it is important to note that a shape can still have text attached to it even if this attribute is not specified as true. A text box is just a specialized shape with specific properties.

## Multimedia in Presentations

Multimedia can be associated with an object using child elements of <nvPr>. The various media types specified in child elements include <audioCd>, <audioFile>, <quickTimeFile>, <videoFile>, <waveAudioFile>. The details for these media types are not covered here.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
