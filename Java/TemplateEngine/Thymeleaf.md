---
title: Thymeleaf
date: 2018-12-21 10:54:18
tags: 
    - 模板引擎
categories: 
    - Java
---

**目录 start**
 
1. [Thymeleaf](#thymeleaf)
    1. [流程控制](#流程控制)
        1. [if](#if)
    1. [集合处理](#集合处理)

**目录 end**|_2019-04-19 15:38_|
****************************************
# Thymeleaf
> 辣鸡

## 流程控制
### if
- lt 小于 
- eq 等于
- gt 大于
- le 小于等于
- ge 大于等于

- 拼接参数：`th:href="@{/student/ChooseTopic/{id} (id=${pageNum}-2)}"`
- 判断块`<th:block th:if="${pageNum lt pageTotal}" ></th:block>`


## 集合处理

- 判断list大小：
```
th:if="${#lists.size(topicList) == 0}"
```
