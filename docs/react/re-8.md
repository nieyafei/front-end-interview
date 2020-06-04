# 在生命周期中的哪一步你应该发起 AJAX 请求？

?> 英：In which lifecycle event do you make AJAX requests and why?

**答：**

> **我们应当将AJAX 请求放到 `componentDidMount` 函数中执行，主要原因有下：**

> - `React` 下一代调和算法 `Fiber` 会通过开始或停止渲染的方式优化应用性能，其会影响到 `componentWillMount` 的触发次数。对于 `componentWillMount` 这个生命周期函数的调用次数会变得不确定，`React` 可能会多次频繁调用 `componentWillMount`。如果我们将 `AJAX` 请求放到 `componentWillMount` 函数中，那么显而易见其会被触发多次，自然也就不是好的选择。

> - 如果我们将 `AJAX` 请求放置在生命周期的其他函数中，我们并不能保证请求仅在组件挂载完毕后才会要求响应。如果我们的数据请求在组件挂载之前就完成，并且调用了`setState`函数将数据添加到组件状态中，对于未挂载的组件则会报错。而在 `componentDidMount` 函数中进行 `AJAX` 请求则能有效避免这个问题。

**参考资料：**

[题目来源](https://segmentfault.com/a/1190000008102870)

[翻译文章](https://tylermcginnis.com/react-interview-questions/)