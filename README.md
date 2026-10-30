# Echo 的学习笔记

Obsidian + Quartz + GitHub Pages。基于 Quartz v4，保留上游 MIT 许可。

## 编辑

在 Obsidian 中选择「打开文件夹为仓库」，打开本项目的 `content` 文件夹。
课程放入 `content/课程`，通用知识放入 `content/知识点`，实践记录放入 `content/实验与排错`。
新笔记在顶部添加 `publish: true`（YAML 属性）才会出现在网站中。

此仓库公开：只放计划公开的笔记和附件。即使页面没有发布，提交到仓库的原文也可见。
附件置于 `content/附件`。需要保密的内容留在另外的私人库，不要复制到本项目。

## 本地预览

要求 Node >= 22、npm >= 10.9.2。

```bash
npm ci
npm run preview
```

打开 http://localhost:8080，按 Ctrl+C 停止。

## 发布

```bash
npm run publish
```

命令会提交并同步修改；GitHub Actions 自动构建并发布到：
https://echowiet.github.io/learning-notes/

在 GitHub 仓库的 Actions 页面查看发布状态。保存文件本身不会自动发布。
本机终端若无法访问 GitHub，可在当前终端会话中使用系统代理；不需要修改全局 Git 配置。

## 增加课程

在 `content/课程` 下新建课程文件夹和 `index.md`，在首页添加指向课程目录的双链。
Quartz 会生成目录树、搜索、反向链接和关系图。
