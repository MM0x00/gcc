# gcc在线体验环境


## 软件简介

GNU编译器集合（GCC）是由GNU项目生成的编译器系统，支持各种编程语言。 GCC是GNU工具链的关键组件。 自由软件基金会（FSF）根据GNU通用公共许可证（GNU GPL）分发GCC。 GCC在自由软件的发展中起着重要的作用，既是一个工具，也是一个例子。

属于编程语言类别，可以支持 C 语言开发。

特点：

1. 自由
2. 支持多种编程语言

License： GPLv3

## 软件官网

https://gcc.gnu.org

## Dockerfile 使用方法

启动运行您的应用程序的GCC实例
使用此图像的最直接的方法是使用gcc容器作为构建和运行时环境。在你的Dockerfile写作中，按照以下的方式编写和运行你的项目：

FROM gcc:4.9

COPY . /usr/src/myapp

WORKDIR /usr/src/myapp

RUN gcc -o myapp main.c

CMD ["./myapp"]

然后，构建并运行Docker映像：

$ docker build -t my-gcc-app .

$ docker run -it --rm --name my-running-app my-gcc-app

## 资源链接

- http://www.csdn.net/tag/gcc
- https://gcc.gnu.org
- https://gcc.gnu.org/onlinedocs/7.1.0/
