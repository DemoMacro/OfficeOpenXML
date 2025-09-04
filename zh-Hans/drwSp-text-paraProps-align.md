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

文本 - 对齐、制表符、其他

## 对齐

形状中段落内文本的对齐方式是通过段落的<a:pPr>元素上的algn属性指定的。最常见的值是：

- l（左，默认值）
- r（右）
- ctr（居中）
- just（两端对齐）
- dist（分散对齐，将文本分布在整个行上）

下面是一个示例形状，其第一段的对齐方式设置为两端对齐（algn="just"）。

<a:pPr algn="just">

<a:spcAft>

<a:spcPts val="1200"/>

</a:spcAft>

</a:pPr>

![Shape with text - alignment](drwImages\drwSp-text-align.gif)

## 字体对齐

行上单词的垂直对齐方式是通过段落的<a:pPr>元素上的fontAlgn属性指定的。当一行中的某些单词比其他单词大时，这很重要。在这种情况下，较小的单词应该相对于较大的单词定位在中间、底部还是顶部？可能的值是：

- auto（当文本流向为水平时，这与下面的base相同）
- b（一行的最底部，可能与基线不同，因为有像g、q和y这样的字母悬挂在基线下方）
- base（基线—默认值）
- ctr（居中）
- t（顶部）

下面是一个字体对齐在顶部的示例（fontAlgn="t"）。

<a:pPr fontAlgn="t"/>

![Shape with text - font alignment](drwImages\drwSp-text-fontAlign.gif)

## 制表符

形状中段落的自定义制表位可以通过<a:pPr>的子元素<a:tabLst>来指定。<a:tabLst>可以包含一个或多个制表位定义，每个定义都在一个<a:tab>中。每个这样的<a:tab>都有一个pos属性，指定相对于左边距的制表位（以EMU为单位或以数字后紧跟单位标识符的形式），每个制表符按顺序增加其pos值。每个<a:tab>还可以有一个algn属性，指定文本的对齐方式。可能的值是ctr、dec（小数点对齐，即小数点前右对齐，小数点后左对齐）、l和r。

默认制表符大小也可以通过<a:pPr>上的defTabSz属性指定。可能的值以EMU为单位或以数字后紧跟单位标识符的形式指定。下面是一个文本之间有制表符的形状，默认大小设置为1英寸或914400 EMU。

<a:pPr defTabSz="914400"/>

![Shape with text - tabs](drwImages\drwSp-text-tabs1.gif)

下面是相同的形状，但具有如下自定义制表符。

<a:pPr>

<a:tabLst>

<a:tab pos="914400" algn="l"/>

<a:tab pos="1371600" algn="l"/>

<a:tab pos="1600200" algn="l"/>

<a:tab pos="1714500" algn="l"/>

<a:tabLst>

</a:pPr>

![Shape with text - tabs](drwImages\drwSp-text-tabs2.gif)

## 单词断行

默认情况下，一个长的拉丁单词可以在没有连字符的情况下断行并换到下一行。但是，可以通过在<a:pPr>上指定latinLnBrk属性来防止这种行为。false或0的值将防止在这种情况下断行。下面首先是latinLnBrk="1"的示例。

![Shape with text - latin line break](drwImages\drwSp-text-latinLnBrk1.gif)

下面是相同的形状和相同的段落，但使用latinLnBrk="0"。

![Shape with text - latin line break](drwImages\drwSp-text-latinLnBrk2.gif)

## 悬挂标点

可以通过在<a:pPr>上指定hangingPunct属性来防止文本运行末尾的标点符号被带到下一行。true或1的值强制标点符号不被带到下一行，而false值允许标点符号被带到下一行。默认值为false。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
