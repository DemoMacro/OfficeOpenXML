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

# DrawingML Pictures

Image Properties - Non-Visual Properties

The <pic:nvPicPr> element within the <pic:pic> element specifies the non-visual propeties of a picture. The actual properties are within two child elements - <pic:cNvPr> and <pic:cNvPicPr>.

Note that the non-visual properties are in different namespaces, depending on the document type. The examples show the picture namespace of drawingML, with prefix 'pic'. For presentations the non-visual properties are in the main presentationML namespace with prefix 'p'. And for spreadsheets the namespace is the spreadsheet drawingML namespace with prefix 'xdr'.

<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">

<pic:nvPicPr>

<pic:cNvPr id="0" name="Blue hills.jpg"/>

<pic:cNvPicPr/>

</pic:nvPicPr>

<pic:blipFill>

. . .

</pic:blipFill>

<pic:spPr>

. . .

</pic:spPr>

</pic:pic>

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.2.2.4.

## Id, Name, Title and Description

An id, name, title and description for a picture can be specified with attributes on the <pic:cNvPr> element: <pic:cNvPr id="222" name="Blue hills.jpg" title="This is the title" descr="This is the description"/>. The id is an integer and specifies a unique identifier. The name is a string and typically stores the original file name. The title is a string that specifies teh caption. The descr is alternative text used for assistive technologies which do not display the picture.

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.2.2.3.

## Picture Resizing, Cropping, Rotating, Changing Aspect Ratio, Moving, Selecting

The locking properties of a picture are specified with the <a:picLocks> element within the <pic:cNvPicPr> element. Various aspects of a picture or shape's size can be specified with attributes on <a:picLocks>. If the attributes are not specified, then it is assumed that the properties can be changed. For example, to disallow changing the aspect ratio, specify the noChangeAspect attribute as true.

The following are the most useful attributes:

- noChangeAspect
- noCrop
- noMove
- noResize
- noRot (no rotation)
- noSelect

Reference: ECMA-376, 3rd Edition (June, 2011), Fundamentals and Markup Language Reference § 20.1.2.2.31.

Note also that the preferRelativeResize attribute on the <pic:cNvPicPr> element specifies whether the user interface should show the resizing of the picture based upon picture's current size (false) or its original size (true).

## Hidden

A picture can be hidden by specifying the hidden attribute on the <pic:cNvPr> element: <pic:cNvPr hidden="true">.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
