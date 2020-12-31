## 宏观经济

### 中国宏观经济

#### 中国宏观杠杆率数据

接口: marco_cmlrd

目标地址: http://114.115.232.154:8080/handler/download.ashx

描述: 获取中国宏观杠杆率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 居民部门 | str | Y | - |
| 非金融企业部门 | str | Y | - |
| 政府部门 | str | Y | - |
| 中央政府 | str | Y | - |
| 地方政府 | str | Y | - |
| 实体经济部门 | str | Y | - |
| 金融部门资产方 | str | Y | - |
| 金融部门负债方 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.marco_cmlrd()
print(df_index)
```

```
年份       居民部门     非金融企业部门  ...      实体经济部门    金融部门资产方    金融部门负债方
0   1993-12   8.311222   91.658000  ...  107.791459   8.896441   7.128428
1   1994-12   7.808230   82.411703  ...   98.354271   9.808787   6.796868
2   1995-12   8.200000   81.000000  ...   97.900000  10.000000   7.000000
3   1996-03   8.400000   81.700000  ...   99.200000  10.200000   7.200000
4   1996-06   8.600000   82.100000  ...   99.700000  10.400000   7.400000
..      ...        ...         ...  ...         ...        ...        ...
```

#### 国内生产总值数据

接口: get_gdp_quarter

目标地址: http://datainterface.eastmoney.com

描述: 获取中国国内生产总值数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 季度 | str | Y | - |
| 国内生产总值 绝对值(亿元) | str | Y | - |
| 国内生产总值 同比增长 | str | Y | - |
| 第一产业 绝对值(亿元) | str | Y | - |
| 第一产业 同比增长 | str | Y | - |
| 第二产业 绝对值(亿元) | str | Y | - |
| 第二产业 同比增长 | str | Y | - |
| 第三产业 绝对值(亿元) | str | Y | - |
| 第三产业 同比增长 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_gdp_quarter()
print(df_index)
```

#### 居民消费价格指数数据(CPI)

接口: get_cpi

目标地址: http://datainterface.eastmoney.com

描述: 获取居民消费价格指数数据(CPI)

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 月份 | str | Y | - |
| 全国当月 | str | Y | - |
| 全国同比增长 | str | Y | - |
| 全国环比增长 | str | Y | - |
| 全国累计 | str | Y | - |
| 城市当月 | str | Y | - |
| 城市同比增长 | str | Y | - |
| 城市环比增长 | str | Y | - |
| 城市累计 | str | Y | - |
| 农村当月 | str | Y | - |
| 农村同比增长 | str | Y | - |
| 农村环比增长 | str | Y | - |
| 农村累计 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_cpi()
print(df_index)
```


#### 工业品出厂价格指数(PPI)

接口: get_ppi

目标地址: http://datainterface.eastmoney.com

描述: 获取工业品出厂价格指数(PPI)

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 月份 | str | Y | - |
| 当月 | str | Y | - |
| 当月同比增长 | str | Y | - |
| 累计 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_ppi()
print(df_index)
```


#### 采购经理人指数(PMI)

接口: get_pmi

目标地址: http://datainterface.eastmoney.com

描述: 获取采购经理人指数(PMI)

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 月份 | str | Y | - |
| 制造业指数 | str | Y | - |
| 制造业同比增长 | str | Y | - |
| 非制造业指数 | str | Y | - |
| 非制造业同比增长 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_pmi()
print(df_index)
```


#### 存款准备金率数据

接口: get_rrr

目标地址: http://datainterface.eastmoney.com

描述: 存款准备金率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 公布时间 | str | Y | - |
| 生效时间 | str | Y | - |
| 大型金融机构 调整前 | str | Y | - |
| 大型金融机构 调整后 | str | Y | - |
| 大型金融机构 调整幅度 | str | Y | - |
| 中小型金融机构 调整前 | str | Y | - |
| 中小型金融机构 调整后 | str | Y | - |
| 中小型金融机构 调整幅度 | str | Y | - |
| 消息公布次日指数涨跌 上证 | str | Y | - |
| 消息公布次日指数涨跌 深证 | str | Y | - |
| 备注 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_rrr()
print(df_index)
```


#### 货币供应量数据

接口: get_money_supply

目标地址: http://datainterface.eastmoney.com

描述: 存款准备金率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 月份 | str | Y | - |
| 货币和准货币(M2) 数量(亿元) | str | Y | - |
| 货币和准货币(M2) 同比增长 | str | Y | - |
| 货币和准货币(M2) 环比增长 | str | Y | - |
| 货币(M1) 数量(亿元) | str | Y | - |
| 货币(M1) 同比增长 | str | Y | - |
| 货币(M1) 环比增长 | str | Y | - |
| 流通中的现金(M0) 数量(亿元) | str | Y | - |
| 流通中的现金(M0) 同比增长 | str | Y | - |
| 流通中的现金(M0) 环比增长 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_money_supply()
print(df_index)
```

#### 外汇和黄金储备数据

接口: get_gold_and_foreign_reserves

目标地址: http://datainterface.eastmoney.com

描述: 外汇和黄金储备数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 月份 | str | Y | - |
| 国家外汇储备(亿美元) 数值 | str | Y | - |
| 国家外汇储备(亿美元) 同比 | str | Y | - |
| 国家外汇储备(亿美元) 环比 | str | Y | - |
| 黄金储备(万盎司) 数值 | str | Y | - |
| 黄金储备(万盎司) 同比 | str | Y | - |
| 黄金储备(万盎司) 环比 | str | Y | - |

接口示例

```
import gopup as gp
df_index = gp.get_gold_and_foreign_reserves()
print(df_index)
```


#### 货币汇率数据

接口: exchange_rate

目标地址: https://chl.cn/

描述: 获取货币汇率数据 

输入参数

 | 名称 | 类型 | 必须 | 描述 | 
 | ---|:---:|:---:|--- | 
 | date | str | N | 日期 默认：当天日期 | 
 | currency | str | N | 币种；默认：美元；覆盖币种有美元、欧元、日元、英镑、卢布、韩元、澳元、加元、泰铢、港币、台币、新币 | 

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| name | str | Y | 货币名称 |
| date | str | Y | 日期 |
| bankConversionPri | float | Y | 央行 汇率中间价 |
| fBuyPri | float | Y | 现汇买入价 |
| mBuyPri | float | Y | 现钞买入价 |
| fSellPri | float | Y | 现汇卖出价 |
| mSellPri | float | Y | 现钞卖出价 |


接口示例

```
import gopup as gp
g = gp.pro_api(token = "……")
df_index = g.exchange_rate(date="2020-10-10", currency="美元")
print(df_index)
```