面向 Cloudflare 的多账号管理平台，提供 Workers 与配套资源（KV / D1 / 域名 / DNS）的集中化管理与批量运维能力。
  <img width="1280" height="567" alt="7f3310fd82aa3f8bcb223963a585d4d0" src="https://github.com/user-attachments/assets/190fbed4-b9fd-4c9a-9a6e-0693800172ab" />

<img width="1376" height="931" alt="ec086bd7b9665610aa0e702077f06d7e" src="https://github.com/user-attachments/assets/3024b23e-5158-4636-9185-31ea70848c11" />

  核心功能
  - 多账号登录与切换，支持保存多组 Email + Global API Key
  - Workers 管理：列表、查看脚本、部署/更新、删除
 - Workers 批量管理：方法有三种 第一可使用内置模板一键部署,第二可远程链接部署,第三可自定义脚本部署
  - Workers 资源绑定：KV / D1 一键绑定到指定 Worker
  - 环境变量管理：普通变量与密钥变量批量维护
  - Workers 子域与自定义域名：开关、添加、删除、查看域名状态
  - KV 管理：命名空间创建/删除、键列表、读写与删除
  - D1 管理：创建/删除数据库、执行 SQL 查询
  - 域名与 DNS 管理：域名添加/删除、DNS 记录增删改查
  - 数据统计：当日请求量统计（Workers + Pages Functions）
  - 支持从外部 URL 拉取脚本内容，便于快速部署
    测试链接https://cf.yifang.qzz.io/

    使用方法

  - 使用Cloudflare得workers部署。
  - 推荐添加变量名称为大写的ACCESS_PASSWORD，建立访问密码。不设则不启用密码保护。
  - 推荐建立任意名称KV空间。 绑定建立的KV空间，变量名为大写的CF_ACCOUNTS_KV，用来存储账号信息，不绑定则存储在本地浏览器。
  - 批量导入格式为：每行一个账号，格式：邮箱|GlobalApiKey。
