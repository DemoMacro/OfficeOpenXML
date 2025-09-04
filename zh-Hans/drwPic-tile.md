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
    - 几何
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
- 文档中的放置
  - [Overview](drwPicInWord.md)
  - [内联对象](drwPicInline.md)
  - [浮动对象](drwPicFloating.md)
    - [定位](drwPicFloating-position.md)
    - [文本环绕](drwPicFloating-textWrap.md)
- 电子表格中的放置
  - [Overview](drwPicInSpread.md)
  - [绝对锚定](drwPicInSpread-absolute.md)
  - [单单元格锚定](drwPicInSpread-oneCell.md)
  - [双单元格锚定](drwPicInSpread-twoCell.md)
- [演示文稿中的放置](drwPicInPresentation.md)

# DrawingML图片

图像属性 - 平铺、拉伸或显示图像的一部分

## 显示图像的一部分（裁剪）

<pic:blipFill>元素内的<a:srcRect>元素指定用于填充的blip或图像的部分。如果未指定任何属性，这表示图像未被裁剪。否则，b（底部）、l（左侧）、r（右侧）和t（顶部）属性指定矩形的裁剪。图像的每个边缘由从边界框边缘的百分比偏移定义。正百分比指定内缩，负百分比指定外延。因此，例如，25%的左侧偏移表示图像的左边缘位于边界框左边缘的右侧，偏移量为边界框宽度的25%。

<pic:blipFill>

<a:blip r:embed="rId4" cstate="print"/>

<a:srcRect l="25000"/>

</pic:blipFill>

Word 2007示例：

![srcRect](drwImages\drwImagesrcRect.gif)

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.1.8.55。

## 拉伸图像

图像可以通过<pic:blipFill>元素内的<a:stretch>元素拉伸以填充目标矩形。<a:stretch>包含一个指定填充矩形的<a:fillRect>元素。填充矩形的每个边缘由从图片边界框相应边缘的百分比偏移定义。正百分比指定内缩，负百分比指定外延。

<pic:blipFill>

<a:blip r:embed="rId4" cstate="print"/>

<a:stretch>

<a:fillRect l="25000"/>

</a:stretch/>

</pic:blipFill>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.1.8.56和§ 20.1.8.30。

<a:fillRect>元素具有与上述<a:srcRect>元素相同的属性。

以下是不拉伸、拉伸但无偏移或外延、以及带内缩的拉伸示例。拉伸图像是相对于图像的边界框而言的。在示例中，边界框（cx="3438400" cy="2828800"）大于图像（cx="2438400" cy="1828800"）。第一个示例没有拉伸。

![no stretching](drwImages\drwStretch-none.gif)

第二个有拉伸，但没有偏移或内缩。

![stretching without offset](drwImages\drwStretch-noOffset.gif)

第三个有拉伸，左侧有25%的内缩。

![stretching with offset](drwImages\drwStretch-Offset.gif)

## 平铺图像

使用<pic:blipFill>元素内的<a:tile>元素指定图像平铺以填充边界框。<a:tile>元素在边界框内定义一个平铺或矩形，该矩形在边界框上平铺以填充整个区域。

<pic:blipFill>

<a:blip r:embed="rId4" cstate="print"/>

<a:tile sx="20%" sy="50%" flip="none" algn="br"/>

</pic:blipFill>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 20.1.8.58。

<a:tile>元素具有以下属性。

| 属性 | 描述                                                                                                                                                                        |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| algn | 指定第一个平铺的对齐位置。对齐发生在缩放之后但在任何偏移之前。可能的值有b（底部）、bl（左下）、br（右下）、ctr（中心）、l（左）、r（右）、t（顶部）、tl（左上）和tr（右上） |
| flip | 指定图像应翻转的方向。可能的值有：none（无）、x（水平）、xy（水平和垂直）和y（垂直）                                                                                        |
| sx   | 指定水平缩放的量。值以百分比表示。                                                                                                                                          |
| sy   | 指定垂直缩放的量。值以百分比表示。                                                                                                                                          |
| tx   | 指定对齐后的额外水平偏移。值以百分比表示。                                                                                                                                  |
| ty   | 指定对齐后的额外垂直偏移。值以百分比表示。                                                                                                                                  |

Word 2007示例：

以下是平铺的示例。第一个平铺位于右下角。图像在任何方向上都没有翻转，但图像在水平方向上缩放到20%，在垂直方向上缩放到50%。

![Picture Tiling](drwImages\drwTile.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
