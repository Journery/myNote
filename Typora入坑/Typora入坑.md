# Typora入坑

用了好几款markdown编辑器，如作业部落的cmd markdown,简书，有道云，感觉都有些不太舒服，偶然看到了typora，希望它不会令我失望

[typora 下载地址](https://typora.io/)

[github markdown语法参考](https://help.github.com/articles/basic-writing-and-formatting-syntax/#headings)

[TOC]

# 基本语法

## 1. 斜体和粗体

使用 * 和 ** 表示斜体和粗体。

示例：

这是 *斜体*，这是 **粗体**。

## 2. 分级标题

```markdown
# 这是一个一级标题

## 这是一个二级标题

### 这是一个三级标题

#### 这是一个四级标题

##### 这是一个五级标题

###### 这是一个六级标题
```


你也可以选择在**行首**加`#`号表示不同级别的标题 (H1-H6)，例如：# H1, ## H2, ### H3，#### H4。

## 3. 外链接

使用 \[描述](链接地址) 为文字增加外链接。

示例：

这是去往 [github](http://github.com) 的链接。

## 4. 无序列表

使用 *，+，- 表示无序列表，可以嵌套。

示例：

- 无序列表项 一
  - 嵌套一
    - 嵌套二
      - 嵌套（符号不会变了）
- 无序列表项 二
- 无序列表项 三

## 5. 有序列表

使用数字和点表示有序列表。

示例：

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

## 6. 文字引用

使用 > 表示文字引用。

示例：

> 野火烧不尽，春风吹又生。

## 7. 行内代码块

使用反引号将代码括起来，如 \`代码` ，表示行内代码块。

示例：

让我们聊聊 `html`。

## 8.  代码块

使用 三个反引号包围的部分 表示代码块。

示例：

```python
if __name__ == '__main__':
    print("hello world")
```





## 9.  插入图像

使用 \!\[描述](图片链接地址) 插入图像。

示例：

在线图片

![百度logo](https://www.baidu.com/img/bd_logo1.png)

本地图片(绝对路径或相对路径)

![school logo](.\logo.png)



# 10.emoji表情

用法：两个冒号包围

:happy: :apple:

:arrow_left:

:cry:

:apple:

# 高阶语法手册

## 1. 内容目录

在段落中填写 `[toc]` 以显示全文内容的目录结构。

[TOC]

## 2. 删除线

使用 ~~ 表示删除线。

 ~~这是一段错误的文本。~~

## 3. 注脚

使用 [^keyword] 表示注脚。

这是一个注脚[^footnote]的样例。

这是第二个注脚[^footnote2]的样例。

## 4. LaTeX 公式

表示整行公式：
$$
E=mc^2
$$

$$
\sum_{i=1}^n a_i=0
$$


$$
f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2
$$


$$
\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}
$$

访问 [MathJax](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) 参考更多使用方法。

## 5. 加强的代码块

支持n种编程语言的语法高亮的显示。

非代码示例：

```
$ sudo apt-get install vim-gnome
```

Python 示例：

```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

JavaScript 示例：

``` javascript
/**
* nth element in the fibonacci series.
* @param n >= 0
* @return the nth element, >= 0.
*/
function fib(n) {
  var a = 1, b = 1;
  var tmp;
  while (--n >= 0) {
    tmp = a;
    a += b;
    b = tmp;
  }
  return a;
}

document.write(fib(10));
```

## 6. 流程图

**示例**

```flow
st=>start: Start:>https://www.baidu.com
io=>inputoutput: verification
op=>operation: Your Operation
cond=>condition: Yes or No?
sub=>subroutine: Your Subroutine
e=>end

st->io->op->cond
cond(yes)->e
cond(no)->sub->io
```

 更多语法参考：[流程图语法参考](http://adrai.github.io/flowchart.js/)

## 7. 序列图

**示例 1**

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

**示例 2**

```sequence
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

 更多语法参考：[序列图语法参考](http://bramp.github.io/js-sequence-diagrams/)



## 8. 表格支持

| 项目   |   价格 | 数量 |
| ------ | -----: | :--: |
| 计算机 | \$1600 |  5   |
| 手机   |   \$12 |  12  |
| 管线   |    \$1 | 234  |

## 9. Html 标签

支持在 Markdown 语法中嵌套 Html 标签，譬如，可以用 Html 写一个纵跨两行的表格：

```html
<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>
```


<table>
    <tr>
        <th rowspan="2">值班人员</th>
        <th>星期一</th>
        <th>星期二</th>
        <th>星期三</th>
    </tr>
    <tr>
        <td>李强</td>
        <td>张明</td>
        <td>王平</td>
    </tr>
</table>
## 10. 待办事宜 Todo 列表

使用带有 [ ] 或 [x] （未完成或已完成）项的列表语法撰写一个待办事宜列表，并且支持子列表嵌套以及混用Markdown语法，例如：

    - [ ] **Cmd Markdown 开发**
        - [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
        - [ ] 支持以 PDF 格式导出文稿
        - [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
        - [x] 改进 LaTex 功能
            - [x] 修复 LaTex 公式渲染问题
            - [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
    - [ ] **七月旅行准备**
        - [ ] 准备邮轮上需要携带的物品
        - [ ] 浏览日本免税店的物品
        - [x] 购买蓝宝石公主号七月一日的船票

对应显示如下待办事宜 Todo 列表：
​        
- [ ] **Cmd Markdown 开发**
    - [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
    - [ ] 支持以 PDF 格式导出文稿
    - [x] 新增Todo列表功能 [语法参考](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments)
    - [x] 改进 LaTex 功能
        - [x] 修复 LaTex 公式渲染问题
        - [x] 新增 LaTex 公式编号功能 [语法参考](http://docs.mathjax.org/en/latest/tex.html#tex-eq-numbers)
- [ ] **七月旅行准备**
    - [ ] 准备邮轮上需要携带的物品
    - [x] 浏览日本免税店的物品
    - [x] 购买蓝宝石公主号七月一日的船票

        
[^footnote]: 这是一个 *注脚* 的 **文本**。

[^footnote2]: 这是另一个 *注脚* 的 **文本**。



