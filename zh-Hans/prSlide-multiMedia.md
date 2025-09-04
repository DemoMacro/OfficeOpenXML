![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 放映
  - [过渡](prSlide-transitions.md)
  - 动画和计时
  - 自定义放映
- 演示文稿属性
- 视图属性
- 幻灯片
  - [Overview](prSlide.md)
  - [内容（通用幻灯片数据）](prCommonSlideData.md)
    - [形状](prSlide-shapeTree.md)
    - [Tables](drwTable.md)
    - [音频和视频](prSlide-multiMedia.md)
  - [幻灯片母版](prSlideMaster.md)
  - [幻灯片版式](prSlideLayout.md)
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

# PresentationML 幻灯片 - 内容 - 多媒体

多媒体（如视频或音频剪辑）作为图片或形状的属性添加到演示文稿中—图片和形状是演示幻灯片内容的基本构建块。

图片或形状的指定方式与其他任何图片或形状的指定方式相同。请参阅[绘图ML - 图片](drwPic.md)和[绘图ML - 形状](drwShape.md)。在下面的示例中，视频的图像使用<a:blip r:embed="rId3" cstate="print"/>元素指定。这引用了幻灯片的.rels文件中的关系（在本例中为slide2.xml.rels）。在该.rels文件中是Id = rId3的关系：<Relationship Id="rId3" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/image Target="../media/image1.png"/>。

附加到图片的视频被指定为图片的非视觉属性的一部分，在<p:nvPr>元素内，该元素是<p:nvPicPr>（如果附加到图片）或<p:nvSpPr>（如果附加到形状）的子元素。下面是指定多媒体的<p:nvPr>可能的子元素。请注意，表示多媒体的每个元素都在主drawingML命名空间中（前缀为'a'），而不是在演示命名空间中（前缀为'p'）。还要注意，媒体的实际外部文件（<a:audioCd>源除外）由r:link属性的值指定，该属性是对幻灯片的.rels部分中的关系的引用；<a:wavAudioFile>源使用r:embed属性。因此，例如，在下面的第一个示例中，实际的视频剪辑文件由<a:videoFile>元素上的r:link="rId1"指定。slide2.xml.rels部分中的相应关系是<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/video Target="file///c:\temp\presentations\sampleMovieClip.wmv" TargetMode="External"/>。

最后，请注意，视频和音频是根据幻灯片的<p:timing>元素激活和播放的，该元素是<p:sld>、<p:sldLayout>和<p:sldMaster>元素的子元素。有关更多信息，请参阅[幻灯片属性 - 计时](prSlide-timing.md)。

### 元素：

| 元素              | 描述                                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <a:audioCd>       | 指定来自CD的音频的存在。有<a:st>和<a:end>子元素，它们指定开始和结束时间。这些元素具有track和time属性。因此，例如，<a:st track="3" time="65"/>指定音频应在第三轨道的1分5秒处（65秒）开始。                                                                                                                                                              |
| <a:audioFile>     | 指定音频文件的存在。此元素有一个contentType属性，用于指定外部文件的类型。如果省略该属性，应用程序应尝试通过读取目标内容来确定类型。建议使用audio/mpeg值。                                                                                                                                                                                              |
| <a:quickTimeFile> | 指定QuickTime文件的存在。                                                                                                                                                                                                                                                                                                                              |
| <a:videoFile>     | 指定视频文件的存在。此元素有一个contentType属性，用于指定外部文件的类型。如果省略该属性，应用程序应尝试通过读取目标内容来确定类型。任何支持的视频类型都是可能的。一些示例是video/avi、video/mpg、video/mpeg和video/quicktime。                                                                                                                         |
| <a:waveAudioFile> | 指定音频WAV文件的存在。此元素有一个contentType属性，用于指定外部文件的类型。如果省略该属性，应用程序应尝试通过读取目标内容来确定类型。任何支持的视频类型都是可能的。一些示例是video/avi、video/mpg、video/mpeg和video/quicktime。还有一个可能的name属性，用于在需要时为音频提供人类可读的名称。如上所述，文件使用r:embed属性而不是r:link属性进行标识。 |

下面是来自幻灯片的示例形状树，其中包含一个电影剪辑，当用户点击电影的第一个图片时播放。第二个示例是一个音频文件的示例，当用户点击通常用于声音的图像时播放。

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="4" name="movieClip.wmv">

<a:hlinkClick r:id="" action="ppaction://media"/>

</p:cNvPr>

<p:cNvPicPr>

<a:picLocks noGrp="1" noChangeAspect="1"/>

</p:cNvPicPr>

<p:nvPr>

<p:ph idx="1"/>

<a:videoFile r:link="rId1"/>

</p:nvPr>

</p:nvPicPr>

<p:blipFill>

<a:blip r:embed="rId3" cstate="print"/>

<a:stretch>

<a:fillRect/>

</a:stretch>

</p:blipFill>

<p:spPr>

<a:xfrm>

<a:off x="1524000" y="2147888"/>

<a:ext cx="6096000" cy="3429000"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

</p:spPr>

</p:pic>

</p:spTree>

![Presentation slide with video](pptxImages\ppSlide-multimedia1.gif)

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:pic>

<p:nvPicPr>

<p:cNvPr id="4" name="Somewhere Over Antartica.mp3">

<a:hlinkClick r:id="" action="ppaction://media"/>

</p:cNvPr>

<p:cNvPicPr>

<a:picLocks noRot="1" noChangeAspect="1"/>

</p:cNvPicPr>

<p:nvPr>

<a:audioFile r:link="rId1"/>

</p:nvPr>

</p:nvPicPr>

<p:blipFill>

<a:blip r:embed="rId3" cstate="print"/>

<a:stretch>

<a:fillRect/>

</a:stretch>

</p:blipFill>

<p:spPr>

<a:xfrm>

<a:off x="4419600" y="3276600"/>

<a:ext cx="304800" cy="304800"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

</p:spPr>

</p:pic>

</p:spTree>

![Presentation slide with audio](pptxImages\ppSlide-multimedia2.gif)

页脚
