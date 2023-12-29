要将本地的 Git 仓库与 GitHub 远程仓库连接，可以按照以下步骤操作：

### 1. 在 GitHub 上创建仓库

首先，在 GitHub 上创建一个新的仓库。登录到 GitHub，点击页面右上角的 "+" 号，选择 "New repository"，然后按照页面提示创建仓库。

### 2. 在本地初始化 Git 仓库

打开 Git Bash 或终端，进入你本地项目的目录，然后运行以下命令来初始化 Git 仓库：

```bash
git init
```

### 3. 配置用户信息

运行以下命令配置你的用户信息，确保它与你在 GitHub 上的账户信息匹配：

```bash
git config --global user.name "Your GitHub Username"
git config --global user.email "your.email@example.com"
```

### 4. 添加远程仓库地址

在 GitHub 上创建完仓库后，复制仓库的地址（HTTPS 或 SSH）。

#### 使用 HTTPS：

```bash
git remote add origin https://github.com/your-username/your-repository.git
```

#### 使用 SSH：

首先，如果还没有设置 SSH 密钥，你需要创建一个。可以按照 [GitHub 的指南](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) 来完成这一步。

然后，将 SSH 地址添加为远程仓库：

```bash
git remote add origin git@github.com:your-username/your-repository.git
```

### 5. 添加、提交和推送

在本地进行一些修改，然后使用以下命令将这些更改提交到 GitHub：

```bash
git add .
git commit -m "Initial commit"
git push -u origin master
```

这将把你的本地代码推送到 GitHub 仓库。如果是第一次推送到 GitHub，你可能需要提供 GitHub 账户的用户名和密码（或者如果你使用了 SSH，则需要输入 SSH 密钥的密码）。

### 6. 查看 GitHub 上的变更

刷新 GitHub 页面，你应该能够看到刚刚推送的变更。此后，你可以通过在本地进行修改并使用 `git add`, `git commit`, 和 `git push` 来更新 GitHub 仓库。

这就是连接本地 Git 仓库与 GitHub 远程仓库的基本步骤。请确保仓库地址、用户名、邮箱等信息都正确无误。