## MathJax@3 與 MathJax 2
MathJax@3 有相當的改進， MathJax 2 裡面的MathJax.Hub.Queue 已經不見了，取而代之的是 MathJax.typeset。
## Mathjax@3
[www.mathjax.org](https://www.mathjax.org/) 是MathJax 的首頁。

第一個例子：
```
<html>
<head>
  ...
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
  ...
<head>
<body>
方程式 \(ax^2+bx+c=0\) 的解為
\[x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\]
</body>
```
## mathjaxcomp
在 [LearningMevn | graphql | client](https://github.com/hjy1210/LearningMevn/tree/master/graphql/client) 裡，參考了MathJax@3 的[configuration](http://docs.mathjax.org/en/latest/web/configuration.html#loading-additional-components) 與 [asciimath support](http://docs.mathjax.org/en/latest/input/asciimath.html) 實作了 [mathjaxcomp.vue](https://github.com/hjy1210/LearningMevn/blob/master/graphql/client/src/components/mathjaxcomp.vue)。

使用方法：
1. 在 index.html head 區段放置  
   ```
   <script>
      MathJax = {
        loader: {load: ['input/asciimath']}
      };
    </script>
    <script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    ```
2. 將 `<mathjaxcomp></mathjaxcomp>` 放在想要放的位置。
3. 在 mathjaxcom 裡面可以用 tex 格式(包括 \\(,\\\)、\\[,\\]、\`,\`標記法)輸入數學式子，按 ctrl+enter 可排版數學


