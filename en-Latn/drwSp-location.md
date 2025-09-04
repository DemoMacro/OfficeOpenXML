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

Bounding Box Location (Presentations)

The location of the bounding box of the shape within a presentation slide is specified with the <a:off> or offset element within the <a:xfrm> element, which is a child element of <p:spPr> (shape properties) element.

NOTE: The location of the bounding box within a spreadsheet is determined by its positioning within the worksheet--whether [absolute](drwPicInSpread-absolute.md), [one-cell](drwPicInSpread-OneCell.md), or [two-cell](drwPicInSpread-twoCell.md) positioning. So although there is an <a:off> element, it will have no effect on the positioning.

The <a:off> is an empty element which specifies with its attributes a coordinate for the bounding box. The coordinate along the x-axis is specified by the x attribute, and the coordinate along the y-axis is specified by the y attribute. Both are specified in either EMUS or by a number followed immediately by a unit identifier (e.g., 2in). Keep in mind the drawingML coordinate system. The origin is at the top left; the x axis increases left to right and the y axis increases top to bottom.

Below is an example of two triangle shapes within a presentation. One is lower and to the right of the other. Compare the values of the x and y attributes.

<p:sp>

. . .

<p:spPr>

<a:xfrm>

<a:off x="1676400" y="914400"/>

<a:ext cx="1219200" cy="1219200"/>

</a:xfrm>

. . .

</p:spPr>

. . .

</p:sp>

<p:sp>

. . .

<p:spPr>

<a:xfrm>

<a:off x="3276600" y="2057400"/>

<a:ext cx="1219200" cy="1219200"/>

</a:xfrm>

. . .

</p:spPr>

. . .

</p:sp>

![Shape location  with a presentation](drwImages\drwSp-location1.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
