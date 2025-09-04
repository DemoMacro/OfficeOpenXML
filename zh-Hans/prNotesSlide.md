![PresentationXML.com](pptxImages\PresentationMLBanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [绘图ML](drwOverview.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md)

- [Presentation](prPresentation.md)
- 演示
  - [过渡效果](prSlide-transitions.md)
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

# PresentationML 幻灯片 - 备注幻灯片

备注幻灯片包含相应演示文稿幻灯片的缩略图以及显示在缩略图下方的备注。幻灯片缩略图包含在类型为'sldImg'的占位符中。备注文本包含在类型为'body'的占位符中。有关占位符的更多信息，请参见[幻灯片 - 概述](prSlide.md)。备注幻灯片可以具有额外内容、不同的页眉和页脚，以及与相应演示文稿幻灯片不同的样式。例如，下面显示了一个带有文本框的备注幻灯片，表明该幻灯片是机密的。下面是同一幻灯片的普通视图，即作为演示文稿幻灯片。

![notes slide with text box](pptxImages\ppNotesSlide1.gif)

同一幻灯片作为演示文稿幻灯片（即普通视图）如下。

![notes slide in normal view](pptxImages\ppNotesSlide2.gif)

备注幻灯片的基础XML如下。缩略图和备注占位符已着色。

<p:notes . . . >

<p:cSld>

. . .

<p:spTree>

. . .

<p:sp>

<p:nvSpPr>

<p:cNvPr id="2" name="幻灯片图像占位符 1"/>

. . .

<p:nvPr>

<p:ph type="sldImg"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="3" name="备注占位符 2"/>

. . .

<p:nvPr>

<p:ph type="body" idx="1"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="幻灯片编号占位符 3"/>

. . .

<p:nvPr>

<p:ph type="sldNum" sz="quarter" idx="10"/>

</p:nvPr>

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="文本框 4"/>

. . .

</p:nvSpPr>

<p:spPr>

. . .

</p:spPr>

<p:txBody>

. . .

<p:p>

<p:r>

<p:rPr . . ./>

<p:t>机密</p:t>

</p:r>

</p:p>

. . .

</p:txBody>

. . .

</p:sp>

</p:spTree>

</p:cSld>

. . .

</p:notes>

演示文稿的备注幻灯片每个都包含在备注幻灯片部件中（在notesSlides文件夹内）。每个有备注的幻灯片都有一个备注幻灯片。如果幻灯片有备注幻灯片，那么该备注幻灯片会在幻灯片的.rels文件中被引用。因此，例如，如果幻灯片2有备注，幻灯片2的.rels文件将有一个与备注幻灯片的关系：<Relationship Id="rId2" Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/notesSlide" Target="../notesSlides/notesSlide2.xml"/>。备注幻灯片在presentation.xml中不被引用。

备注幻灯片的内容模型与演示文稿幻灯片类似，只是它不包含计时或过渡元素。显著差异与它们拥有的占位符有关。演示文稿有一组带有占位符的形状和其他内容。备注幻灯片不具有与其相应演示文稿幻灯片相同的形状和内容。它只有演示文稿幻灯片缩略图像的占位符，以及备注内容的占位符，并且它可以根据需要具有其他形状和内容（在备注母版中为所有备注幻灯片定义，或在该备注幻灯片中为特定备注幻灯片定义）。有关各种幻灯片类型内容模型的比较，请参见[幻灯片 - 概述](prSlide.md)。备注幻灯片的根元素是<p:notes>元素。下面是一个显示根元素可能子元素的表格，后跟一个显示根<p:notes>元素属性的表格。

### 元素：

| 元素          | 描述                                                                                                              |
| ------------- | ----------------------------------------------------------------------------------------------------------------- |
| <p:clrMapOvr> | 指定对母版幻灯片中<p:clrMap>指定的配色方案的覆盖。有关详细信息，请参见[幻灯片属性 - 配色方案](prSlide-color.md)。 |
| <p:cSld>      | 指定幻灯片内容。有关详细信息，请参见[幻灯片 - 通用幻灯片数据](prCommonSlideData.md)。                             |

属性如下：

### 属性：

| 属性             | 描述                                                 |
| ---------------- | ---------------------------------------------------- |
| showMasterPhAnim | 指定是否显示母版幻灯片中占位符上的动画。值为布尔值。 |
| showMasterSp     | 指定是否应在幻灯片上显示母版中的形状。值为布尔值。   |

页脚
