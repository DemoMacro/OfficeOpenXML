![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [Overview](drwOverview.md)
- 图片
  - [Overview](drwPic.md)
  - 图片属性
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

文本 - 间距、缩进和边距

## 段落内的垂直行间距

形状中文本段落内行之间的垂直间距是通过段落的<a:pPr>元素内的<a:lnSpc>元素指定的。间距可以指定为百分比或点大小。百分比使用<a:spcPct>作为<a:lnSpc>的子元素来指定。该百分比基于段落中尺寸最大的运行。以点大小表示的间距使用<a:spcPts>作为<a:lnSpc>的子元素来指定，其中100等于1点，1200等于12点。两个子元素都在val属性中指定实际值。如果未指定行间距，则间距由行中最大的文本片段的大小决定。下面是一个行间距设置为双倍间距或200%的示例形状。

<a:pPr>

<a:lnSpc>

<a:spcPct val="200000"/>

</a:lnSpc>

</a:pPr>

![Shape with text - line spacing](drwImages\drwSp-text-vertSpace1.gif)

## 段落前后的间距

形状内段落前后的间距分别使用<a:spcBef>和<a:spcAft>元素指定。每个都可以使用子元素<a:spcPct>和<a:spcPts>指定为百分比或点数。下面是一个具有两个段落的形状，段落后的间距指定为12点。

<a:pPr>

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - line spacing](drwImages\drwSp-text-spcAft.gif)

## 边距

形状中文本段落的左边距和右边距分别使用<a:pPr>元素上的marL和marR属性指定。这些边距是文本正文内边距之外的额外边距。请参阅[文本正文属性 - 定位和内边距](drwSp-text-bodyPr-inset.md)。边距值在0到51206400之间。下面是一个具有两个段落的形状；第一个段落的左边距设置为1/2英寸（marL="457200"）。

<a:pPr marL="457200">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - margins](drwImages\drwSp-text-margins.gif)

## 缩进

段落中文本第一行的缩进是通过<a:pPr>元素上的indent属性指定的。该值以EMU（英制公制单位）指定，如果省略该属性，则隐含值为-342900。下面是与上面相同的形状和文本，只是第一段落应用了0.3英寸的缩进。

<a:pPr marL="457200" indent="274320">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - margins](drwImages\drwSp-text-indent.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
