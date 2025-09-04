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

Text - Body Properties - Columns, Vertical Text and Rotation

## Columns:

Columns for text within a shape may be specified by adding a numCols attribute on <a:bodyPr>. The value indicates the number of columns. When columns are applied, the width of the bounding box is divided by the number of columns. The columns are then treated as overflow containers--when the previous colun is filled, text flows to the next column. When all columns have been filled, the overflow properties are used. See text fit at [Shapes - Text - Fit, Wrap, Warp and 3D](drwSp-text-bodyPr-fit.md).

Below is an example of a shape with three columns (<a:bodyPr anchor="ctr" numCols="3"/>).

![Shape with text - anchoring](drwImages\drwSp-text-col1.gif)

To change the column order to a right-to-left order, add the rtlCol attribute (<a:bodyPr anchor="ctr" numCols="3" rtlCol="1" />). A value of false is assumed if this attribute is omitted.

![Shape with text - anchoring](drwImages\drwSp-text-col2.gif)

The space between columns can be specified with the spcCol attribute. The value is in EMUs. Below is the same shape as above, but with a half an inch of space between columns (<a:bodyPr anchor="ctr" numCols="3" rtlCol="1" spcCol="457200"/>).

![Shape with text - anchoring](drwImages\drwSp-text-col3.gif)

## Vertical Text:

Text within a shape may be displayed vertically by specifying the vert attribute on <a:bodyPr>. Possible values for this attribute are:

- eaVert (East Asian vertical)
- horz (horizontal--the default)
- mongolianVert (some fonts are displayed as if rotated 90 degrees while others--mostly East Asian--are displayed vertically; text flows top down, left to right)
- vert (vertical)
- vert270 (each line is 270 degrees rotated clockwise, so it goes bottom to top and each line is to the right of the previous)
- wordArtVert ("one letter on top of another")
- wordArtVertRtl (vertical WordArt should be shown from right to left rather than left to right)

Below is a shape with text displayed vertically (<a:bodyPr anchor="ctr" vert="vert"/>).

![Shape with text - anchoring](drwImages\drwSp-text-vert1.gif)

## Text Rotation:

Text within the bounding box of a shape can be rotated independently of the shape by specifying a rotation with the rot attribute on <a:bodyPr>. Values are in 60,000ths of a degree. Below is a sample shape and text, first with no rotation and then with a 45 degree rotation (<a:bodyPr anchor="ctr" rot="2700000"/>).

![Shape with text - rotation](drwImages\drwSp-text-rotate1.gif) ![Shape with text - rotation](drwImages\drwSp-text-rotate2.gif)

To show the shape and text rotating independently, below is a sample shape with a 90 degree rotation and the text with a 45 degree rotation.

<p:spPr>

<a:xfrm rot="5400000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" rot="2700000"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-rotate3.gif)

To prevent text from rotating when a shape is rotated, the text can be rotated with a negative value in the same amount as the shape rotation. Below is a shape rotated 45 degrees and the text rotated -45 degrees. The shape appears to remain fixed.

<p:spPr>

<a:xfrm rot="2700000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" rot="-2700000"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-rotate4.gif)

Note that a similar result can be achieved using the upright attribute discussed below.

## Text Upright:

Text can be specified to remain upright using the upright attribute on <a:bodyPr>. This will keep the text upright regardless of the transform applied to it or to the accompanying shape. Values are either true or false; false is the default value. Below is a the same shape as above (a 45 degree rotation has been applied), but the text is specified to remain upright.

<p:spPr>

<a:xfrm rot="2700000"/>

. . .

</a:xfrm>

. . .

</p:spPr>

. . .

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" upright="1"/>

. . .

</p:txBody>

![Shape with text - rotation](drwImages\drwSp-text-upright1.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
