![OfficeOpenXML.com](images/banner1.png)

[主页](index.md) | [文字处理ML (docx)](anatomyofOOXML.md) | [电子表格ML (xlsx)](anatomyofOOXML-xlsx.md) | [演示文稿ML (pptx)](anatomyofOOXML-pptx.md) | [绘图ML](drwOverview.md)

- [内容概述](WPcontentOverview.md)
- [示例Docx视图](WPsampleDoc.md)
- [Document](WPdocument.md)
- 段落
  - [Overview](WPparagraph.md)
  - [Properties](WPparagraphProperties.md)
    - [水平对齐](WPalignment.md)
    - [Borders](WPborders.md)
    - [分隔符](WPtextSpecialContent-break.md)
    - [Indentation](WPindentation.md)
    - [底纹和背景](WPshading.md)
    - [Spacing](WPspacing.md)
    - [Styles](WPstyleParStyles.md)
    - [Tabs](WPtab.md)
    - [垂直对齐](WPborders.md)
- [文本框](WPparagraph-textFrames.md)
- 文本
  - [Overview](WPtext.md)
  - [Properties](WPtextFormatting.md)
    - [Borders](WPtextBorders.md)
    - [Fonts](WPtextFonts.md)
    - [Shading](WPtextShading.md)
    - [Spacing](WPtextSpacing.md)
    - [特殊内容](WPtextSpecialContent.md)
      - [分隔符](WPtextSpecialContent-break.md)
      - [符号](WPtextSpecialContent-symbol.md)
    - [Styles](WPstyleCharStyles.md)
- 表格
  - 结构
    - [Overview](WPtable.md)
    - [定义列或表格网格](WPtableGrid.md)
    - [Rows](WPtableRow.md)
    - [Cells](WPtableCell.md)
  - [表格属性](WPtableProperties.md)
    - [Alignment](WPtableAlignment.md)
    - [Borders](WPtableBorders.md)
    - [边框冲突](WPtableCellBorderConflicts.md)
    - [Captions](WPtableCaption.md)
    - [Indentation](WPtableIndent.md)
    - [Shading](WPtableShading.md)
    - [Width](WPtableWidth.md)
    - [Styles](WPstyleTableStyles.md)
    - [单元格边距](WPtableCellMargins.md)
    - [单元格间距](WPtableCellSpacing.md)
    - [自动调整/宽度布局](WPtableLayout.md)
    - [绝对定位或浮动表格](WPfloatingTables.md)
    - [条件格式](WPtblLook.md)
  - [表格属性例外](WPtablePropertyExceptions.md)
  - [行属性](WPtableRowProperties.md)
  - [单元格属性](WPtableCellProperties.md)
    - [边框](WPtableCellProperties-Borders.md)
    - [单元格边框冲突](WPtableCellBorderConflicts.md)
    - [边距](WPtableCellProperties-Margins.md)
    - [底纹](WPtableCellProperties-Shading.md)
    - [垂直对齐](WPtableCellProperties-verticalAlignment.md)
    - [宽度](WPtableCellProperties-Width.md)
    - [隐藏单元格结束标记](WPhideMark.md)
- 编号、级别和列表
  - [Overview](WPnumbering.md)
  - [定义编号方案](WPnumberingAbstractNum.md)
  - [定义特定级别](WPnumberingLvl.md)
    - [编号级别文本](WPnumberingLevelText.md)
    - [编号格式](WPnumbering-numFmt.md)
    - [仅显示为数字](WPnumbering-isLgl.md)
    - [重新开始编号](WPnumbering-restart.md)
    - [图片或图像作为编号符号](WPnumbering-imagesAsSymbol.md)
    - [对齐方式](WPnumbering-lvlJc.md)
  - [覆盖编号定义](WPnumberingOverride.md)
- 节
  - [Overview](WPsection.md)
  - [Columns](WPsectionCols.md)
  - [Footers](WPsectionFooterReference.md)
  - [Headers](WPsectionHeaderReference.md)
  - [Borders](WPsectionBorders.md)
  - [页边距](WPsectionPgMar.md)
  - [页码](WPSectionPgNumType.md)
  - [行号](WPsectionLineNumbering.md)
- 样式
  - [Overview](WPstyles.md)
  - [定义默认格式](WPstyleDefaults.md)
  - [定义样式](WPstyle.md)
    - [常规样式属性](WPstyleGenProps.md)
    - [字符样式](WPstyleCharStyles.md)
    - [段落样式](WPstyleParStyles.md)
    - [表格样式](WPstyleTableStyles.md)
      - [条件格式](WPstyleTableStylesCond.md)
    - [编号样式](WPstyleNumStyles.md)
- [Fonts](WPfonts.md)
- [Headers](WPheaders.md)
- [Footers](WPfooters.md)
- [页码](WPSectionPgNumType.md)
- 链接
  - [Overview](WPhyperlink.md)
  - [Bookmarks](WPbookmark.md)
