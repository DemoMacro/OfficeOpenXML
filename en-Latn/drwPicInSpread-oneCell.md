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

# DrawingML Pictures

Positioning within a Spreadsheet Document - One Cell Anchoring

An object can be anchored to a single cell in a spreadsheet using the <xdr:oneCellAnchor> element. The object moves with the anchor cell. The position of the anchor is specified with the child element <xdr:from>. The <xdr:from> element is defined by first specifying the column and row for the anchor; the origin is at the top left corner of the cell. The column is given with <xdr:col> element and the row with a <xdr:row> element. The contents of each of these elements is a xero-based index for the column and row.

From the top left corner of the cell any offset from the column and row may be specified. That is, the anchor does not have to be exactly at the upper left corner of the cell, but can instead fall within the cell. Any offset from the edge upper left corner of the cell is defined by specifying an offset from the column (<xdr:colOff>) and row (<xdr:rowOff>); both are in either EMUs or as a number immediately followed by a unit identifier (e.g., 2in). Keep in mind the drawingML coordinate system. The origin is at the top left; the x axis increases left to right and the y axis increases top to bottom. So a complete specification for an anchor contains both a <xdr:col> and <xdr:colOff>, and a <xdr:row> and <xdr:rowOff>. Below is an example of a starting anchor at the fourth column and fourth row, with a half-inch offset from the column and none from the row.

<xdr:wsDr . . .>

<xdr:oneCellAnchor>

<xdr:from>

<xdr:col>3</xdr:col>

<xdr:colOff>457200</xdr:colOff>

<xdr:row>3</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

<xdr:ext cx="2438400" cy="1828800"/>

<xdr:pic>

. . .

</xdr:pic>

<xdr:clientData/>

</xdr:oneCellAnchor>

</xdr:wsDr>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.24.

Word 2007 Example:

![Spreadsheet Picture - One Anchor](drwImages\drwInSpread-oneAnchor.gif)

Below is an example of how the picture follows the anchor when the cells are resized. The underlying XML is the same.

![Spreadsheet Picture - One Anchor - Resized cells](drwImages\drwInSpread-oneAnchor2.gif)

Below are the possible child elements of <xdr:oneCellAnchor>. There are no attributes (compare with <xdr:twoCellAnchor>).

### Elements:

| Element      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| clientData   | An empty element which specifies (via attributes) certain properties related to printing and selection of the drawing object. The fLocksWithSheet attribute (either true or false) determines whether to disable selection when the sheet is protected, and fPrintsWithSheet attribute (either true or false) determines whether the object is printed when the sheet is printed. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.3.                                                                                                                              |
| contentPart  | Specifies a reference to XML content in a format not defined by the ECMA-376 specification, such as MathML or SVG content. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.12.                                                                                                                                                                                                                                                                                                                                                                                    |
| cxnSp        | Specifies the properties for a connection shape, such as a line, which connects two other shapes. Not discussed here. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.13.                                                                                                                                                                                                                                                                                                                                                                                         |
| ext          | Specifies the length and width of the object as it is displayed (including any scaling) in EMUs. The element is an empty element with two attributes: the cx attribute giving the length and the cy attribute giving the width. E.g., <xdr:ext cx="2438400" cy="1828800"/>. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.14.                                                                                                                                                                                                                                   |
| from         | Specifies the starting anchor by specifying the column and row of the cell containing the anchor, and any offset from the upper left corner of the cell. The child elements are <xdr:col>, <xdr:colOff>, <xdr:row>, and <xdr:rowOff>. The column and row values are based on a zero-based index for the column and row. The offsets are given in either EMUs or as a number immediately followed by a unit identifier (e.g., 2in). The x axis increases left to right and the y axis increases top to bottom. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.15. |
| graphicFrame | Specifies a graphical object frame for a spreadsheet that contains a graphical object (e.g., chart, diagram or table). Not discussed here. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.16.                                                                                                                                                                                                                                                                                                                                                                    |
| grpSp        | Specifies a group shape. Not discussed here. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.17.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| pic          | Specifies the existence of a picture within a spreadsheet. See [Drawing - Pictures - Overview](drwPic.md). Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.25.                                                                                                                                                                                                                                                                                                                                                                                                    |
| sp           | Specifies a shape. Not discussed here. Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.5.2.29.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
