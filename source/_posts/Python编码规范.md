---
title: python编码规范
date: 2024-11-06 11:11:40
tags: python 
category: python
---
以下为python代码规范

### 名称类型

| 名称类型                         | 公共                          | 内部                           |
|----------------------------------|-------------------------------|--------------------------------|
| Modules                          | `lower_with_under`            | `_lower_with_under`            |
| Packages                         | `lower_with_under`            |                                |
| Classes                          | `CapWords`                    | `_CapWords`                    |
| Exceptions                       | `CapWords`                    |                                |
| Functions                        | `lower_with_under()`          | `_lower_with_under()`          |
| Global/Class Constants           | `CAPS_WITH_UNDER`             | `_CAPS_WITH_UNDER`             |
| Global/Class Variables           | `lower_with_under`            | `_lower_with_under`            |
| Instance Variables               | `lower_with_under`            | `_lower_with_under` (protected)|
|                                  |                               | `__lower_with_under` (private)|
| Method Names                     | `lower_with_under()`          | `_lower_with_under()` (protected) |
|                                  |                               | `__lower_with_under()` (private)|
| Function/Method Parameters       | `lower_with_under`            |                                |
| Local Variables                  | `lower_with_under`            |                                