- 域
  - [Overview](WPfields.md)
  - [域指令](WPfieldInstructions.md)
  - [域定义](WPfieldDefinitions.md)
  - [常规域格式](WPgeneralFieldSwitches.md)
  - [日期和时间域格式](WPdateTimeFieldSwitches.md)
  - [数字域格式](WPnumericFieldSwitches.md)
- [目录](WPtableOfContents.md)

# 文字处理文本

相关的Open Office/ODF讨论  
相关的HTML/CSS讨论

格式设置

运行格式通过<w:rPr>元素内的元素指定。

<w:rPr>

<w:b w:val="true"/>

<w:u w:val="single"/>

</w:rPr>

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.28。

![Sample text formatting](images\wp-text-formatting-1.gif)

---

以下是一些最常用的格式元素。其他文本格式，如间距、底纹和边框，在单独的页面中介绍。

### 元素：

| 元素 | 描述                                                                                                                        |
| ---- | --------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| b    | 指定文本运行的文本应为粗体：<w:b />。这是一个切换属性。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.1。  |
| i    | 指定文本运行的文本应为斜体：<w:i />。这是一个切换属性。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.16。 |
| caps | 指定任何小写字符应显示为其大写等效字符。它不能与smallCaps在同一文本运行中出现：<w:caps w:val="true" />。这是一个切换属性。  | ![caps](images\wp-caps-1.gif) |

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.5。

