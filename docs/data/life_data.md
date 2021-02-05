### 中国油价数据

#### 汽柴油历史调价信息

接口: energy_oil_hist

目标地址: http://data.eastmoney.com/cjsj/oil_default.html

描述: 获取东方财富-中国油价-汽柴油历史调价信息；全部中国油价的所有历史数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 日期 | str | - | 价格调整的日期 | 
| 汽油价格 | float | - | 价格(元/吨) | 
| 柴油价格 | float | - | 价格(元/吨) | 
| 汽油涨幅 | str | - | 价格(元/吨) | 
| 柴油涨幅 | str | - | 价格(元/吨) | 

接口示例

```
import gopup as gp
df_index = gp.energy_oil_hist()
print(df_index)
```

#### 调价日的地区油价历史数据

接口: energy_oil_detail

目标地址: http://data.eastmoney.com/cjsj/oil_default.html

描述: 获取东方财富-中国油价-地区油价

输入参数

|名称|类型|必选|描述|
---|:---:|:---:|---
| date | str | Y | 价格调整的日期 |

此日期为调价日期, 通过调用 energy_oil_hist 可以获取历史调价日期

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 日期 | str | - | 价格调整的日期 | 
| 汽油价格 | float | - | 价格(元/吨) | 
| 柴油价格 | float | - | 价格(元/吨) | 
| 汽油涨幅 | str | - | 价格(元/吨) | 
| 柴油涨幅 | str | - | 价格(元/吨) | 

接口示例

```
import gopup as gp
df_index = gp.energy_oil_detail(date="2020-11-06")
print(df_index)
```

### 迁徙数据-百度

#### 迁入与迁出地详情

接口: migration_area_baidu

目标地址: https://qianxi.baidu.com/?from=shoubai#city=0

描述: 获取百度迁徙-迁入/迁出地数据接口

限量: 单次返回前 50 个城市, 由于百度接口限制, 目前只能返回前 50 个城市

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
area|str|Y|area="武汉", 输入需要查询的省份或者城市, 都需要用全称, 比如 湖北省, 武汉市
indicator|str|Y|indicator="move_in", 返回迁入地详情, indicator="move_in", 返回迁出地详情
date|str|Y|date="20200201", 需要滞后一天

输出参数

名称|类型|描述
---|:---:|---
city_name|str|城市名称
province_name|str|所属省份	
value|str|迁徙规模, 比例	
接口示例

```
import gopup as gp
migration_area_baidu_df = gp.migration_area_baidu(area="湖北省", indicator="move_in", date="20200201")
print(migration_area_baidu_df)
```

数据示例

```
   city_name province_name  value
0        上海市           上海市   5.77
1        阜阳市           安徽省   4.68
2        上饶市           江西省   4.57
3        亳州市           安徽省   2.44
4        重庆市           重庆市   2.34
..       ...           ...    ...
95       咸阳市           陕西省   0.26
96       潍坊市           山东省   0.25
97       烟台市           山东省   0.25
98       常德市           湖南省   0.25
99       沈阳市           辽宁省   0.24
```

#### 迁徙规模

接口: migration_scale_baidu

目标地址: https://qianxi.baidu.com/?from=shoubai#city=0

描述: 获取百度迁徙-迁徙规模

- 迁徙规模指数：反映迁入或迁出人口规模，城市间可横向对比
- 城市迁徙边界采用该城市行政区划，包含该城市管辖的区、县、乡、村

限量: 单次返回当前城市的去年和今年的迁徙规模数据, 查询参数中的 start_date 不要随意更改

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
area|str|Y|area="武汉市", 输入需要查询的省份或者城市, 都需要用全称, 比如 湖北省, 武汉市
indicator|str|Y|indicator="move_in", 返回迁入地详情, indicator="move_in", 返回迁出地详情
date|str|Y|date="20200201", 往后查询如 20200202 之后

输出参数

名称|类型|描述
---|:---:|---
日期|索引|去年和今年的日期
迁徙规模指数|str|定义参见百度, 同 covid_baidu 定义

接口示例

```
import gopup as gp
migration_scale_baidu_df = gp.migration_scale_baidu(area="湖北省", indicator="move_out", date="20200201")
print(migration_scale_baidu_df)
```

数据示例

```
    迁徙规模指数
2019-01-12  82153.440
2019-01-13  75818.916
2019-01-14  82712.988
2019-01-15  83889.108
2019-01-16  90118.008
               ...
2020-01-28  29054.052
2020-01-29  22622.328
2020-01-30  20901.564
2020-01-31  19023.984
2020-02-01  15723.072
```

### 诗词数据

#### 唐代诗人

接口: poetry_author

描述: 获取唐朝诗人姓名及诗词作品数量 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| name | str | - | 诗人姓名 | 
| dynasty | str | - | 所属朝代 | 
| poetry_num | int | - | 诗词作品数量 | 

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.poetry_author()
print(df_index)
```

#### 唐诗数据

接口: poetry_data

描述: 获取诗词作品 

输入参数

| 名称 | 类型 | 必须 | 描述 |
|---|:---:|:---:|---|
| name | str | Y | 诗人姓名 |

可从poetry_author接口获取诗人姓名

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| title | str | - | 题目 | 
| name | str | - | 作者 | 
| dynasty | str | - | 朝代 | 
| content | int | - | 诗词 | 

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.poetry_data(name="李白")
print(df_index)
```


### 影视数据

#### 实时电影票房数据

接口: realtime_boxoffice

目标地址: https://www.endata.com.cn

