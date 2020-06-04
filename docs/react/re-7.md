# Controlled Component 与 Uncontrolled Component 之间的区别是什么？

?> 英：What is the difference between a controlled component and an uncontrolled component?

**答：**

> `React` 的核心组成之一就是能够维持内部状态的自治组件，不过当我们引入原生的`HTML`表单元素时（`input,select,textarea` 等），我们是否应该将所有的数据托管到 `React` 组件中还是将其仍然保留在 `DOM` 元素中呢？这个问题的答案就是受控组件与非受控组件的定义分割。

> 受控组件（`Controlled Component`）代指那些交由 `React` 控制并且所有的表单数据统一存放的组件。譬如下面这段代码中username变量值并没有存放到DOM元素中，而是存放在组件状态数据中。任何时候我们需要改变username变量值时，我们应当调用`setState`函数进行修改。

```js
class ControlledForm extends Component {
  state = {
    username: ''
  }
  updateUsername = (e) => {
    this.setState({
      username: e.target.value,
    })
  }
  handleSubmit = () => {}
  render () {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type='text'
          value={this.state.username}
          onChange={this.updateUsername} />
        <button type='submit'>Submit</button>
      </form>
    )
  }
}
```

> 而非受控组件（`Uncontrolled Component`）则是由`DOM`存放表单数据，并非存放在 `React` 组件中。我们可以使用 `refs` 来操控`DOM`元素：

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

> 竟然非受控组件看上去更好实现，我们可以直接从 `DOM` 中抓取数据，而不需要添加额外的代码。不过实际开发中我们并不提倡使用非受控组件，因为实际情况下我们需要更多的考虑表单验证、选择性的开启或者关闭按钮点击、强制输入格式等功能支持，而此时我们将数据托管到 `React` 中有助于我们更好地以声明式的方式完成这些功能。引入 `React` 或者其他 `MVVM` 框架最初的原因就是为了将我们从繁重的直接操作 `DOM` 中解放出来。


**参考资料：**

[题目来源](https://segmentfault.com/a/1190000008102870)

[翻译文章](https://tylermcginnis.com/react-interview-questions/)