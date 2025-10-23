你可能想要使用**事件**来触发您编写的任何 JavaScript 函数。

事件可以由用户或浏览器触发。

- 用户事件：
  - 鼠标事件（单击、双击、鼠标悬停）
  - 键盘事件（按键、键盘按下、键盘弹起）
  - 触摸事件（触摸开始、移动、触摸结束）

- 浏览器事件：
  - 页面加载事件（加载、卸载）
  - 窗口事件（调整大小、滚动）
  - 时间事件（setInterval、setTimeout）

最简单的方法是制作一个按钮并为其添加 `onclick` 属性。

在**漫画人物**项目中，你使用了一个按钮来触发显示用户人物概要的功能。

添加一个带有事件 `onclick="displaySummary()"` 的 `<button>` 元素。

将文本“创建”添加到 `<button>` ，以便用户知道该按钮的作用。

--- code ---
---
language: html
filename:
line_numbers: false
---

<button onclick="displaySummary()">创建</button>

--- /code ---

**提示：**将函数更改为用户单击按钮时想要使用的任何函数。 另外，更新文本以便用户知道按钮的作用。

**使用其他事件**

在**漫画人物**中，你还使用了 `DOMContentLoaded` 事件在页面加载时触发代码。

像这样使用 `.addEventListener`：

--- code ---
---
language: js
filename: 
line_numbers: false
line_number_start: 
line_highlights: 
---
   
element.addEventListener(eventType, callbackFunction);

--- /code ---

- element：要附加事件监听器的 HTML 元素
- eventType：你想要监听的事件类型（例如“click”、“keydown”、“DOMContentLoaded”）
- callbackFunction：事件发生时执行的函数

--- code ---
---
language: js
filename: scripts.js
line_numbers: true
line_number_start: 65
line_highlights: 69
---

// 检查本地存储
document.addEventListener("DOMContentLoaded", function () {    
  
  if (localStorage.getItem("lightMode") == "true") {
    document.body.classList.toggle("light-mode");
  }

});

--- /code ---