描述: 获取实时电影票房数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| BoxOffice | str | Y | 实时票房（万） |
| MovieName | str | Y | 影片名 |
| BoxPer | float | Y | 票房占比 （%） |
| MovieDay | float | Y | 上映天数 |
| SumBoxOffice | float | Y | 累计票房（万） |
| default_url | str | Y | 海报 |

接口示例

```
import gopup as gp
df_index = gp.realtime_boxoffice()
print(df_index)
```

#### 单日电影票房数据

接口: day_boxoffice

目标地址: https://www.endata.com.cn

描述: 获取单日电影票房数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
date | str | Y | 日期 如：2020-10-01

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| BoxOffice | float | Y | 单日票房(万) |
| MovieName | str | Y | 影片名 |
| BoxOffice_Up | float | Y | 环比变化 |
| AvgPrice | float | Y | 平均票价 |
| AvpPeoPle | float | Y | 场均人次 |
| RapIndex | float | Y | 口碑指数 |
| SumBoxOffice | float | Y | 累计票房（万） |
| default_url | str | Y | 海报 |

接口示例

```
import gopup as gp
df_index = gp.day_boxoffice(date="2020-10-10")
print(df_index)
```

#### 单日影院票房

接口: day_cinema

目标地址: https://www.endata.com.cn

描述: 获取单日影院票房

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
date | str | Y | 日期 如：2020-10-01

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| RowNum | str | Y | 排名 |
| CinemaName | str | Y | 影院名称 |
| TodayBox | float | Y | 单日票房(元) |
| TodayShowCount | float | Y | 单日场次 |
| AvgPeople | float | Y | 场均人次 |
| price | float | Y | 场均票价(元) |
| Attendance | float | Y | 上座率 |

接口示例

```
import gopup as gp
df_index = gp.day_cinema(date="2020-10-10")
print(df_index)
```

#### 实时电视剧播映指数

接口: realtime_tv

目标地址: https://www.endata.com.cn

描述: 获取实时电视剧播映指数

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| TvName | str | Y | 名称 |
| Genres | str | Y | 类型 |
| PlayIndex | float | Y | 播映指数 |
| MediaHot | float | Y | 媒体热度 |
| UserHot | float | Y | 用户热度 |
| AnswerHot | float | Y | 好评度 |
| PlayHot | float | Y | 观看度 |
| date | str | Y | 日期 |

接口示例

```
import gopup as gp
df_index = gp.realtime_tv()
print(df_index)
```

#### 实时综艺播映指数

接口: realtime_show

目标地址: https://www.endata.com.cn

描述: 获取实时综艺播映指数

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| TvName | str | Y | 名称 |
| Genres | str | Y | 类型 |
| PlayIndex | float | Y | 播映指数 |
| MediaHot | float | Y | 媒体热度 |
| UserHot | float | Y | 用户热度 |
| AnswerHot | float | Y | 好评度 |
| PlayHot | float | Y | 观看度 |
| date | str | Y | 日期 |

接口示例

```
import gopup as gp
df_index = gp.realtime_show()
print(df_index)
```


#### 艺人商业价值

接口: realtime_artist

目标地址: https://www.endata.com.cn

描述: 获取艺人商业价值

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| StarBaseName | str | Y | 排名 |
| BusinessValueIndex_L1 | float | Y | 商业价值 |
| MajorHotIndex_L2 | float | Y | 专业热度 |
| FocusHotIndex_L2 | float | Y | 关注热度 |
| PredictHotIndex_L2 | float | Y | 预测热度 |
| ReputationIndex_L3 | float | Y | 美誉度 |

接口示例

```
import gopup as gp
df_index = gp.realtime_artist()
print(df_index)
```

#### 艺人流量价值

接口: realtime_artist_flow

目标地址: https://www.endata.com.cn

描述: 获取艺人流量价值

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| Irank | str | Y | 排名 |
| StarBaseName | str | Y | 排名 |
| FlowValueIndex_L1 | float | Y | 流量价值 |
| MajorHotIndex_L2 | float | Y | 专业热度 |
| FocusHotIndex_L2 | float | Y | 关注热度 |
| PredictHotIndex_L2 | float | Y | 预测热度 |
| TakeGoodsIndex_L2 | float | Y | 带货力 |

接口示例

```
import gopup as gp
df_index = gp.realtime_artist_flow()
print(df_index)
```


### 全国高等学校名单

#### 全国普通高等学校名单

接口: university

目标地址: http://www.moe.gov.cn/

描述: 获取全国普通高等学校名单

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 序号 | str | Y | - |
| 学校名称 | str | Y | - |
| 学校标识码 | str | Y | - |
| 主管部门 | float | Y | - |
| 所在省市 | float | Y | - |
| 所在地 | float | Y | - |
| 办学层次 | str | Y | - |
| 备注 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.university()
print(df_index)
```

#### 全国成人高等学校名单

接口: adult_university

目标地址: http://www.moe.gov.cn/

描述: 获取全国成人高等学校名单

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 序号 | str | Y | - |
| 学校名称 | str | Y | - |
| 学校标识码 | str | Y | - |
| 主管部门 | float | Y | - |
| 备注 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.adult_university()
print(df_index)
```

#### 全国高等学校详情数据

接口: details_university

目标地址: http://www.moe.gov.cn/

描述: 获取全国高等学校详情数据 

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
name | str | Y | 高校名称

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| name | str | Y | 高校名称 |
| logo | str | Y | 高校logo |
| summary | str | Y | 高校概要 |
| imgs | str | Y | 高校图片 |
| tags | str | Y | 高校标签 |
| attrs | str | Y | 高校属性 |

接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.details_university(name="北京大学")
print(df_index)
```