![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [Overview](drwOverview.md)
- 图片
  - [Overview](drwPic.md)
  - 图像属性
    - [图像数据](drwPic-ImageData.md)
    - [平铺或拉伸图像以填充](drwPic-tile.md)
    - [效果](drwPic-effects.md)
  - [非视觉属性](drwPic-nvPicPr.md)
  - [形状属性](drwSp-SpPr.md)
- 形状
  - [Overview](drwShape.md)
  - [非视觉属性](drwSp-nvSpPr.md)
  - [视觉属性](drwSp-SpPr.md)
    - [边界框大小](drwSp-size.md)
    - [边界框位置](drwSp-location.md)
    - 几何图形
      - [预设](drwSp-prstGeom.md)
      - [自定义](drwSp-custGeom.md)
    - [形状填充](drwSp-shapeFill.md)
      - [纯色填充](drwSp-SolidFill.md)
      - [图片填充](drwSp-PictFill.md)
      - [渐变填充](drwSp-GradFill.md)
      - [图案填充](drwSp-PattFill.md)
      - [组填充](drwSp-grpFill.md)
    - [效果](drwSp-effects.md)
    - [轮廓样式](drwSp-outline.md)
    - [2D变换](drwSp-rotate.md)
    - 3D
      - [形状属性](drwSp-3dProps.md)
      - [场景属性](drwSp-3dScene.md)
  - [样式](drwSp-styles.md)
  - [文本](drwSp-text.md)
    - [文本正文属性](drwSp-text-bodyPr.md)
      - [定位和内边距](drwSp-text-bodyPr-inset.md)
      - [适应、换行、变形和3D](drwSp-text-bodyPr-fit.md)
      - [列、垂直文本和旋转](drwSp-text-bodyPr-columns.md)
    - [段落](drwSp-text-paragraph.md)
      - [段落属性](drwSp-text-paraProps.md)
        - [项目符号和编号](drwSp-text-paraProps-numbering.md)
        - [间距、缩进和边距](drwSp-text-paraProps-margins.md)
        - [对齐、制表符、其他](drwSp-text-paraProps-align.md)
      - [文本运行属性](drwSp-text-runProps.md)
    - [列表属性](drwSp-text-lstPr.md)
- [Connectors](drwCxnSp.md)
  - [非视觉属性](drwSp-nvCxnSpPr.md)
- [文本](drwSp-textbox.md)
- 图表
- 图表
- [Tables](drwTable.md)
  - [定义结构](drwTableGrid.md)
  - [行、单元格、单元格内容](drwTableRowAndCell.md)
  - 单元格属性
    - [对齐、边距、方向](drwTableCellProperties-alignment.md)
    - [边框和填充](drwTableCellProperties-bordersFills.md)
  - [表格样式和属性](drwTableStyles.md)
- 在文档中的放置
  - [Overview](drwPicInWord.md)
  - [内联对象](drwPicInline.md)
  - [浮动对象](drwPicFloating.md)
    - [定位](drwPicFloating-position.md)
    - [文本环绕](drwPicFloating-textWrap.md)
- 在电子表格中的放置
  - [Overview](drwPicInSpread.md)
  - [绝对锚定](drwPicInSpread-absolute.md)
  - [单单元格锚定](drwPicInSpread-oneCell.md)
  - [双单元格锚定](drwPicInSpread-twoCell.md)
- [在演示文稿中的放置](drwPicInPresentation.md)

# DrawingML形状

文本 - 正文属性 - 适应、换行、变形和3D

## 文本适应：

形状内的文本可以被指定为自动缩放以适应文本框。或者，可以缩放形状以适应文本。文本缩放也可以关闭，这样文本框外的文本就不会显示。实际上，这是默认行为—不缩放。最后，有两个属性会影响文本在水平和垂直方向上的适应。（请注意，文本换行也会影响文本是否保留在框内。请参阅下面的文本换行。）首先，我们讨论通过<a:bodyPr>的子元素指定的整体缩放。

要缩放文本，请将<a:normAutoFit>添加为<a:bodyPr>的子元素。有两个属性会影响缩放。首先，您可以使用fontScale属性指定文本缩放到的原始字体大小的百分比，该属性以百分比表示。（如果省略，则假定为100%。）其次，使用lnSpcReduction属性指定段落行距减少的百分比，也是以百分比表示。（如果省略，则假定为0%。）

<xdr:txBody>

<a:bodyPr vertOverflow="clip" rtlCol="0" anchor="ctr">

<a:normAutoFit fontScale="75%" lnSpcReduction="20%"/>

</a:bodyPr>

<a:lstStyle/>

<a:p>

<a:pPr algn="l"/>

<a:r>

<a:rPr lang="en-US" sz="1100"/>

<a:t>这是形状内的一段文本。</a:t>

</a:r>

</a:p>

<a:p>

<a:pPr algn="ctr"/>

<a:r>

<a:rPr lang="en-US" sz="1100"/>

<a:t>这是第二段。</a:t>

</a:r>

</a:p>

</xdr:txBody>

下面是一个带文本的形状示例。文本适合框内。

![Shape with text](drwImages\drwSp-text-fit1.gif)

下面是相同的形状，但增加了一段文本。当我们指定<a:normAutoFit fontScale="75%" lnSpcReduction="20%"/>时，文本会缩放以适应形状，如下所示。

![Shape with text - text scaling](drwImages\drwSp-text-fit4.gif)

如果我们通过将<a:normAutoFit>替换为<a:noAutoFit />来关闭缩放，文本将不再适合框内，如下面的两张图片所示。

![带文本的形状](drwImages\drwSp-text-fit2.gif) ![带文本的形状](drwImages\drwSp-text-fit3.gif)

如果我们希望形状本身缩放以适应文本，那么我们添加<a:spAutoFit />。下面是带有额外第三段的形状，但还输入了额外的第四段和第五段。请注意，在Word中，只有在向形状添加更多文本后才会发生调整大小。

![Shape with text - text scaling](drwImages\drwSp-text-fit5.gif)

除了影响整体缩放的上述元素外，<a:bodyPr>还有两个属性会影响形状内文本的适应。它们是horzOverflow和vertOverflow。它们决定文本是否可以在水平和垂直方向上流出边界框。horzOverflow的可能值是：

- clip（在水平溢出处裁剪文本）
- overflow（允许水平溢出—默认值）

vertOverflow的可能值是：

- clip（在垂直溢出处裁剪文本）
- ellipsis（使用省略号表示有不可见的文本）
- overflow（允许垂直溢出—默认值）

下面是一个带有过多文本的示例形状，首先是默认行为。第二个示例显示了垂直溢出设置为clip的形状（<a:bodyPr rtlCol="0" anchor="ctr" vertOverflow="clip"/>）。第三个示例显示了垂直溢出设置为ellipsis的形状（<a:bodyPr rtlCol="0" anchor="ctr" vertOverflow="ellipsis"/>）。

![Shape with text - text overflow](drwImages\drwSp-text-over1.gif)

![带文本的形状 - 文本溢出](drwImages\drwSp-text-over2.gif) ![带文本的形状 - 文本溢出](drwImages\drwSp-text-over3.gif)

## 文本换行：

可以通过<a:bodyPr>上的wrap属性打开或关闭文本换行。可能的值是square和none。默认情况下，文本在边界框内换行（<a:bodyPr . . . wrap="square" />）。下面是一个关闭换行的形状（<a:bodyPr . . . wrap="none" />）。

![Shape with text - text wrap](drwImages\drwSp-text-wrap1.gif)

## 文本变形：

形状内的一段文本可以通过指定应用于文本的预设形状来变形，从而使文本变形。这是通过将<a:prstTxWarp>元素作为<a:bodyPr>的子元素来完成的。作为变形效果应用的实际形状在<a:prstTxWarp>的prst属性中给出。可能的值如下所示。请注意，形状调整值列表（<a:avLst>）可以指定为<a:prstTxWarp>的子元素。这些调整值在此不涉及。

- textArchDown
- textArchDownPour
- textArchUp
- textArchUpPour
- textButton
- textButtonPour
- textCanDown
- textCanUp
- textCascadeDown
- textCascadeUp
- textChevron
- textChevronInverted
- textCircle
- textCirclePour
- textCurveDown
- textCurveUp
- textDeflate
- textDeflateBottom
- textDeflateInflate
- textDeflateInflateDeflate
- textDeflateTop
- textDoubleWave1
- textFadeLeft
- textFadeRight
- textFadeUp
- textInflate
- textInflateBottom
- textInflateTop
- textNoShape
- textPlain
- textRingInside
- textRingOutside
- textSlantDown
- textSlantUp
- textStop
- textTriangle
- textTriangleInverted
- textWave1
- textWave2
- textWave4

下面是一些应用了向下拱形（textArchDown）的文本。

<xdr:txBody>

<a:bodyPr vertOverflow="clip" rtlCol="0" anchor="ctr">

<a:prstTxWarp prst="textArchDown"/>

<a:avLst/>

</a:prstTxWarp>

</a:bodyPr>

<. . .;

</xdr:txBody>

![Shape with text](drwImages\drwSp-text-warp1.gif)

## 行间距：

<a:bodyPr>上有几个属性会影响形状内文本行的间距。首先，spcFirstLastPara确定用户指定的段落间距是否适用于形状内的第一段和最后一段。如果属性值设置为false（默认值），则第一段和最后一段不遵循段落间距。下面是一个带有文本段落的形状，指定的段前间距为12磅。第一个示例遵循段落间距（<a:bodyPr anchor="ctr" rtlCol="0" spcFirstLastPara="1"/>），第二个示例不遵循（<a:bodyPr anchor="ctr" rtlCol="0" spcFirstLastPara="0"/>）。

![带文本的形状 - 行间距](drwImages\drwSp-text-lineSp2.gif) ![带文本的形状 - 行间距](drwImages\drwSp-text-lineSp1.gif)

还有一个compatLnSpc属性，它指定行间距是否以简单的方式使用字体场景确定。值可以是trust或false（默认值）。

## 抗锯齿文本：

通过在<a:bodyPr>上指定forceAA属性，可以强制形状内的文本以抗锯齿方式渲染，无论字体大小如何。值为true将强制抗锯齿；默认值为false。

## 3D属性：

与形状一样，可以为形状内的文本指定3D属性。它们为形状内的文本指定的方式与形状相同，只是包含元素是<a:bodyPr>元素而不是<a:spPr>元素。有关挤出、轮廓和斜角的详细信息，请参见[3D形状属性](drwSp-3dProps.md)。有关相机和灯光装置的详细信息，请参见[3D场景属性](drwSp-3dScene.md)。请注意，还有一个<a:flatTx>元素用于指示3D场景中不应有文本。它是span class="featuredItem"><a:bodyPr>的空子元素。

下面是一个具有3D属性的带文本的示例形状。

<xdr:txBody>

<a:bodyPr rtlCol="0" anchor="ctr">

<a:scene3d>

<a:camera prst="isometricRightUp"/>

<a:lightRig rig="freezing" dir="t">

<a:rot lat="0" lon="0" rev="15600000"/>

</a:lightRig>

</a:scene3d>

<a:sp3d extrusionH="57150" contourW="31750" prstMaterial="softEdge">

<a:bevelT w="38100" h="38100" prst="relaxedInset"/>

<a:bevelB w="38100" h="38100" prst="coolSlant"/>

<a:extrusionClr>

<a:schemeClr val="accent2">

<a:lumMod val="6000">

<a:lumOff val="4000">

</a:schemeClr>

</a:extrusionClr>

<a:contourClr>

<a:schemeClr val="tx2">

<a:lumMod val="6000">

<a:lumOff val="4000">

</a:schemeClr>

</a:contourClr>

</a:sp3d>

</a:bodyPr>

<. . .;

</xdr:txBody>

![Shape with text in 3D](drwImages\drwSp-text-3d.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
