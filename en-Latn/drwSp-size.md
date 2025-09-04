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

Bounding Box Size

The size of the bounding box of the shape is specified with the <a:ext> or extents element within the <a:xfrm> element, which is a child element of <a:spPr> (shape properties) element. The <a:ext> is an empty element; the length and width of the bounding box are specified by two attributes of <a:ext>: cx specifies the width in EMUs, and cy specifies the height in EMUs. Below is an example of a triangle shape, followed by the same triangle that has had its height extended.

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="371475" cy="428625"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-size1.gif)

Below is the same triangle with its height extended from 428625 EMUs to 1514475 EMUs.

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="371475" cy="1514475"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-size2.gif)

Note: If the shape is placed in the worksheet at the corner of a cell, with no offset, then the values for the <xdr:to> element (indicating the bottom right corner) should be the same as the size as indicated by the <a:ext> element. See [Positioning within a Spreadsheet Document - Two-Cell Anchoring](drwPicInSpread-twoCell.md) for more on positioning within spreadsheets and the <xdr:to> element.

<xdr:twoCellAnchor>

<xdr:from>

<xdr:col>1</xdr:col>

<xdr:colOff>0</xdr:colOff>

<xdr:row>1</xdr:row>

<xdr:rowOff>0</xdr:rowOff>

</xdr:from>

<xdr:to>

<xdr:col>1</xdr:col>

<xdr:colOff>876300</xdr:colOff>

<xdr:row>1</xdr:row>

<xdr:rowOff>990600</xdr:rowOff>

</xdr:to>

. . .

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1819275" y="619125"/>

<a:ext cx="876300" cy="990600"/>

</a:xfrm>

. . .

</xdr:spPr>

. . .

</xdr:sp>

</xdr:twoCellAnchor>

![Shape size](drwImages\drwSp-size3.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
