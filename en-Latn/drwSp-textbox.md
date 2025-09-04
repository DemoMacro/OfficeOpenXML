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

# DrawingML Text

Text and Text Boxes

Wordprocessing and spreadsheet documents contain text as a fundamental characteristic of their structure. Create a document and begin entering text, and the text will flow in a familiar and well-defined manner. Each of these document types can also contain text of a more graphic, specialized nature, inserted into a text box or shape. The text box or shape can be located and styled apart from the other text in the document. For each of these document types, the graphical text is inserted as a drawing is inserted, in a specialized namespace covering drawingML for that document type. See [Positioning within a Spreadsheet Document](drwPicInSpread.md) and [Positioning within a Word Processing Document](drwPicInWord.md). A presentation document is not so fundamentally text-oriented, and all text within a presentation must be within a text box or shape. Its placement is defined within the main drawingML specification and namespace.

Although the way in which the text is placed within the document varies from document type to document type, the definition of the text itself remains the same. Text within a text box is really just a specialized shape containing text. See [Shapes - Text](drwSp-text.md). Every shape contains a set of non-visual properties for the canvas within the <nvSpPr> element. Within the <nvSpPr> element is <cNvSpPr>, containing a set of non-visual properties for the shape. That element has an attribute txBox, which can be either true or false. If true, then the shape is a text box. If false, or if the attrubute is not present, then the shape is not specifically a text box. In fact, though, there is little difference between a text box and a shape with text. For presentations and spreadsheets the [geometry (<a:prstGeom>)](drwSp-prstGeom.md) can be omitted. But it can and often is set with a value of rectangle (<a:prstGeom prst="rect">).

Below is a sample containing first a text box and then a shape with text. Both are shapes within a <p:sp> element. The text box has the attribute txBox="1". It also has no <p:style> element, though it could. For the shape, the style information within the <p:style> element is overridden by the lack of line and fill as specified in the <a:prstGeom> element.

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="TextBox 3"/>

<p:cNvSpPr txBox="1"/>

<p:nvPr/>

</p:nvSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2362200" y="1066800"/>

<a:ext cx="2362200" cy="369332"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

<a:noFill/>

</p:spPr>

<p:txBody>

<a:bodyPr wrap="square" rtlCol="0">

<a:spAutoFit/>

</a:bodyPr>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>This is a textbox</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</p:txBody>

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="Rectangle 4"/>

<p:cNvSpPr/>

<p:nvPr/>

</p:nvSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2133600" y="1600200"/>

<a:ext cx="2438400" cy="990600"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

<a:noFill/>

<a:ln/>

<a:noFill/>

</a:ln/>

</p:spPr>

<p:style>

<a:lnRef idx="2">

<a:schemeClr val="accent1">

<a:shade val="50000"/>

</a:schemeClr>

</a:lnRef>

<a:fillRef idx="1">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="lt1"/>

</a:fontRef>

</p:style>

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr"/>

<a:lstStyle/>

<a:p>

<a:pPr algn="ctr"/>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0">

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

</a:rPr>

<a:t>This is in a shape</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

</a:endParaRPr>

</a:p>

</p:txBody>

</p:sp>

![Presentation with textbox and shape with text](drwImages\drwSp-textbox1.gif)

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
