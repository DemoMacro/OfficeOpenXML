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

Text - Body Properties - Positioning and Insets

## Text Positioning or Anchoring:

The anchoring position of the text within a shape is specified with a anchor attribute on <a:bodyPr>. Possible values are:

- b (bottom of the bounding box)
- ctr (middle of the bounding box)
- dist (The text is distributed vertically. When text is horizontal, this spaces out the actual lines of text, which is identical to the value just below. When text is vertical, it distributes the letters vertically, which is different from just below because it always forces distribution of the words.)
- just (Text is justified vertically. When text is vertical, it justifies the letters vertically. This is different from dist above because in some cases, such as when there is very little text in a line, it does not justify.)
- t (top of the bounding box). This is the default.

Below is an example of positioning in the center (<a:bodyPr rtlCol="0" anchor="ctr" />), followed by positioning at the top (<a:bodyPr rtlCol="0" anchor="t" />).

![Shape with text - anchoring](drwImages\drwSp-text-anchor1.gif) ![Shape with text - anchoring](drwImages\drwSp-text-anchor2.gif)

Horizontal centering of the bounding box can be set using the anchorCtr attribute on <a:bodyPr>. Values are either true or false. This attribute causes the smallest possible bounding box for the text to be centered. It is different than paragraph alignment, which aligns the text within the bounding box. This attribute is appropriate for all the different vertical anchoring values. Below is a shape that has horizontal text, with paragraphs aligned right, vertical centering of the bounding box and no horizontal centering of the box.

<a:bodyPr vert="horz" rtlCol="0" anchor="ctr" anchorCtr="0"/>

![Shape with text - anchoring](drwImages\drwSp-text-anchor3.gif)

Below is the same shape, but also with horizontal anchoring of the bounding box.

<a:bodyPr vert="horz" rtlCol="0" anchor="ctr" anchorCtr="1"/>

![Shape with text - anchoring](drwImages\drwSp-text-anchor4.gif)

## Text Inset:

Insets of the bounding box are specified by four attributes on <a:bodyPr>, one for each side: bIns (bottom inset), tIns (top inset), lIns (left inset), and rIns (rightInset). Insets are used as internal margins for text boxes within shapes. The values of the attributes are specified either in EMUs or as a number immediately followed by the unit identifier--e.g., 0.5in. If an attribute is not specified for a side, a value of 45720 or 0.05 inches is implied.

Below is an example of a shape with inset at the bottom of .1 inch, .5 inch at the top, and none on the left and right.

<xdr:txBody>

<a:bodyPr rtlCol="0" anchor="ctr" bIns="91440" tIns="475200" lIns="0" rIns="0"/>

<a:lstStyle/>

. . .

</xdr:txBody>

![Shape with text - inset](drwImages\drwSp-text-inset2.gif)

If the inset attributes are removed, we get the shape and text as shown below.

![Shape with text - inset](drwImages\drwSp-text-inset1.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
