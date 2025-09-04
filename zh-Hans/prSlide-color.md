![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 演示
  - [切换效果](prSlide-transitions.md)
  - 动画和计时
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

# PresentationML 幻灯片 - 属性 - 配色方案

幻灯片上使用的颜色始于演示文稿的主题部分。在主题部分的<a:themeElements>元素内是一个<a:clrScheme>元素。主题的配色方案定义了12种颜色：2种深色（<a:dk1>和<a:dk2>），2种浅色（<a:lt1>和<a:lt2>），6种强调色（<a:accent1至accent6>），以及超链接颜色（<a:hlink>）和已访问的超链接颜色（<a:folHlink>）。每种颜色都可以通过任何指定颜色的方法来定义。请参见下面的"定义颜色"。配色方案可能还有一个名称属性（<a:clrScheme name="Flow">），它会显示在用户界面上，通常对应于主题的名称。

此主题配色方案中定义的颜色随后被映射到幻灯片中用于背景、文本和强调色的颜色。这种映射首先发生在幻灯片、讲义或备注母版级别，使用<p:clrMap>（一个空元素），它是根母版元素（例如<p:sldMaster>元素）的子元素。配色方案通过<p:clrMap>的属性进行映射，这些属性对应于12种颜色。例如，下面是主题部分中定义的配色方案，后面是母版幻灯片中的映射。

<a:clrScheme name="Flow">

<a:dk1>

<a:sysClr val="windowText" lastClr="000000"/>

</a:dk1>

<a:lt1>

<a:sysClr val="window" lastClr="FFFFFF"/>

</a:lt1>

<a:dk2>

<a:srgbClr val="04617B"/>

</a:dk2>

<a:lt2>

<a:srgbClr val="DBF5F9"/>

</a:lt2>

<a:accent1>

<a:srgbClr val="0F6FC6"/>

</a:accent1>

<a:accent2>

<a:srgbClr val="009DD9"/>

</a:accent2>

<a:accent3>

<a:srgbClr val="0BD0D9"/>

</a:accent3>

<a:accent4>

<a:srgbClr val="10CF9B"/>

</a:accent4>

<a:accent5>

<a:srgbClr val="7CCA62"/>

</a:accent5>

<a:accent6>

<a:srgbClr val="A5C249"/>

</a:accent6>

<a:hlink>

<a:srgbClr val="E2D700"/>

</a:hlink>

<a:folHlink>

<a:srgbClr val="85DFD0"/>

</a:folHlink>

</a:clrScheme>

母版幻灯片内的颜色映射如下。例如，第一种文本颜色映射到主题中的dk1，即<a:sysClr val="windowText" lastClr="000000"/>；第二种背景颜色映射到主题中的lt2，即<a:srgbClr val="DBF5F9"/>。

<p:clrMap bg1="lt1" tx1="dk1" bg2="lt2" tx2="dk2" accent1="accent1" accent2="accent2" accent3="accent3" accent4="accent4" accent5="accent5" accent6="accent6" hlink="hlink" folHlink="folHlink"/>

![Slide color map](pptxImages\ppSlide-colorMap1.gif)

如果我们更改母版幻灯片中的映射，使第一种背景颜色映射到accent4而不是lt1（即bg1="accent4"），我们会得到如下所示的幻灯片。背景现在更改为accent4颜色，因为母版幻灯片中的背景颜色设置为<a:schemeClr val="bg1"/>

![Slide color map](pptxImages\ppSlide-colorMap2.gif)

母版幻灯片中找到的这些颜色映射可以在幻灯片布局或幻灯片中使用<p:clrMapOvr>进行覆盖，它是<p:sld>、<p:sldLayout>或<p:notes>的子元素。<p:clrMapOvr>元素可以有两个子元素之一：<a:masterClrMapping>或<a:overrideClrMapping>。（注意子元素的不同命名空间 - 在主要的drawingML命名空间中。）当指定<a:masterClrMapping />（一个没有属性的空元素）时，使用母版幻灯片中定义的配色方案。或者，可以指定<a:overrideClrMapping>，就像<a:clrMap>一样，使用属性将文本、背景和强调色映射到主题颜色。例如，假设我们开始使用Flow主题中的标题幻灯片，母版幻灯片中使用以下颜色映射：

<p:clrMap bg1="lt1" tx1="dk1" bg2="lt2" tx2="dk2" accent1="accent1" accent2="accent2" accent3="accent3" accent4="accent4" accent5="accent5" accent6="accent6" hlink="hlink" folHlink="folHlink"/>

如果我们在幻灯片的<p:clrMapOvr>中指定<a:masterClrMapping />，我们会得到以下幻灯片：

![Slide color map](pptxImages\ppSlide-colorMapOverride1.gif)

现在，在幻灯片中指定一个覆盖，反转bg1和accent1颜色，使accent1分配给bg1颜色，lt1分配给accent1颜色：

<p:clrMapOvr>

<a:overrideClrMapping bg1="accent1" tx1="dk1" bg2="lt2" tx2="dk2" accent1="lt1" accent2="accent2" accent3="accent3" accent4="accent4" accent5="accent5" accent6="accent6" hlink="hlink" folHlink="folHlink"/>

</p:clrMapOvr>

此更改对幻灯片产生以下结果：

![Slide color map](pptxImages\ppSlide-colorMapOverride2.gif)

## 定义颜色

颜色可以在OOXML文档中的许多点指定。在wordprocessingML文档中，颜色被指定为RGB值或主题颜色值。例如，一段文本的颜色可以通过运行属性中的<w:color w:val="FFFF00"/>指定为RGB值，或通过<w:color w:themeColor="accent2"/>指定为主题颜色。表格的边框被指定为边框的属性：例如，<w:top w:val="single" w:sz="12" w:space="0" w:color="FF0000"/>或<w:top w:val="single" w:sz="12" w:space="0" w:color="accent2"/>。

在spreadsheetML文档中指定颜色的方式与在wordprocessingML文档中相同；可以是RGB值，也可以通过引用主题颜色。例如，单元格的前景色可以在<patternFill>元素内使用<fgColor rgb="FFFFFF00"/>指定，或者单元格内的文本可以在运行属性元素内使用<color theme="1"/>分配主题颜色，后者使用主题部分<clrScheme/>的索引。

在drawingML（包括主题）中，因此在presentationML文档中，有6种不同的指定颜色的方法，它们对应于6个不同的元素。

- 作为预设颜色（<a:prstClr val="black"/>）。有关枚举值的完整列表，请参见ECMA-376第3版（2011年6月），基础和标记语言参考第20.1.10.47节。
- 使用色相、饱和度和亮度（<a:hslClr hue="14400000" sat="100%" lum="50%"/>）
- 方案（或主题）颜色（<a:schemeClr val="lt1"/>）
- 系统颜色（<a:sysClr val="windowText"/>）
- 作为RGB百分比（<a:scrgbClr r="50%" g="50%" b="50%"/>
- 作为RGB十六进制数<a:srgbClr val="BCBCBC"/>)

