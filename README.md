# git-backup

git-backup.

##安装
如果你的hexo版本是 2.x.x, 你需要使用以下代码安装:

``` bash
$ npm install hexo-git-backup@0.0.91 --save
```

如果你的hexo版本是 3.x.x, 你需要使用以下代码安装:

``` bash
$ npm install hexo-git-backup --save
```

## 升级

如果你已经安装了, 你必须先移除再进行升级.

``` bash
$ npm remove hexo-git-backup
$ npm install hexo-git-backup --save
```

## 配置

你需要在 `_config.yml`文件中配置.

``` yaml
backup:
    type: git
    repository:
       github: git@github.com:xxx/xxx.git,branchName
       gitcafe: git@github.com:xxx/xxx.git,branchName
```

## 使用
```
hexo backup 
```
or
```
hexo b
```
## 选项

如果你想备份你的主题,只需要在 `_config.yml`中添加`theme: your theme name`.

``` yaml
backup:
    type: git
    theme: coney,landscape,xxx
    repository:
       github: git@github.com:xxx/xxx.git,branchName
       gitcafe: git@github.com:xxx/xxx.git,branchName
```
**注意: 如果你这样做, `themes/coney/.git`文件夹将会被删除**

如果你先提交备注信息, 只需要添加 'message: update xxx'.
``` yaml
backup:
    type: git
    message: update xxx
    repository:
       github: git@github.com:xxx/xxx.git,branchName
       gitcafe: git@github.com:xxx/xxx.git,branchName
```


现在你可以开始备份你的博客了！
## 问题

你可能会因为你的计算机权限而遇到一些问题.

###Error: EISDIR, open
这是因为权限许可引起的.
只需要这样做: 'sudo hexo b' 
```
sudo hexo b
```
