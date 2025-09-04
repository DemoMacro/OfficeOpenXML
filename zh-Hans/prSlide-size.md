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

# PresentationML 幻灯片 - 属性 - 大小

演示文稿中幻灯片的大小是通过演示文稿根元素中的<p:sldSZ>元素为整个演示文稿设置的，而备注幻灯片的大小是通过演示文稿根元素中的<p:notesSz>设置的。<p:sldSZ>和<p:notesSz>是具有三个属性的空元素。cx和cy属性分别指定幻灯片矩形的长度和宽度（以EMU为单位）。注意，对象可以在矩形外部指定；该大小指定了演示文稿在演示或打印时显示的背景表面。<p:sldSZ>有第三个属性type，它指定应使用的大小类型，以预期演示文稿的交付平台。可能的值如下所列。

- 35毫米
- A3
- A4
- B4ISO
- B4JIS
- B5ISO
- B5JIS
- 横幅
- 自定义
- hagakiCard（日本明信片）
- 分类账
- 信纸
- 投影仪
- 屏幕16x10
- 屏幕16x9
- 屏幕4x3

下面是示例幻灯片和备注大小。

<p:presentation>

. . .

<p:sldSz cx="9144000" cy="6858000" type="screen4x3"/>

<p:notesSz cx="6858000" cy="9144000"/>

. . .

</p:presentation>

![Slide background - bgPr](pptxImages\ppSlide-size1.gif)

下面是相同的幻灯片，但幻灯片长度已减少到cx="7144000"。

![Slide background - bgPr](pptxImages\ppSlide-size2.gif)

页脚
