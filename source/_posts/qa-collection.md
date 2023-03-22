---
title: 开发遇见的问题合集
date: 2023-10-26 02:44:26
cover: /images/preview3.jpg
coverWidth: 1600
coverHeight: 900
tags:
    - qa
categories: 
    - qa
---

[__SSH相关问题__](#ssh)
[-1.SSH如何保持连接不自动断开](#ssh_keepalive)
[__Linux 遇到的问题__](#linux)
[-1.Sed -e expression #1, char 14: unknown option to `s'](#sed_err1)
[__Mac M1 遇到的问题__](#mac)

# <h2 id="ssh">SSH相关问题</h2>

# <h3 id="ssh_keepalive">1.SSH如何保持连接不自动断开</h3>

```bash
cat > ~/.ssh/config << EOF
Host *
    ServerAliveInterval 60
EOF
```

# <h2 id="linux">Linux 遇到的问题</h2>

# <h3 id="sed_err1">1.unknown option to 's'</h3>

Q: __Sed -e expression #1, char 14: unknown option to 's'__
A: __sed使用变量替换,且变量含有'/'时__

```bash
var="/etc/host"
// 习惯写法
sed -i "s/regex/$var/" file
// 可用 # ~ 替换
sed -i "s~regex~$var~" file
```

# <h2 id="mac">Mac M1 遇到的问题</h2>

__{% post_link mac-issue Mac M1 遇到的问题 %}__

