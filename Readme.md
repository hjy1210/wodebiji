# 我的筆記

## Markdowm
  
用 [Markdown](./markdown/markdown.md) 格式寫網頁比用 [html](https://www.w3schools.com/html/) 格式輕鬆許多。

## MathJax

用 [MathJax](./mathjax/mathjax.md) 可讓網頁呈現數學公式。

## Graphics

在網頁裡利用圖形進行人機互動，效用顯著。
[threejs](https://threejs.org/) 與 [D3](https://d3js.org/) 是其中的佼佼者。


[魔術方塊玩耍](http://hjy1210.github.io/magiccube/mcn.html) 與 [台灣地區104年7月原住民人口](http://hjy1210.github.io/Geo/201507natives.html) 是兩個圖形應用網頁。

`魔術方塊玩耍` 利用 `threejs`，說明在[這裡](./graphics/three.md)。

`台灣地區104年7月原住民人口` 則是利用 `D3`，說明在[這裡](./graphics/d3.md)。




目前，用 [Observable](https://observablehq.com/) 來學習 D3 蔚為主流。Observable 類似 Jupyter Notebook 或 Rmd 檔案，是一種筆記本，文章與程式混合。雖然也是由cell 所組成，但有下列特色：
* cell 的順序與程式的順序無關
* 文章可以將變數的值內插進來
* 程式語言為 javascript，可以 import/require NPM 套件或他人的筆記本

使用 Observable 學 D3 的教材在[這裡](https://observablehq.com/@d3/learn-d3)，可在
 [gallery](https://observablehq.com/@d3/gallery) 尋找範例加以改造成自己需要的。 

## Javascript

[javascriptconcepts.md](./javascript/javascriptconcepts.md)



## QTI3.0

[qtitestform](https://sheltered-inlet-07281.herokuapp.com/cmlbank/qtitestform) 是放在網上的進行測驗的實例，他利用 heroku-mlab 與 qti-demo 兩專案來完成。

[qti-demo](https://github.com/hjy1210/qti-demo) 專案可以將 `cml` 檔案轉成可用來考試與評分的 `json` 檔案。

[heroku-mlab](https://github.com/hjy1210/heroku-mlab) 專案可以用前述的 `json` 檔案，製作網頁進行線上練習/考試。
