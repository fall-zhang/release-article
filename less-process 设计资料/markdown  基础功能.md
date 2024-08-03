文章内容部分引用自

- https://www.appinn.com/markdown
- https://www.zybuluo.com/mdeditor

### 标题

# 一级标题

段落内容

> 一级标题，一般在一篇文章中只会出现一次

## 二级标题

段落内容

### 三级标题

段落内容

#### 四级标题

段落内容

##### 五级标题

段落内容

###### 六级标题

段落内容

### 普通文本

有效沟通是指信息的发送者和接收者之间能够清晰、准确地传达和理解信息的过程。它不仅涉及语言的使用，还包括非语言交流（如肢体语言、面部表情、语音语调等），以及倾听和反馈。有效沟通的特点包括：

- **清晰性**：信息表达明确，不模糊。使用简单易懂的语言，避免行业术语或复杂表达。
- **准确性**：所传达的信息真实可靠，避免误导。
- **理解**：接收者能够准确理解信息的内容。这需要沟通者关注听众的背景和理解能力。
- **反馈**：有效的沟通应鼓励双向交流，接收者可以提问或表达自己的看法，确保双方在同一理解层面上。
- **同理心**：在沟通中考虑对方的感受和观点，这有助于建立信任和理解。
- **适应性**：根据不同的情境、文化和受众调整沟通风格和方式。

Effective communication refers to the process in which the sender and receiver of information are able to convey and understand messages clearly and accurately. It encompasses not only verbal language but also non-verbal communication (such as body language, facial expressions, and tone of voice) as well as active listening and feedback. The characteristics of effective communication include:

- **Clarity**: Messages are expressed in a clear and straightforward manner, avoiding vagueness. Simple and understandable language is used, with minimal jargon or complex expressions.
- **Accuracy**: The information conveyed is truthful and reliable, preventing misinformation.
- **Understanding**: The receiver is able to accurately comprehend the content of the message. This requires the communicator to consider the background and understanding capabilities of the audience.
- **Feedback**: Effective communication encourages two-way interaction, allowing the receiver to ask questions or express their thoughts, ensuring both parties are on the same understanding level.
- **Empathy**: Considering the feelings and perspectives of the other party during communication helps build trust and understanding.
- **Adaptability**: Adjusting communication styles and methods based on different contexts, cultures, and audiences.

> 如果碰到不能输入的字符，可能需要转义字符 `\` 即 `\<`



### 超链接

超链接：https://npm.taobao.org/mirrors/git-for-windows/

### 文本变体

**加粗** **Bold**

*斜体* *emphasis*

> 一般不建议使用汉字的斜体变体，斜体一般在英文排版中使用。

### 引用文本（Blockquotes）

使用 `>` 表示块引用

> 默认引用文本

> - 引用文本
>   - 引用文本列表嵌套第二层

### 列表

以下内容都可以表示列表

**无序列表**

```text
- 这是一个列表
* 这是一个列表
-   这也是一个列表
*   这也是一个列表
```

有序列表

```text
1. 这是一个有序列表
2. 使用数字加上英文 `.` 表示有序列表 
```



- 列表嵌套引用文本

- 这是一个列表
- > 列表嵌套引用文本

- 这是最外层列表

  - 这是列表嵌套第二层
    - 列表嵌套第三层

### 分割线

以下内容都可以表示分割线

```text
* * *

***

*****

- - -

---------------------------------------
```

---

### 代码块

使用以下方式来创建代码块

````text
```js
let apple = 2
```

`let apple = 3`
````

以下内容就是是代码块

```js
let apple = 2
```

以下内容是行内代码块

`let apple = 3`

> [更多代码块](#更多代码块)

### 链接

使用以下方式来创建链接

```
[一个链接](http://example.com/)
```

以下内容就是创建好的链接样式

[一个链接](http://example.com/)

### 图片

![Static Badge](https://img.shields.io/badge/远程图片示例-图片-blue)

## 更多代码块

### JavaScript

语言别名：JS

衍生语言：JSX、TS、TSX



```js
var d1= '2014/3/13'
var d2= '2019-4-8'
alert(minuesDate(d1,d2))
function minuesDate(date1,date2){
  let day1 = new Date(date1)
  let day2 = new Date(date2)
  let time1 = day1.getTime()
  let time2 = day2.getTime()
  let time = Math.abs(time1-time2)
  return parseInt(time/1000/3600/24)
}
```

### CSS

相似语言：less、sass

```css
.pure-table {
  border-collapse: collapse;
  border-spacing: 0;
  empty-cells: show;
  border: 1px solid #cbcbcb;
}
.pure-table caption {
  color: #000;
  font: italic 85%/1 arial,sans-serif;
  padding: 1em 0;
  text-align: center;
}
```

### HTML

相似的语言：XML

```html
<p>
  <del>删除了内容</del>
  <ins>一般是下划线修饰</ins>
</p>
<style>
.pure-table {
  border-collapse: collapse;
  border-spacing: 0;
  empty-cells: show;
  border: 1px solid #cbcbcb;
}
</style>
```

### Java

```java
public class StudyFall {
  public static void main(String[] args){
    boolean result1 = 10 > 10;
    boolean result3 = 10 < 9 ;
    boolean result4 = 10 <= 7;
    boolean result5 = "fall" instanceof String;
    boolean result6 = 10 == 7;
    if(10 >= 10){
      System.out.println("10 大于等于 10");
    }
  }
}
```

### PHP

```php
<?php
	echo "<h1>笨蛋给爷死</h1>"
	echo("<h1>笨蛋给爷死</h1>")
    print_r("<h1>笨蛋给爷死</h1>")
    var_dump(100);
	/* var_dump输出的是数据类型和基本信息，类似于console.log()   多用于测试输出程序 */
?>
```

### python

```python
import turtle#turtle 的引入
turtle.setup(720,480,200,200) #设置窗口宽度，长度，窗口位置的x,y坐标
turtle.penup()#起笔，之后将不会画出轨迹=turtle.pu
turtle.pendown()#=turtle.pd 落笔
turtle.pensize()# =turtle.width设置画笔的宽度
```

### Rust

```rust
// 所有权转移
fn main() {
    let str: String = String::from("Hello");
    // 会转移所有权，将函数交给子函数释放
  take_ownership(str);
    let num = 31;
    make_copy(num);
    println!("{}", num);
    println!("{}", str); // 报错，因为所有权在执行 take_ownership 时被移交了出去
}
fn take_ownership(str: String)->String {
    println!("some uddudu {}", str);
}
fn make_copy(num: u32) {
    println!("some 928282 {}", num);
}
```

### JSX

### Vue

### JSON

### YAML

### TOML

### Bash

相关语言：sh、powershell、cmd

```
```

### C

### C++

### C#

### Dart

### go

### nginx

### XML









