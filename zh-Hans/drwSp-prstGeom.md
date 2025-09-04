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
      - [适应、环绕、弯曲和3D](drwSp-text-bodyPr-fit.md)
      - [列、垂直文本和旋转](drwSp-text-bodyPr-columns.md)
    - [段落](drwSp-text-paragraph.md)
      - [段落属性](drwSp-text-paraProps.md)
        - [项目符号和编号](drwSp-text-paraProps-numbering.md)
        - [间距、缩进和边距](drwSp-text-paraProps-margins.md)
        - [对齐、制表符、其他](drwSp-text-paraProps-align.md)
      - [运行属性](drwSp-text-runProps.md)
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

# DrawingML 形状

预设几何图形

The geometry or form of a shape can be either preset or custom. A set of preset geometric shapes are specified in the ECMA specification which any application should be able to render. A preset form is specified with a <a:prstGeom> element. The actual shape is specified with an attribute prst on that element. The possible values are specified below. Note that the preset geometry can be adjusted by specifying a list of shape adjustment values within a <a:avLst>, which is a child element of <a:prstGeom>. Shape adjustment values are not covered here. Note also that any preset geometrical shape can be alternately specified as a custom geometry. The alternate custom drawingML for each preset shape is found in the DrawingMLGeometries Appendix D to the ECMA specification, in an xml file called presetShapeDefinitions.xml

以下是预设梯形几何形状的示例。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

<a:off x="1171575" y="485775"/>

<a:ext cx="1171575" cy="647700"/>

</a:xfrm>

<a:prstGeom prst="trapezoid">

<a:avLst/>

</a:prstGeom>

<a:solidFill>

<a:schemeClr val="accent6"/>

<a:lumMod val="75000"/>

</a:schemeClr>

</a:solidFill>

</xdr:spPr>

. . .

</xdr:sp>

![Shape with preset geometry (trapezoid)](drwImages\drwSp-prstGeom.gif)

prst（即预定义形状）的可能值如下所示。有关形状的示例，请参见ECMA-376第3版（2011年6月），基础和标记语言参考§20.1.10.54。

- accentBorderCallout1
- accentBorderCallout2
- accentBorderCallout3
- accentCallout1
- accentCallout2
- accentCallout3
- actionButtonBackPrevious
- actionButtonBeginning
- actionButtonBlank
- actionButtonDocument
- actionButtonEnd
- actionButtonForwardNext
- actionButtonHelp
- actionButtonHome
- actionButtonInformation
- actionButtonMovie
- actionButtonReturn
- actionButtonSound
- 弧形
- bentArrow
- bentConnector2
- bentConnector3
- bentConnector4
- bentConnector5
- bentUpArrow
- bevel
- blockArc
- borderCallout1
- borderCallout2
- borderCallout3
- bracePair
- bracketPair
- callout1
- callout2
- callout3
- can
- chartPlus
- chartStar
- chartX
- chevron
- chord
- circularArrow
- cloud
- cloudCallout
- corner
- cornerTabs
- cube
- curvedConnector2
- curvedConnector3
- curvedConnector4
- curvedConnector5
- curvedDownArrow
- curvedLeftArrow
- curvedRightArrow
- curvedUpArrow
- decagon
- diagStripe
- diamond
- dodecagon
- donut
- doubleWave
- downArrow
- downArrowCallout
- ellipse
- ellipseRibbon
- ellipseRibbon2
- flowChartAlternateProcess
- flowChartCollate
- flowChartConnector
- flowChartDecision
- flowChartDelay
- flowChartDisplay
- flowChartDocument
- flowChartExtract
- flowChartInputOutput
- flowChartInternalStorage
- flowChartMagneticDisk
- flowChartMagneticDrum
- flowChartMagneticTape
- flowChartManualInput
- flowChartManualOperation
- flowChartMerge
- flowChartMultidocument
- flowChartOfflineStorage
- flowChartOffpageConnector
- flowChartOnlineStorage
- flowChartOr
- flowChartPredefinedProcess
- flowChartPreparation
- flowChartProcess
- flowChartPunchedCard
- flowChartPunchedTape
- flowChartSort
- flowChartSummingJunction
- flowChartTerminator
- folderCorner
- frame
- funnel
- gear6
- gear9
- halfFrame
- heart
- heptagon
- hexagon
- homePlate
- horizontalScroll
- irregularSeal1
- irregularSeal2
- leftArrow
- leftArrowCallout
- leftBrace
- leftBracket
- leftCircularArrow
- leftRightArrow
- leftRightArrowCallout
- leftRightCircularArrow
- leftRightRibbon
- irregularSeal1
- leftRightUpArrow
- leftUpArrow
- lightningBolt
- line
- lineInv
- mathDivide
- mathEqual
- mathMinus
- mathMultiply
- mathNotEqual
- mathPlus
- moon
- nonIsoscelesTrapezoid
- noSmoking
- notchedRightArrow
- octagon
- parallelogram
- pentagon
- pie
- pieWedge
- plaque
- plaqueTabs
- plus
- quadArrow
- quadArrowCallout
- rect
- ribbon
- ribbon2
- rightArrow
- rightArrowCallout
- rightBrace
- rightBracket
- round1Rect
- round2DiagRect
- round2SameRect
- roundRect
- rtTriangle
- smileyFace
- snip1Rect
- snip2DiagRect
- snip2SameRect
- snipRoundRect
- squareTabs
- star10
- star12
- star16
- star24
- star32
- star4
- star5
- star6
- star7
- star8
- straightConnector1
- stripedRightArrow
- sun
- swooshArrow
- teardrop
- trapezoid
- triangle
- upArrow
- upArrowCallout
- upDownArrow
- upDownArrowCallout
- uturnArrow
- verticalScroll
- wave
- wedgeEllipseCallout
- wedgeRectCallout
- wedgeRoundRectCallout

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
