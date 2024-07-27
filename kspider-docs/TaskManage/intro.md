## 简介

Kspider 是一个爬虫\WEB 自动化开发平台，流程的正式运行需要通过任务驱动形式，注入`metedata`以一次性或周期性运行方式，本文当将介绍 Kspider 的`metedata`注入方式，以及任务运行方式，涵盖`任务创建`、`定时任务`、`产物下载`等

## metedata

`metedata`是一个`json`格式的数据，包含任务所需要的参数，通常为该任务对应流程的可变参数，`流程`相当于函数，而`任务`相当于使用者，`metedata`则为使用者的具体参数

如设计的流程目的为爬取指定年份`西安今年人均收入`，并截图搜索页面，其中可以看出，如果需要让该流程通用，则`西安`是一个`metedata`属性，则可定义为如下：

```json
{
    "city": "西安"
}
```

将此`metedata`注入到任务中，即可完成任务创建，后续`流程`所有节点都可访问此属性

## 任务创建

创建流程任务，驱动流程运行

## 定时任务

使流程以一次性或周期性运行

## 产物下载

流程输出的数据、文件等下载