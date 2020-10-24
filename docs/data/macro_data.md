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

#### 年度国内生产总值数据

接口: get_gdp_year

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取年度国内生产总值数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| year | - | Y | 统计年度 |
| gdp | - | Y | 国内生产总值(亿元) |
| pc_gdp | - | Y | 人均国内生产总值(元) |
| gnp | - | Y | 国民生产总值(亿元) |
| pi | - | Y | 第一产业(亿元) |
| si | - | Y | 第二产业(亿元) |
| industry | - | Y | 工业(亿元) |
| cons_industry | - | Y | 建筑业(亿元) |
| ti | - | Y | 第三产业(亿元) |
| trans_industry | - | Y | 交通运输仓储邮电通信业(亿元) |
| lbdy | - | Y | 批发零售贸易及餐饮业(亿元) |

接口示例

```
import gopup as gp
df_index = gp.get_gdp_year()
print(df_index)
```

```
    year       gdp   pc_gdp  ...        ti  trans_industry      lbdy
0   2019  990865.0  70892.0  ...  534233.0         42802.0  113886.0
1   2018  919281.0  64644.0  ...  489701.0         40550.2  100223.8
2   2017  820754.3  59201.0  ...  425912.1         37172.6   92348.2
3   2016  740060.8  53680.0  ...  383373.9         33058.8   84648.8
4   2015  685992.9  50028.0  ...  346178.0         30487.8   78340.4
```

#### 季度国内生产总值数据

接口: get_gdp_quarter

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取季度国内生产总值数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| quarter | - | Y | 季度 |
| gdp | - | Y | 国内生产总值(亿元) |
| gdp_yoy | - | Y | 国内生产总值同比增长(%) |
| pi | - | Y | 第一产业增加值(亿元) |
| pi_yoy | - | Y | 第一产业增加值同比增长(%) |
| si | - | Y | 第二产业增加值(亿元) |
| si_yoy | - | Y | 第二产业增加值同比增长(%) |
| ti | - | Y | 第三产业增加值(亿元) |
| ti_yoy | - | Y | 第三产业增加值同比增长(%) |

接口示例

```
import gopup as gp
df_index = gp.get_gdp_quarter()
print(df_index)
```

```
    quarter       gdp  gdp_yoy       pi  ...        si  si_yoy        ti  ti_yoy
0    2019.4  990865.1      6.1  70466.7  ...  386165.3     5.7  534233.1     6.9
1    2019.3  712845.4      6.2  43005.0  ...  276912.5     5.6  392927.9     7.0
2    2019.2  460636.7      6.3  23207.0  ...  179122.1     5.8  258307.5     7.0
3    2019.1  218062.8      6.4   8769.4  ...   81806.5     6.1  127486.9     7.0
4    2018.4  900309.5      6.6  64734.0  ...  366000.9     5.8  469574.6     7.6
```

#### 三大需求对GDP贡献数据

接口: get_gdp_for

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取三大需求对GDP贡献数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
year | - | Y | 统计年度
end_for | - | Y | 最终消费支出贡献率(%)
for_rate | - | Y | 最终消费支出拉动(百分点)
asset_for | - | Y | 资本形成总额贡献率(%)
asset_rate | - | Y | 资本形成总额拉动(百分点)
goods_for | - | Y | 货物和服务净出口贡献率(%)
goods_rate | - | Y | 货物和服务净出口拉动(百分点)
        
接口示例

```
import gopup as gp
df_index = gp.get_gdp_for()
print(df_index)
```

```
    year  end_for  for_rate  asset_for  asset_rate  goods_for  goods_rate
0   2019     57.8       NaN       31.2         NaN       11.0         NaN
1   2018     76.2       5.0       32.4         2.2       -8.6        -0.6
2   2017     57.6       3.9       33.8         2.3        8.6         0.6
3   2016     66.5       4.5       43.1         2.9       -9.6        -0.7
4   2015     59.7       4.1       41.6         2.9       -1.3        -0.1
5   2014     48.8       3.6       46.9         3.4        4.3         0.3
```

