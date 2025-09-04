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

# DrawingML Object Placement

Placement within a Presentation Document

Presentations are organized into slides or <p:sld> elements. Pictures, shapes, tables, and text on a given slide are specified inline in the part for that slide (e.g., slide1.xml, slide2.xml, etc.). The <p:sld> element contains a <p:cSld> element which acts as a container for common slide data such as pictures, shapes, and tables. (The <p:sld> element can also contain information regarding timing and transition. This information is not covered here.) All shapes, pictures and other content are further nested within a shape tree or <p:spTree> element.

Note: The high-level elements used to place shapes, pictures, and tables into slides in presentations are within the main presentationML namespace xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main".

The shape tree contains non-visual properties of a group shape, visual properties that are common to all shapes (which can be overridden by the properties in individual shapes), and then one or more shapes, pictures, connection shapes, group shapes, and/or graphic frames (i.e., containers for tables and graphics generated from an external source). So all shapes and other content for a slide are contained within the <p:spTree> element. Each shape and picture is positioned on the slide within the properties for that particular shape or picture. For example, for a shape, the positioning is within the <a:xfrm>, which is in the <p:spPr> element containing the shape properties. See [Shapes - Bounding Box Location](drwSp-location.md).

The order of the shapes and other content within the <p:spTree> element is important, as the order determines the z-order of the objects on the slide. The first object listed has the lowest z-order (and is thus on the bottom of the object stack) and the last has the highest order (and is on the top of the stack of objects). The z-order is important when objects overlap, and it also determines the tab or navigation order, with objects being navigated in ascending z-order. Below is an example of a stack of four objects on a slide, with the oval shape first, followed by a picture, followed by another picture, followed by an arrow shape.

<p:sld . . .>

<p:cSld>

<p:nvGrpSpPr>

. . .

<p:nvGrpSpPr>

<p:grpSpPr>

. . .

<p:grpSpPr>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="Oval 3"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="5" name="Picture 4" descr="Blue hills.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="8" name="Picture 7" descr="Winter.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="9" name="Right Arrow 8"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:cSld>

. . .

</p:sld>

![Placement of shapes within a presentation](drwImages\drwInPresentation1.gif)

If we reverse the order of the last two objects, placing the arrow shape before the picture of winter, we get the following, with the picture of winter over the arrow:

<p:sld . . .>

<p:cSld>

<p:nvGrpSpPr>

. . .

<p:nvGrpSpPr>

<p:grpSpPr>

. . .

<p:grpSpPr>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="Oval 3"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="5" name="Picture 4" descr="Blue hills.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="9" name="Right Arrow 8"/>

. . .

</p:nvSpPr>

. . .

<p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="8" name="Picture 7" descr="Winter.jpg"/>

. . .

</p:nvPicPr>

. . .

<p:pic>

<p:cSld>

. . .

</p:sld>

![Placement of shapes within a presentation](drwImages\drwInPresentation2.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
