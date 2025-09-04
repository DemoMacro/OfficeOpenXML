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

Text - Alignment, Tabs, Other

## Alignment

Alignment of text within a paragraph in a shape is specified with the algn attribute on the <a:pPr> element for the paragraph. The most common values are:

- l (left, the default value)
- r (right)
- ctr (centered)
- just (justified)
- dist (distributed, which distributes text across the entire line)

Below is a sample shape with alignment on the first paragraph set to justified (algn="just").

<a:pPr algn="just">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - alignment](drwImages\drwSp-text-align.gif)

## Font Alignment

Vertical alignment of words on a line is specified with the fontAlgn attribute on the <a:pPr> element for the paragraph. This is relevant when some words on a line are larger than others. In such a case, should the smaller words be positioned in the middle relative to the larger words, at the bottom or top? Possible values are:

- auto (when the text flow is horizontal, this is the same as base below)
- b (the very bottom of a line, which may be different than base because of letters such as g, q, and y, which hang below the baseline)
- base (the baseline--the default)
- ctr (centered)
- t (top)

Below is a sample with font alignment at the top (fontAlgn="t").

<a:pPr fontAlgn="t"/>

![Shape with text - font alignment](drwImages\drwSp-text-fontAlign.gif)

## Tabs

Custom tab stops can be specified for a paragraph within a shape with the <a:tabLst> child element of <a:pPr>. The <a:tabLst> can contain one or more tab stop definitions, each within a <a:tab>. Each such <a:tab> has a pos attribute specifying the stop relative to the left margin (either in EMUs or by a number immediately followed by a unit identifer), with each tab in the order increasing its pos value. Each <a:tab> may also have a algn attribute which specifies the alignment of text. Possible values are ctr, dec (the decimals are lined up, so right-aligned until the decimal and then left aligned after the decimal), l and r.

The default tab size can also be specified with the defTabSz attribute on <a:pPr>. Possible values are specified either in EMUs or as a number immediately followed by a unit identifier. Below is a shape with tabs between text, and the default size is set to 1 inch or 914400 EMUs.

<a:pPr defTabSz="914400"/>

![Shape with text - tabs](drwImages\drwSp-text-tabs1.gif)

Below is the same shape, but with custom tabs as follows.

<a:pPr>

<a:tabLst>

<a:tab pos="914400" algn="l"/>

<a:tab pos="1371600" algn="l"/>

<a:tab pos="1600200" algn="l"/>

<a:tab pos="1714500" algn="l"/>

<a:tabLst>

</a:pPr>

![Shape with text - tabs](drwImages\drwSp-text-tabs2.gif)

## Word Breaks

A long Latin word by default can be broken and wrapped onto the next line without a hyphen. However, it is possible to prevent this behavior by specifying the latinLnBrk attribute on <a:pPr>. A value of false or 0 will prevent a line break in such a case. Below is first a sample with latinLnBrk="1".

![Shape with text - latin line break](drwImages\drwSp-text-latinLnBrk1.gif)

Below is the same shape and same paragraph, but with latinLnBrk="0".

![Shape with text - latin line break](drwImages\drwSp-text-latinLnBrk2.gif)

## Hanging Punctuation

It is possible to prevent punctuation at the end of a run from being carried onto the next line by specifying the hangingPunct attribute on <a:pPr>. A value of true or 1 forces the punctuation to not be carried over and a value of false allows the punctuation to be carried to the next line. The default is false.

[About this site](aboutThisSite.md) | [Contact us](contactUs.md)  
Copyright © 2023. All Rights Reserved.
