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

# DrawingML文本

文本和文本框

文字处理和电子表格文档将文本作为其结构的基本特征。创建文档并开始输入文本，文本将以熟悉且明确定义的方式流动。这些文档类型中的每一种也可以包含更具图形性、专业性质的文本，插入到文本框或形状中。文本框或形状可以独立于文档中的其他文本进行定位和样式设置。对于这些文档类型中的每一种，图形文本的插入方式与插入绘图的方式相同，在覆盖该文档类型drawingML的专用命名空间中。请参阅[电子表格文档中的定位](drwPicInSpread.md)和[文字处理文档中的定位](drwPicInWord.md)。演示文稿文档不是那么以文本为导向的，演示文稿中的所有文本必须位于文本框或形状内。其位置在主drawingML规范和命名空间中定义。

尽管文本在文档中的放置方式因文档类型而异，但文本本身的定义保持不变。文本框中的文本实际上只是一个包含文本的专门形状。请参阅[形状 - 文本](drwSp-text.md)。每个形状在<nvSpPr>元素内包含一组画布的非视觉属性。在<nvSpPr>元素内是<cNvSpPr>，包含一组形状的非视觉属性。该元素有一个txBox属性，可以是true或false。如果为true，则该形状是文本框。如果为false，或者该属性不存在，则该形状不是专门的文本框。然而，实际上，文本框和带文本的形状之间几乎没有区别。对于演示文稿和电子表格，可以省略[几何图形(<a:prstGeom>)](drwSp-prstGeom.md)。但它可以而且经常被设置为矩形的值(<a:prstGeom prst="rect">)。

下面是一个示例，首先包含一个文本框，然后是一个带文本的形状。两者都是<p:sp>元素内的形状。文本框具有txBox="1"属性。它也没有<p:style>元素，尽管它可以有。对于形状，<p:style>元素内的样式信息被<a:prstGeom>元素中指定的缺少线条和填充所覆盖。

<p:sp>

<p:nvSpPr>

<p:cNvPr id="4" name="文本框 3"/>

<p:cNvSpPr txBox="1"/>

<p:nvPr/>

</p:nvSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2362200" y="1066800"/>

<a:ext cx="2362200" cy="369332"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

<a:noFill/>

</p:spPr>

<p:txBody>

<a:bodyPr wrap="square" rtlCol="0">

<a:spAutoFit/>

</a:bodyPr>

<a:lstStyle/>

<a:p>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0"/>

<a:t>这是一个文本框</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

</a:p>

</p:txBody>

</p:sp>

<p:sp>

<p:nvSpPr>

<p:cNvPr id="5" name="矩形 4"/>

<p:cNvSpPr/>

<p:nvPr/>

</p:nvSpPr>

<p:spPr>

<a:xfrm>

<a:off x="2133600" y="1600200"/>

<a:ext cx="2438400" cy="990600"/>

</a:xfrm>

<a:prstGeom prst="rect">

<a:avLst/>

</a:prstGeom>

<a:noFill/>

<a:ln/>

<a:noFill/>

</a:ln/>

</p:spPr>

<p:style>

<a:lnRef idx="2">

<a:schemeClr val="accent1">

<a:shade val="50000"/>

</a:schemeClr>

</a:lnRef>

<a:fillRef idx="1">

<a:schemeClr val="accent1"/>

</a:fillRef>

<a:effectRef idx="0">

<a:schemeClr val="accent1"/>

</a:effectRef>

<a:fontRef idx="minor">

<a:schemeClr val="lt1"/>

</a:fontRef>

</p:style>

<p:txBody>

<a:bodyPr rtlCol="0" anchor="ctr"/>

<a:lstStyle/>

<a:p>

<a:pPr algn="ctr"/>

<a:r>

<a:rPr lang="en-US" dirty="0" smtClean="0">

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

</a:rPr>

<a:t>这是在一个形状中</a:t>

</a:r>

<a:endParaRPr lang="en-US" dirty="0"/>

<a:solidFill>

<a:schemeClr val="tx1"/>

</a:solidFill>

</a:endParaRPr>

</a:p>

</p:txBody>

</p:sp>

![Presentation with textbox and shape with text](drwImages\drwSp-textbox1.gif)

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权 © 2023。保留所有权利。
