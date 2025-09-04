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

# DrawingML 表格 - 行、单元格和单元格内容

表格由一行或多行组成，一行包含一个或多个单元格。

表格行使用<a:tr>元素定义。行元素可以包含高度属性(h)，可以是EMU或后跟单位标识符的数字。行元素包含一个或多个单元格元素(<a:tc>)。

表格中的所有内容都在单元格元素中定义。单元格只能包含文本。单元格也可以有属性。（注意，表格也可以有属性，但行除了高度外没有其他属性。）<a:tc>允许的子元素包括用于文本的<a:txBody>和用于单元格属性的<a:tcPr>。

单元格还可以具有以下属性，这些属性在[DrawingML - 表格 - 结构](dwrTableGrid.md)中有更详细的讨论。

| 属性     | 描述                                                                                                                    |
| -------- | ----------------------------------------------------------------------------------------------------------------------- |
| gridSpan | 指定合并单元格跨越的列数。与其他单元格上的hMerge属性结合使用，以指定水平合并的起始单元格                                |
| hMerge   | 值为布尔值。当设置为1或true时，该单元格将与前一个水平表格单元格合并。                                                   |
| id       | 指定单元格的唯一标识符。标识符在表格内必须是唯一的，并用于使用headers子元素将单元格标识为表格内其他单元格的标题单元格。 |
| rowSpan  | 指定合并单元格跨越的行数。与其他单元格上的vMerge属性结合使用，以指定水平合并的起始单元格。                              |
| vMerge   | 值为布尔值。当设置为1或true时，该单元格将与前一个垂直表格单元格合并。                                                   |

### 单元格内的文本内容

演示表格单元格内的文本的指定方式与drawingML形状中的文本指定方式相同—即在<a:txBody>元素内。有关详细信息，请参阅[DrawingML - 形状 - 文本](drwSp-text.md)。注意一个区别。<a:txBody>元素的命名空间是主要的drawingML命名空间（前缀'a'），而不是演示文稿（'p'）或其他命名空间。

下面是一个包含三行的示例演示表格。中间行有文本。表格下方是包含文本的行的xml。

![DrawingML - Table](drwImages\drwTableWithText.gif)

<a:tr h="370840">

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>巴赫</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr/>

</a:tc>

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>贝多芬</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr/>

</a:tc>

<a:tc>

<a:txBody>

<a:bodyPr/>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>勃拉姆斯</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</a:txBody>

<a:tcPr/>

</a:tc>

</a:tr>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