#### 三大产业对GDP拉动数据

接口: get_gdp_pull

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取三大产业对GDP拉动数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
year | - | Y | 统计年度
gdp_yoy | - | Y | 国内生产总值同比增长(%)
pi | - | Y | 第一产业拉动率(%)
si | - | Y | 第二产业拉动率(%)
industry | - | Y | 其中工业拉动(%)
ti | - | Y | 第三产业拉动率(%)
        
接口示例

```
import gopup as gp
df_index = gp.get_gdp_pull()
print(df_index)
```

```
    year  gdp_yoy   pi   si  industry   ti
0   2019      6.1  NaN  NaN       NaN  NaN
1   2018      6.6  0.3  2.4       2.1  3.9
2   2017      6.8  0.3  2.4       2.1  4.0
3   2016      6.7  0.3  2.6       2.1  3.9
4   2015      6.9  0.3  2.9       2.4  3.7
5   2014      7.3  0.3  3.5       2.9  3.5
```

#### 三大产业贡献率数据

接口: get_gdp_contrib

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取三大产业贡献率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
year | - | Y | 统计年度
gdp_yoy | - | Y | 国内生产总值
pi | - | Y | 第一产业献率(%)
si | - | Y | 第二产业献率(%)
industry | - | Y | 其中工业献率(%)
ti | - | Y | 第三产业献率(%)
        
接口示例

```
import gopup as gp
df_index = gp.get_gdp_contrib()
print(df_index)
```

```
    year  gdp_yoy    pi    si  industry    ti
0   2018    100.0   4.2  36.1      31.7  59.7
1   2017    100.0   4.8  35.7      31.8  59.6
2   2016    100.0   4.1  38.2      30.8  57.7
3   2015    100.0   4.5  42.5      35.5  53.0
4   2014    100.0   4.6  47.9      39.2  47.5
5   2013    100.0   4.2  48.5      40.5  47.2
```

#### 居民消费价格指数数据

接口: get_cpi

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取居民消费价格指数数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
month | - | Y | 统计月份
cpi | - | Y | 价格指数
        
接口示例

```
import gopup as gp
df_index = gp.get_cpi()
print(df_index)
```

```
       month     cpi
0     2020.2  105.17
1     2020.1  105.38
2    2019.12  104.46
3    2019.11  104.49
4    2019.10  103.76
```

#### 工业品出厂价格指数

接口: get_ppi

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取工业品出厂价格指数数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
month | - | Y | 统计月份
ppiip | - | Y | 工业品出厂价格指数
ppi | - | Y | 生产资料价格指数
qm | - | Y | 采掘工业价格指数
rmi | - | Y | 原材料工业价格指数
pi | - | Y | 加工工业价格指数
cg | - | Y | 生活资料价格指数
food | - | Y | 食品类价格指数
clothing | - | Y | 衣着类价格指数
roeu | - | Y | 一般日用品价格指数
dcg | - | Y | 耐用消费品价格指数
        
接口示例

```
import gopup as gp
df_index = gp.get_ppi()
print(df_index)
```

```
       month  ppiip   ppi     qm   rmi  ...     cg   food  clothing   roeu   dcg
0    2019.10   98.4  97.4   98.1  94.4  ...  101.4  104.4     100.6  100.4  98.2
1     2019.9   98.8  98.0  100.6  95.2  ...  101.1  103.3     100.9  100.8  98.2
2     2019.8   99.2  98.7  102.8  96.5  ...  100.7  102.6     100.9  100.6  98.0
3     2019.7   99.7  99.3  103.2  97.1  ...  100.8  102.0     101.3  100.8  98.8
4     2019.6  100.0  99.7  104.5  97.9  ...  100.9  102.2     101.6  100.5  99.1
```

#### 存款利率数据

接口: get_deposit_rate

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取存款利率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
date | - | Y | 变动日期
deposit_type | - | Y | 存款种类
rate | - | Y | 利率（%）
        
接口示例

