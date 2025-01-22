# Bilibil-auto-ticket

## 本项目仅供Python编程学习、urllib/requests库网络请求操作学习、Selenium操作学习使用，请勿用于商业以及危害网站正常运行及数据安全用途

## 截止到 2025/01/18 在不触发风控下仍然可用

> 本软件无法保证 100% 命中率和 100% 不受哔哩哔哩安全团队行为风险控制限制，一切交给天意
>
> 本软件可能无法及时跟进哔哩哔哩/极验Geetest验证码机制更新，望知悉
>
> 本项目遵循GPL（GNU General Public License）协议进行开源，仅供学习使用，请在24小时之后删除

# 原介绍

本项目核心借鉴自https://github.com/Hobr 佬

感谢原开发者 [fengx1ao](https://github.com/fengx1a0/Bilibili_show_ticket_auto_order)

极验验证码自动化解决方案提供：[BiliTicker-gt-python](https://github.com/Amorter/biliTicker_gt)

本脚本仅供学习交流使用, 不得用于商业用途, 如有侵权请联系删除

## 功能介绍

纯api请求。

命令行界面。

不建议多开脚本抢票。（如需多开，请重新在其他文件目录下克隆并运行）

已接入PushPlus推送。

目前已经支持漫展演出等的 无证 / 单证 / 一人一证 的购买


## 使用

首先电脑端禁止抢票是前端限制，使用特殊的办法电脑也能抢；其次脚本是直接与后端通讯，不经过前端，得到的数据也会比一般看到的更多一些。所以无论怎么限制电脑端，怎么不能抢，人能做到的，脚本也能做到
登录和抢票分开的，先运行登录.exe，登陆后再运行抢票.exe

第一次使用务必先运行登录.exe

### 执行脚本

安装所需依赖
```shell
pip install -r requirements.txt
```

依次运行
```shell
python login.py     //登录.exe
python main.py      //抢票
python geetest.py   //极验滑块验证（暂时废弃）
```

### 新功能：微信公众号推送结果

需要关注pushplus微信公众号，关注后激活，然后点击个人中心-获取token，在config.txt中填入token即可在需要验证或者抢票成功后收到微信公众号通知

## 配置说明

config.txt为配置文件，不指定值为None

- proxies 指定代理 如：127.0.0.1:8080 (IP:PORT 请不要加前缀)
- specificID 多个用户登陆后指定某一个人uid(bilibili) (多用户还没做等后面有必要再写)
- sleep设置每次抢票请求间隔时间
- token设置pushplus的个人token

## 关于风控

bilibili现已加强风控政策，抢骗面临的一切后果自行负责，与开发者无关

该脚本暂不具备风控滑块验证能力，请自行斟酌使用

大佬和有能力者可以研究下风控滑块

## 关于代理

多开在4以下的无需代理

多开超过4的请自行查找代理并添加至config.txt

## 问题报告

提issue即可
