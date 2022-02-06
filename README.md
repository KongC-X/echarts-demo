Cannot read property ‘init‘ of undefined
在项目中导入 echarts 插件时，报了这个问题，当时以为是，没有获取到 dom 元素，所以用 $refs 的形式获取 dom 元素
于是，最后在网上搜索之后，发现需要在导入包的时候添加上 _ as 即可
import _ as ECharts from 'echarts'

There is a chart instance already initialized on the dom！警告
if (document.getElementById(id) == null) {
return
}
echarts.dispose(document.getElementById(id))
this.charts = echarts.init(document.getElementById(id))
this.charts.setOption({})
