### 新闻联播文字稿(会员)

接口: cctv_news

目标地址: http://www.xwlbo.com/

描述: 获取新闻联播文字稿, 数据区间从 2018-至今；

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
date | str | Y | 日期 如：2020-10-01

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| date | str | Y | 新闻日期 |
| title | str | Y | 新闻标题 |
| content | str | Y | 新闻内容 |

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.cctv_news(date="2020-10-10")
print(df_index)
```