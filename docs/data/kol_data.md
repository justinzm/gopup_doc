## KOL数据

### 微博数据

#### 账户基本数据

接口: weibo_user

目标地址: http://www.weibo.com/

描述: 通过关键词获得相关微博账户信息 

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
user_id | str | Y | 账户ID

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 用户id | int | Y | 用户ID |
| 用户昵称 | str | Y | 用户昵称 |
| 性别 | str | Y | 性别 |
| 生日 | str | Y | 生日 |
| 所在地 | str | Y | 所在地 |
| 小学 | str | Y | 小学 |
| 初中 | str | Y | 初中 |
| 高中 | str | Y | 高中 |
| 大学 | str | Y | 大学 |
| 公司 | str | Y | 公司 |
| 注册时间 | str | Y | 注册时间 |
| 阳光信用 | str | Y | 阳光信用 |
| 微博数 | str | Y | 微博数 |
| 粉丝数 | str | Y | 粉丝数 |
| 关注数 | str | Y | 关注数 |
| 描述 | str | Y | 描述 |
| 网址 | str | Y | 网址 |
| 头像 | str | Y | 头像 |
| 头像原图 | str | Y | 头像原图 |
| urank | str | Y | urank |
| mbrank | str | Y | mbrank |
| 是否认证 | str | Y | 是否认证 |
| 认证类型 | str | Y | 认证类型 |
| 微博认证 | str | Y | 微博认证 |

接口示例

```
import gopup as gp
df = gp.weibo_user(user_id="2609084213")
print(df)
```

#### 微博信息

接口: weibo_list

目标地址: http://www.weibo.com/

描述: 通过微博账户获取微博的信息（用于研究只提供15天内的原创信息） 

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
user_id | str | Y | 账户ID

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 用户ID | int | Y | 用户ID |
| 微博名 | str | Y | 微博名 |
| 正文 | str | Y | 正文 |
| 头条文章url | str | Y | 头条文章url |
| 原始图片url | str | Y | 原始图片url |
| 视频url | str | Y | 视频url |
| 位置 | str | Y | 位置 |
| 发布日期 | str | Y | 发布日期 |
| 来源 | str | Y | 来源 |
| 点赞数 | str | Y | 点赞数 |
| 评论数 | str | Y | 评论数 |
| 转发数 | str | Y | 转发数 |
| 话题 | str | Y | 话题 |
| @用户 | str | Y | @用户 |

接口示例

```
import gopup as gp
df = gp.weibo_list(user_id="2609084213")
print(df)
```