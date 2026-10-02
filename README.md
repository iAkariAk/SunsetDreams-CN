# Sunset Dreams (日落之梦) 汉化项目

本项目是对**ElRichMC**百万粉丝特别企划西班牙语地图**Sunset Dreams**的基于[**MCT**](https://github.com/iAkariAk/mct)中文汉化项目

## 项目结构

```plain
mappings.json  硬编码的键与值映射
terms.json     术语表
mct.toml       mct项目配置
patterns/*     该项目自定义的mct pattern
src/           原地图文件
```

**注意:** 出于版权保护, 本项目不上传Sunset Dreams原始地图文件, 也不会直接分发成品世界文件.
请从[该视频](https://www.youtube.com/watch?v=rRhNB19SExc)的简介下载链接下载, 并解压地图到src目录.

## 构建指南

初次clone后, 按照上述`注意`所描述步骤放置地图源文件. 

- 使用`mct project update` 提取地图文字
- 使用`mct project build`  构建成品世界
- 使用`mct project patch`  构建分发补丁

## 贡献指南

若你在游玩过程中发现缺翻情况, 请附带截图通过issue上报; 若觉得译文质量欠缺, 您可在issue讨论.
当然：**PR WELCOME**

## 补丁使用

```bash
mct patch apply -i <原地图目录> -p <补丁路径>
```

若输出验证失败, 则说明你的地图文件与原始地图文件不一致. 若你100%确认有关数据包、区块mca等文件的确没有修改, 可追加参数
`--validation-strategy=Warning`忽略验证失败
