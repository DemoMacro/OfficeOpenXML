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

# PresentationML 幻灯片 - 属性 - 切换效果

幻灯片之间的切换效果存储在幻灯片级别，因此如果需要，每张幻灯片可以有不同的切换效果。存储在幻灯片内的切换效果在该幻灯片内容呈现后发生。因此，首先呈现第一张幻灯片，然后是幻灯片1中存储的切换效果，接着是幻灯片2，然后是幻灯片2中存储的切换效果，依此类推。切换效果信息在<p:transition>元素中指定，该元素可以是<p:sld>、<p:sldLayout>或<p:sldMaster>的子元素。

切换效果基本上有三个组成部分：(1)切换效果的类型，(2)触发切换效果的因素，以及(3)切换效果的速度。类型由<p:transition>的子元素指定，其他两个组成部分作为属性指定。

下面是一个示例切换效果，包含一个持续2秒的中速棋盘切换效果。

<p:sld>

<p:cSld>

. . .

</p:cSld>

<p:clrMapOvr>

. . .

</p:clrMapOvr>

<p:transition spd="med" advTm="2000">

<p:checker/>

</p:transition>

<p:timing>

. . .

</p:timing>

</p:sld>

## 切换效果类型

切换效果的类型被指定为<p:transition>元素的子元素。以下是可能的切换效果类型。

| 元素           | 描述                                                                                                                                                                       |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p:blinds/>    | 具有一个dir属性来指定方向，可能的值为horz和vert。                                                                                                                          |
| <p:checker/>   | 具有一个dir属性来指定方向，可能的值为horz和vert。                                                                                                                          |
| <p:circle/>    | 具有一个dir属性来指定方向，可能的值为horz和vert。                                                                                                                          |
| <p:comb/>      | 具有一个dir属性来指定方向，可能的值为horz和vert。                                                                                                                          |
| <p:cover/>     | 具有一个dir属性来指定方向，可能的值为d（下）、l（左）、r（右）、u（上）、ld（左下）、lu（左上）、rd（右下）、ru（右上）。                                                  |
| <p:cut/>       | 具有一个thruBlk（通过黑色过渡）属性来指定切换效果是否从黑屏开始，然后通过黑色过渡到新幻灯片；可能的值为布尔值。                                                            |
| <p:diamond/>   |
| <p:dissolve/>  |
| <p:fade/>      | 具有一个thruBlk（通过黑色过渡）属性来指定切换效果是否从黑屏开始，然后通过黑色过渡到新幻灯片；可能的值为布尔值。                                                            |
| <p:newsflash/> |
| <p:plus/>      |
| <p:pull/>      | 具有一个dir属性来指定方向，可能的值为d（下）、l（左）、r（右）、u（上）、ld（左下）、lu（左上）、rd（右下）、ru（右上）。                                                  |
| <p:push/>      | 具有一个dir属性来指定方向，可能的值为d（下）、l（左）、r（右）、u（上）。                                                                                                  |
| <p:random/>    | 应用程序随机应用可用的切换效果之一。                                                                                                                                       |
| <p:randomBar/> | 具有一个dir属性来指定方向，可能的值为horz和vert。                                                                                                                          |
| <p:sndAc>      | 指定要使用的声音动作。该元素包含停止（<p:endSnd/>）和开始（<p:stSnd/>）动作的子元素。这些元素中的每一个都包含一个声音元素<p:snd r:embed="rId2"/>，与嵌入的声音文件有关系。 |
| <p:split/>     | 具有一个dir属性来指定方向，可能的值为in和out。还有一个orient属性来指定方向，值为horz和vert。                                                                               |
| <p:strips/>    | 具有一个dir属性来指定方向，可能的值为ld（左下）、lu（左上）、rd（右下）、ru（右上）。                                                                                      |
| <p:wedge/>     |
| <p:wheel/>     | 具有一个spokes属性来指定轮子中的辐条数量；值为整数。                                                                                                                       |
| <p:wipe/>      | 具有一个dir属性来指定方向，可能的值为d（下）、l（左）、r（右）、u（上）。                                                                                                  |
| <p:zoom/>      | 具有一个dir属性来指定方向，可能的值为in和out。                                                                                                                             |

## 切换效果触发器

幻灯片可以通过鼠标点击前进并发生切换效果，或者在指定时间后自动前进。要指定鼠标点击应触发切换效果，请为<p:transition>的advClick属性指定true值。请注意，如果未指定该属性，这是默认行为。即使幻灯片将在指定时间后自动前进，如果未指定此属性或将其设置为true，鼠标点击仍将使幻灯片前进。如果设置了<p:transition>的advTm属性，幻灯片将在指定时间后自动前进，无需鼠标点击。该属性的值以毫秒为单位，表示切换效果应该发生的时间。在上面的示例中，切换效果将在2秒后发生（<p:transition spd="med" advTm="2000">）。

## 切换效果速度

幻灯片切换效果的速度由<p:transition>的spd属性指定。可能的值为fast、med和slow。

页脚
