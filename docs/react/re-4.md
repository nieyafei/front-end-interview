# React 中 refs 的作用是什么？

?> 英：What are refs in React and why are they important?

**答：**

> `Refs` 是 `React` 提供给我们的安全访问 `DOM` 元素或者某个组件实例的句柄。我们可以为元素添加`ref`属性然后在回调函数中接受该元素在 `DOM` 树中的句柄，该值会作为回调函数的第一个参数返回：

```js
class UnControlledForm extends Component {
  handleSubmit = () => {
    console.log("Input Value: ", this.input.value)
  }
  render () {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type='text'
          ref={(input) => this.input = input} />
        <button type='submit'>Submit</button>
      </form>
    )
  }
}
```

> 上述代码中的`input`域包含了一个`ref`属性，该属性声明的回调函数会接收`input`对应的 `DOM` 元素，我们将其绑定到`this`指针以便在其他的类函数中使用。另外值得一提的是，`refs` 并不是类组件的专属，函数式组件同样能够利用闭包暂存其值：

```js
function CustomForm ({handleSubmit}) {
  let inputElement
  return (
    <form onSubmit={() => handleSubmit(inputElement.value)}>
      <input
        type='text'
        ref={(input) => inputElement = input} />
      <button type='submit'>Submit</button>
    </form>
  )
}
```

**参考资料：**

[题目来源](https://segmentfault.com/a/1190000008102870)

[翻译文章](https://tylermcginnis.com/react-interview-questions/)