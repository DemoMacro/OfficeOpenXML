![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 演示
  - [切换效果](prSlide-transitions.md)
  - 动画和时序
  - 自定义演示
- 演示文稿属性
- 视图属性
- 幻灯片
  - [Overview](prSlide.md)
  - [内容（通用幻灯片数据）](prCommonSlideData.md)
    - [形状](prSlide-shapeTree.md)
    - [Tables](drwTable.md)
    - [音频和视频](prSlide-multiMedia.md)
  - [幻灯片母版](prSlideMaster.md)
  - [幻灯片布局](prSlideLayout.md)
  - [Slide](prPresentationSlide.md)
  - [备注母版](prNotesMaster.md)
  - [备注幻灯片](prNotesSlide.md)
  - 讲义母版
- 幻灯片属性
  - [大小](prSlide-size.md)
  - [背景](prSlide-background.md)
  - [页眉和页脚](prSlide-footer.md)
  - 样式和格式
    - [填充、字体、轮廓、效果](prSlide-styles-themes.md)
    - [文本样式](prSlide-styles-textStyles.md)
  - [配色方案](prSlide-color.md)
  - 幻灯片编号

# PresentationML 演示文稿

<p:presentation>元素是演示文稿主要内容起始部分的根元素（位于Microsoft Powerpoint程序包的ppt文件夹中的presentation.xml）。它位于主演示文稿命名空间中：xmlns:p="http://schemas.openxmlformats.org/presentationml/2006/main"。它包含构成演示文稿的各种幻灯片的规范，以及一些演示文稿范围的属性。

<p:presentation . . . saveSubsetFonts="1">

<p:sldMasterIdLst>

. . .

</p:sldMasterIdLst>

<p:notesMasterIdLst>

. . .

</p:notesMasterIdLst>

<p:handoutMasterIdLst>

. . .

</p:handoutMasterIdLst>

<p:handoutMasterIdLst>

. . .

</p:handoutMasterIdLst>

<p:sldIdLst>

. . .

</p:sldIdLst>

<p:sldSz cx="9144000" cy="6858000" type="screen4x3"/>

<p:notesSz cx="6858000" cy="9144000" type="screen4x3"/>

<p:defaultTextStyle>

. . .

</p:defaultTextStyle>

</p:presentation>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 §§ 17.2.3。

### 元素：

以下是<p:presentation>最常用的子元素。

| 元素                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p:custShowLst>        | 默认情况下，演示文稿显示会按照<p:sldIdLst>元素中指定的顺序显示演示文稿中的所有幻灯片。但是，可以创建一个或多个自定义演示，在其中可以指定不同的顺序和可用幻灯片的子集。自定义演示在此元素中指定。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p:defaultTextStyle>   | 演示文稿的默认文本样式使用此元素指定。当添加与幻灯片母版无关的新幻灯片或未为文本指定样式信息时，默认样式是相关的。此元素可以指定子元素<a:defPPr>中的默认段落样式以及子元素<a:lvl1pPr>到<a:lvl9pPr>中的列表级别样式。有关这些默认样式属性的详细信息，请参见[形状 - 文本 - 列表属性和默认样式](drwSp-text-lstPr.md)。请注意，默认段落和列表样式元素位于主drawingML命名空间中，而父元素<p:defaultTextStyle>位于主presentationML命名空间中。下面是一个具有粗体和以'B'开头的第一级（lvl="0"）列表编号样式的默认段落样式示例。<p:presentation . . . > . . . <p:defaultTextStyle> <a:defPPr> <a:defRPr b="1"/> </a:defPPr> <a:lvl1pPr> <a:defRPr b="1"/> <a:lvl1pPr algn="r"> <a:buAutoNum type="alphaUcPeriod" startAt="2"/> </a:lvl1pPr> </p:defaultTextStyle> </p:presentation>                                                                         |
| <p:embeddedFontLst>    | 演示文稿中的嵌入字体列表列在嵌入字体列表<p:embeddedFontLst>中。每种字体在列表中指定为<p:embeddedFont>元素。字体的实际字体数据存储在文档包中（通常在ppt/fonts文件夹中），并由<p:embeddedFont>元素引用。这些引用位于presentation.xml.rels部分中。下面是一个具有四个版本字体的示例—常规、粗体、斜体和粗斜体。 <p:presentation . . . > . . . <p:embeddedFontLst> <p:font typeface="MyFont" pitchfamily="34" charset="0"/> <p:regular r:id="rId3"/> <p:bold r:id="rId4"/> <p:italic r:id="rId5"/> <p:boldItalic r:id="rId6"/> </p:embeddedFontLst> . . . </p:presentation> 上面的常规字体引用了rId3关系。演示文稿的.rels部分中的该关系如下所示：<Relationship Id="rId3" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/font" Target="fonts/font1.fntdata"/>。                                                                 |
| <p:handoutMasterIdLst> | 讲义是演示文稿的打印版本。打印版本的格式和布局在讲义母版中指定。演示文稿的讲义母版在此元素中指定，使用子元素<p:handoutMasterId>，该元素仅引用演示文稿的.rels部分中的关系。 <p:presentation . . . > . . . <p:handoutMasterIdLst> <p:handoutMasterId r:id="rId7"/> </p:handoutMasterIdLst> . . . </p:presentation> 上面的讲义母版使用关系ID rId7引用。演示文稿的.rels部分中的该关系如下所示：<Relationship Id="rId7" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/handoutMaster" Target="handoutMasters/handoutMaster1.xml"/>。实际的母版在该部分（handoutMaster1.xml）中指定。有关讲义母版的详细信息，请参见？？？？。                                                                                                                                                                                                  |
| <p:notesMasterIdLst>   | 备注幻灯片是专门为打印幻灯片及其附加备注而设计的幻灯片。备注幻灯片的格式和布局在备注母版中指定。演示文稿的备注母版在此元素中指定，使用子元素<p:notesMasterId>，该元素仅引用演示文稿的.rels部分中的关系。 <p:presentation . . . > . . . <p:notesMasterIdLst> <p:notesMasterId r:id="rId6"/> </p:notesMasterIdLst> . . . </p:presentation> 上面的备注母版使用关系ID rId6引用。演示文稿的.rels部分中的该关系如下所示：<Relationship Id="rId6" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/notesMaster" Target="notesMasters/notesMaster1.xml"/>。实际的母版在该部分（notesMaster1.xml）中指定。有关备注母版的详细信息，请参见？？？？。                                                                                                                                                                                  |
| <p:notesSz>            | 此元素指定用于备注幻灯片和讲义幻灯片的幻灯片表面大小。（常规内容或演示幻灯片的大小由<p:sldSz>元素指定。）该元素为空，具有两个属性cx和cy，分别表示长度和宽度，单位为EMU。 <p:presentation . . . > . . . <p:notesSz cx="6858000" cy="9144000"/> . . . </p:presentation>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p:sldIdLst>           | 演示文稿中的内容幻灯片在此元素中指定为ID列表，使用子元素<p:sldId>。每个<p:sldId>仅引用演示文稿的.rels部分（presentation.rels.xml）中的关系。请注意，幻灯片列出的顺序很重要，因为它决定了幻灯片显示的顺序（在没有自定义演示的情况下）。下面是一个包含三张幻灯片的演示文稿。请注意，每个幻灯片都有一个id属性和一个关系id属性id，后者引用幻灯片的部分。 <p:presentation . . . > . . . <p:sldIdLst> <p:sldId id="256" r:id="rId2"/> <p:sldId id="257" r:id="rId3"/> <p:sldId id="258" r:id="rId4"/> </p:sldIdLst> . . . </p:presentation> 上面的第一张幻灯片使用关系ID rId2引用。演示文稿的.rels部分中的该关系如下所示：<Relationship Id="rId2" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slide" Target="slides/slide1.xml"/>。实际的幻灯片内容在该部分（slide1.xml）中指定。有关幻灯片部分的详细信息，请参见？？？？。 |
| <p:sldMasterIdLst>     | 母版幻灯片是构建幻灯片的基础或模板。它指定要使用的主题和可用的布局等内容。每个演示文稿至少有一个母版幻灯片；如果您希望幻灯片使用不同的主题，则每个主题将需要不同的母版幻灯片。演示文稿的母版幻灯片在<p:sldMasterIdLst>元素中指定，为每个母版幻灯片使用子元素<p:sldMasterId>。此元素仅引用演示文稿的.rels部分中的关系。 <p:presentation . . . > <p:sldMasterIdLst> <p:sldMasterId id="2147483660" r:id="rId1"/> </p:sldMasterIdLst> . . . </p:presentation> 上面的幻灯片母版使用关系ID rId1引用。演示文稿的.rels部分（presentation.rels.xml）中的该关系如下所示：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideMaster" Target="slideMasters/slideMaster1.xml"/>。实际的母版在该部分（slideMaster1.xml）中指定。有关母版幻灯片的详细信息，请参见[母版幻灯片](prSlideMaster.md)。             |
| <p:sldSz>              | 此元素指定用于内容或演示幻灯片的幻灯片表面大小。（备注和讲义幻灯片的大小由<p:notesSz>元素指定。）该元素为空，具有属性cx和cy，分别表示长度和宽度，单位为EMU，以及一个type属性，指定应使用的幻灯片类型。这标识了预期的交付平台。可能的值包括：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

- 35毫米
- A3
- A4
- 横幅
- 自定义
- 分类账
- 信纸
- 投影仪
- 屏幕16x10
- 屏幕16x9
- 屏幕4x3

<p:presentation . . . > . . . <p:sldSz cx="9144000" cy="6858000" type="screen4x3"/> . . . </p:presentation>

页脚
