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

# DrawingML Tables - Structure

A table is defined within a <a:tbl> element, which itself contains a definition of the table structure (within a <a:tblGrid> element), table properties (within a <a:tblPr> element), and content (within one or more <a:tr> table row elements).

The columns of a table are defined by the <a:tblGrid> element. The <a:tblGrid> contains an element <a:gridCol> for each possible cell size (sometimes called logical columns) in the table. The number of <a:gridCol> elements needed for the table's <a:tblGrid> is determined by extending each cell's vertical borders and counting the total number of columns defined by the lines. For example, a table which has three columns with no cells that are merged needs 3 <a:gridCol> elements in its <a:tblGrid>.

Things become more complicated when cells are not of equal length from row to row. For example, the table below has four possible or logical columns and so needs 4 <a:gridCol> elements in its <a:tblGrid> element.

![DrawingML - Table](drwImages\drwTableGrid2.png)

The <a:tblGrid> for this table is below.

<a:tbl>

. . .

<a:tblGrid>

<a:gridCol w="1219200"/>

<a:gridCol w="1143000"/>

<a:gridCol w="2362200"/>

<a:gridCol w="1371600"/>

</a:tblGrid>

The <a:tblGrid> element contains one or more <a:gridCol> elements -- one for each column. The <a:gridCol> element has one attribute w which specifies the width of the column in EMUs.

### Cell Spanning

The table shown above contains examples of cells that span both vertically and horizontally. For example, cells 1-1, 1-2, 2-1, and 2-2 have been merged and contain the text "Merged vertically and horizontally. Cell spanning in drawingML tables is indicated differently that it is in WordprocesingML tables. First, in wordprocessingML tables cells that have been merged do not appear in the XML for the row. That is, there are only as many cell elements in the row as there are cells that appear visually. In drawingML tables, every row contains as many <a:tc> elements as there are logical columns or <a:gridCol> elements. Second, cell spanning in wordprocessingML is indicated with elements (<w:gridSpan> and <w:vMerge>). However, in drawingML cell spanning is indicated with attributes of <a:tc>.

Tables contains rows or <a:tr> elements. Each <a:tr> element contains the same number of <a:tc> elements are there are <a:gridCol> elements. If two or more cells are merged horizontally, then the first cell contains a gridSpan attribute specifying the number of cells that are merged. Subsequent cells that are merged contain a hMerge attribute set to true (hMerge="1"). If two or more cells are merged vertically, then the first cell (that is, the cell containing the content) contains a rowSpan attribute specifying the number of rows that a cell spans. Corresponding cells in rows below that cell (that is, the cells that have been merged with the cell above) contain a vMerge attribute set to true (vMerge="1").

The sample below shows the XML for the table above. The cells that are spanned vertically or horizontally have matching colors for their related attributes (gridSpan and hMerge="1", or rowSpan and vMerge).

<a:tbl>

. . .

<a:tblGrid>

<a:gridCol w="1219200"/>

<a:gridCol w="1143000"/>

<a:gridCol w="2362200"/>

<a:gridCol w="1371600"/>

</a:tblGrid>

<a:tr h="370840">

<a:tc rowSpan="2" gridSpan="2">

. . .

<a:t>Merged vertically and horizontally</a:t>

. . .

</a:tc>

<a:tc rowSpan="2" hMerge="1">

. . .

</a:tc>

<a:tc>

. . .

<a:t>Cell 1-3</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>Cell 1-4</a:t>

. . .

</a:tc>

</a:tr>

<a:tr h="370840">

<a:tc gridSpan="2" vMerge="1">

. . .

</a:tc>

<a:tc hMerge="1" vMerge="1">

. . .

</a:tc>

<a:tc gridSpan="2">

. . .

<a:t>Merged horizontally</a:t>

. . .

</a:tc>

<a:tc hMerge="1">

. . .

</a:tc>

</a:tr>

<a:tr h="370840">

<a:tc>

. . .

<a:t>Cell 3-1</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>Cell 3-2</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>Cell 3-3</a:t>

. . .

</a:tc>

<a:tc>

. . .

<a:t>Cell 3-4</a:t>

. . .

</a:tc>

</a:tr>

. . .

</a:tbl>

![DrawingML - Table](drwImages\drwTableGrid1.png)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
