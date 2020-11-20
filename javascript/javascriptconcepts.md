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