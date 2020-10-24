## 指数数据

### 微博指数数据
接口: weibo_index

目标地址: https://data.weibo.com/index/newindex

描述: 获取指定 **词语** 的微博指数

输入参数

 | 名称 | 类型 | 必须 | 描述 | 
 | ---|:---:|:---:|--- | 
 | word | str | Y | 关键词 | 
 | time_type | str | Y | time_type="1hour"; 1hour, 1day, 1month, 3month 选其一. | 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| date | datetime | Y | 日期-索引 |
| index | float | Y | 指数 |

接口示例

```
import gopup as gp
df_index = gp.weibo_index(word="疫情", time_type="3month")
print(df_index)
```

### 百度指数数据

#### 百度搜索数据

接口: baidu_search_index

目标地址: http://index.baidu.com/v2/main/index.html

描述: 获取指定 **词语** 的百度搜索指数

输入参数

名称 | 类型 | 必选 | 描述
---|:---:|:---:|---
word|str|Y|word="股票"
start_date|str|Y|start_date="2010-12-27"
end_date|str|Y|end_date="2019-12-01"
cookie|str|Y|cookie="您在网页端登录百度指数后的 cookie 数据"; 

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
date|datetime|Y|日期-索引
index|float|Y|指数

接口示例

```
import akshare as ak
cookie = "此处输入您在网页端登录百度指数后的 cookie 数据"
index_df = ak.baidu_search_index(word="口罩", start_date='2020-01-01', end_date='2020-03-01', cookie=cookie)
print(index_df)
```

#### 百度资讯指数

接口: baidu_info_index

目标地址: http://index.baidu.com/v2/main/index.html

描述: 获取指定 **词语** 的百度资讯指数

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
word|str|Y|word="股票"
start_date|datetime.datetime|Y|start_date="2017-07-03"
end_date|datetime.datetime|Y|end_date="2019-12-01"
cookie|str|Y|cookie="您在网页端登录百度指数后的 cookie 数据"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
date|datetime|Y|日期-索引
index|float|Y|指数

接口示例

```
import gopup as gp
cookie = "此处输入您在网页端登录百度指数后的 cookie 数据"
index_df = gp.baidu_info_index(word="口罩", start_date='2020-01-01', end_date='2020-03-01', cookie=cookie)
print(index_df)
```

#### 百度媒体指数

接口: baidu_media_index

目标地址: http://index.baidu.com/v2/main/index.html

描述: 获取指定 **词语** 的百度媒体指数

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
word|str|Y|word="股票"
start_date|datetime.datetime|Y|start_date="2010-12-27"
end_date|datetime.datetime|Y|end_date="2019-12-01"
cookie|str|Y|cookie="您在网页端登录百度指数后的 cookie 数据"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
date|datetime|Y|日期-索引
index|float|Y|指数

接口示例

```
import gopup as gp
cookie = "此处输入您在网页端登录百度指数后的 cookie 数据"
index_df = gp.baidu_media_index(word="口罩", start_date='2020-01-01', end_date='2020-03-01', cookie=cookie)
print(index_df)
```

### 头条数据

#### 头条指数数据

接口: toutiao_index

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条指数

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
datetime|datetime|Y|日期
index|float|Y|指数

接口示例

```
import gopup as gp
index_df = gp.toutiao_index(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条相关性分析

接口: toutiao_relation

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条相关性分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
relation_word|str|Y|相关词
relation_score|float|Y|相关性值
score_rank|int|Y|相关性值排名
search_hot|float|Y|搜索热点值
search_ratio|float|Y|搜索比率

接口示例

```
import gopup as gp
index_df = gp.toutiao_relation(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条情感分析

接口: toutiao_sentiment

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条情感分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
keyword|str|Y|相关词
score|float|Y|情感值

接口示例

```
import gopup as gp
index_df = gp.toutiao_sentiment(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条地域分析

接口: toutiao_province

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条地域分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
name|str|Y|省份
value|float|Y|渗透率

接口示例

```
import gopup as gp
index_df = gp.toutiao_province(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条城市分析

接口: toutiao_city

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条城市分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
name|str|Y|城市
value|float|Y|渗透率

接口示例

```
import gopup as gp
index_df = gp.toutiao_city(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条年龄分析

接口: toutiao_age

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条年龄分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
name|str|Y|年龄区间
value|float|Y|渗透率

接口示例

```
import gopup as gp
index_df = gp.toutiao_age(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条性别分析

接口: toutiao_gender

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条性别分析

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
name|str|Y|性别
value|float|Y|渗透率

接口示例

```
import gopup as gp
index_df = gp.toutiao_gender(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


#### 头条用户阅读兴趣分类

接口: toutiao_interest_category

目标地址: https://index.toutiao.com/

描述: 获取指定 **词语** 的头条用户阅读兴趣分类

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="20201016"
end_date|str|Y|end_date="20201022"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
name|str|Y|分类
value|float|Y|渗透率

接口示例

```
import gopup as gp
index_df = gp.toutiao_interest_category(keyword="口罩", start_date='20201016', end_date='20201022')
print(index_df)
```


### 谷歌数据

#### 谷歌指数数据

接口: google_index

目标地址: https://trends.google.com

描述: 获取指定 **词语** 的谷歌指数数据；需要翻墙获取接口数据

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|keyword="股票"
start_date|str|Y|start_date="2019-12-10T10"
end_date|str|Y|end_date="2019-12-10T23"

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
date|str|Y|日期时间
value|str|Y|谷歌指数

接口示例

```
import gopup as gp
index_df = gp.google_index(keyword="口罩", start_date='2019-12-10T10', end_date='2019-12-10T23')
print(index_df)
```


#### 谷歌事实查证

接口: google_fact_check

目标地址: https://toolbox.google.com

描述: 获取指定 **词语** 的谷歌事实查证；需要翻墙获取接口数据

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
keyword|str|Y|查证关键词
offset|int|Y|起始数
limit|int|Y|每次获取数量 300篇最大
hl|str|N|语言 默认为全部；中文：zh，英文：en

输出参数

名称|类型|默认显示|描述
---|:---:|:---:|---
title|str|Y|信息标题
url|str|Y|信息链接
type|str|Y|查证类型
remark|str|Y|查证摘要
check|str|Y|查核机构
source_data|str|Y|信息来源
news_img|str|Y|信息图像
value|str|Y|事实查证值
date|str|Y|日期时间

接口示例

```
import gopup as gp
index_df = gp.google_fact_check(keyword="口罩", offset=0, limit=100, hl=None)
print(index_df)
```