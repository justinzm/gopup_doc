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

名称|类型|必选|描述
---|:---:|:---:|---
| date | str | Y | date="2020-03-19" | 

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
df_index = gp.energy_oil_hist()
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