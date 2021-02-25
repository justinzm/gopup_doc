### 新闻联播文字稿

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
df_index = gp.cctv_news(date="2020-10-10")
print(df_index)
```

### 历史上的今日

接口: history_daily

目标地址: http://www.baidu.com/

描述: 获取当天历史上的今日事件信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| year | str | Y | 事件年 |
| title | str | Y | 标题 |
| type | str | Y | 类型 |
| link | str | Y | 网址 |
| desc | str | Y | 概述 |

接口示例

```
import gopup as gp
df_index = gp.history_daily()
print(df_index)
```

### 百度风云榜

#### 百度实时热点榜

接口: baidu_hot_list

目标地址: http://www.baidu.com/

描述: 获取百度实时热点榜事件信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| id | str | Y | ID |
| title | str | Y | 标题 |
| status | str | Y | 类型 |
| link_video | str | Y | 视频网址 |
| link_search | str | Y | 搜索网址 |
| link_news | str | Y | 新闻网址 |
| link_img | str | Y | 图片网址 |
| hot | str | Y | 热度 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.baidu_hot_list()
print(df_index)
```

#### 百度今日热点榜

接口: baidu_today_hot_list

目标地址: http://www.baidu.com/

描述: 获取百度今日热点榜事件信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| id | str | Y | ID |
| title | str | Y | 标题 |
| status | str | Y | 类型 |
| link_video | str | Y | 视频网址 |
| link_search | str | Y | 搜索网址 |
| link_news | str | Y | 新闻网址 |
| link_img | str | Y | 图片网址 |
| hot | str | Y | 热度 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.baidu_today_hot_list()
print(df_index)
```


#### 百度百科热词榜

接口: baidu_hot_word_list

目标地址: http://www.baidu.com/

描述: 获取百度百科热词榜事件信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| status | str | Y | 类型 |
| link | str | Y | 网址 |
| description | str | Y | 描述 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.baidu_hot_word_list()
print(df_index)
```

### 微博热搜榜

#### 微博热搜榜

接口: weibo_hot_search_list

目标地址: http://www.weibo.com/

描述: 获取微博热搜榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| tag | str | Y | TAG |
| link | str | Y | 网址 |
| hot | str | Y | 热度 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.weibo_hot_search_list()
print(df_index)
```


#### 微博新时代榜

接口: weibo_new_era_list

目标地址: http://www.weibo.com/

描述: 获取微博新时代榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| link | str | Y | 网址 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.weibo_new_era_list()
print(df_index)
```


### 微信热词榜

#### 微信热词榜

接口: weibo_hot_search_list

目标地址: http://wx.qq.com/

描述: 获取微信热词榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| link | str | Y | 网址 |
| hot_rank | str | Y | 热度 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.weibo_hot_search_list()
print(df_index)
```

#### 微信热门榜

接口: wx_hot_list

目标地址: http://wx.qq.com/

描述: 获取微信热门榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| link | str | Y | 网址 |
| img | str | Y | 图片 |
| description | str | Y | 描述 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.wx_hot_list()
print(df_index)
```

### 知乎热搜榜

#### 知乎热搜榜

接口: zhihu_hot_search_list

目标地址: http://www.zhihu.com/

描述: 获取知乎热搜榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| query | str | Y | 搜索词 |
| display_query | str | Y | 搜索内容 |
| link | str | Y | 网址 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.zhihu_hot_search_list()
print(df_index)
```

#### 知乎热榜

接口: zhihu_hot_list

目标地址: http://www.zhihu.com/

描述: 获取知乎热榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| link | str | Y | 网址 |
| img | str | Y | 图片 |
| description | str | Y | 描述 |
| hot | str | Y | 热度 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.zhihu_hot_list()
print(df_index)
```

### 豆瓣排行榜

#### 豆瓣新片榜

接口: douban_movie_list

目标地址: http://www.douban.com/

描述: 获取豆瓣新片榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| titleCn | str | Y | 中文标题 |
| link | str | Y | 网址 |
| img | str | Y | 图片 |
| description | str | Y | 描述 |
| rate | str | Y | 等级 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.douban_movie_list()
print(df_index)
```

#### 豆瓣一周口碑榜

接口: douban_week_praise_list

目标地址: http://www.douban.com/

描述: 获取豆瓣一周口碑榜信息 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | Y | 标题 |
| trend | str | Y | 趋势 |
| link | str | Y | 网址 |
| ranking | str | Y | 排名 |

接口示例

```
import gopup as gp
df_index = gp.douban_week_praise_list()
print(df_index)
```