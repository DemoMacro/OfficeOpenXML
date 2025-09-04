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

3D场景属性

可选的3D场景属性与形状相对于观察者的位置有关—例如背景、观察者的视角和照明。它们在容器<a:scene3d>元素中指定，该元素位于<a:spPr>（形状属性）元素内。有三种可能的3D场景属性—背景（此处未涵盖）、相机和灯光装置。每个都是<a:scene3d>的子元素。下面是一个形状，其相机位置设置为预设的等轴左下，但已从预设位置旋转，并使用顶部的预设"日落"照明。

<xdr:sp macro="" textlink="">

. . .

<xdr:spPr>

<a:xfrm>

. . .

</a:xfrm>

<a:prstGeom>

. . .

</a:prstGeom>

<a:solidFill>

. . .

</a:solidFill>

<a:scene3d>

<a:camera prst="isometricLeftDown"></a:camera>

<a:lightRig rig="sunset" dir="t"/>

</a:scene3d>

<a:sp3d extrusionH="254000"/>

</xdr:spPr>

. . .

</xdr:sp>

![Shape size](drwImages\drwSp-3Dscene1.gif)

## 相机

3D场景中相机的位置和属性修改场景的视图，并通过<a:camera>元素指定。有多个预设的相机位置位置可以通过prst属性指定。它们定义了空间中常见预设旋转的起点。可能的值包括：

- 等轴底部向下
- 等轴底部向上
- 等轴左侧向下
- 等轴左侧向上
- 等轴偏轴1左侧
- 等轴偏轴1右侧
- 等轴偏轴1顶部
- 等轴偏轴2左侧
- 等轴偏轴2右侧
- 等轴偏轴2顶部
- 等轴偏轴3底部
- 等轴偏轴3左侧
- 等轴偏轴3右侧
- 等轴偏轴4底部
- 等轴偏轴4左侧
- 等轴偏轴4右侧
- 等轴右侧向下
- 等轴右侧向上
- 等轴顶部向下
- 等轴顶部向上
- 斜角底部
- 斜角底部左侧
- 斜角底部右侧
- 斜角左侧
- 斜角右侧
- 斜角顶部
- 斜角顶部左侧
- 斜角顶部右侧
- 正交正面
- 透视上方
- 透视上方左朝向
- 透视上方右朝向
- 透视下方
- 透视对比左朝向
- 透视对比右朝向
- 透视正面
- 透视英雄极左朝向
- 透视英雄极右朝向
- 透视英雄极左朝向
- 透视英雄右朝向
- 透视左侧
- 透视放松
- 透视适度放松
- 透视右侧

预设位置可以通过指定子元素<a:rot>来更改。<a:rot>元素通过指定纬度坐标（lat属性）、经度坐标（lon属性）和绕轴旋转（rev属性）来定义旋转。每个属性以1度的60000分之一为单位。例如，上面的形状指定了isometricLeftDown的预设位置，但未使用<a:rot>元素更改该位置。让我们添加一个2700000或45度的旋转：

<a:scene3d>

<a:camera prst="isometricLeftDown">

<a:rot lat="2100000" lon="2700000" rev="2700000"/>

</a:camera>

</a:scene3d>

![Shape size](drwImages\drwSp-3Dscene2.gif)

可以通过向<a:camera>元素添加zoom属性来对相机位置应用缩放。它是一个百分比。下面是上面的第一个形状，但具有200%的缩放。

<a:scene3d>

<a:camera prst="isometricLeftDown" zoom="200%"></a:camera>

<a:lightRig rig="sunset" dir="t"/

</a:scene3d>

![Shape size](drwImages\drwSp-3Dscene3-zoom.gif)

最后，可以通过向<a:camera>元素添加fov属性来修改预设相机设置所设置的视图的视野。值以1度的60000分之一为单位，范围从0到180度。

## 灯光装置

灯光装置在存在3D斜角时是相关的。灯光装置定义与场景相关联的照明属性，并通过<a:lightRig>元素指定。它具有一个rig属性，该属性指定相对于场景以特定方式定向的预设灯光组。可能的值是：

- 平衡
- 明亮房间
- 寒冷
- 对比
- 平面
- 泛光
- 冰冷
- 发光
- 刺眼
- 传统平面1到传统平面4
- 传统刺眼1到传统刺眼4
- 传统正常1到传统正常4
- 早晨
- 柔和
- 日出
- 日落
- 三点
- 两点

灯光装置相对于场景的朝向方向由dir属性指定。它定义了灯光整体的朝向，而不是装置内的各个灯光。因此，例如，如果灯光装置的方向是左侧，这并不保证光线来自左侧，而是整个装置的朝向旋转到了左侧。可能的值是：

- b（底部）
- bl（左下）
- br（右下）
- l（左侧）
- t（顶部）
- tl（左上）
- tr（右上）

最后，与<a:camera>元素一样，<a:lightRig>元素可以包含<a:rot>子元素，该元素使用其lat、lon和rev属性定义旋转。有关详细信息，请参见上面关于<a:camera>元素的讨论。下面是使用预设freezing的<a:lightRig>示例。

<a:scene3d>

<a:camera prst="orthographicFront"/>

<a:lightRig rig="freezing" dir="t">

<a:rot lat="0" lon="0" rev="3000000"/>

</a:lightRig>

</a:scene3d>

![Shape size](drwImages\drwSp-3Dscene6-lightRig.gif)

如果我们更改旋转点的坐标，会得到以下结果。

<a:scene3d>

<a:camera prst="orthographicFront"/>

<a:lightRig rig="freezing" dir="t">

<a:rot lat="2100000" lon="2700000" rev="3000000"/>

</a:lightRig>

</a:scene3d>

![Shape size](drwImages\drwSp-3Dscene7-lightRig.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
