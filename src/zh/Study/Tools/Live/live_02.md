---
title: Markdown 示例
category:
  - Study
  - Tools
  - Live
  - MD
---

## 一、通用 Markdown 示例

### 1.1 标题

```markdown
H1: # Header 1
H2: ## Header 2
H3: ### Header 3
H4: #### Header 4
H5: ##### Header 5
H6: ###### Header 6
```


### 1.2 文本

这句话里拥有**加粗**、*倾斜*和删除

```markdown
这句话里拥有**加粗**、*倾斜*和~~删除~~
```

### 1.3 段落

这是一个段落。

这是另一个段落。

```markdown
这是一个段落

这是另一个段落。
```

### 1.3 换行

这是一句话不过我要在这里
换行且
再次换行

```markdown
这是一句话不过我要在这里  
换行且\
再次换行
```

提示

上方的代码中 `这里` 后面有两个空格

### 1.4 引用

> 引用也可以连用
>
> > 可以添加额外的大于号制造更深的引用

```markdown
> 引用也可以连用
>
> > 可以添加额外的大于号制造更深的引用
```

### 1.4 列表

#### 1.4.1 无序列表

- 无序列表项

- 无序列表项

  - 列表中的列表项

    - 更多的列表项
    - 更多的列表项
    - 更多的列表项

  - 列表中的长列表项，这个列表项很长。

    而且由很多个段落构成。

    甚至最后一个段落还包含了[链接](/demo.html#链接)。

- 无序列表项

```markdown
- 无序列表项
- 无序列表项

  - 列表中的列表项
    - 更多的列表项
    - 更多的列表项
    - 更多的列表项
  - 列表中的长列表项，这个列表项很长。

    而且由很多个段落构成。

    甚至最后一个段落还包含了[链接](#链接)。

- 无序列表项
```

#### 1.4.2 有序列表

1. 有序列表第一项
2. 有序列表第二项
   第二项的需要换行
   再次换行
3. 有序列表第三项

```markdown
1. 有序列表第一项
1. 有序列表第二项  
   第二项的需要换行\
   再次换行
1. 有序列表第三项
```

提示

上方的代码中`换行`后面有也两个空格

### 1.5 分割线

------

```markdown
---
```

### 1.6 链接

[根目录访问主页](https://theme-hope.vuejs.press/v2/)

[相对路径访问主页](https://theme-hope.vuejs.press/zh/)

[根目录访问贡献指南](https://theme-hope.vuejs.press/v2/contribution)

[相对路径访问贡献指南](https://theme-hope.vuejs.press/zh/contribution.html)

```markdown
[根目录访问主页](/v2/)

[相对路径访问主页](../../README.md)

[根目录访问贡献指南](/v2/contribution)

[相对路径访问贡献指南](../../contribution.md)
```

提示

VuePress 还兼容如下跳转到主页的写法:

- [相对路径访问，兼容 Markdown 编写时相互跳转](https://theme-hope.vuejs.press/zh/)
- [根目录访问主页 2](https://theme-hope.vuejs.press/)
- [HTML 形式](https://theme-hope.vuejs.press/zh/index.html)

如果希望在使用编辑器编辑 Markdown 时也能够进行相互跳转的话，则需要全部使用**相对路径**，并且`README.md`**不能省略**。

代码:

```markdown
[根目录访问主页 2](/README.md)

[相对路径访问，兼容 Markdown 编写时相互跳转](../../README.md)

[HTML 形式](../../index.html)
```

### 1.7 图片

![image-20230924191057309](https://yong-gan-niu-niu-1311841992.cos.ap-beijing.myqcloud.com/images/image-20230924191057309.png)



### 1.8 Emoji

经典方式:

😉 😢 😆 😋

```markdown
:wink: :cry: :laughing: :yum:
```

简写:

😎 😃 :* 😦 😃 😦 😉

```markdown
8-) :) :\* :( :-) :-( ;)
```

提示

### 1.9 表格

|     居中      |         右对齐 | 左对齐         |
| :-----------: | -------------: | :------------- |
| 居中使用`:-:` | 右对齐使用`-:` | 左对齐使用`:-` |
|       b       |      aaaaaaaaa | aaaa           |
|       c       |           aaaa | a              |

```markdown
|     居中      |         右对齐 | 左对齐         |
| :-----------: | -------------: | :------------- |
| 居中使用`:-:` | 右对齐使用`-:` | 左对齐使用`:-` |
|       b       |      aaaaaaaaa | aaaa           |
|       c       |           aaaa | a              |
```

### 1.10 代码

行内代码效果: `code`

```markdown
行内代码效果: `code`
```

缩进代码:

```text
// Some comments
line 1 of code
line 2 of code
line 3 of code
```

实际代码:

```markdown
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

块级代码

~~~markdown
Sample text here...
块级代码

```
Sample text here...
```
~~~

高亮格式:

~~~javascript
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
高亮格式:

```js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```
~~~

