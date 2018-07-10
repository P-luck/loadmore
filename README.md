# 概括
 loadmore 为移动端 ，下拉刷新 上拉加载提供方法
    
    
### 使用方法
	引入组到项目中
		import Loadmore from 'mint-loadmore';    
	注册组件，全局注册和局部注册组件
		Vue.component('loadmore', Loadmore);	
	使用
		<loadmore :top-method="loadTop" :bottom-method="loadBottom" :bottom-all-loaded="allLoaded">
  		...
  		</loadmore>
  		

	
#### api 各参数说明

# API
| Option            | Description                                                      | Value    | Default     |
|-------------------|------------------------------------------------------------------|----------|-------------|
| autoFill          | 如果是`true`	，则会检查并填充容器， | Boolean  | true        |
| topPullText       | 下拉时顶部的文按显示	 | String   | '下拉刷新'  |
| topDropText       | 当组件准备释放是顶部的文案  | String   | '释放更新'  |
| topLoadingText    | 当执行 `topMethod`时，顶部的文案  | String   | '加载中...' |
| topDistance       | 顶部下拉的触发 `topMethod` 方法的距离 | Number   | 70          |
| topMethod         | 下拉时要执行的方法                                       | Function |             |
| bottomPullText    | 组件上拉时底部的文案  | String   | '上拉刷新'  |
| bottomDropText    | 组件准备释放时 底部的文案    | String   | '释放更新'  |
| bottomLoadingText | 当执行 `bottomMethod` 时 ，底部的文案  | String   | '加载中...' |
| bottomDistance    | 底部上拉的触发 `bottomMethod ` 方法的距离    | Number   | 70          |
| bottomMethod      | 上拉时的方法     | Function |             |
| bottomAllLoaded   | 当为`true`, `bottomMethod`将不会被触发  | Boolean  | false       |
| bottomAllLoadedTxt  | 当`bottomAllLoaded `为 `true` 时，底部的文案   | String           | 到底啦～ |
| canScrollMore  |`false`是触发bottomMethod 的方法是上拉 ，`true` 为滚动到底部触发方法  | Boolean |            |


#### 说明
改loadmore 组件 原组件是mint-ui 的loadmore 组件， 对原组件做了一些修改，解决了一些兼容性问题和使组件更可扩展

1、例如检测是否滑动到组件底部的判断 方法 checkBottomReached 做了修复  
2、将到底了的文案扩张到组件中，使用时，需要在外层判断是否有内容，有则使用loadmore 组件，没有就不展示出来，否则会都显示出来。    
3、`canscrollMore` 属性是为了 兼容更多了下拉加载的效果，一般常用的就是页面滑倒底部触发方法，或者页面滑倒底部，上拉才出发方法，目前支持这两种方法，根据需要选择，默认还是需要滑动的啦～～


#### 问题反馈
如有问题，反馈给我  thanks～～
