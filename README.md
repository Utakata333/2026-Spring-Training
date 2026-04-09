<h1 align="center">📘 HnuSec 2026-Spring春季培训</h1>

<p align="center">
  2026 春季培训第一周作业专用提交仓库
</p>

> 「提交时间：2026 年 4 月 9 日 - 2026 年 4 月 19 日」

## ✨ 提交说明

| 项目     | 内容                                   |
| -------- | -------------------------------------- |
| 提交范围 | 2026 春季培训第一周作业                |
| 提交时间 | 2026 年 4 月 9 日至 2026 年 4 月 19 日 |
| 提交格式 | 仅支持 Markdown（`.md`）               |
| 命名格式 | `年级-方向-id-姓名`                    |
| PR 要求  | 一个作业对应一个 PR                    |

## 📂 项目结构

- 根目录按不同专业方向划分，当前包括 `Cry/`、`Misc/`、`Pwn/`、`Re/`、`Web/`。
- 每个方向下设置独立的 `submissions/` 目录用于提交作业。
- 每个方向的第一周作业布置在 `submissions/README.md` 中。
- 请将个人作业pr在对应方向的 `submissions/` 目录中。

```text
learning/
├── Cry/
│   └── submissions/
├── Misc/
│   └── submissions/
├── Pwn/
│   └── submissions/
├── Re/
│   └── submissions/
├── Web/
│   └── submissions/
└── README.md
```

## 📝 提交规范

- 提交文件格式仅限 `.md`。
- 请自行学习markdown语法，这里提供一个学习链接：https://markdown.com.cn/basic-syntax/
- 文件名统一为 `年级-方向-id-姓名.md`。
- 请按所属方向提交到对应的 `submissions/` 目录。
- 示例：`Web/submissions/25-web-Jatopos-xxx.md`

## 📋 内容建议

建议作业文档包含以下内容：

- 标题与作业名称
- 简介或题目说明
- 环境与依赖信息
- 解题思路或步骤说明
- 关键代码片段
- 结果与总结
- 参考文章

代码片段建议使用标准 Markdown 代码块，并注明语言类型，例如：

```python
print("hello, world")
```

示例模板（大家参考就好，可以根据自己的情况修改，但是一定要具有格式化的Markdown语法）：

```
# Writeup 标题
- ID:your_id
- 方向：Cry / Misc / Pwn / Re / Web
- 日期：YYYY-MM-DD
- 平台/来源：CTFd / HackTheBox / AttackDefense / 其他
- 题目名称：Example Challenge
- 分类与分值：Web / 200 pts（难度：Medium）
- 题目链接/附件：<题目链接或附件说明>

## 目标与范围
- 靶机/远程地址：<host:port 或 docker>
- 漏洞类型：例如 SQLi / XSS / BOF / 逻辑漏洞
- 约束与规则：仅在授权范围内操作，避免影响真实生产环境

## 环境与依赖
- 操作系统：Windows / Linux / macOS
- 工具与版本：pwntools 4.x / nmap 7.x / BurpSuite / Ghidra / sqlmap / IDA Free 等
- 语言与版本：Python 3.10 / GCC 12 / Node.js 20
- 复现实验：提供启动/连接方式（如 docker、nc、ssh、HTTP）

## 解题过程
1. 信息收集与初步分析
2. 漏洞定位与可利用性验证
3. 构造 Payload / Exploit 步骤
4. 拿到 Flag 的过程（如需，flag 内容可脱敏为 `flag{redacted}`）
5. 常见坑与绕过技巧

## 关键代码
```python
# Pwn 示例：使用 pwntools 连接并构造溢出
from pwn import *
context.log_level = 'info'
# r = process('./vuln')  # 本地调试
# 或远程：
# r = remote('challenge.host', 31337)
payload = b'A' *  cyclic_find(b'aaaa') + p64(0xdeadbeef)
# r.sendline(payload)
# r.interactive()
```

## 🔄 PR 规则

- 请阅读当前目录下的 `如何PR.md`
- PR 标题格式统一为：`年级-方向-id-姓名`
- 示例：`25-web-Jatopos-xxx`

## 📌 提交提醒

- 本仓库当前仅接收第一周作业。
- 提交前请确认方向无误、文件命名规范、文档内容完整。
- 请在截止时间前完成提交和 PR 发起。
