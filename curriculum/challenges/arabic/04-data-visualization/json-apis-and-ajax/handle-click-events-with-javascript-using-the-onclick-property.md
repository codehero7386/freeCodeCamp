---
id: 587d7fad367417b2b2512be1
title: Handle Click Events with JavaScript using the onclick property
challengeType: 6
forumTopicId: 301503
dashedName: handle-click-events-with-javascript-using-the-onclick-property
---

# --description--

You want your code to execute only once your page has finished loading. لهذا الغرض، يمكنك إرفاق حدث (event) من JavaScript لمستند مسمى `DOMContentLoaded`. إليك كود الذي يفعل ذلك:

```js
document.addEventListener('DOMContentLoaded', function() {

});
```

يمكنك تنفيذ معالجات الأحداث (event handlers) التي تحدث داخل وظيفة `DOMContentLoaded`. يمكنك تفعيل معالج الحدث `onclick` الذي يُفَعل عندما ينقر المستخدم على العنصر مع معرف `getMessage`، عن طريق إضافة الرمز التالي:

```js
document.getElementById('getMessage').onclick = function(){};
```

# --instructions--

أضف معالج أحداث النقر داخل وظيفة `DOMContentLoaded` للعنصر مع معرف `getMessage`.

# --hints--

يجب أن تستخدم كودك طريقة `document.getElementById` لتحديد عنصر `getMessage`.

```js
assert(code.match(/document\s*\.getElementById\(\s*?('|")getMessage\1\s*?\)/g));
```

يجب أن تضيف إلى كودك معالج الحدث `onclick`.

```js
assert(typeof document.getElementById('getMessage').onclick === 'function');
```

# --seed--

## --seed-contents--

```html
<script>
  document.addEventListener('DOMContentLoaded', function(){
    // Add your code below this line


    // Add your code above this line
  });
</script>

<style>
  body {
    text-align: center;
    font-family: "Helvetica", sans-serif;
  }
  h1 {
    font-size: 2em;
    font-weight: bold;
  }
  .box {
    border-radius: 5px;
    background-color: #eee;
    padding: 20px 5px;
  }
  button {
    color: white;
    background-color: #4791d0;
    border-radius: 5px;
    border: 1px solid #4791d0;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    background-color: #0F5897;
    border: 1px solid #0F5897;
  }
</style>
<h1>Cat Photo Finder</h1>
<p class="message box">
  The message will go here
</p>
<p>
  <button id="getMessage">
    Get Message
  </button>
</p>
```

# --solutions--

```html
<script>
  document.addEventListener('DOMContentLoaded', function(){
    // Add your code below this line
    document.getElementById('getMessage').onclick = function(){ };
    // Add your code above this line
  });
</script>

<style>
  body {
    text-align: center;
    font-family: "Helvetica", sans-serif;
  }
  h1 {
    font-size: 2em;
    font-weight: bold;
  }
  .box {
    border-radius: 5px;
    background-color: #eee;
    padding: 20px 5px;
  }
  button {
    color: white;
    background-color: #4791d0;
    border-radius: 5px;
    border: 1px solid #4791d0;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    background-color: #0F5897;
    border: 1px solid #0F5897;
  }
</style>
<h1>Cat Photo Finder</h1> 
<p class="message box">
  The message will go here
</p>
<p>
  <button id="getMessage">
    Get Message
  </button>
</p>
```
