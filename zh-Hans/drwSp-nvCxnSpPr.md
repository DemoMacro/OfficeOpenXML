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
      - [适应、环绕、变形和3D](drwSp-text-bodyPr-fit.md)
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

# DrawingML 连接符

非视觉属性

<cxnSp>元素内的<nvCxnSpPr>元素指定连接符的非视觉属性。实际属性位于子元素中 - <cNvPr>（用于id、名称、标题、描述和隐藏）和<cNvCxnSpPr>（锁定属性和连接符端点）。演示文稿还有第三个子元素<nvPr>（用于与连接符关联的多媒体）。

<p:cxnSp>

<p:nvCxnSpPr>

<p:cNvPr id="9" name="直线箭头连接符 8"/>

<p:cNvCxnSpPr/>

<a:stCxn id="4" idx="3"/>

<a:endCxn id="5" idx="1"/>

</p:cNvCxnSpPr/>

</p:nvCxnSpPr>

. . .

</p:cxnSp>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 19.3.1.29（演示文稿）和 § 20.5.2.19（电子表格）。

## ID、名称、标题和描述

连接符的id、名称、标题和描述可以通过<cNvPr>元素的属性指定：<cNvPr id="9" name="直线箭头连接符 8" title="我的连接符" descr="这是描述"/>。id是一个整数，指定唯一标识符。name是一个字符串。title是一个指定标题的字符串。descr是用于不显示对象的辅助技术的替代文本。最后，请注意<cNvPr>可以有用于链接的子元素<hlinkClick>和<hlinkhover>；这些内容在此不作介绍。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 19.3.1.12（演示文稿）和 § 20.5.2.8（电子表格）。

## 隐藏

可以通过在<cNvPr>元素上指定hidden属性来隐藏连接符：<cNvPr hidden="true">。但是，请注意应用程序可能有允许显示该对象的设置。

## 形状调整大小、裁剪、旋转、更改纵横比、移动、选择

形状的锁定属性通过<cNvCxnSpPr>元素内的<cxnSpLocks>元素指定。连接符可以更改和编辑的各个方面通过<cxnSpLocks>上的属性指定。如果未指定属性，则假定可以更改这些属性。例如，要禁止更改纵横比，请将noChangeAspect属性指定为true。

以下是最有用的属性：

- noAdjustHandles（应用程序不应显示调整手柄）
- noChangeArrowHandles（应用程序不应允许箭头更改）
- noChangeAspect
- noChangeShapeType
- noEditPoints（应用程序不应允许形状点更改）
- noGrp（禁止形状分组）
- noMove
- noResize
- noRot（无旋转）
- noSelect

## 连接符起点和终点

<cNvCxnSpPr>元素有子元素<stCxn>和<endCxn>，它们指定连接符的起点和终点连接到哪些形状以及形状上的哪些点。两个子元素都有id属性和idx属性。id属性指定起点或终点所附加到的形状的id。也就是说，每个形状都有一个由<p:nvSpPr>元素内的<p:cNvPr>元素的id属性指定的id（假设是演示文稿文档）。这是stCxn或endCxn的id属性所引用的属性。因此，例如，假设我有三个id分别为4、5和6的形状，以及一个连接形状4和5的连接符。XML如下所示。

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4 name="圆角矩形 3"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="圆角矩形 4"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="圆角矩形 5"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:cxnSp>

<p:nvCxnSpPr>

<p:cNvPr id="8" name="直线箭头连接符 7"/>

<p:cNvCxnSpPr>

<a:stCxn id="4" idx="3"/>

<a:endCxn id="5" idx="1"/>

</p:cNvCxnSpPr>

<p:nvPr/>

</p:nvCxnSpPr>

</p:cxnSp>

![Connector in a presentation](drwImages\drwSp-connector2.gif)

要改为连接到id=6的下方形状，我按如下所示更改XML。

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4 name="圆角矩形 3"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="圆角矩形 4"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="6" name="圆角矩形 5"/>

. . .

</p:nvSpPr>

. . .

</p:sp>

<p:cxnSp>

<p:nvCxnSpPr>

<p:cNvPr id="8" name="直线箭头连接符 7"/>

<p:cNvCxnSpPr>

<a:stCxn id="4" idx="3"/>

<a:endCxn id="6" idx="0"/>

</p:cNvCxnSpPr>

<p:nvPr/>

</p:nvCxnSpPr>

</p:cxnSp>

![Connector in a presentation](drwImages\drwSp-connector3.gif)

起点和终点元素上的idx属性指定形状上连接点的索引。在上面的示例中，连接符从形状4（在连接点3）连接到形状6，在索引为0的连接点。如果我们将终点的idx值更改为<a:endCxn id="6" idx="1"/>，我们就会移动连接符在形状6上的附加位置。

![Connector in a presentation](drwImages\drwSp-connector4.gif)

最后，请记住连接符形状的端点类型和样式由<a:ln>元素确定。有关这些属性的详细信息，请参见[形状 - 轮廓](drwSp-outline.md)。

## 演示文稿中的多媒体

可以使用<nvPr>的子元素将多媒体与对象关联。子元素中指定的各种媒体类型包括<audioCd>、<audioFile>、<quickTimeFile>、<videoFile>、<waveAudioFile>。这些媒体类型的详细信息在此不作介绍。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
