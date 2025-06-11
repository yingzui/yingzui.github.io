---
title: Git
slug: git-z2oilwm
url: /post/git-z2oilwm.html
date: '2024-12-17 10:31:30+08:00'
lastmod: '2025-06-11 13:47:14+08:00'
toc: true
isCJKLanguage: true
---



# Git

```plaintext
$ mkdir gittest                     # 创建测试目录
$ cd gittest/                       # 进入测试目录
$ echo "This is a README file." >> README     # 创建 README.md 文件并写入内容
$ ls                                        # 查看目录下的文件
README
$ git init                                  # 初始化
$ git add README.md                         # 添加文件
$ git commit -m '初始化项目版本'				#提交并备注信息
[master (root-commit) 8632b4b] 初始化项目版本
 2 files changed, 1 insertion(+)
 create mode 100644 111.txt
 create mode 100644 README
```

配置好sshkey

![image](/images/image-20241217103655-snghbxw.png)

![image](/images/image-20241217103803-jxr5zl2.png)

粘贴到如下地方

![image](/images/image-20241217103638-uyyqp4s.png)

![image](/images/image-20241217103600-50dm44r.png)

验证一下

```plaintext
ssh -T git@github.com
```

![image](/images/image-20241217103854-70s084b.png)

```plaintext
# 提交到 Github
$ git remote add origin git@github.com:yingzui/test.git
$ git branch -M main
$ git push -u origin main
```

![image](/images/image-20241217103927-5cjqbwi.png)

提交成功

![image](/images/image-20241217103944-a9u50ev.png)

‍

后续提交只需要

```plaintext
git add 222
git commit -m '在222里面添加了些内容'
git push -u origin main
```

![image](/images/image-20241217104530-dzmdjvh.png)

再加333文件也可以

```plaintext
git add 333.md
git commit -m "新建333文件"
git push -u origin main
```

![image](/images/image-20241217104755-z8n1grm.png)

要查看当前配置有哪些远程仓库，可以用命令：

![image](/images/image-20241217110027-1fptoth.png)

# 简单来说

```plaintext
# 初始化本地仓库
git init
# 添加文件
git add.
# 进行提交
git commit -m "Initial commit"
git branch -M main
# 关联远程仓库
git remote add origin <远程仓库地址>
# 推送本地 main 分支到远程仓库并建立关联
git push -u origin main
```

**代码解释**：

1. ​`git init`​：创建一个新的本地 Git 仓库。
2. ​`git add.`​：将当前目录下的所有文件添加到 Git 的暂存区。这里的 `.`​ 表示当前目录。
3. ​`git commit -m "Initial commit"`​：将暂存区的文件提交到本地仓库，并添加了一条提交信息 "Initial commit"。
4. ​`git remote add origin <远程仓库地址>`​：将本地仓库与一个远程仓库进行关联，其中 `<远程仓库地址>`​ 是远程仓库的 URL。
5. ​`git push -u origin main`​：将本地的 `main`​ 分支推送到远程仓库 `origin`​ 的 `main`​ 分支，并建立本地 `main`​ 分支和远程 `main`​ 分支的关联。

**后续操作**：

- 一旦你使用 `git push -u origin main`​ 建立了关联，后续你可以直接使用 `git push`​ 或 `git pull`​ 来推送和拉取 `main`​ 分支的更改，而不需要再次指定 `origin main`​。例如：

```plaintext
# 进行新的提交
git add.
git commit -m "Add new feature"
# 直接推送
git push
```

![image](/images/image-20241217111426-sqjkue4.png)

![image](/images/image-20241217111438-stogi1c.png)

总之，`git push -u origin main`​ 是将本地的 `main`​ 分支推送到远程 `origin`​ 仓库的 `main`​ 分支，并设置了后续推送和拉取的默认分支，方便后续操作。

https://jincheng9.github.io/post/hugo-add-img/

​​

‍
