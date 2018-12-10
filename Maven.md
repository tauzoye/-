# Maven # 

## Maven一键构建部署 ##
1. cmd 进入 maven工程目录
2. 输入命令：mvn tomocat:run

## Maven目录 ##
1. bin mvn构建命令
2. boot maven自身使用的类加载器
3. conf 配置文件 setting.xml
4. lib maven自身运行所需jar包（有tomocat jar包）

## 仓库种类 ##
1. 本地仓库
2. 远程仓库（私服）
3. 中央仓库

## Maven标准目录结构 ##
1. 核心代码部分	src/main/java
2. 配置文件部分	src/main/resource
3. 测试代码部分	src/test/java
4. 测试配置文件	src/test/resource
5. 页面资源		src/main/webapp	

## Maven常用命令 ##
1. mvn clean （以下命令为一套生命周期，clean 是清除生命周期）
2. mvn compile
3. mvn test
4. mvn pakage(生成war包或者其他的包看pom.xml中的pakage属性)
5. mvn install(执行上面三个命令，并把war打入本地maven仓库)
6. mvn deploy

## maven概念模型图 ##
- ![概念图](C:/Users/Administrator/Desktop/maven概念模型图.png)

## IDEA配置 ##
- Maven - Runner  -VM Options:-DarchetypeCatalog=internal

### Live Template ###
- 定制文件模板

### 使用骨架 ###
- java工程使用quickstart骨架
- web工程 使用 webapp骨架 

## 工程包 ##
1. 作用域
- <scope>provided</scpoe>  只在编译时使用，运行时不适用
- <scope>compile</scpoe> 编译运行都适用
- <scope>runtime</scpoe> 只在运行时适用
- <scope>test</scpoe>	只在测试时使用

## 修改运行环境 ##
```
- <build>
- <plugins>
- <plugin>
- <configration>
- <port>(Tomcat端口)
- </port>
- <target> //（jdk1.8）
- </target>
- <source> //（1.8）
- </source>
- <endcoding>
- </endcoding>
- </configration>
- </plugin>
- </plugins>
- </build>//项目运行环境（jdk或者tomocat等）

```

## jar包冲突 ##
### 三个原则 ###
1. 第一声明原则  （哪个jar包坐标先声明，最终进入项目的就是哪个jar）
2. 路径近者优先原则 （直接依赖路径比传递依赖路径近）
3. 直接排除法 (使用exclusion标签直接排除某包)
```
<exclusions><exclusion>
```

## pom文件内容说明 ##
### 统一管理jar包管理 ###
```
//<properties> 定义变量
<properties>
<spring.version>1.8</spring.version> 
</properties> 
//<dependencyManager>锁定jar包版本  路径近者优先原则
```

## Maven项目模块拆分聚合 ##
- java工程打Jar包；
- web工程打war包
- 父工程打pom包

## 常用标签 ##
- <import resource="classpath:path"/>