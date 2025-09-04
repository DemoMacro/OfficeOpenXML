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

Group Fill

A set of shapes can be grouped together with a <xdr:grpSp> (or <p:grpSp>) element. That group of shapes has a set of properties (within a <grpSpPr>), and one of the properties can be a fill. The individual shapes within the shape group can specify their own fill types or they can use the fill type of the group by specifying <a:grpFill/> for their fill. Below is an example of three shapes grouped together within a spreadsheet. The group fill is specified as a solid fill of black. The triangle uses the group fill, as specified with the <a:grpFill/> element for the triangle shape's fill within its <spPr>. The rectangle and oval both specify their own solid fills.

<xdr:grpSp>

. . .

<xdr:grpSpPr>

. . .

<a:solidFill>

<a:prstClr val="black"/>

<a:solidFill>

</xdr:grpSpPr>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="2" name="Rectangle 1"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:solidFill>

<a:srgbClr val="FFFF00"/>

</a:solidFill>

</xdr:spPr>

</xdr:sp>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="3" name="Isoceles Triangle 2"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:grpFill/>

</xdr:spPr>

</xdr:sp>

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="4" name="Oval 3"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

<xdr:spPr>

. . .

<a:solidFill>

<a:srgbClr val="00B0F0"/>

</a:solidFill>

</xdr:spPr>

</xdr:sp>

</xdr:grpSp>

![Shape with solid fill in spreadsheet](drwImages\drwSp-grpFill.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