color | 指定用于显示文本的颜色：<w:color w:val="FFFF00" />可能的属性有themeColor、themeShade、themeTint和val。val属性以RRGGBB格式的十六进制值指定颜色，或者可以指定auto以允许使用软件确定颜色。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.6。  
dstrike | 指定内容应显示为每个字符有两条水平线穿过：<w:dstrike w:val="true"/>。它不能与strike在同一文本运行中出现。这是一个切换属性。 | ![dstrike](images\wp-dstrike-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.37。

emboss | 指定内容应显示为好像浮雕效果，使文本看起来好像从页面上凸起：<w:emboss w:val="true" />。这是一个切换属性。 | ![浮雕文本](images\wp-embossedText-1.gif)

---

![](images/note.png) 注意：上面的示例指定了emboss，但还将颜色设置为白色：<w:emboss/><w:color w:val="FFFFFF"/>。这似乎是必要的，否则结果看起来像imprint。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.13。

imprint | 指定内容应显示为好像压印（或雕刻）到页面中：<w:imprint w:val="true"/>。它不能与emboss或outline同时存在。这是一个切换属性。 | ![压印文本](images\wp-imprint-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.18。

outline | 指定内容应显示为好像有轮廓。在每个字符的内外边框周围绘制一个像素的边框。<outline w:val="true"/>。这是一个切换属性。 | ![文本轮廓](images\wp-outline-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.23。

rStyle | 指定用于格式化运行内容的字符样式的样式ID。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.29。  
shadow | 指定内容应显示为好像每个字符都有阴影：<w:shadow w:val="true"/>。对于从左到右的文本，阴影在文本下方和右侧。shadow不能与emboss或imprint同时存在。这是一个切换属性。 | ![阴影文本](images\wp-textShadow-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.31。

smallCaps | 指定任何小写字符应显示为其大写等效字符，但字体大小比指定字体小两点：<w:smallCaps w:val="true"/>。它不能与caps在同一文本运行中出现。这是一个切换属性。 | ![小型大写字母](images\wp-smallCaps-1.gif)

---

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.33。

strike | 指定内容应显示为在行中心有一条水平线穿过：<w:strike w:val="true"/>。它不能与dstrike在同一文本运行中出现。这是一个切换属性。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.37。  
sz | 以半点为单位指定字体大小：<w:sz w:val="28"/>。注意，szCs用于复杂脚本字体，如阿拉伯语。单个属性val以半点（1/144英寸）为单位指定测量值。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.38。  
u | 指定内容应显示为带下划线：<w:u w:val="double"/>。最常见的属性如下（省略了与主题相关的属性）：

- color \- 指定下划线的颜色。值以十六进制值（RRGGBB格式）给出。没有#，与HTML/CSS中的十六进制值不同。例如，color="FFFF00"。也允许使用auto值，这将允许使用的字处理器根据上下文确定颜色。
- val \- 指定用于创建下划线的模式。可能的值有：
  - dash \- 虚线
  - dashDotDotHeavy \- 一系列粗虚线、点、点字符
  - dashDotHeavy \- 一系列粗虚线、点字符
  - dashedHeavy \- 一系列粗虚线
  - dashLong \- 一系列长虚线字符
  - dashLongHeavy \- 一系列粗、长、虚线字符
  - dotDash \- 一系列虚线、点字符
  - dotDotDash \- 一系列虚线、点、点字符
  - dotted \- 一系列点字符
  - dottedHeavy \- 一系列粗点字符
  - double \- 双线
  - none \- 无下划线
  - single \- 单线
  - thick \- 单粗线
  - wave \- 单波浪线
  - wavyDouble \- 一对波浪线
  - wavyHeavy \- 单粗波浪线
  - words \- 所有非空格字符下方的单线

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.40。  
vanish | 指定内容在显示时应隐藏。<vanish/>。这是一个切换属性。参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.41。  
vertAlign | 下标和上标。<vertAlign w:val="superscript"/>。单个属性是val。允许的值有：

- baseline \- 常规垂直定位
- subscript \- 将文本降低到基线以下并更改为小尺寸
- superscript \- 将文本提高到基线以上并更改为较小尺寸

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.3.2.42。

---

# 相关的开放文档格式（ODF）属性：

在OpenDocument格式中，格式属性（即使是"手动"或直接样式）存储在样式（<style:style>）中。样式与引用该样式的内容存储在同一文件中，或存储在单独的styles.xml文件中。样式可能包含<style:text-properties>元素，该元素存储样式的文本属性。实际属性存储为<style:text-properties>的属性。

<style:style style:name="P1" style:family="paragraph" style:parent-style-name="Standard">

<style:text-properties fo:font-weight="bold" style:font-weight-asian="bold" style:font-weight-complex="bold"/>

</style:style>

参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 16.27.28。

| 文本属性              | ODF实现[<style:text-properties/>的属性]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| bold                  | fo:font-weight。可能的值有normal、bold、100、200等直到900。例如，<style:text-properties fo:font-weight="bold" . . ./>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.186。                                                                                                                                                                                                                                                                                                                                                                                                                      |
| italics               | fo:font-style。可能的值有italic、normal和oblique。例如，<style:text-properties fo:font-style="italic" . . ./>参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.184。                                                                                                                                                                                                                                                                                                                                                                                                                                |
| capitalization        | fo:text-transform。可能的值有none、lowercase、uppercase和capitalize。例如，<style:text-properties fo:text-transform="uppercase"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.220。                                                                                                                                                                                                                                                                                                                                                                                                          |
| color                 | fo:font-color。可能的值采用#rrggbb形式。例如，<style:text-properties fo:font-color="#FF6600" . . ./>参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.180。                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| strike through        | style:text-line-through-style。可能的值有none、dash、dot-dash、dot-dot-dash、dotted、long-dash、solid和wave。例如，<style:text-properties style:text-line-through-style="solid"/>。其他相关属性确定线条的颜色和宽度等属性。附带的style:text-line-through-type属性可以指定线条是单线还是双线。例如，以下将创建双删除线：<style:text-properties style:text-line-through-style="solid" style:text-line-through-type="double"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.363。                                                                                                                |
| shadow                | fo:text-shadow。可能的值是none或XSL 1.0规范7.16.5中指定的值—即，由阴影偏移的两个长度值加上可选的模糊半径和可选颜色组成的字符串。例如，<fo:text-shadow="1pt 1pt"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.219。                                                                                                                                                                                                                                                                                                                                                                          |
| small caps            | fo:font-variant。可能的值有normal或small-caps。例如，<fo:font-variant="small-caps"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.185。                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| size                  | fo:font-size。值可以是绝对大小或百分比。例如，<fo:font-size="18pt"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.183。                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| underline             | style:text-underline-style。可能的值有none、dash、dot-dash、dot-dot-dash、dotted、long-dash、solid和wave。例如，<style:text-underline-style="solid" style:text-underline-width="auto" style:text-underline-color="font-color"/>。其他相关属性确定下划线的其他属性。例如，style:text-underline-color确定颜色；style:text-underline-mode确定下划线是应用于单词还是也应用于单词之间的空格；style:text-underline-type确定下划线是单线还是双线；style:text-underline-with确定宽度，可能的值有auto、bold、thin、medium、thick、百分比或正数。参考：办公应用程序开放文档格式版本1.2（2011年5月）§§ 20.378-382。 |
| hidden                | text:display。可能的值有condition（文本在text:condition属性中指定的条件下显示）、none和true。例如，<text:display="none"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.417。                                                                                                                                                                                                                                                                                                                                                                                                                  |
| superscript/subscript | style:text-position。它可能有一个或两个由空格分隔的值。第一个值指定垂直文本位置作为当前字体高度的百分比，或者取值sub或super。负百分比将文本置于基线以下。第二个值（如果存在）将字体高度指定为当前字体高度的百分比。例如，<style:text-position="super 58%"/>。参考：办公应用程序开放文档格式版本1.2（2011年5月）§ 20.374。                                                                                                                                                                                                                                                                                |

---

# 相关的HTML/CSS属性：

font-weight:bold;  
font-style:italic;  
text-decoration:line-through;  
text-decoration:underline;  
text-transform:uppercase;  
font-size: 16px;  
color: #00FF00;  
text-shadow:2px 2px #FF0000; [IE中不支持]  
&ltsup>返回&lt/sup>以&ltsub>分享我们的生活&lt/sub>  
visibility: hidden 或 display:none

CSS示例：

然后他们开始颤抖，他们呼唤我们的名字，一旦我们认出他们的声音，咒语就被打破了。我们已经拯救了他们：他们已经战胜了死亡，回来分享我们的生活。我们自己的过去也是如此。试图重温它是徒劳的：我们智力的所有努力都将是徒劳的。

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
