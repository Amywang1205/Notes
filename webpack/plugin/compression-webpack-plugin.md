```js
new CompressionPlugin({
  asset: "[path].gz[query]",
  algorithm: "gzip",
  test: /\.(js|css)$/,
  threshold: 10240,
  minRatio: 0.8
})
```
 
