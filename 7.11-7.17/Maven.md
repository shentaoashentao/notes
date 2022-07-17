### Maven

提供依赖管理的机制

依赖管理就是管理项目所依赖的第三方资源

需要做的就是在 POM 文件里指定依赖 Jar 包的名称、版本号，Maven 会自动下载，并递归地去下载依赖的进一步依赖。（本次仓库--私服--中央仓库）

常用命令

   compile：编译

 clean：清理

test ：测试

package：打包

install：安装

依赖范围

![img](https://cdn.nlark.com/yuque/0/2022/png/29500568/1657965298334-9b56369c-fc90-410b-a43d-7e325e79cfee.png)