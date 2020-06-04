# Doctype的文档类型

**Doctype作用? 严格模式与混杂模式如何区分？有何意义？**
> - <!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前.
> - <!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。
> - 严格模式的排版和 JS 运作模式是 以该浏览器支持的最高标准运行。
> - DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现
> - 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。


**Doctype文档类型**
该标签可声明三种 DTD 类型，分别表示严格版本、过渡版本以及基于框架的 HTML 文档。

- HTML5 只有一种`<!DOCTYPE html>`
- HTML 4.01 规定了三种文档类型：Strict、Transitional 以及 Frameset。
- XHTML 1.0 规定了三种 XML 文档类型：Strict、Transitional 以及 Frameset。
- Standards （标准）模式（也就是严格呈现模式）用于呈现遵循最新标准的网页，而 Quirks
- （包容）模式（也就是松散呈现模式或者兼容模式）用于呈现为传统浏览器而设计的网页。

**知识点：HTML常用的 DOCTYPE 声明**
```
# HTML 5
<!DOCTYPE html>

# HTML 4.01 Strict
该 DTD 包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

# HTML 4.01 Transitional
该 DTD 包含所有 HTML 元素和属性，包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

# HTML 4.01 Frameset
该 DTD 等同于 HTML 4.01 Transitional，但允许框架集内容。
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
"http://www.w3.org/TR/html4/frameset.dtd">
```
**知识点：XHTML常用的 DOCTYPE 声明**
```
# XHTML 1.0 Strict
该 DTD 包含所有 HTML 元素和属性，但不包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。必须以格式正确的 XML 来编写标记。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

# XHTML 1.0 Transitional
该 DTD 包含所有 HTML 元素和属性，包括展示性的和弃用的元素（比如 font）。不允许框架集（Framesets）。必须以格式正确的 XML 来编写标记。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "
http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

# XHTML 1.0 Frameset
该 DTD 等同于 XHTML 1.0 Transitional，但允许框架集内容.
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">

# XHTML 1.1
该 DTD 等同于 XHTML 1.0 Strict，但允许添加模型（例如提供对东亚语系的 ruby 支持）。
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```