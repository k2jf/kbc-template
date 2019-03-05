# kbc-template

## 功能
springboot template

## 维护者
wangyanan

## 注意事项
```
1.前端代码统一放到src/main/jscode目录下,如果需要修改可通过修改pom.xml中
  frontend-maven-plugin插件下的workingDirectory标签的指定路径
  
2.前端代码编译后生成的dist目录输出到src/main/resources目录下
-src
 -main
  -resources
   -dist
```