
### Git + GitHub 版本管理

将 Vault 初始化为 Git 仓库，推送到 GitHub 私有仓库。

#### 实例：初始化 Vault 为 Git 仓库

``` 
# 1.进入你的 Vault 目录
cd personal-knowledge-base

# 2.首次初始化（仅执行一次）
git init

# 创建 .gitignore 文件
echo ".obsidian/workspace.json" >> .gitignore
echo ".obsidian/workspace-mobile.json" >> .gitignore
echo ".trash/" >> .gitignore

git add .
git commit -m "初始化知识库"

git remote add origin https://github.com/user_name/vault_name.git
git branch -M main
git push -u origin main

# 3.日常更新知识库
cd personal-knowledge-base

git add .
git commit -m "备注"
git push

# 4.获取 GitHub 上的新修改 
git pull
```

> Git 同步需要**手动 commit + push + pull**，不能像 iCloud 那样自动同步。适合有 Git 使用习惯的用户，或者作为其他同步方案的补充（额外增加一层版本保护）。
