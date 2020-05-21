# package source
- https://parceljs.org/transforms.html

配置文件（例如 .babelrc）默认情况下不会应用于第三方node_modules中的文件。但是，如果这个模块目录是软链接的（这在一些 monorepo 约定中很常见）并且这个模块的package.json有source字段，那么将遵守当前模块目录下的配置文件。下列是source字段支持的类型值：

将所有文件视为源码，不做解析

```json
{
  "main": "foo.js",
  "source": true
}
```
