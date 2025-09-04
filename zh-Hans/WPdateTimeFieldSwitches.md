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

# 文字处理域

日期和时间域格式

日期和时间域格式开关具有以下格式：

\@ _开关参数_

日期和时间域开关参数由一系列"图片项"组成。以下是最常用的。

参考：ECMA-376，第3版（2011年6月），基础和标记语言参考 § 17.16.4.1。

### 日期和时间域开关图片项：

| 图片项       | 描述                                                                     |
| ------------ | ------------------------------------------------------------------------ |
| d            | 将星期几或月份中的日期格式化为数字，单位数日期不显示前导零。             |
| dd           | 将月份中的日期格式化为两位数，单位数日期显示前导零。                     |
| ddd          | 根据包含域指令的运行上的lang元素指定的语言，将星期几格式化为缩写形式。   |
| dddd         | 根据包含域指令的运行上的lang元素指定的语言，将星期几格式化为完整名称。   |
| M            | 将月份格式化为数字，单位数月份不显示前导零。                             |
| MM           | 将月份格式化为数字，单位数月份显示前导零。                               |
| MMM          | 根据包含域指令的运行上的lang元素指定的语言，将月份格式化为缩写形式。     |
| MMMM         | 根据包含域指令的运行上的lang元素指定的语言，将月份格式化为完整名称。     |
| W            | 根据包含域指令的运行上的lang元素指定的语言，将星期几格式化为缩写形式。   |
| yy           | 将年份格式化为两位数。                                                   |
| yyyy         | 将年份格式化为四位数。                                                   |
| h或H         | 将12小时制的小时格式化为数字，单位数小时不显示前导零。                   |
| hh           | 将12小时制的小时格式化为数字，单位数小时显示前导零。                     |
| H            | 将24小时制的小时格式化为数字，单位数小时不显示前导零。                   |
| HH           | 将24小时制的小时格式化为数字，单位数小时显示前导零。                     |
| m            | 将分钟格式化为数字，单位数分钟不显示前导零。                             |
| mm           | 将分钟格式化为数字，单位数分钟显示前导零。                               |
| s            | 将秒数格式化为数字，单位数秒不显示前导零。                               |
| ss           | 将秒数格式化为两位数，单位数秒显示前导零。                               |
| am/pm或AM/PM | 根据包含域指令的运行上的lang元素指定的语言，格式化大写的12小时制指示符。 |
| 其他字符     | 在结果中的该位置包含指定字符。例如，冒号(:)、连字符(-)、斜杠(/)和空格。  |
| 'text'       | 在结果中包含*文本*。                                                     |

以下是美国英语的一些日期和时间示例。

### 日期和时间开关示例：

| 开关                             | 结果                  |
| -------------------------------- | --------------------- |
| DATE \@ "M/d/yyyy"               | 1/3/2006              |
| DATE \@ "dddd, MMMM dd, yyyy"    | 星期二, 2006年1月03日 |
| DATE \@ "MMMM d, yyyy"           | 2006年1月3日          |
| DATE \@ "M/d/yy"                 | 1/3/06                |
| DATE \@ "yyyy-MM-dd"             | 2006-01-03            |
| DATE \@ "d-MMM-yy"               | 3-1月-06              |
| DATE \@ "M.d.yyyy"               | 1.3.2006              |
| DATE \@ "MMM. d, yy"             | 1月. 3, 06            |
| DATE \@ "d MMMM yyyy"            | 3 2006年1月           |
| DATE \@ "MMMM yy"                | 2006年1月             |
| DATE \@ "M/d/yyyy h:mm am/pm"    | 1/3/2006 5:28 下午    |
| DATE \@ "M/d/yyyy h:mm:ss am/pm" | 1/3/2006 5:28:34 下午 |
| DATE \@ "h:mm am/pm"             | 5:28 下午             |
| DATE \@ "h:mm am/pm"             | 5:28:34 下午          |
| DATE \@ "HH:mm"                  | 17:28                 |
| DATE \@ "'Today is 'HH:mm:ss"    | 今天是 17:28:34       |

[关于本站](aboutThisSite.md) | [联系我们](contactUs.md)  
版权所有 © 2023。保留所有权利。