```
import gopup as gp
df_index = gp.get_deposit_rate()
print(df_index)
```

```
           date            deposit_type  rate
0    2015-10-24                定活两便(定期)    --
1    2015-10-24            定期存款整存整取(半年)  1.30
2    2015-10-24            定期存款整存整取(二年)  2.10
3    2015-10-24           定期存款整存整取(三个月)  1.10
4    2015-10-24            定期存款整存整取(三年)  2.75
```


#### 贷款利率数据

接口: get_loan_rate

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取贷款利率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
date | - | Y | 执行日期
loan_type | - | Y | 存款种类
rate | - | Y | 利率（%）
        
接口示例

```
import gopup as gp
df_index = gp.get_loan_rate()
print(df_index)
```

```
           date         loan_type   rate
0    2015-10-24       短期贷款(六个月以内)   4.35
1    2015-10-24      短期贷款(六个月至一年)   4.35
2    2015-10-24       中长期贷款(三至五年)   4.75
3    2015-10-24       中长期贷款(五年以上)   4.90
4    2015-10-24       中长期贷款(一至三年)   4.75
```

#### 存款准备金率数据

接口: get_rrr

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取存款准备金率数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
date | - | Y | 变动日期
before | - | Y | 调整前存款准备金率(%)
now | - | Y | 调整后存款准备金率(%)
changed | - | Y | 调整幅度(%)

接口示例

```
import gopup as gp
df_index = gp.get_rrr()
print(df_index)
```

```
          date before    now changed
0   2020-01-01  13.00  12.50   -0.50
1   2019-09-16  13.00  13.00   -0.50
2   2019-01-25  13.50  13.00   -0.50
3   2019-01-15  14.00  13.50   -0.50
4   2018-10-15  15.00  14.00   -1.00
5   2018-07-05  15.50  15.00   -0.50
```


#### 货币供应量数据

接口: get_money_supply

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取货币供应量数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
month | - | Y | 统计时间
m2 | - | Y | 货币和准货币（广义货币M2）(亿元)
m2_yoy | - | Y | 货币和准货币（广义货币M2）同比增长(%)
m1 | - | Y | 货币(狭义货币M1)(亿元)
m1_yoy | - | Y | 货币(狭义货币M1)同比增长(%)
m0 | - | Y | 流通中现金(M0)(亿元)
m0_yoy | - | Y | 流通中现金(M0)同比增长(%)
cd | - | Y | 活期存款(亿元)
cd_yoy | - | Y | 活期存款同比增长(%)
qm | - | Y | 准货币(亿元)
qm_yoy | - | Y | 准货币同比增长(%)
ftd | - | Y | 定期存款(亿元)
ftd_yoy | - | Y | 定期存款同比增长(%)
sd | - | Y | 储蓄存款(亿元)
sd_yoy | - | Y | 储蓄存款同比增长(%)
rests | - | Y | 其他存款(亿元)
rests_yoy | - | Y | 其他存款同比增长(%)

接口示例

```
import gopup as gp
df_index = gp.get_money_supply()
print(df_index)
```

```
       month          m2 m2_yoy  ... sd_yoy      rests rests_yoy
0     2020.2  2030830.42   8.80  ...     --  237842.08        --
1     2020.1  2023066.49   8.40  ...     --  232436.92        --
2    2019.12  1986488.82   8.70  ...     --  227831.79        --
3    2019.11  1961429.56   8.20  ...     --  227764.13        --
4    2019.10  1945600.55   8.40  ...     --  220312.05        --
```

#### 货币供应量数据

接口: get_money_supply_bal

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取货币供应量(年底余额)数据

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
year | - | Y | 统计年度
m2 | - | Y | 货币和准货币(亿元)
m1 | - | Y | 货币(亿元)
m0 | - | Y | 流通中现金(亿元)
cd | - | Y | 活期存款(亿元)
qm | - | Y | 准货币(亿元)
ftd | - | Y | 定期存款(亿元)
sd | - | Y | 储蓄存款(亿元)
rests | - | Y | 其他存款(亿元)

