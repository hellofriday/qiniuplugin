# qiniuplugin

七牛webpack插件，webpack版本要求webpack5
### 使用方式
```js
const QiniuPlugin = require('./qiniu');
const qiniuPlugin = new QiniuPlugin({
  accessKey: (process.argv.slice(2))[0], // 读取 npm / yarn 第一个参数
  secretKey: (process.argv.slice(2))[1], // 读取 npm / yarn 第二个参数
  bucket: '七牛设置的存储空间名称',
  path: '配置的七牛cname',
});

plugins: [qiniuPlugin]
```

为了安全，accessKey和secretKey需要从命令行传入。
比如:
```shell
yarn build:cdn $QN_accessKey $QN_secretKey
```
