![PresentationXML.com](images\PresentationMLBanner.png)

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

# DrawingML Tables

Tables in DrawingML are found mostly within presentations. The core table model is defined within the main drawingML namespace (xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main) at section 21.1 of the ECMA OOXML specification (3rd edition). As noted at the [overview of DrawingML](drwOverview.md), OOXML has three different table models--one for wordprocessing, one for spreadsheets, and one for drawingML (used mostly in presentationML documents). The drawingML table model is similar to the wordprocessing model, but it allows for the application of drawingML effects on the tables or cells.

A table is added to a presentation slide within a <p:graphicFrame> container, within the main presentationML namespace (prefix 'p'). Within the<p:graphicFrame> container is a <a:graphic> element in the drawingML namespace. And within that element is the <p:graphicData> element with its uri attribute that declares the type of data as table data: uri="http://schemas.openxmlformats.org/drawingml/2006/table".

The <p:graphicFrame> container is within the shape tree for the slide (<p:spTree>), along with other shapes and pictures found on the slide. The shape tree element is itself contained within the slide's common slide data container element <p:cSld>. See the [DrawingML Overview](drwOverview.md) and [Drawing Object Placement](drwPicInPresentation.md) for details of placement of tables. Below is a sample presentation slide with one shape and one table.

<p:sld . . . >

. . .

<p:cSld>

<p:spTree>

<p:sp>

. . .

</p:sp>

<p:graphicFrame>

. . .

<a:graphic>

<a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/table">

<a:tbl>

<. . .

</a:tbl>

</a:graphicData>

</a:graphic>

</p:graphicFrame>

</p:spTree>

</p:cSld>

. . .

</p:sld>

![DrawingML - Table](drwImages\drwTable.gif)

The table itself is defined within the <a:tbl> element, which itself contains a definition of the table structure (within a <a:tblGrid> element), table properties (within a <a:tblPr> element), and content (within one or more <a:tr> table row elements). A drawingML table can contain only text.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
