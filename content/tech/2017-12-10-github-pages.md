Title: 使用Github Pages + pelican搭建个人Blog
Date: 2010-12-03 10:20
Modified: 2010-12-05 19:30
Category: Tech
Tags: pelican, publishing
Slug: tech2
Authors: Quan
Summary: Short version for index and feeds

### Mac安装Jekyll

```
gem install jekyll bundler
```
如果碰到权限之类的问题需要用：
```
sudo gem install jekyll bundler
```
还是不行的话用这个：
```
sudo gem install -n /usr/local/bin jekyll bundler
```

### 安装Hyde主题

克隆Hyde到Github pages

### 启动Jekyll方便本地调试
cd到Github pages对应的文件夹
```
jekyll serve
```
很可能报错，需要装各种依赖包，比如：
```
sudo gem install jekyll-paginate
sudo gem install jekyll-gist
sudo gem install pygments.rb
sudo gem install redcarpet
```

### Mac 杀掉占用某个端口的进程
两个小命令:
`lsof -i :端口`
`kill -9 进程ID`
