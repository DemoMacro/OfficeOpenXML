![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[Home](index.md) | [WordprocessingML (docx)](anatomyofOOXML.md) | [SpreadsheetML (xlsx)](anatomyofOOXML-xlsx.md) | [DrawingML](drwOverview.md) | [PresentationML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- Shows
  - [Transitions](prSlide-transitions.md)
  - Animation and Timing
  - Custom Shows
- Presentation Properties
- View Properties
- Slides
  - [Overview](prSlide.md)
  - [Content (Common Slide Data)](prCommonSlideData.md)
    - [Shapes](prSlide-shapeTree.md)
    - [Tables](drwTable.md)
    - [Audio and Video](prSlide-multiMedia.md)
  - [Slide Master](prSlideMaster.md)
  - [Slide Layout](prSlideLayout.md)
  - [Slide](prPresentationSlide.md)
  - [Notes Master](prNotesMaster.md)
  - [Notes Slide](prNotesSlide.md)
  - Handout Master
- Slide Properties
  - [Size](prSlide-size.md)
  - [Background](prSlide-background.md)
  - [Headers and Footers](prSlide-footer.md)
  - Styles and Formatting
    - [Fill, Fonts, Outines, Effects](prSlide-styles-themes.md)
    - [Text Styles](prSlide-styles-textStyles.md)
  - [Color Scheme](prSlide-color.md)
  - Slide Number

# PresentationML Slides - Properties - Size

The size of slides in a presentation is set for the entire presentation with the <p:sldSZ> element within the presentation root element, and by the <p:notesSz> within the presentation root element for notes slides. The <p:sldSz> and <p:notesSz> are empty elements with three attributes. The cx and cy attributes specify the length and width, respectively, of the rectangle of the slide (in EMUs). Note that objects can be specified outside of the rectangle; the size specifies the background surface that is shown when the presentation is presented or printed. There is a third attribute type for <p:sldSz>, which specifies the kind of size that should be used, anticipating the delivery platform for the presentation. Possible values are listed below.

- 35mm
- A3
- A4
- B4ISO
- B4JIS
- B5ISO
- B5JIS
- banner
- custom
- hagakiCard
- ledger
- letter
- overhead
- screen16x10
- screen16x9
- screen4x3

Below is a sample slide and notes size.

<p:presentation>

. . .

<p:sldSz cx="9144000" cy="6858000" type="screen4x3"/>

<p:notesSz cx="6858000" cy="9144000"/>

. . .

</p:presentation>

![Slide background - bgPr](pptxImages\ppSlide-size1.gif)

Below is the same slide, but with the slide size reduced in length to cx="7144000".

![Slide background - bgPr](pptxImages\ppSlide-size2.gif)

Footer
