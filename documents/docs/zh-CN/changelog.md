## 介绍
<el-card>

为 `layui table` 扩展的插件， 计划和目标（有好的想法/建议/BUG反馈，可以加入QQ群：<a target="_blank" href="//shang.qq.com/wpa/qunwpa?idkey=3cbfbd2169afc3f4d11732101388941b0db5330a64755e68f27740b604409629"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="layui-使用交流" title="layui-使用交流"></a>）

当前layui版本 `v2.4.5`, 新版稳定后，将会做兼容性工作

</el-card>

## 功能介绍

<el-card>

1.表头筛选、自定义条件（支持前端筛选、后台筛选）

2.拖动列调整顺序、隐藏显示列

3.excel导出（根据筛选条件和列顺序导出）

4.子表（表中表、无限层级、子表同样支持前3个功能）

</el-card>



## 更新日志

### **1.2.10** <small>`2019-07-23`</small>
[优化] excel导出 修复excel列宽和表格列宽同步

### **1.2.9** <small>`2019-07-18`</small>
[修复] 记忆 修复记忆的key添加了hash兼容单页应用使用

[修复] 筛选 修复 使用 myTable.reload 清除表头条件时未还原处理

[优化] 使用了新的文档系统

[优化] 子表 `tableChild.js`可以单独使用 通过 `tableChild.render(this)` 使用

[优化] 子表 阻止了子表冒泡事件，且增加了主表的行点击事件

[新增] 单元格合并 引入了作者很早实现的一个合并插件

### **1.2.8** <small>`2019-07-16`</small>
[新增] 子表 新增 isChild 字段，用于根据当前行数据是否显示子表入口

### **1.2.7** <small>`2019-07-12`</small>
[修复] 筛选 拼接筛选条件时，没有判空，导致空数据抛出异常的问题

### **1.2.6** <small>`2019-07-10`</small>
[新增] 离线字体包 项目中引入离线字体包，方便获取

### **1.2.5** <small>`2019-07-08`</small>
[修复] 滚动条 修复窗口大小变化时，fixed列高度计算错误，导致遮挡横向滚动条的问题

### **1.2.4** <small>`2019-07-03`</small>
[修复] 子表 修复子表展开模式下表头拖拽列宽的鼠标样式丢失问题

[修复] 子表 修复子表 tableId 获取不统一造成的cache数据查找失败的问题

[修复] 拖拽 修复拖拽 tableId 获取不统一造成列获取失败的问题

### **1.2.3** <small>`2019-07-02`</small>
[增加] 筛选 tableFilter 暴露变量 cache ，用于在页面可以方便获取 表格所有数据。 tableFilter.cache

### **1.2.2** <small>`2019-06-28`</small>
[修复] 筛选 修复使用 table.render ，保存筛选条件判断的bug

### **1.2.1** <small>`2019-06-26`</small>
[修复] 筛选 修复后台筛选时数据为空的判断

### **1.2.0** <small>`2019-06-25`</small>
[修复] 筛选 前端不分页时，不设置limit时，筛选条件去除后只会显示10条数据的问题（layui源码bug，但是通过此插件解决）

[修复] 筛选 后台筛选没有重载表头的问题

[修复] 隐藏列/调整列顺序 修复以移动列后，disabled的列计算错误的问题

[修复] 拖拽列 修复 firefox 下拖拽列出现的边框消失的问题

[增强] 子表 子表扩展了 单击行/双击行 事件，并给tool等事件引入父表当前行参数

[新增] 列宽 双击列自适应宽度

### **1.1.1** <small>`2019-06-24`</small>
[修复] 筛选 修复后端筛选丢失查询条件的问题

[修改] 筛选 默认 table.reload 不会清除"表头筛选"的条件。当然可以配置 clearFilter 为 true 来清除筛选条件

### **1.1.0** <small>`2019-06-19`</small>
[新增] 前端缓存配置，当前仅包含：列顺序、隐藏列。可以参考 基本功能->记忆功能，即便刷新页面也会保存列配置。

### **1.0.7** <small>`2019-05-05`</small>
[新增] excel导出，添加格式指定：单元格类型: b 布尔值, n 数字, e 错误, s 字符, d 日期

### **1.0.6** <small>`2019-04-17`</small>
[修复] 拖拽 修复事件未释放造成的ui错乱

[修复] 拖拽 禁止checkbox、radio列及右侧固定列移动

### **1.0.5** <small>`2019-04-15`</small>
[修复] 子表 由于dom选择bug造成的无限层级子表出现问题

[新增] 子表 新增 spread 参数，加载主表后自动加载子表

[新增] 子表 url 可传入方法，可以根据主表数据修改url，可用于 路径参数 请求

### **1.0.4** <small>`2019-04-12`</small>
[修复] 筛选 修复数字类型不兼容问题

[新增] 筛选 新增 bottom 参数，用于选择是否加载底部筛选行

### **1.0.3** <small>`2019-04-09`</small>
[修复] 拖动 禁止固定列移动

[修复] 子表 修复主表事件覆盖，导致主表tool事件失效的问题

[新增] 子表 添加参数 toolEvent 用于处理子表行事件

### **1.0.2** <small>`2019-04-08`</small>
[优化] 筛选 如果没有筛选列，则不渲染底部筛选

[修复] 筛选 修复固定列筛选问题

[新增] 子表 添加参数 data，可使用数组数据渲染子表

### **1.0.1** <small>`2019-04-04`</small>
[修复] 拖动 修复排序造成的拖动bug

### **1.0.0** <small>`2019-01-27`</small>
[新增] 创建项目