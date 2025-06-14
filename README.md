# Github-
简单写一个Github上传项目教程，来当作我第一个项目实践。适合：完全没用过 GitHub 和 Git 的初学者 教你一步步把本地的项目上传到 GitHub 上去

# ✨ GitHub上传项目小白教程（超详细）

> 适合：完全没用过 GitHub 和 Git 的初学者  
> 教你一步步把本地的项目上传到 GitHub 上去！

---

## 🧩 第一步：准备工作

### ✅ 你需要准备的东西：

1. **一个 GitHub 账号** 👉 [注册GitHub](https://github.com/)
2. **一台电脑，装好了 Git 工具** 👉 [Git下载安装地址](https://git-scm.com/)
3. **一个你已经写好的项目文件夹**（比如你写了一个网页、Python程序等等）

---

## 🧱 第二步：创建 GitHub 仓库（就是放你项目的空间）

1. 打开 GitHub 官网，登录
2. 右上角点击 `+` → 选择 `New repository`
3. 填写：
   - **仓库名字（Repository name）**：随便起，比如 `my-first-project`
   - **描述（Description）**：可以写也可以不写
   - 建议选择：✅ `Public`（公开）
4. 点击绿色按钮 **Create repository**

📌 这时你就会进入一个新页面，上面有一堆命令，不要怕，我们等下会用到！

---

## 💻 第三步：打开你的项目文件夹，初始化 Git

### ✅ 方法一：右键 Git Bash（推荐）

如果你装了 Git，可以在项目文件夹里点右键 → Git Bash Here（或者用终端也可以）

输入下面的命令：

```bash
git init
```

这句话是告诉系统：“我要开始用 Git 管理这个项目啦”

---

## 📦 第四步：把文件添加到 Git 管理中

```bash
git add .
```

意思是：把这个项目文件夹里的所有文件都加进来

然后提交一下：

```bash
git commit -m "第一次提交"
```

这个 `"第一次提交"` 是你对这次上传的说明，随便写，但必须加引号。

---

## 🔗 第五步：连接远程仓库（也就是 GitHub）

在 GitHub 的页面上，找到一段像这样的链接：

```bash
https://github.com/你的用户名/你的仓库名.git
```

然后回到终端，输入：

```bash
git remote add origin 你的链接
```

例如：

```bash
git remote add origin https://github.com/zhangxiaobai/my-first-project.git
```

---

## 🚀 第六步：推送到 GitHub

继续在终端输入：

```bash
git branch -M main
git push -u origin main
```

这两行命令的意思是：

- 设置默认分支为 `main`
- 把项目推送到 GitHub 上

如果是第一次推送，GitHub 可能会要求你登录账户或输入 Token。现在 GitHub 不支持密码登录，推荐用 [Token 登录方法](https://docs.github.com/zh/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

---

## 🎉 恭喜你！

如果你操作成功，现在打开你的 GitHub 仓库，就能看到你上传的项目啦！

---

## 🧠 小贴士

- 以后每次更新项目，只要运行以下三条命令即可：

```bash
git add .
git commit -m "更新了什么内容"
git push
```

---

## 📎 常见错误提示 & 解决办法

| 错误信息 | 可能原因 | 解决方法 |
|----------|----------|----------|
| `fatal: remote origin already exists.` | 你重复添加了远程仓库 | 运行：`git remote remove origin` 再重新添加 |
| `authentication failed` | GitHub 不再支持密码登录 | 去 GitHub 创建 Token，用 Token 代替密码 |
