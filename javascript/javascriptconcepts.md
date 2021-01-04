[MDN web javasript guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide) 與 [node guides](https://nodejs.org/en/docs/guides/) 是 javascript 的重要指引。

MDN 的 [reference:Statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements) 裡的
[async_function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) 講解了Promise, Async/await。


[node guides](https://nodejs.org/en/docs/guides/) 裡的 [learn](https://nodejs.dev/learn) 是重要的學習資源，包括:

* [the-nodejs-event-loop](https://nodejs.dev/learn/the-nodejs-event-loop) 對 setTimeout, Promises 與 Async/await 有精闢的講解。
* [understanding-process-nexttick
](https://nodejs.dev/learn/understanding-process-nexttick)
* [understanding-setimmediate](https://nodejs.dev/learn/understanding-setimmediate)
* [discover-javascript-timers](https://nodejs.dev/learn/discover-javascript-timers)
* [javascript-asynchronous-programming-and-callbacks](https://nodejs.dev/learn/javascript-asynchronous-programming-and-callbacks)
* [understanding-javascript-promises](https://nodejs.dev/learn/understanding-javascript-promises)
* [modern-asynchronous-javascript-with-async-and-await](https://nodejs.dev/learn/modern-asynchronous-javascript-with-async-and-await)



[MDN async_function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) 說明如何利用 async funtion 使用 promise
```
async function getProcessedData(url) {
  let v
  try {
    v = await downloadData(url)  // downloadData(url) is a promise
  } catch(e) {
    v = await downloadFallbackData(url) // downloadFallbackData(url) is a promise
  }
  return processDataInWorker(v) // processDataInWorker(v) is also a promise
}
```

```
async function getProcessedData(url) {
  let v
  try {
    v = await downloadData(url)
  } catch(e) {
    v = await downloadFallbackData(url)
  }
  try {
    return await processDataInWorker(v)  // Note the `return await` vs. just `return`
  } catch (e) {
    return null
  }
}
```