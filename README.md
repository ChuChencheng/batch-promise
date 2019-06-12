# batch-promise

练手的小工具。

最初写这个的动机是想找个代替 `Promise.all` 的，即使 reject 也能等所有 Promise 执行完的方法。

如果只需要满足上面这个需求，也不必写这么多。还有个需求是控制同时进行的 Promise 数量。

所以这是一个保证所有 Promise 执行完才 resolve ，同时带并发控制的一个 Promise 小工具。

# Usage

与 `Promise.all` 不同的是，第一个参数传入的是返回 `Promise` 的函数的数组。

如果 `rejectOnError` 为 true ，则这个方法就是个加了并发控制的类 `Promise.all` 。

`concurrent` 是并发的最大数量。

npm 上已经有个同名的包，所以不上传了。
