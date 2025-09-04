![PresentationXML.com](images\PresentationMLBanner.png)

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

# DrawingML 表格 - 单元格属性 - 文本对齐、边距和方向

每个单元格可能有一组在<a:tcPr>元素中指定的属性，该元素是<a:tc>元素的子元素。

与水平和垂直对齐、边距、内容方向和文本溢出相关的属性由<a:tcPr>元素的属性决定。以下是允许的属性。

| 属性   | 描述                                                                        |
| ------ | --------------------------------------------------------------------------- |
| anchor | 定义文本在单元格内的垂直对齐方式。例如，<a:tcPr anchor="ctr">。可能的值有： |

- b \- 底部
- ctr \- 中心
- dist \- 垂直分布。当文本为水平时，行的间距与值为just时几乎相同。当文本为垂直时，字母会分布，这与just不同，因为它总是强制分布，即使只有一两个词。
- just \- 垂直分布。当文本为水平时，这会使行间距变大，与值为dist时几乎相同。当文本为垂直时，它会垂直对齐字母。
- t \- 顶部

anchorCtr | 值为布尔值。当为true时，它会修改anchor属性并将文本框本身居中，例如，文本可以沿着单元格的中心左对齐。  
horzOverflow | 指定单元格的裁剪行为。当值为overflow（<a:tcPr horzOverflow="overflow">）时，单元格中的文本自由流出单元格边界并可见。当值为clip时，文本被裁剪，不会出现在单元格边界之外。  
marB | 指定单元格的底部边距。例如，<a:tcPr marB="45720" anchor="ctr">。值可以是EMU或后跟单位标识符的数字。  
marL | 指定单元格的左边距。值可以是EMU或后跟单位标识符的数字。  
marR | 指定单元格的右边距。值可以是EMU或后跟单位标识符的数字。  
marT | 指定单元格的顶部边距。值可以是EMU或后跟单位标识符的数字。  
vert | 定义单元格的文本方向。可能的值包括（省略东亚选项）：

- horz \- 水平（默认）
- vert \- 垂直，每行顺时针旋转90度，使下一行位于前一行的左侧
- vert270 \- 垂直，每行顺时针旋转270度，使其从底部到顶部，下一行位于前一行的右侧
- wordArtVert \- 确定所有文本是否垂直（"一个字母在另一个字母之上"）
- wordArtVertRtl \- 指定垂直艺术字应从右到左显示，而不是从左到右

## 文本对齐

下面是一个内容垂直居中的单元格示例—即anchor属性的值为ctr。

<a:tr h="370840">

<a:tc>

. . .

<a:t>Bach</a:t>

. . .

<a:tcPr/>

</a:tc>

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>Beethoven</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr anchor="ctr"/>

</a:tc>

<a:tc>

. . .

<a:t>Brahms</a:t>

. . .

<a:tcPr/>

</a:tc>

</a:tr>

![DrawingML - Table](drwImages\drwTable-textAlignment1.gif)

如果我们更改上述xml，将anchorCtr设置为true（<a:tcPr anchor="ctr" anchorCtr="1"/>），文本将居中，如下所示：

![DrawingML - Table](drwImages\drwTable-textAlignment2.gif)

## 单元格边距

单元格内文本的边距由<a:tcPr>元素上的属性值设置。例如，下面是一个左边距和上边距设置为一英寸或914400 EMU的单元格示例（<a:tcPr marL="914400" marT="914400"/>）：

![DrawingML - Table](drwImages\drwTable-textAlignment3.gif)

## 文本方向

表格单元格内文本的方向由<a:tcPr>元素上的vert属性决定。下面是一个方向设置为vert的示例（<a:tcPr vert="vert"/>）。

![DrawingML - Table - Vertical alignment](drwImages\drwTable-textAlignment5.gif)

下面是一个方向设置为vert270的示例（<a:tcPr vert="vert270"/>）。

![DrawingML - Table - Vertical alignment](drwImages\drwTable-textAlignment4.gif)

## 文本溢出

文本是流出单元格还是被裁剪由<a:tcPr>元素上的horzOverflow属性决定。下面是一个overflow设置为overflow的示例（<a:tcPr vert="wordArtVert" horzOverflow="overflow"/>）。

![DrawingML - Table - Text Overflow](drwImages\drwTable-textOverflow.gif)

要裁剪文本，将overflow设置为clip（<a:tcPr vert="wordArtVert" horzOverflow="clip"/>）。

![DrawingML - Table - Text Overflow](drwImages\drwTable-textOverflow2.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
