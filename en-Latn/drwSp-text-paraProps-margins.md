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

Text - Spacing, Indents and Margins

## Vertical Line Spacing within a Paragraph

Vertical spacing between lines within a paragraph of text in a shape is specified with the <a:lnSpc> element within the <a:pPr> element for the paragraph. Spacing can be specified as either a percentage or as point size. A percentage is specified using the <a:spcPct> as a child element of <a:lnSpc>). The percentage is based on the run that has the largest size in the paragraph. Spacing in terms of point size is specified using the <a:spcPts> as a child element of <a:lnSpc>), with 100 equal to 1 point and 1200 equal to 12 points. Both child elements specify the actual value within the val attribute. If line spacing is not specified, then the spacing is determined by the size of the largest piece of text in the line. Below is a sample shape with line spacing set to double spacing or 200%.

<a:pPr>

<a:lnSpc>

<a:spcPct val="200000"/>

</a:lnSpc>

</a:pPr>

![Shape with text - line spacing](drwImages\drwSp-text-vertSpace1.gif)

## Space before and after a Paragraph

Spacing before and after paragaphs within a shape are specified with the elements <a:spcBef> and <a:spcAft>, respectively. Each may be specified as a percentage or in points using the child elements <a:spcPct> and <a:spcPts>. Below is a shape with two paragraphs and space after the paragraph specified as 12 points.

<a:pPr>

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - line spacing](drwImages\drwSp-text-spcAft.gif)

## Margins

The left and right margins for a paragraph of text in a shape are specified with the marL and marR attributes on the <a:pPr> element, respectively. These margins are in addition to the text body inset. See [Text Body Properties - Positioning and Insets](drwSp-text-bodyPr-inset.md). The margin values are between 0 and 51206400. Below is a shape with two paragraphs; the first paragraph has a left margin set at 1/2 inch (marL="457200").

<a:pPr marL="457200">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - margins](drwImages\drwSp-text-margins.gif)

## Indent

Indentation for the first line of text in a paragraph is specified with the indent attribute on the <a:pPr> element. The value is specified in EMUs, and if the attribute is omitted, then a value of -342900 is implied. Below is the same shape and text as above, except that an indent of .3 inches has been applied to the first paragraph.

<a:pPr marL="457200" indent="274320">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - margins](drwImages\drwSp-text-indent.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
