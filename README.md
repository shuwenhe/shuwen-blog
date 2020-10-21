## 技术选型

1. web:[gin](https://github.com/gin-gonic/gin)
2. orm:[gorm](https://github.com/jinzhu/gorm)
3. database:[mysql](https://github.com/go-sql-driver/mysql)
4. 文件存储:[七牛云存储](https://www.qiniu.com/)
5. Pjax

## 项目结构

```
-webBlog
    |-config 配置文件目录
    |-controller 控制器目录
        |-admin 后台控制器
        |-home 默认前台模板
        |-api 前台接口
    |-helper 公共函数目录
    |-model model层
    |-middlermare 中间件
    |-static 静态资源目录
    |-view 模板文件目录
        |-admin 后台模板
    |-main.go 程序执行入口
    |-go.mod go官方依赖管理
```

## 进度

- [√] 登录管理
- [√] 分类管理
- [√] 文章管理
- [√] 轮播图管理
- [√] 网站配置管理
- [√] 导航管理
- [√] 友链管理
- [√] markdown 接入
- [√] 七牛云存储
- [ ] 评论功能
- [ ] 前台接口
- [ ] 前台模板渲染
- ...

## 安装部署

本项目使用 go mod 管理依赖包，所以你的 go 版本必须是 1.11 及以上

```
cd webBlog
go run main.go [-app_conf_file="配置文件地址"]
```

## 使用方法

### 使用说明

1. 修改 app_bck.ini，设置 mysql 配置及其他可选配置，并重命名为 app.ini
2. 七牛云存储，请在 app.ini 设置 qiniu 相关配置项，不设置也行，就是文章没封面图~~~
3. 系统运行会自动基于配置 account 生成后台管理账户
4. 打开 site:8080/admin/login 登录
