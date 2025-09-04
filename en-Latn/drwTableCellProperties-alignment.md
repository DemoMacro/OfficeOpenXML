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

# DrawingML Tables - Cell Properties - Text Alignment, Margins and Direction

Each cell may have a set of properties specified within a <a:tcPr> element, which is a child of the <a:tc> element.

Properties related to horizontal and vertical alignment, margins, content direction, and text overflow are determined by attributes of the <a:tcPr> element. Below are the permitted attributes.

| Attribute | Description                                                                                               |
| --------- | --------------------------------------------------------------------------------------------------------- |
| anchor    | Defines the alignment of text vertically within a cell. E.g., <a:tcPr anchor="ctr">. Possible values are: |

- b \- bottom
- ctr \- center
- dist \- distributed vertically. When text is horizontal the lines are spaced out much the same as when the value is just. When text is vertical, the letters are distributed, which is different from just because it always forces distribution even if there are only one or two words.
- just \- distributed vertically. When text is horizontal, this spaces out the lines and is nearly identical to when the value is dist. When text is vertical, it justifies the letters vertically.
- t \- top

anchorCtr | Values are booleans. When true, it modifies the anchor attribute and centers the text box itself so that, for example, the text can be left-aligned along the center of the cell.  
horzOverflow | Specifies the clipping behavior of the cell. When the value is overflow (<a:tcPr horzOverflow="overflow">), text in the cell freely flows outside the cell boundaries and is visible. When the value is clip, the text is clipped and does not appear outside of the cell boundaries.  
marB | Specifies the bottom margin of the cell. E.g., <a:tcPr marB="45720" anchor="ctr">. Values can be in EMUs or as a number followed by a unit identifier.  
marL | Specifies the left margin of the cell. Values can be in EMUs or as a number followed by a unit identifier.  
marR | Specifies the right margin of the cell. Values can be in EMUs or as a number followed by a unit identifier.  
marT | Specifies the top margin of the cell. Values can be in EMUs or as a number followed by a unit identifier.  
vert | Defines the text direction for the cell. Possible values include (omitting the East Asian options):

- horz \- horizontal (the default)
- vert \- vertical, with each line rotated 90 degrees clockwise so that each next line is to the left of the previous
- vert270 \- vertical, with each line rotated 270 degrees clockwise so it goes from bottom to top, with each next line to the right of the previous
- wordArtVert \- determines if all of the text is vertical ("one letter on top of another")
- wordArtVertRtl \- specifies that vertical WordArt should be shown from right to left rather than left to right

## Text Alignment

Below is a sample of a cell that has its content centered vertically--i.e., the anchor attribute has a value of ctr.

<a:tr h="370840">

<a:tc>

. . .

<a:t>Bach</a:t>

. . .

<a:tcPr/>

</a:tc>

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>Beethoven</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr anchor="ctr"/>

</a:tc>

<a:tc>

. . .

<a:t>Brahms</a:t>

. . .

<a:tcPr/>

</a:tc>

</a:tr>

![DrawingML - Table](drwImages\drwTable-textAlignment1.gif)

If we change the above xml to add the anchorCtr to true (<a:tcPr anchor="ctr" anchorCtr="1"/>), the text centers as shown below:

![DrawingML - Table](drwImages\drwTable-textAlignment2.gif)

## Cell Margins

Margins for text within a cell are set by attribute values on the <a:tcPr> element. For example, below is a sample of a cell with left and top margins set to one inch or 914400 EMUs (<a:tcPr marL="914400" marT="914400"/>):

![DrawingML - Table](drwImages\drwTable-textAlignment3.gif)

## Text Direction

The direction of text within a table cell is determined by the vert attribute on the <a:tcPr> element. Below is an example of the direction set to vert (<a:tcPr vert="vert"/>).

![DrawingML - Table - Vertical alignment](drwImages\drwTable-textAlignment5.gif)

Below is an example of the direction set to vert270 (<a:tcPr vert="vert270"/>).

![DrawingML - Table - Vertical alignment](drwImages\drwTable-textAlignment4.gif)

## Text Overflow

Whether text flows outside of the cell or is clipped is determined by the horzOverflow attribute on the <a:tcPr> element. Below is an example of the overflow set to overflow (<a:tcPr vert="wordArtVert" horzOverflow="overflow"/>).

![DrawingML - Table - Text Overflow](drwImages\drwTable-textOverflow.gif)

To clip the text, set the overflow to clip (<a:tcPr vert="wordArtVert" horzOverflow="clip"/>).

![DrawingML - Table - Text Overflow](drwImages\drwTable-textOverflow2.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
