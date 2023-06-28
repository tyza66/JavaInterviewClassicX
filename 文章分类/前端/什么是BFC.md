# 什么是BFC
- BFC是Block Formatting Contexts (块级格式化上下文)的简称， 是 W3C CSS2.1 规范中的一个概念
- BFC是浏览器中创建了一个独立的渲染区域，并且拥有一套渲染规则，他决定了其子元素如何定位，以及和其他元素的关系和相互作用
- 具有BFC特性的元素可以看作是隔离了的独立容器，容器里面的元素不会在布局上影响到外面的元素，而且BFC具有普通容器所没有的一些特性。换句话说就是，创建了BFC的元素就是一个独立的容器，里面的子元素不会影响到外面的元素，反之也如此。
- BFC布局的规则：内部的Box会在垂直方向，一个接一个的放置。Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠。每个元素的margin box的左边，与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。BFC的区域不会与float box重叠。BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之亦然。计算BFC的高度时，浮动元素也参与计算
- 触发BFC的条件：根元素、float属性不为none、position为absolute或fixed的、display为inline-block、table-cell、table-caption、flex、inline-flex之一的元素、overflow不为visible的、display为flow-root的元素
- CFC在布局中的应用场景：清除盒子垂直反方向上外边距合并（盒子垂直方向的距离由margin决定）。属于同一个BFC的两个相邻盒子垂直方向的margin会发生重叠。为了解决这个问题可以给其中一个盒子包裹一个盒子父元素，并处罚其BFC功比如添加ovweflow:hidden）,这样垂直方向的两个盒子就不在同一个BFC中了，因此也不会出现垂直边距合并的问题了