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

非视觉属性

<sp>元素内的<nvSpPr>元素指定形状的非视觉属性。实际属性位于子元素中 - <cNvPr>（用于ID、名称、标题、描述和隐藏）和<cNvSpPr>（锁定属性和文本框）。演示文稿还有第三个子元素<nvPr>（用于与形状关联的多媒体以及幻灯片布局和幻灯片母版中的占位符）。

请注意，非视觉属性位于不同的命名空间中，具体取决于文档类型。示例显示了带有前缀'xdr'的电子表格drawingML命名空间。对于演示文稿，非视觉属性位于带有前缀'p'的主演示文稿ML命名空间中。

<xdr:sp macro="" textlink="">

<xdr:nvSpPr>

<xdr:cNvPr id="2" name="圆角矩形 1"/>

<xdr:cNvSpPr/>

</xdr:nvSpPr>

. . .

</xdr:sp>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 19.3.1.34（演示文稿）和§ 20.5.2.23（电子表格）。

## ID、名称、标题和描述

图片的id、名称、标题和描述可以通过<cNvPr>元素的属性指定：<cNvPr id="222" name="圆角矩形 1" title="我的形状" descr="这是描述"/>。id是一个整数，指定唯一标识符。名称是一个字符串。标题是一个指定标题的字符串。descr是用于不显示对象的辅助技术的替代文本。最后，请注意<cNvPr>可以有子元素<hlinkClick>和<hlinkhover>用于此处未涵盖的链接。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 19.3.1.12（演示文稿）和§ 20.5.2.8（电子表格）。

## 隐藏

可以通过在<cNvPr>元素上指定hidden属性来隐藏形状：<cNvPr hidden="true">。但是，请注意应用程序可能有允许显示对象的设置。

## 形状调整大小、裁剪、旋转、更改纵横比、移动、选择

形状的锁定属性通过<cNvSpPr>元素内的<spLocks>元素指定。形状大小的各个方面可以通过<spLocks>上的属性指定。如果未指定属性，则假定可以更改这些属性。例如，要禁止更改纵横比，请将noChangeAspect属性指定为true。

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
- noTextEdit

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考§ 19.3.1.13（演示文稿）和§ 20.5.2.9（电子表格）。

## 文本框

<cNvSpPr>元素有一个txBox属性，它指定形状是文本框。该值是一个布尔值。但是，需要注意的是，即使此属性未指定为true，形状仍然可以附加文本。文本框只是具有特定属性的特殊形状。

## 演示文稿中的多媒体

可以使用<nvPr>的子元素将多媒体与对象关联。子元素中指定的各种媒体类型包括<audioCd>、<audioFile>、<quickTimeFile>、<videoFile>、<waveAudioFile>。此处不涵盖这些媒体类型的详细信息。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
