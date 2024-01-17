1.link本地项目<br />      使用umi link了本地包,框架默认的webpack.resolve.symlinks=true,需要配置extraBabelInclude:[link项目路径]，不然bableLoader识别不到也会导致，autoCssModule失效。<br />2."umi"与“@umijs/max”的区别<br />    umi dev 不会自动加载 presets Plugin,导致antd,qiankuan插件无法使用 需要手动设置 umi配置项preset:       [require("@umijs/max/dist/preset")],<br />  max dev会自识别<br />3.如果package.json有引入@babel/runtime，会自动开启plugin-transform-runtime插件

4.ts.config修改
```
{
  "extends": "./src/.umi/tsconfig.json",
  
}
```
5.去除项目中的@import '~antd/es/style/themes/default.less';
