# path resolve
- https://parceljs.org/module_resolution.html

## 绝对路径
> /foo相对于入口根目录解析成foo。

## 波浪号路径
> ~/foo解析成foo相对于最近的包的根目录，如果不存在则是入口根目录

## Glob 文件路径
~~~
Globs 可以使用通配符一次导入多个资源，匹配一些文件(/assets/*.png)，或者匹配多个目录中的文件(/assets/**/*)
此示例打包了一个文件中的所有 png 并返回了 dist 的 URLs。
~~~

```js
import foo from '/assets/*.png'
// {
//   'file-1': '/file-1.8e73c985.png',
//   'file-2': '/file-1.8e73c985.png'
// }

```

## alias

```json
  "alias": {
    "react": "preact-compat",
    "react-dom": "preact-compat",
    "local-module": "./custom/modules"
  }
```

## TypeScript ~ 解析
> TypeScript 需要了解你是如何使用 ~ 进行模块解析和别名映射。 更多信息请参考 TypeScript 模块解析文档

```js
// tsconfig.json

{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "~*": ["./src/*"]
    }
  }
}
```

## Monorepo 解析
> 下列是 Monorepo 目前建议的用法

### 建议：

使用相对路径
若使用根目录时，使用 /

### 不建议：
> 避免在 monorepo 中使用 ~
