![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 放映
  - [切换效果](prSlide-transitions.md)
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

# PresentationML 幻灯片 - 概述

演示文稿中显示的幻灯片是由三个组成层次结构的组件组合而成的结果：(1) 底层是基于幻灯片所依据的母版幻灯片指定的内容，(2) 中间是应用于幻灯片的版式，(3) 顶层是实际的幻灯片内容。

母版幻灯片是构建幻灯片的模板；它指定了标题、正文和页脚的字体样式、文本和对象的占位符位置、项目符号样式和背景等属性。版式是设计的第二层，可以增强或覆盖母版幻灯片中指定的内容。最后，幻灯片本身将指定母版幻灯片和幻灯片版式尚未指定的内容和格式。幻灯片版式中定义的属性和内容将覆盖母版幻灯片中指定的类似属性和内容，而幻灯片中指定的属性和内容将覆盖版式中定义的类似属性和内容。

这三个组件中的每一个都是一个单独的部分（例如，slideMaster1.xml、slideLayout1.xml 和 slide1.xml），具有不同的根元素（<p:sldMaster>、<p:sldLayout> 和 <p:sld>）。它们各自的内容模型略有不同，但它们共享一些通用元素。下表显示了幻灯片类型以及它们可以包含的元素。

| 幻灯片母版       | 幻灯片版式 | 幻灯片 | 备注母版 | 备注 | 讲义母版 |
| ---------------- | ---------- | ------ | -------- | ---- | -------- | --- |
| <p:clrMap>       | X          |        |          | X    |          | X   |
| <p:cSld>         | X          | X      | X        | X    | X        | X   |
| <p:hf>           | X          | X      |          | X    |          | X   |
| <p:notesStyle>   |            |        |          | X    |          |
| <p:clrMapOvr>    |            | X      | X        |      | X        |
| <p:sldLayoutLst> | X          |        |          |      |          |
| <p:timing>       | X          | X      | X        |      |          |
| <p:transition>   | X          | X      | X        |      |          |
| <p:txStyles>     | X          |        |          |      |          |

## 占位符、幻灯片/版式/母版层次结构以及覆盖属性和内容

要理解幻灯片层次结构如何工作，必须理解占位符的使用。占位符将三个层链接在一起，以便能够进行覆盖。幻灯片、版式和母版都是由形状类似地构建的。从上表注意，每种幻灯片类型都有一个 <p:cSld> 或通用幻灯片数据元素。在该元素内是一个或多个形状的组，无论是几何形状、文本框、幻灯片编号字段、日期字段、页脚等—它们都在形状（<p:sp> 元素）内。每个形状元素包含一组非视觉属性（<p:nvSpPr>）。在该元素内是用于非视觉属性的 <p:nvPr>，该元素可以包含用于占位符的 <p:ph> 元素。占位符元素是空的，但确实有几个可能的属性。正是使用 idx 和 type 属性，形状在三种幻灯片类型之间进行链接。

占位符是在母版和版式级别创建的。也就是说，它们可以在这些级别添加和删除，但不能在幻灯片级别添加和删除。在幻灯片级别，它们仅被引用或链接到较低的版式层。也就是说，幻灯片可以引用版式级别的占位符，但不能引用母版级别的占位符。同样，版式可以引用母版幻灯片级别的占位符。

<p:ph> 元素具有以下可能的属性。没有子元素。

| 属性            | 描述                                                                                   |
| --------------- | -------------------------------------------------------------------------------------- |
| hasCustomPrompt | 指示占位符是否应具有自定义提示。值为布尔值。                                           |
| idx             | 指定占位符的索引。这在应用模板或更改版式时用于将一个模板或母版上的占位符与另一个匹配。 |
| sz              | 指定占位符的大小。可能的值为 full、half 和 quarter。                                   |
| type            | 指定占位符要包含的内容类型。可能的值为                                                 |

- body（包含正文文本，允许在幻灯片、版式、幻灯片母版、备注和备注母版中使用；可以是水平或垂直的）
- chart（包含图表或图形，允许在幻灯片和版式中使用）
- clipArt（包含单个剪贴画图像，允许在幻灯片和版式中使用）
- ctrTitle（包含旨在在幻灯片上居中的标题，允许在幻灯片和版式中使用）
- dgm（包含图表，允许在幻灯片和版式中使用）
- dt（包含日期和时间，允许在幻灯片、版式、幻灯片母版、备注、备注母版和讲义母版中使用）
- ftr（包含用作页脚的文本，允许在幻灯片、版式、幻灯片母版、备注、备注母版和讲义母版中使用）
- hdr（包含用作页眉的文本，允许在备注、备注母版和讲义母版中使用）
- media（包含音频或电影等多媒体内容，允许在幻灯片和版式中使用）
- obj（包含任何内容类型，允许在幻灯片和版式中使用）
- pic（包含图片，允许在幻灯片和版式中使用）
- sldImg（包含幻灯片的图像，允许在备注和备注母版中使用）
- sldNum（包含幻灯片的编号，允许在幻灯片、版式、幻灯片母版、备注、备注母版和讲义母版中使用）
- subTitle（包含副标题，允许在幻灯片和版式中使用）
- tbl（包含表格，允许在幻灯片和版式中使用）
- title（包含幻灯片标题，允许在幻灯片、版式和幻灯片母版中使用；可以是水平或垂直的）

以下是母版幻灯片、版式和演示幻灯片的示例，相应的占位符使用相同的颜色。

### 幻灯片母版

下面的示例母版幻灯片指定了五个形状，这些形状是标题、内容、日期、页脚和幻灯片编号的占位符。母版可以指定占位符内容的格式，或者可以省略并在版式幻灯片或幻灯片级别指定。

![Master slide](pptxImages\ppMasterSlide1.gif)

<p:sldMaster . . . >

<p:cSld>

. . .

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="22" name="标题占位符 21"/>

. . .

<p:nvPr>

<p:ph type="title"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="13" name="文本占位符 12"/>

. . .

<p:nvPr>

<p:ph type="body" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="14" name="日期占位符 13"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="2"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="页脚占位符 2"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="3"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="23" name="幻灯片编号占位符 22"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="4"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sldMaster>

### 幻灯片版式

用于特定幻灯片的幻灯片版式在幻灯片的 .rels 部分中指定。下面是演示文稿中第二张幻灯片的版式。在 slide2.xml.rels 文件中有以下关系：<Relationship Id="rId1" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/slideLayout" Target="../slideLayouts/slideLayout2.xml"/>。下面是上述母版幻灯片的一种可能版式。

<p:sldLayout . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

<p:nvPr>

<p:ph type="title"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="日期占位符 3"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="10"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="页脚占位符 4"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="11"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="幻灯片编号占位符 5"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="12"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="8" name="内容占位符 7"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sldLayout>

### 演示幻灯片

演示幻灯片内容可以通过 <p:ph> 元素的 idx 和 type 属性链接到版式占位符。如果在版式中指定了多个给定类型的占位符，则每个占位符必须使用唯一的 idx 值，与所应用版式的相应占位符匹配。当然，演示幻灯片上的内容不必基于占位符；在这种情况下，不为包含内容的形状指定 <p:ph> 元素。下面是使用上述版式的示例幻灯片。

![Presentation slide](pptxImages\ppSlide1.gif)

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

<p:nvPr>

<p:ph type="title"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="内容占位符 2"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="日期占位符 3"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="10"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="幻灯片编号占位符 4"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="12"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="页脚占位符 5"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="11"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sld>

我们可以采用上面的版式并添加两个更多的内容占位符，如下所示。

<p:sldLayout . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

<p:nvPr>

<p:ph type="title"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="日期占位符 3"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="10"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="页脚占位符 4"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="11"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="幻灯片编号占位符 5"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="12"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="8" name="内容占位符 7"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="19" name="内容占位符 18"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="13"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="21" name="文本占位符 20"/>

. . .

<p:nvPr>

<p:ph type="body" sz="quarter" idx="14"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sldLayout>

下面是基于上述编辑版式的演示幻灯片，以及一个不基于占位符的附加文本框。

<p:sld . . . >

<p:cSld>

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="标题 1"/>

. . .

<p:nvPr>

<p:ph type="title"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="日期占位符 3"/>

. . .

<p:nvPr>

<p:ph type="dt" sz="half" idx="10"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="页脚占位符 5"/>

. . .

<p:nvPr>

<p:ph type="ftr" sz="quarter" idx="11"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="幻灯片编号占位符 4"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="12"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="内容占位符 2"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="11" name="内容占位符 10"/>

. . .

<p:nvPr>

<p:ph sz="quarter" idx="13"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="12" name="文本占位符 11"/>

. . .

<p:nvPr>

<p:ph type="body" sz="quarter" idx="14"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="9" name="文本框 8"/>

. . .

<p:nvPr/>

</p:nvSpPr>

. . .

</p:sp>

</p:spTree>

</p:cSld>

</p:sld>

![Presentation slide](pptxImages\ppSlide2.gif)

页脚
