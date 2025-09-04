![OfficeOpenXML.com](drwImages/drawingMLbanner.png)

[主页](index.md) | [字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [Overview](drwOverview.md)
- 图片
  - [Overview](drwPic.md)
  - 图像属性
    - [图像数据](drwPic-ImageData.md)
    - [平铺或拉伸图像填充](drwPic-tile.md)
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
    - [文本主体属性](drwSp-text-bodyPr.md)
      - [定位和边距](drwSp-text-bodyPr-inset.md)
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

文本 - 运行属性

形状内文本的运行级属性通过<a:rPr>元素的子元素和属性指定，该元素是<a:r>元素的子元素。需要注意的是，形状内的运行属性通常与字处理ML文档中的运行属性指定方式不同。例如，在字处理ML文档中，斜体和字体大小等属性被指定为运行元素的子元素，而在形状中，它们被指定为运行元素的属性。

## 颜色/填充、高亮和轮廓

各种类型的填充可以应用于文本运行。最常见的是应用纯色填充来为文本着色，如下例所示。填充被指定为<a:rPr>的子元素，使用与应用于整个形状的填充相同的子元素。有关如何指定各种填充类型的更多信息，请参见[形状填充](drw-Sp-shapeFill.md)。

<a:p>

<a:pPr/>

. . .

</a:pPr/>

<a:r>

<a:rPr . . . >

. . .

</a:rPr>

<a:t>欲望使 </a:t>

</a:r>

<a:r>

<a:rPr lan="en-US" dirty="0" smtClean="0">

<a:solidFill>

<a:schemeClr val="accent5">

<a:lumMod val="75000"/>

</a:schemeClr>

</a:solidFill>

</a:rPr>

<a:t>一切</a:t>

</a:r>

. . .

</a:p>

![Shape with text - run properties - fill1](drwImages\drwSp-text-rpr-fill1.gif)

高亮可以通过<a:rPr>的子元素<a:highlight>指定。<a:highlight>元素内包含颜色规范。可以使用以下颜色选项之一指定颜色：作为预设颜色(<a:prstClr>)，使用色相、饱和度和亮度(<a:hslClr>)，方案颜色(<a:schemeClr>)，系统颜色(<a:sysClr>)，或作为RGB百分比或十六进制数(<a:scrgbClr>或<a:srgbClr>)。请注意，这些对应于颜色规范方法的元素也可以有转换基础颜色的子元素。下面是一个黄色高亮的示例。

<a:r>

<a:rPr lan="en-US" dirty="0" smtClean="0">

<a:highlight>

<a:srgbClr val="FFFF00"/>

</a:highlight>

</a:rPr>

<a:t>一切</a:t>

</a:r>

![Shape with text - run properties - highlight](drwImages\drwSp-text-rpr-highlight.gif)

可以通过<a:rPr>的子元素<a:ln>为运行指定轮廓样式。各种虚线样式、颜色、端点等可以通过<a:ln>上的属性和子元素指定。有关轮廓的更多信息，请参见[形状轮廓](drwSp-outline.md)页面。

<a:r>

<a:rPr lan="en-US" dirty="0" smtClean="0">

<a:ln w="50800" cap="rnd" cmpd="dbl">

<a:solidFill>

<a:srgbClr val="FFFF00"/>

</a:solidFill>

<a:prstDash val="dash"/>

</a:ln>

</a:rPr>

<a:t>一切</a:t>

</a:r>

![Shape with text - run properties - outline](drwImages\drwSp-text-rpr-ln.gif)

## 粗体、斜体、删除线、下划线、大小和大写

许多常见的运行属性通过<a:rPr>上的属性指定。

| 属性 | 描述                                                                                       |
| ---- | ------------------------------------------------------------------------------------------ |
| b    | 指定文本运行的文本应为粗体：b="1"。                                                        |
| i    | 指定文本运行的文本应为斜体：i="1"。                                                        |
| cap  | 指定大写类型。类型由属性值决定。请注意，这不会改变存储的实际字符，只改变渲染。可能的值有： |

- all（所有字母都大写）
- none（没有字母大写）
- small（对文本应用小型大写字母）

sz | 指定文本的大小：sz="1200"。整点以100为增量指定。12磅字体大小将是1200。  
strike | 指定文本运行的文本应格式化为删除线文本。可能的值有：

- dblStrike（双删除线）
- noStrike（无删除线）
- sngStrike（单删除线）

u | 指定文本运行的文本应有下划线。可能的值有：

- dash \- 虚线
- dashHeavy \- 一系列粗虚线
- dashLong \- 一系列长虚线字符
- dashLongHeavy \- 一系列粗长虚线字符
- dbl \- 双线
- dotDash \- 一系列虚线、点字符
- dotDashHeavy \- 一系列粗虚线、点字符
- dotDotDash \- 一系列虚线、点、点字符
- dotDotDashHeavy \- 一系列粗虚线、点、点字符
- dotted \- 一系列点字符
- dottedHeavy \- 一系列粗点字符
- heavy \- 一条粗单线
- none \- 无下划线
- sng \- 单线
- wavy \- 单波浪线
- wavyDbl \- 一对波浪线
- wavyHeavy \- 一条粗波浪线
- words \- 所有非空格字符下方的单线

<a:rPr>也有可以影响下划线的子元素。见下文。

下面是一个运行示例，该运行为粗体、斜体、单下划线、双删除线，且为24磅。

<a:r>

<a:rPr lan="en-US" sz="2400" b="1" i="1" u="sng" strike="dblStrike" dirty="0" smtClean="0">

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

</a:rPr>

<a:t>危险</a:t>

</a:r>

![Shape with text - run properties - bold](drwImages\drwSp-text-rpr-bold.gif)

<a:rPr>有可以影响下划线的子元素。例如，可以使用<a:uFill>指定下划线填充。可以在<a:uFill>内指定通常的填充类型。参见[形状填充](drw-Sp-shapeFill.md)。因此，例如，如果您希望下划线有颜色，可以指定纯色填充，如下所示。

<a:r>

<a:rPr lan="en-US" sz="2400" b="1" i="1" u="sng" strike="dblStrike" dirty="0" smtClean="0">

<a:uFill>

<a:solidFill>

<a:srgbClr val="FF00FF"/>

</a:solidFill>

</a:uFill>

</a:rPr>

<a:t>危险</a:t>

</a:r>

![Shape with text - run properties - underline](drwImages\drwSp-text-rpr-underline.gif)

要指定下划线的填充颜色应与文本颜色相同，请将<a:uFillTx>指定为<a:rPr>的子元素。要指定下划线的样式应跟随文本，请指定<a:uLnTx>

## 间距、上标/下标、字距调整、字体

运行内字符之间的间距通过<a:rPr>上的spc属性指定。值以磅为单位，100为1磅，1200为12磅。下面是一个将第一句间距设置为12磅的示例：<a:rPr lan="en-US" sz="1200" spc="1200">。

![Shape with text - run properties - spacing](drwImages\drwSp-text-rpr-spc.gif)

字距调整，即比例字体中字符间距的调整，可以通过<a:rPr>上的kern属性指定。属性值指定运行发生字距调整的最小字体大小，因此值以磅为单位。

上标和下标通过<a:rPr>上的baseline属性指定。值以百分比表示，正值表示上标，负值表示下标。下面是"Love"一词下标(<a:rPr lan="en-US" sz="1200" baseline="-40000">)和"striking"一词上标(<a:rPr lan="en-US" sz="1200" baseline="30000">)的示例。

![Shape with text - run properties - superscript and subscript](drwImages\drwSp-text-rpr-baseline.gif)

字体（基于拉丁文的）可以通过<a:rPr>的子元素<a:latin>为运行指定。typeface属性指定字体名称。下面是一个使用Wingding字体运行的形状。

<a:r>

<a:rPr lan="en-US" sz="1600" dirty="0" smtClean="0">

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

<a:latin typeface="Wingdings" pitchFamily="2" charset="2"/>

</a:rPr>

<a:t>striking</a:t>

</a:r>

![Shape with text - run properties - typeface](drwImages\drwSp-text-rpr-latin.gif)

## 链接

形状内文本中的超链接通过<a:rPr>的子元素<a:hlinkClick>插入。id属性指定包含链接目标的关系id。因此，例如，<a:hlinkClick r:id="rId2"/>引用幻灯片(slide1.xml.rels)的.rels文件中id为rId2的关系。该关系如下所示：

<Relationship Id="rId2" Type="http://. . ./hyperlink" Target="http://www.google.com/" TargetMode="External"/>

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
