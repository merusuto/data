梅露可图鉴
===
查看人物和魔宠属性的APP

Installation
---
项目开发环境没有做Windows兼容，建议不要使用Windows环境开发  
Windows下可以尝试使用Vagrant和Virtual Box，搭建一个Linux开发环境  
Vagrant文档：https://docs.vagrantup.com/v2/

进入Linux或Mac命令行后
```shell
# 进入项目目录
cd path/to/project

# 安装 git
sudo apt-get install git

# 安装 ruby, https://www.brightbox.com/docs/ruby/ubuntu/
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:brightbox/ruby-ng
sudo apt-get update
sudo apt-get install ruby2.2

# 安装 Ruby 依赖库
sudo gem install bundler
bundle install
```

Usage
---
```shell
# 爬取日服资源
# 类型：unit 或 monster
# 起始ID、结束ID：资源的起止ID
# 例如：ruby bin/image_spider.rb unit 0 800
ruby bin/image_spider.rb [类型] [起始ID] [结束ID]

# 爬取国服资源
# 抓取的方式和日服不同，不需要传参
ruby bin/image_spider2.rb

# 爬取日文WIKI资料
# 类型：unit 或 monster
ruby bin/wiki_spider.rb [类型]

# 合并用户提交的数据（已审核数据）
ruby bin/update_path.rb

# 部属新数据，网页到Github Pages
# 需要联系我，开通项目写权限
ruby bin/website_deploy.rb
```
