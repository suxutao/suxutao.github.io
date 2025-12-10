---
date: 2025-12-09T15:57:45+08:00
draft: false
title: Python生成requirements.txt依赖文件
tags: ["Python","项目依赖"]
categories: ["项目开发"]
---

分别用两种方法生成依赖文件

# 1.freeze

命令：

```bash
pip freeze > requirements.txt
```

![img](https://viewbed.top/20251210115501022.png)

优点：python内置工具，会生成当前环境所有的依赖包
缺点：可能把项目中没用的依赖包也包括进去了

# 2.pipreqs
需要先安装库：

```bash
pip install pipreqs
```

然后生成文件：

```bash
pipreqs ./  --force --use-local --ignore .venv
```

![img](https://viewbed.top/20251209160714050.png)

优点：只包括项目需要的依赖包，无用的依赖或间接依赖（依赖的依赖）不会被包括进去
缺点：生成的包可能不准确

# 安装依赖

有了这个文件之后就可以一键安装依赖

```bash
pip install -r requirements.txt
```

