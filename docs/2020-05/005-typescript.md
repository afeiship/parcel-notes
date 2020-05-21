# typescript


```shell
npm install --save-dev typescript
npm install --save-dev parcel-bundler
```


## html
```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
  <head> </head>
  <body>
    <!-- 这里 👇 -->
    <script src="./myTypescriptFile.ts"></script>
  </body>
</html>
```

## scripts
```json
// package.json
"scripts": {
  "start": "parcel index.html"
}
```

## build
```json
// package.json
"scripts": {
  "start": "parcel myTypescriptFile.ts"
}
```
