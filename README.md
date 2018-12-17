## 注意事项
以下测试用例均在Ubuntu 16.04 tls中跑过

## 需要的组件
`docker` `docker-compose` `nc` `git` 等等 其中git nc 很多ubuntu自带如果没有请用`apt-get`或者`apt`安装

## 安装docker
```
# 安装docker
curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh
# 安装docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## 下载项目
```
git clone --recursive https://github.com/rc452860/SSRPanelDC.git
```

## 启动数据库
```
cd SSRPanelDC\db
bash start.sh
```


## 启动web
拿到本机ip之后填入`SSRPanelDC/web/src/.env`文件中替换`DB_HOST`
```
docker-compose up
```

等待安装完成访问本机ip地址即可.
