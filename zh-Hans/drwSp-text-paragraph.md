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
    - 3-D
      - [形状属性](drwSp-3dProps.md)
      - [场景属性](drwSp-3dScene.md)
  - [样式](drwSp-styles.md)
  - [文本](drwSp-text.md)
    - [文本正文属性](drwSp-text-bodyPr.md)
      - [定位和边距](drwSp-text-bodyPr-inset.md)
      - [适应、换行、弯曲和3D](drwSp-text-bodyPr-fit.md)
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

文本 - 内容

形状的文本内容包含在一个或多个<a:p>元素中。形状中文本的内容模型与文字处理ML文档中的内容模型相似但不完全相同。以下是<a:p>的允许元素。

### 元素：

| 元素       | 描述                                                                                                                                                                                                                                                                                                                                |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| br         | 指定换行符。请注意，在文字处理ML文档中，换行符包含在文本运行(<a:r>)内。然而，在形状内，换行符直接包含在段落元素中。形状内的换行符可以具有由<a:rPr>元素指定的文本运行属性。如果稍后在换行符位置插入文本，则可以生成具有指定格式的新文本运行。有关<a:rPr>元素的更多信息，请参见[形状 - 文本 - 文本运行属性](drwSp-text-runProps.md)。 |
| endParaRPr | 指定如果在最后一个文本运行之后插入另一个文本运行时要使用的文本运行属性。如果未指定，则应用程序可以确定要应用的属性。有关详细信息，请参见[形状 - 文本 - 文本运行属性](drwSp-text-runProps.md)。                                                                                                                                      |
| r          | 指定段落中的内容运行。它是可以具有属性的最低级别的文本分隔符。如果未指定任何属性，则使用默认文本运行属性元素(<a:defRPr>)中指定的属性。文本运行可以具有文本运行属性和文本元素(<a:t>)。有关文本运行属性的详细信息，请参见[形状 - 文本 - 文本运行属性](drwSp-text-runProps.md)。                                                       |
| pPr        | 指定段落的一组属性。请参见[形状 - 文本 - 段落属性](drwSp-text-paraProps.md)。请注意，如果未指定任何属性，则使用<a:defPPr>元素中指定的默认属性。有关默认段落属性的更多信息，请参见形状 - 文本 - 列表样式。                                                                                                                           |
| fld        | 指定包含应用程序定期更新的生成文本的文本字段。文本类型仅限于日期和时间或幻灯片编号。fld元素的id属性由应用程序生成。type属性指定文本类型。保留值为：                                                                                                                                                                                 |

- 幻灯片编号
- datetime（应用程序的默认日期时间格式）
- datetime1 (MM/DD/YYYY)
- datetime2 (Day, Month DD YYYY)
- datetime3 (MM/DD/YYYY)
- datetime4 (MM/DD/YYYY)
- datetime5 (MM/DD/YYYY)
- datetime6 (MM/DD/YYYY)
- datetime7 (MM/DD/YYYY)
- datetime8 (MM/DD/YYYY)
- datetime9 (MM/DD/YYYY)
- datetime10 (MM/DD/YYYY)
- datetime11 (MM/DD/YYYY)
- datetime12 (MM/DD/YYYY)
- datetime13 (MM/DD/YYYY)

<a:fld>元素可以包含文本(<a:t>)以及段落和文本运行属性元素。有关详细信息，请参见[形状 - 文本 - 段落属性](drwSp-text-paraProps.md)和[形状 - 文本 - 文本运行属性](drwSp-text-runProps.md)。下面是一个带有日期字段的示例形状。<p:txBody> <a:bodyPr rtlCol="0" anchor="ctr"/> <a:lstStyle/> <a:p> <a:pPr algn="ctr"/> <a:r> <a:rPr . . . > . . . </a:rPr> <a:t>时间是 </a:t> </a:r> <a:fld id="8DE09930-A1F0-4970-A755-490F150ACA4" type="datetime4"> <a:rPr lang="en-US" smtClean="0"> . . . </a:rPr> <a:t> 2012年10月26日 </a:t> </a:fld <a:endParaRPr . . .> . . . </a:endParaRPr> </a:p> </p:txBody> ![带文本的形状 - 旋转](drwImages\drwSp-text-field.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
