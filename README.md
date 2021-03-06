# ⭐ ChaoxingSign | 超星学习通签到
PHP 版超星学习用自动签到，支持多用户签到，二次开发便捷！

`PHP 7.3` 测试通过，理应 `PHP 5.4` 及以上都能够使用

- 登录方式：

支持手机号码登录，不支持！！！学号登录

- 签到功能：

支持普通签到，~~手势签到，二维码签到，位置签到，拍照签到~~ （这些未测试

# 🧀 使用方法
1. 下载源码：

    直接下载：https://github.com/PrintNow/ChaoxingSign/archive/master.zip
    
    克隆源码：`git clone https://github.com/PrintNow/ChaoxingSign`

2. 🚀 运行
    1. 上传到**网站根目录**运行
    
        然后访问 `http://你的域名/main.php?account=你的超星账号&password=你的超星密码`
    
    2. 或者使用**命令行**运行
       ```
       php main.php -A "你的超星账号" -P "你的超星密码"
       ```

3. ⚙ 实现自动签到
    > 推荐大于等于 **10 分钟** 执行一次，避免出现异常
    > 
    > 我已经硬编仅能在每天的 08:00 ~ 22:00 之间运行，
    > 如果要取消或修改这一限制，请删除或注释
    > `main.php` 第 7~9 行
    1. 如果以**网页方式**运行，定时监控 `http://你的域名/main.php?account=你的超星账号&password=你的超星密码` 即可
    2. 如果使用**命令行方式**运行，添加 `crontab` 任务即可，具体添加 `crontab 任务` 方法可以网上搜。
    每天 早上8点到晚上22点之间，每10分钟签到一次 crontab 表达式：`0 */10 8-22 * * * *`

# √ 运行输出
签到成功：
```
正在签到：卡路里与健康：教你如......应该签到成功

正在签到：数据库管理与应用...应该签到成功
```

没有签到任务：
```
没有待签到的任务
```

# ❗ 注意
超星屏蔽了如 阿里云、腾讯云、百度云... 等 IDC IP 地址，故有可能出现未知的错误（我没测试，我仅在家庭宽带中测试成功）

# 🙇‍ 感谢
> 本项目的实现参考了以下文章

- https://www.z2blog.com/index.php/learn/423.html
- https://www.z2blog.com/index.php/default/459.html

> 本项目中使用到的 `Selector.php` 来自 [PHPSpider](https://github.com/owner888/phpspider) 

# License
遵循 [MIT License](./License) 协议

## 其他签到脚本推荐
> 排名部分先后

| 项目地址                                                | 开发语言   | 备注                                         |
| ------------------------------------------------------- | ---------- | ------------------------------------------  |
| https://github.com/Wzb3422/auto-sign-chaoxing           | TypeScript | 超星学习通自动签到，梦中刷网课                |
| https://github.com/Huangyan0804/AutoCheckin             | Python     | 学习通自动签到，支持手势，二维码，位置，拍照等 |
| https://github.com/mkdir700/chaoxing_auto_sign          | Python     | 超星学习通自动签到脚本&多用户多任务&API       |
| https://github.com/aihuahua-522/chaoxing-testforAndroid | Java       | 学习通（超星）自动签到                       |
| https://github.com/yuban10703/chaoxingsign              | Python     | 超星学习通自动签到                           |