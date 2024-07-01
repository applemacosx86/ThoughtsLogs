---
title : 'YAML”转译符“是什么'
date : 2024-06-19T23:29:50+08:00
draft : false
---

## YAML”转译符“(escape character)是什么?
来自Gemini的解释

在 YAML 中，转义符用于指示字符串中的特殊字符，使其能够按原样表示，而不是作为特殊字符解释。例如，如果要在字符串中包含冒号 (:)，则需要对其进行转义，否则 YAML 解析器会将其解释为键值对分隔符。

以下是一些常见的 YAML 转义符：

\: 转义冒号 (:)
\": 转义双引号 (")
': 转义单引号 (')
\t: 转义制表符 (TAB)
\n: 转义换行符 (LF)
\r: 转义回车符 (CR)
\\: 转义反斜杠 ()
例如，以下 YAML 代码将字符串 "Hello, world!" 转义为字面值：

YAML
"Hello, world!"
Use code with caution.
content_copy
如果不转义冒号，则以下 YAML 代码将无效：

YAML
"Hello: world!"
Use code with caution.
content_copy
因为 YAML 解析器会将冒号解释为键值对分隔符，并将 "world!" 解析为值。要正确表示字符串 "Hello: world!"，需要对其进行转义：

YAML
"Hello\: world!"
Use code with caution.
content_copy
以下是转义符的另一个示例：

YAML
- key1: value1
- key2:
    - item1
    - item2:
        - "\tnested item"
Use code with caution.
content_copy
在这个示例中，制表符 (\t) 用于缩indent嵌套列表项。如果不转义制表符，则 YAML 解析器会将它们解释为普通的空格，这会导致缩indent不一致。

总而言之，YAML 转义符用于指示字符串中的特殊字符，使其能够按原样表示，而不是作为特殊字符解释。这对于在 YAML 文件中包含特殊字符或避免 YAML 解析器误解字符串非常重要。