接口示例

```
import gopup as gp
df_index = gp.get_money_supply_bal()
print(df_index)
```

```
    year          m2         m1  ...        ftd         sd      rests
0   2018  1826744.20  551685.90  ...  340178.90  721688.60  213190.80
1   2017  1690235.30  543790.10  ...  320196.20  649341.50  176907.40
2   2016  1550066.70  486557.20  ...  307989.60  603504.20  152015.60
3   2015  1392278.10  400953.40  ...  288240.70  552073.50  151010.50
4   2014  1228374.80  348056.40  ...  264055.70  508878.10  107384.60
5   2013  1106525.00  337291.10  ...  232696.60  467031.10   69506.20
```

#### 外汇储备

接口: get_gold_and_foreign_reserves

目标地址: http://money.finance.sina.com.cn/mac/api/jsonp.php ……

描述: 获取外汇储备

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
month | - | Y | 统计时间
gold | - | Y | 黄金储备(万盎司)
foreign_reserves | - | Y | 外汇储备(亿美元)

接口示例

```
import gopup as gp
df_index = gp.get_gold_and_foreign_reserves()
print(df_index)
```

```
       month     gold foreign_reserves
0     2020.2  6264.00         31067.18
1     2020.1  6264.00         31154.97
2    2019.12  6264.00         31079.24
3    2019.11  6264.00         30955.91
4    2019.10  6264.00         31051.61
```

### 利率数据

#### Shibor数据
接口: shibor_data

目标地址: http://www.shibor.org

描述: 获取上海银行间同业拆放利率（Shibor）

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
year | int | N | 年份 默认：今年

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| date | datetime | Y | 日期-索引 |
| ON | float | Y | 隔夜拆放利率 |
| 1W | float | Y | 1周拆放利率 |
| 2W | float | Y | 2周拆放利率 |
| 1M | float | Y | 1个月拆放利率 |
| 3M | float | Y | 3个月拆放利率 |
| 6M | float | Y | 6个月拆放利率 |
| 9M | float | Y | 9个月拆放利率 |
| 1Y | float | Y | 1年拆放利率 |

接口示例

```
import gopup as gp
df_index = gp.shibor_data(year="2020")
print(df_index)
```

#### Shibor报价数据
接口: shibor_quote_data

目标地址: http://www.shibor.org

描述: 获取获取Shibor银行报价数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
year | int | N | 年份 默认：今年

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| date | datetime | Y | 日期-索引 |
| bank | str | Y | 报价银行名称 |
| ON | str | Y | 隔夜 |
| 1W_B | float | Y | 1周 |
| 2W_B | float | Y | 2周 |
| 1M_B | float | Y | 1个月 |
| 3M_B | float | Y | 3个月 |
| 6M_B| float | Y | 6个月 |
| 9M_B | float | Y | 9个月 |
| 1Y | float | Y | 1年 |

接口示例

```
import gopup as gp
df_index = gp.shibor_quote_data(year="2020")
print(df_index)
```


#### Shibor均值数据
接口: shibor_ma_data

目标地址: http://www.shibor.org

描述: 获取获取Shibor均值数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
year | int | N | 年份 默认：今年

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| date | datetime | Y | 日期-索引 |
| _5 _10 _20 | str | Y | 各周期5、10、20均价 |

接口示例

```
import gopup as gp
df_index = gp.shibor_ma_data(year="2020")
print(df_index)
```

#### 贷款市场报价利率（LPR）
接口: lpr_data

目标地址: http://www.shibor.org

描述: 获取贷款市场报价利率（LPR）

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
startDate | int | Y | 起止日期
endDate | int | Y | 截止日期

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| showDateCN | datetime | Y | 日期 |
| 1Y | float | Y | 1年贷款基础利率 |
| 5Y | float | Y | 5年贷款基础利率 |

接口示例

```
import gopup as gp
df_index = gp.lpr_data(startDate="2020-09-01", endDate="2020-09-30")
print(df_index)
```