这些对应于颜色指定方法的元素也可以有子元素，这些子元素可以转换基础颜色。因此，例如，在下面的示例中，方案或主题颜色被指定为accent6，但对该基础颜色应用了亮度调制。

<a:schemeClr val="accent6">

<a:lumMod val="75000"/>

</a:schemeClr>

## 主题中的颜色占位符

注意颜色占位符如何在主题中使用。例如，主题可能定义一个纯色填充，如下所示，使用"phClr"或占位符作为值。这意味着填充将使用引用主题填充样式时指定的颜色。假设主题中出现以下内容。

<a:fillStyleLst>

<a:solidFill>

<a:schemeClr val="phClr"/>

</a:solidFill>

. . .

</a:fillStyleLst>

此填充可以在形状中使用<p:style>元素引用，使用样式中<a:fillRef>元素的idx属性。<a:fillRef>通过子<a:schemeClr>元素指定主题颜色。下面accent2颜色被指定为用于替换主题中占位符的颜色。

<p:style>

. . .

<a:fillRef idx="1">

<a:schemeClr val="accent2"/>

</a:fillRef>

. . .

</p:style>

在这个例子中，这似乎不必要地晦涩。但是，请记住，主题内<a:schemeClr>元素的规范可以指定许多不同的颜色效果和更改（作为子元素），因此颜色可能只是整体填充外观的一个组成部分。

页脚
