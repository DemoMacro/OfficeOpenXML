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

图像属性 - 非视觉属性

<pic:pic>元素内的<pic:nvPicPr>元素指定了图片的非视觉属性。实际属性位于两个子元素中 - <pic:cNvPr>和<pic:cNvPicPr>。

请注意，非视觉属性位于不同的命名空间中，具体取决于文档类型。示例显示了drawingML的图片命名空间，前缀为'pic'。对于演示文稿，非视觉属性位于主presentationML命名空间中，前缀为'p'。对于电子表格，命名空间是电子表格drawingML命名空间，前缀为'xdr'。

<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">

<pic:nvPicPr>

<pic:cNvPr id="0" name="Blue hills.jpg"/>

<pic:cNvPicPr/>

</pic:nvPicPr>

<pic:blipFill>

. . .

</pic:blipFill>

<pic:spPr>

. . .

</pic:spPr>

</pic:pic>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.2.2.4。

## ID、名称、标题和描述

图片的id、名称、标题和描述可以通过<pic:cNvPr>元素的属性指定：<pic:cNvPr id="222" name="Blue hills.jpg" title="This is the title" descr="This is the description"/>。id是一个整数，指定唯一标识符。name是一个字符串，通常存储原始文件名。title是一个字符串，指定标题。descr是替代文本，用于不显示图片的辅助技术。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.2.2.3。

## 图片调整大小、裁剪、旋转、更改纵横比、移动、选择

图片的锁定属性通过<pic:cNvPicPr>元素内的<a:picLocks>元素指定。图片或形状大小的各个方面可以通过<a:picLocks>上的属性指定。如果未指定属性，则假定这些属性可以更改。例如，要禁止更改纵横比，请将noChangeAspect属性指定为true。

以下是最有用的属性：

- noChangeAspect
- noCrop
- noMove
- noResize
- noRot（无旋转）
- noSelect

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 20.1.2.2.31。

还要注意，<pic:cNvPicPr>元素上的preferRelativeResize属性指定用户界面是否应根据图片的当前大小（false）或其原始大小（true）显示图片的调整大小。

## 隐藏

可以通过在<pic:cNvPr>元素上指定hidden属性来隐藏图片：<pic:cNvPr hidden="true">。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
