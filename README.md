# kbc-template

## 功能
springboot template

## 维护者
wangyanan

## 注意事项
```
1.如果前后端代码不合并到同一个项目下, 需将pom.xml中的frontend-maven-plugin插件注释掉
 
2.前端代码统一放到src/main/jscode目录下,如果需要修改可通过修改pom.xml中
  frontend-maven-plugin插件下的workingDirectory标签的指定路径
  
3.前端代码编译后生成的dist目录输出到src/main/resources目录下
-src
 -main
  -resources
   -dist
 
4.由于vue-cli3把webpack的配置做了封装,所以要修改vue项目编译后的输出路径
  需要在项目的根目录下新建vue.config.js文件,配置信息:
    module.exports = {
        // 输出文件目录
        outputDir: '../resources/dist',
        // 编译后,后台会使用webui映射dist目录
        publicPath: '/webui/'
    }
 
5.在pom.xml中frontend-maven-plugin插件在编译jscode时使用了npm run build命令,
  这里需要注意前端的papckage.json文件中scrip对象中是否含有build属性
  "scripts": {
      "serve": "vue-cli-service serve",
      "build": "vue-cli-service build",
      "lint": "vue-cli-service lint",
      "test:unit": "vue-cli-service test:unit"
    },
```