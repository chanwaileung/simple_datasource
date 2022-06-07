### 步骤

1、安装npm

2、使用npx初始化一个grafana插件项目
```
npx @grafana/toolkit plugin:create my-plugin
```
在创建初始化项目时候需要选择`plugin type`，记得要选`Backend Datasource Plugin`

3、构建二进制文件
```
cd my-plugin
yarn install
yarn build
mage -v
```

4.修改[my-plugin/pkg/plugin/plugin.go中的query方法](https://github.com/chanwaileung/simple_datasource/blob/master/plugin.go#L74) ，控制其返回的数据