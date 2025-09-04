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

# DrawingML Object Positioning

Positioning within a Word Processing Document - Floating Pictures - Text Wrapping

Text wrapping around an anchored object (<wp:anchor>) is specified with one of five text wrapping-related child elements. (Note that for inline objects <wp:inline>), the object simply becomes part of the line or the run's content, so there is no sense of wrapping.) The five possible child elements are:

- <wrapNone>
- <wrapSquare>
- <wrapThrough>
- <wrapTight>
- <wrapTopAndBottom>

## <wrapNone>

To specify that no text wrapping should be performed, an empty <wp:wrapNone/> element is placed within <wp:anchor>. Text is then displayed in front of or behind the picture based upon the value of the behindDoc attribute of <wp:anchor> element. If behindDoc is true, then the text is in front. If behindDoc is false, then the text is behind.

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>right</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:wrapNone/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - None](drwImages\drw-textWrap-none.gif)

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.4.2.15.

## <wrapSquare>

To specify text wrapping around a virtual rectangle surrounding the object, the <wp:wrapSquare> element is placed within <wp:anchor>. The virtual rectangle is specified either by the <wp:effectExtent> element of the parent <wp:anchor> or, if present, a child <wp:effectExtent> element.

The distance of text from each side of the object is specified in attributes on the <wp:wrapSquare> element: distB (distance from the bottom of the object), distL (distance from the left edge of the object), distR (distance from the right edge of the object), and distT (distance from the top of the object). The values are given in EMUs. A wrapText attribute may also be used to specify which side(s) of the object the text should wrap around. Possible values are:

- bothSides
- largest (text wraps around the largest side; if the object is centered, then text wraps around the side on which text is first encountered)
- left
- right

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="114300" distR="114300" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="19050" t="0" r="0" b="0"/>

<wp:wrapSquare wrapText="left" distT="360000" distB="360000" distL="360000" distR="0"/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - Square Wrapping](drwImages\drw-wrapSquare.gif)

Below is another example, with wrapping on both sides, but no distance between text and object on the right side.

<wp:wrapSquare wrapText="bothSides" distT="360000" distB="360000" distL="360000" distR="0"/>

![Text Wrapping - Square Wrapping](drwImages\drw-wrapSquare2.gif)

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.4.2.17.

## <wrapThrough>

With <wrapThrough>, a polygon shape can be specified around or within the object, and text will wrap around that polygon instead of around the object. The polygon is specified with a <wrapPolygon> child element of <wrapThrough>. The <wp:wrapPolygon> element itself is defined by first specifying a starting point (and ending point) using the child element <wp:start> (with accompanying x and y attributes specifying the x and y coordinates, relative to the upper-left corner of the object). Two or more <wp:lineTo> elements (with the same x and y attributes) are also specified as child elements to define points of the polygon. The x and y attributes can be in either EMUs or as a number immediately followed by a unit identifier (e.g., 2in). The <wp:wrapThrough> element may also have the distL (distance from the left edge of the object) and distR (distance from the right edge of the object) attributes, like <wp:wrapSquare> above, as well as the wrapText attribute. (Note that the coordinate system of DrawingML uses two-dimensional coordinates, with the origin (0,0) in the upper left-hand corner. The x-axis grows positively as one moves left to right, and the y-axis grows positively as one moves from top to bottom.)

Below is a sample that defines a rectangle polygon for the object in inches.

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="0" distR="0" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="0" t="0" r="0" b="0"/>

<wp:wrapThrough wrapText="bothSides">

<wp:wrapPolygon>

<wp:start>x="0in" y="0in"/>

<wp:lineTo>x="0in" y="-1in"/>

<wp:lineTo>x="1in" y="-1in"/>

<wp:lineTo>x="1in" y="0in"/>

<wp:lineTo>x="0in" y="0in"/>

</wp:wrapPolygon>

</wp:wrapThrough>

</wp:anchor>

</w:drawing>

![](images/note.png)Note: Microsoft Word does not seem to not fully support this wrap capability.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.4.2.18.

## <wrapTight>

The <wp:wrapTopAndBottom> is very similar to the <wp:wrapThrough>. A polygon is specified, and text wraps around that polygon. However, <wp:wrapTight> does not allow text anywhere within the maximum and minimum extents of the polygon. The graphic below depicts the difference.

![Text Wrapping - Tight Wrapping](drwImages\drw-wrapTight.gif)

![](images/note.png)Note: Microsoft Word does not seem to not fully support this wrap capability.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.4.2.19.

## <wrapTopAndBottom>

This wrap specifies that text should wrap around the top and bottom of the object, but not the sides. It can have distB (distance from the bottom of the object) and distT (distance from the top of the object) attributes to specify the distance of text from the bottom and top of the object. It can also have a child <wp:effectExtent> element to add to the object's extent to account for effects.

<w:drawing>

<wp:anchor distT="0" distB="0" distL="0" distL="0" distR="0" simplePos="0" relativeHeight="251658240" behindDoc="1" locked="0" layoutInCell="1" allowOverlap="1">

<wp:simplePos x="3219450" y="1504950"/>

<wp:positionH relativeFrom="margin">

<wp:align>center</wp:align>

</wp:positionH>

<wp:positionV relativeFrom="margin">

<wp:align>top</wp:align>

</wp:positionV>

<wp:extent cx="2438400" cy="1828800"/>

<wp:effectExtent l="0" t="0" r="0" b="0"/>

<wp:wrapTopAndBottom"/>

. . .

</wp:anchor>

</w:drawing>

![Text Wrapping - Top and Bottom](drwImages\drw-wrapTopAndBottom.gif)

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.4.2.20.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
