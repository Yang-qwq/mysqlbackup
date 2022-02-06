# mysqlbackup - git

一个通过git自动备份mysql数据库的脚本

## 使用方法

1. 在任意代码托管平台创建仓库，并初始化本地储存库

```bash
git init
```

2. 添加远端储存库地址，并执行第一次提交与推送

```bash
git remote add origin https://git.example.net/backup.git
git add *
git commit -m "初始化储存库"
git push --set-upstream origin master
```

3. 添加计划执行任务（如crontab）

```bash
crontab -e
# 进入crontab编辑模式
#editor:
0 2 */7 * * /path/to/script/backup

# 然后按下Ctrl+S 和 Ctrl+X
crontab: installing new crontab
```

4. 大功告成！

ps: 如果你想执行手动备份，可以直接在执行时加入要提交的内容即可，如

```bash
./backup 这是一个手动提交的例子
```

如果想为这个项目做贡献，欢迎提交**issue**或者发起**pr**
