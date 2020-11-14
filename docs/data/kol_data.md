## KOL数据

### 微博数据

#### 微博账户数据

接口: weibo_user

目标地址: http://www.weibo.com/

描述: 通过关键词获得相关微博账户信息(vip接口，找作者所要token)

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
keyword | str | Y | 关键词

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| user_id | int | Y | 用户ID |
| nink_name | str | Y | 用户昵称 |
| avatar | str | Y | 头像 |
| province | str | Y | 省 |
| city | str | Y | 市 |
| gender | str | Y | 性别 |
| friends_count | str | Y | 关注量 |
| followers_count | str | Y | 粉丝量 |
| favourites_count | str | Y | 收藏量 |
| statuses_count | str | Y | 微博量 |
| created_at | str | Y | 创建时间 |

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.weibo_user(keyword="雷军")
print(df_index)
```

#### 微博运营数据

接口: weibo_urls

目标地址: http://www.weibo.com/

描述: 通过微博链接获取该微博的基本数据(vip接口，找作者所要token)

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
urls | list | Y | 微博文章url

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| user_id | int | Y | 用户ID |
| nink_name | str | Y | 用户昵称 |
| url | str | Y | 微博URL |
| province | str | Y | 省 |
| city | str | Y | 市 |
| source | str | Y | 来源 |
| text | str | Y | 文章内容 |
| reposts_count | str | Y | 转发量 |
| comments_count | str | Y | 评论量 |
| attitudes_count | str | Y | 点赞量 |
| pic_urls | str | Y | 图片url |
| created_at | str | Y | 创建时间 |

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.weibo_urls(urls=["https://weibo.com/3151530492/JsWLgaBPp"])
print(df_index)
```