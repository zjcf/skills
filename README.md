# Agent Skills

收集和维护适用于不同项目与场景的 Agent 技能。

| 技能 | 作用 |
| --- | --- |
| [accessctl-ssh](skills/accessctl-ssh/SKILL.md) | 通过 SSH 登录服务器或网络设备、执行远程命令，并保存和复用 SSH 登录凭据。 |
| [accessctl-web](skills/accessctl-web/SKILL.md) | 登录网站或设备管理页面，保存和复用网站账号、填写登录表单，并按需提交。 |

## 工具依赖

`accessctl-ssh` / `accessctl-web` 依赖 x-gateway 提供的外部工具 `xssh` / `xweb`，使用前须安装并加入 PATH。安装说明见 [x-gateway README](https://github.com/zjcf/x-gateway/blob/main/README.md)。

## 从本地仓库安装技能

已具备 Node.js、npm 和 Skills CLI 时，可在需要技能的项目目录执行以下命令。`/path/to/skills` 替换为本仓库的本地绝对路径。

```sh
npx --no-install skills add /path/to/skills
```

该命令从本地仓库读取技能，由 Skills CLI 选择技能和目标 Agent；未指定 `-g`，默认安装到当前项目。`--no-install` 要求使用已有 Skills CLI，避免隐式下载。技能安装不会安装外部工具。
