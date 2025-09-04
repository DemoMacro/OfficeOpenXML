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

# DrawingML Connectors

Overview

A connector is just a special type of shape that is used to connect two shapes (<xdr:sp> or <p:sp>) within a spreadsheet or presentation document.

Connection shapes within spreadsheets are specified with a <xdr:cxnSp> element in the spreadsheetML drawing namespace - xmlns:xdr="http://schemas.openxmlformats.org/drawingml/2006/speadsheetDrawing". Similarly, connection shapes within presentations are specified with a <p:cxnSp> element as defined within the main presentationML namespace - xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main".

As with any shape, a connector is inserted into the package for the document using the placement method as discussed at [Placement within Spreadsheets](drwPicInSpread.md) and Placement within Presentations. In short, spreadsheets put shapes within a separate drawing part. Presentations put shapes inline with the other content for the slide, and the shapes are contained within a <p:spTree> or <p:grpSp> element. However, unlike other shapes, connectors do not have a defined position; rather, their position is defined by the shapes they connect. Once a connection is specified, it is left to the generating application to determine the exact path the connector takes.

For each of the document types, although the placement within the document varies by document type, the actual details of the connection shape itself are the same in most respects. Word processing documents implement shapes differently both with respect to placement with the document and to details of the shape. See [Shapes - Overview](drwShape.md) for more on shapes within wordprocessingML documents.

There are three basic components of a connection shape, corresponding to the three child elements. Note that unlike other shapes, connection shapes can have no text, so there is no child <txBody> element.

1. <nvCxnSpPr> \- non-visual properties for a connection shape. See [Connectors - Non-Visual Properties](drwSp-nvCxnSpPr.md).
2. <spPr> \- shape properties. See [Shapes - Shape Properties](drwSp-SpPr.md).
3. <style> \- shape styles. See [Shapes - Styles](drwSp-styles.md).

The type and style of the connector are determined mostly by two things -- (1) the specified geometry of the shape, and (2) the outline of the shape. The geometry is specified as part of the shape properties within <spPr>\--e.g., <a:prstGeom prst="bentConnector2">. See [Shapes - Preset Geometry](drwSp-prstGeom.md) for a complete list of the possible connector shape types. The outline of the shape is also specified as part of the shape properties within the <a:ln> element. The outline determines such characteristics as the size or weight of the connector, the color, and the styles of the ends. See [Shapes - Outline](drwSp-outline.md) for details of the outline properties.

Below is an example of a connector shape (in red) between two shapes within a presentation document.

<p:cxnSp>

<p:nvCxnSpPr>

<p:cNvPr id="9" name="Straight Arrow Connector 8"/>

<p:cNvCxnSpPr>

<a:stCxn id="4" idx="3"/>

<a:endCxn id="5" idx="1"/>

</p:cNvCxnSpPr/>

<p:nvPr/>

</p:nvCxnSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2514600" y="3086100"/>

<a:ext cx="1143000" cy="38100"/>

</a:xfrm>

<a:prstGeom prst="StraightConnector1">

<a:avLst/>

</a:prstGeom>

<a:ln w="57150">

<a:solidFill>

<a:srgbClr val="FF0000"/>

</a:solidFill>

<a:headEnd type="oval" w="med" len="med"/>

<a:tailEnd type="triangle" w="med" len="med"/>

</a:ln>

</p:spPr>

<p:style>

<a:lnRef idx="1">

<a:schemeClr val="accent1"/>

</a:lnRef>

<a:fillRef idx="0">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="tx1"/>

</a:fontRef>

</p:style>

</p:cxnSp>

![Connector in a presentation](drwImages\drwSp-connector.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
