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

# DrawingML Tables - Cell Properties - Borders and Fill

The borders and fill of a table cell are specified by child elements of the table cell properties element <a:tcPr> element, which is a child of the <a:tc> element. Keep in mind that this is how direct formatting of a table cell is applied. To apply a table cell style to a cell, see [DrawingML - Tables - Styles](drwTableStyles.md).

## Borders

A cell can have borders on the sides, plus two diagonal lines (bottom left to top right and top left to bottom right) for a total of 6 possible borders, each specified by a child element of the table cell properties element. Each border is further customized by a set of attributes and child elements common to all borders. Below is sample table with borders in the second cell of the first row -- an orange dashed top border and a red dashed border top left to bottom right.

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">

<a:solidFill>

<a:schemeClr val="accent6"/>

</a:solidFill>

<a:prstDash val="sysDash"/>

<a:round/>

<a:headEnd type="none" w="med" len="med"/>

<a:tailEnd type="none" w="med" len="med"/>

</a:lnT>

<a:lnTlToBr w="76200" cap="flat" cmpd="sng">

<a:solidFill>

<a:prstClr val="red"/>

</a:solidFill>

<a:prstDash val="sysDash"/>

<a:round/>

<a:headEnd type="none" w="med" len="med"/>

<a:tailEnd type="none" w="med" len="med"/>

</a:lnTlToBr>

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder1.gif)

The elements for the six possible borders are below.

| Elements | Description                                                                                                                                                         |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| lnB      | Specifies the bottom border line and its properties. See below for the various attributes and child elements that can further specify the properties of the line.   |
| lnBlToTr | Specifies the line running bottom left to top right. See below for the various attributes and child elements that can further specify the properties of the line.   |
| lnL      | Specifies the left border. See below for the various attributes and child elements that can further specify the properties of the line.                             |
| lnR      | Specifies the right border. See below for the various attributes and child elements that can further specify the properties of the line.                            |
| lnT      | Specifies the top border. See below for the various attributes and child elements that can further specify the properties of the line.                              |
| lnTlToBr | Specifies the border running top left to bottom right. See below for the various attributes and child elements that can further specify the properties of the line. |

### Border Color, Fill and Weight/Thickness

Border line thickness is specified with a w attribute on the line element. E.g., <a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">. Values are in EMUs.

Colors and special line fills are specified just as they are in other areas of drawingML. For details, see [DrawingML - Shapes - Fill](http://www.officeopenxml.com/drwSp-shapeFill.md). In the example above, a color is specified with solid fill and a preset color of red: <a:solidFill><a:prstClr val="red"/></a:solidFill>

### Border Line Type (Dashes, etc.)

The dash type is specified as either a preset type or a custom type. (Custom types are not covered here). Preset dash types are specified with the <a:prstDash> element, which has a single val attribute specifying the type of line. E.g., <a:prstDash val="sysDash"/>. The possible preset values are:

- dash
- dashDot
- dot
- lgDash (large dash)
- lgDashDotDot
- sysDash (system dash)
- sysDashDot
- sysDashDotDot
- sysDot

Border lines can also be compound lines. The type of compound line is specified by the cmpd attribute on the line element. E.g., <a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">. Possible values are :

- dbl (double)
- sng (single - the default)
- thickThin
- thinThick
- tri (thin thick thin)

Below is a sample top border with a double line and a preset dash set to dashDot:

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">

<a:solidFill>

<a:schemeClr val="accent6"/>

</a:solidFill>

<a:prstDash val="dashDot"/>

. . .

</a:lnT>

. . .

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder2.gif)

### Alignment

Alignment of the underline or border can be specified with the algn attribute on the line element. E.g., <a:lnT w="76200" cap="flat" cmpd="dbl" algn="ctr">. Possible values are ctr (to specify the line to be at the center of the path stroke) and in (to specify that the line is to be on the inside edge). Note that in the sample above, the value was set to ctr . If we instead set it to in, we get the line as shown below.

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder3.gif)

### Line Endings

Line endings can also be specified with the following two child elements of the line element: <a:headEnd> and <a:tailEnd>. Each of these can have attributes that specify the type (type), length (len) and width (w) of the end. The length and width have values of either lg (large), med (medium), or sm (small) and are in relation to the line width. The type can have the following values:

- arrow
- diamond
- none
- oval
- stealth
- triangle

Below is a sample top border with an oval head end and an arrow tail end.

<a:tcPr>

<a:lnT w="76200" cap="flat" cmpd="sng" algn="ctr">

. . .

<a:headEnd type="oval" w="med" len="med"/>

<a:tailEnd type="arrow" w="med" len="med"/>

</a:lnT>

</a:tcPr>

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder4.gif)

There is also a cap attribute on each of the line elements that can have values of either flat, rnd (a round end) or sq (a square end). So a line with no specified head or tail ending element can still alter the ending by applying one of the cap types. For example, below is a cell with a top border that has round ends: <a:lnT w="76200" cap="rnd" cmpd="sng" algn="ctr">

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder5.gif)

The joints where lines connect can be customized to specify that the joints should be beveled, mitered, or rounded by specifying either <a:bevel/>, <a:miter/>, or <a:round/> as a child element of the line element. For example, below is a sample of the top and left and right borders that are specified as mitered.

![DrawingML - Table - Cell borders](drwImages\drwTable-cellBorder6.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
