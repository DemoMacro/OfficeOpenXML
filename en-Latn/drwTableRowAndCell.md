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

# DrawingML Tables - Rows, Cells and Cell Content

A table is comprised of one or more rows, and a row contains one or more cells.

A table row is defined with the <a:tr> element. The row element can contain a height attribute (h), as either EMUs or as a number followed by a unit identifier. The row element contains one or more cell elements (<a:tc>).

All content within a table is defined within the cell element. A cell can contain only text. A cell may also have properties. (Note that a table may also have properties, but a row does not have properties other than a height.) The permitted child elements of <a:tc> include <a:txBody> for text and <a:tcPr> for cell properties.

A cell may also have the following attributes, which are discussed more fully at [DrawingML - Tables - Structure](dwrTableGrid.md).

| Attribute | Description                                                                                                                                                                                                      |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gridSpan  | Specifies the number of columns that a merged cell spans. Used in combination with the hMerge attribute on other cells in order to specify the beginning cell of a horizontal merge                              |
| hMerge    | Values are booleans. When set to 1 or true, the cell is to be merged with the previous horizontal table cell.                                                                                                    |
| id        | Specifies a unique identifier for the cell. The identifier must be unique within the table, and is used to identify the cell as a header cell for other cells within the table, using the headers child element. |
| rowSpan   | Specifies the number of rows that a merged cell spans. Used in combination with the vMerge attribute on other cells in order to specify the beginning cell of a horizontal merge.                                |
| vMerge    | Values are booleans. When set to 1 or true, the cell is to be merged with the previous vertical table cell.                                                                                                      |

### Text Content within a Cell

Text within a presentation table cell is specified like text is specified within a drawingML shape -- that is, within a <a:txBody> element. For details, see [DrawingML - Shapes - Text](drwSp-text.md). Note one difference. The namespace for the <a:txBody> element is the main drawingML namespace (prefix 'a') rather than the presentation ('p') or other namespace.

Below is a sample presentation table with three rows. The middle row has text. Below the table is the xml for the row that contains the text.

![DrawingML - Table](drwImages\drwTableWithText.gif)

<a:tr h="370840">

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>Bach</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

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

<a:tcPr/>

</a:tc>

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>Brahms</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr/>

</a:tc>

</a:tr>

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
