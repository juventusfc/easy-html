---
title: HTML 知识地图
date: 2019-11-15 14:31:27
categories: "技术"
tags:
  - HTML
  - 知识地图
description: HTML 用于定义网页的结构
---

HTML 是一种标记语言，用于定义网页的结构。

HTML 的基本结构为：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>基本结构</title>
  </head>
  <body></body>
</html>
```

## 实体

### WHAT

实体是以 `&` 开头，以 `;` 结尾的一串文本，其语法为 `&实体的名字;`。

### WHY

当发生如下两种情况，需要用到实体：

- 浏览器解析到保留字符时

  比如， `<` 是 HTML 中保留字。当页面上需要显示 `<` 时，如果直接在 HTML 中写 `<`，由于标签的开头也是 `<`，浏览器会解析为标签开始了。

- 浏览器解析到不可见的字符时

  HTML 中的多个空格，默认情况会自动被浏览器解析为一个空格。这种情况下，空格实体就派上了用场。

### HOW

常见的实体：

- `&amp;`：&
- `&quot;`: "
- `&gt;`：>
- `&lt;`：<
- `&nbsp;`：空格
- `&copy;`：版权符号

## 块标签和行内标签

- 块标签（block element）。在网页中一般通过块标签来对页面进行布局。

- 行内标签（inline element）。行内标签主要用来包裹文字。

一般情况下会在块标签中放行内标签，而不会在行内标签中放块标签。块标签中基本上什么都能放。p 标签中不能放任何的块标签。

## 非语义化标签

- `div` 标签

  没有语义，就用来表示一个区块，目前来讲 `div` 还是我们主要的布局元素。

- `span` 标签

  行内元素，没有任何的语义，一般用于在网页中选中文字。

- `a` 标签

  超链接可以让我们从一个页面跳转到其他页面，或者是当前页面的其他的位置。主要属性有：

  - `href` 指定跳转的目标路径。值可以是一个外部网站的地址，也可以写一个内部页面的地址。
  - `target` 用来指定超链接打开的位置。可选值主要有：
    - `_self` 默认值 在当前页面中打开超链接
    - `_blank` 在一个新的标签页中打开超链接

## 注释

使用 `<!-- COMMENT -->` 进行注释。

## 标签中的属性

属性是一个名值对（x=y）。属性用来设置标签中的内容如何显示。属性和标签名或其他属性应该使用空格隔开。属性不能瞎写，应该根据文档中的规定来编写，有些属性有属性值，有些没有。如果有属性值，属性值应该使用引号引起来。如 `<font color="red" size='3'>`。

## 编码

所有的数据在计算机中存储时都是以二进制形式存储的，文字也不例外,所以一段文字在存储到内存中时，都需要转换为二进制编码。当我们读取这段文字时，计算机会将编码转换为字符，供我们阅读。

- 编码：将字符转换为二进制码的过程称为编码。
- 解码：将二进制码转换为字符的过程称为解码。
- 字符集（charset）：编码和解码所采用的规则称为字符集
- 乱码问题：如果编码和解码所采用的字符集不同就会出现乱码问题
- 常见的字符集：
  - ASCII
  - ISO88591
  - GB2312
  - GBK
  - UTF-8，在开发时我们使用的字符集都是 UTF-8

## 表格

- `table` 标签来创建一个表格
- `tr` 表示表格中的一行
- `td` 表示一个单元格
- `rowspan` 纵向的合并单元格
- `colspan` 横向的合并单元格
- `thead` 头部
- `tbody` 主体
- `tfoot` 底部
- `th` 表示头部的单元格

## 表单

- `form` 创建一个表单。其中的属性 action 表示表单要提交的服务器的地址。
- `input`
  - `<input type="text" name="username" />` 文本框
  - `<input type="password" name="password" />` 密码框
  - `<input type="radio" name="hello" value="b" checked />` 单选按钮
  - `<input type="checkbox" name="test" value="1" />` 多选框
  - `<input type="submit" value="注册" />` 提交按钮
  - `<input type="reset">` 重置按钮
  - `<input type="button" value="按钮" />` 普通的按钮
- `button`
  - `<button type="submit">提交</button>` 提交按钮
  - `<button type="reset">重置</button>` 重置按钮
  - `<button type="button">按钮</button>` 普通的按钮
- `<select name="haha"> <option value="i">选项一</option> <option selected value="ii">选项二</option> <option value="iii">选项三</option> </select>` 下拉框
