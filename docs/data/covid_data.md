## 疫情数据

### 网易疫情数据

接口: covid_163

目标地址: https://news.163.com/special/epidemic/

描述: 获取网易-新型冠状病毒肺炎-疫情数据

限量: 单次返回指定 indicator 的数据

输入参数 indicator

- 数据说明
- 中国实时数据
- 中国历史时点数据
- 中国历史累计数据
- 世界历史时点数据
- 世界历史累计数据
- 全球所有国家及地区时点数据
- 全球所有国家及地区累计数据
- 中国各地区时点数据
- 中国各地区累计数据
- 疫情学术进展
- 实时资讯新闻播报
- 实时医院新闻播报
- 前沿知识
- 权威发布
- 滚动新闻

#### 数据说明

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="数据说明"; 返回网易对相关字段的数据说明

输出参数-数据说明

名称|类型|默认显示|描述
---|:---:|:---:|---
info|-|-|数据说明


接口示例-数据说明

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="数据说明")
print(covid_163_df)
```

数据示例-数据说明

```
                                                   info
0             数据来源：国家卫健委、各省市区卫健委、各省市区政府、港澳台官方渠道公开数据。
1   数据更新时间：实时更新全国、各省市区数据，因核实计算需要，与官方的发布时间相比，将有一定时...
2   实时数据统计原则：① 每日上午优先将全国各类数据与国家卫健委公布数据对齐（此时各省市区数据...
3           疫情趋势图：全国数据使用国家卫健委公布的截至前一日24:00数据，每日更新一次。
4    网易新闻全力以赴提供权威、准确、及时的疫情数据，如有任何疑问，欢迎通过网易新闻客户端留言反馈。
```

#### 中国实时数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国实时数据"; 返回中国实时疫情统计数据

输出参数-中国实时数据

名称|类型|默认|描述
---|:---:|:---:|---
-|-|-|参见: 数据示例-中国实时数据


接口示例-中国实时数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="中国实时数据")
print(covid_163_df)
```

数据示例-中国实时数据

```
                  today    total extData
confirm            41.0  81062.0     NaN
suspect            39.0    113.0     NaN
heal             1390.0  67039.0     NaN
dead               10.0   3204.0     NaN
severe           -384.0   3226.0     NaN
                 ...      ...     ...
suspectNote         NaN      NaN        
healNote            NaN      NaN        
deadNote            NaN      NaN        
incrConfirmNote     NaN      NaN        
incrSevereNote      NaN      NaN        
```

#### 中国历史时点数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国历史时点数据", 返回中国历史每日新增数据

输出参数-中国历史时点数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国历史时点数据


接口示例-中国历史时点数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="中国历史时点数据")
print(covid_163_df)
```

数据示例-中国历史时点数据

```
            confirm  suspect  heal  dead  severe storeConfirm
2020-01-20      291       27    25     6       0         None
2020-01-21      149       26     0     3       0         None
2020-01-22      131      257     3     8       0         None
2020-01-23      259      680     6     8       0         None
2020-01-24      457     1118     4    16       0         None
             ...      ...   ...   ...     ...          ...
2020-03-10       24       31  1578    22       0         None
2020-03-11       15       33  1318    11       0         None
2020-03-12       20       33  1318     7       0         None
2020-03-13       11       17  1430    13       0         None
2020-03-14       20       39  1370    10       0         None
```

#### 中国历史累计数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国历史累计数据", 返回中国历史每日累计数据

输出参数-中国历史累计数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国历史累计数据


接口示例-中国历史累计数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="中国历史累计数据")
print(covid_163_df)
```

数据示例-中国历史累计数据

```
            confirm  suspect   heal  dead  severe
2020-01-20      291       54     25     6       0
2020-01-21      440       37     25     9     102
2020-01-22      571      393     28    17      95
2020-01-23      830     1072     34    25     177
2020-01-24     1287     1965     38    41     237
             ...      ...    ...   ...     ...
2020-03-10    80778      285  61475  3158    4492
2020-03-11    80793      253  62793  3169    4257
2020-03-12    80813      147  64111  3176    4020
2020-03-13    80824      115  65541  3189    3610
2020-03-14    80844      113  66911  3199    3226
```

#### 世界历史时点数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="世界历史时点数据", 返回世界历史每日新增数据

输出参数-世界历史时点数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-世界历史时点数据


接口示例-世界历史时点数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="世界历史时点数据")
print(covid_163_df)
```

数据示例-世界历史时点数据

```
        confirm  suspect    heal  dead  severe storeConfirm
中国         41.0     39.0  1393.0  10.0  -384.0         None
日本        107.0      NaN    14.0   5.0     NaN         None
泰国         44.0      0.0     0.0   0.0     0.0         None
新加坡        26.0      0.0     8.0   0.0     0.0         None
韩国         76.0      NaN   120.0   3.0     NaN         None
         ...      ...     ...   ...     ...          ...
苏里南         NaN      0.0     NaN   NaN     0.0         None
刚果（布）       1.0      0.0     0.0   0.0     0.0         None
乌兹别克斯坦      1.0      0.0     0.0   0.0     0.0         None
刚果（金）       0.0      NaN     0.0   0.0     NaN         None
中非共和国       1.0      0.0     0.0   0.0     0.0         None
```

#### 世界历史累计数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="世界历史累计数据", 返回世界历史每日累计数据

输出参数-世界历史累计数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-世界历史累计数据


接口示例-世界历史累计数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="世界历史累计数据")
print(covid_163_df)
```

数据示例-世界历史累计数据

```
        confirm  suspect   heal  dead  severe
中国        81062      113  67042  3204    3226
日本         1515        0    525    31       0
泰国          114        0     35     1       0
新加坡         226        0    105     0       0
韩国         8162        0    834    75       0
         ...      ...    ...   ...     ...
苏里南           1        0      0     0       0
刚果（布）         1        0      0     0       0
乌兹别克斯坦        1        0      0     0       0
刚果（金）         2        0      0     0       0
中非共和国         1        0      0     0       0
```

#### 全球所有国家及地区时点数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球所有国家及地区时点数据", 返回全球所有国家及地区时点数据

输出参数-全球所有国家及地区时点数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球所有国家及地区时点数据


接口示例-全球所有国家及地区时点数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="全球所有国家及地区时点数据")
print(covid_163_df)
```

数据示例-全球所有国家及地区时点数据

```
        confirm  suspect    heal  dead  severe storeConfirm
中国         41.0     39.0  1393.0  10.0  -384.0         None
湖北          4.0      NaN  1346.0  10.0     NaN         None
武汉          4.0      0.0  1192.0  10.0     0.0         None
孝感          0.0      NaN    16.0   0.0     NaN         None
黄冈          0.0      NaN     8.0   0.0     NaN         None
         ...      ...     ...   ...     ...          ...
苏里南         NaN      0.0     NaN   NaN     0.0         None
刚果（布）       1.0      0.0     0.0   0.0     0.0         None
乌兹别克斯坦      1.0      0.0     0.0   0.0     0.0         None
刚果（金）       0.0      NaN     0.0   0.0     NaN         None
中非共和国       1.0      0.0     0.0   0.0     0.0         None
```

#### 全球所有国家及地区累计数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球所有国家及地区累计数据", 返回全球所有国家及地区累计数据

输出参数-全球所有国家及地区累计数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球所有国家及地区累计数据


接口示例-全球所有国家及地区累计数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="全球所有国家及地区累计数据")
print(covid_163_df)
```

数据示例-全球所有国家及地区累计数据

```
        confirm  suspect   heal  dead  severe
中国        81062      113  67042  3204    3226
湖北        67794        0  54289  3085       0
武汉        49999        0  37643  2456       0
孝感         3518        0   3253   126       0
黄冈         2907        0   2738   125       0
         ...      ...    ...   ...     ...
苏里南           1        0      0     0       0
刚果（布）         1        0      0     0       0
乌兹别克斯坦        1        0      0     0       0
刚果（金）         2        0      0     0       0
中非共和国         1        0      0     0       0
```

#### 中国各地区时点数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国各地区时点数据", 返回中国各地区时点数据

输出参数-中国各地区时点数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国各地区时点数据


接口示例-中国各地区时点数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="中国各地区时点数据")
print(covid_163_df)
```

数据示例-中国各地区时点数据

```
     confirm  suspect  heal  dead  severe storeConfirm
湖北         4      NaN  1346    10     NaN         None
广东         4      NaN     5     0     NaN         None
河南         0      NaN     1     0     NaN         None
浙江         4      NaN     0     0     NaN         None
湖南         0      0.0     5     0     0.0         None
..       ...      ...   ...   ...     ...          ...
内蒙古        0      NaN     0     0     NaN         None
台湾         9      0.0     0     0     0.0         None
青海         0      NaN     0     0     NaN         None
澳门         0      NaN     0     0     NaN         None
西藏         0      NaN     0     0     NaN         None
```

#### 中国各地区累计数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国各地区累计数据", 返回中国各地区累计数据

输出参数-中国各地区累计数据

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国各地区累计数据


接口示例-中国各地区累计数据

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="中国各地区累计数据")
print(covid_163_df)
```

数据示例-中国各地区累计数据

```
     confirm  suspect   heal  dead  severe
湖北     67794        0  54289  3085       0
广东      1360        0   1304     8       0
河南      1273        0   1250    22       0
浙江      1231        0   1211     1       0
湖南      1018        0   1014     4       0
..       ...      ...    ...   ...     ...
内蒙古       75        0     71     1       0
台湾        59        0     20     1       0
青海        18        0     18     0       0
澳门        10        0     10     0       0
西藏         1        0      1     0       0
```

#### 疫情学术进展

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="疫情学术进展", 返回疫情学术进展数据

输出参数-疫情学术进展

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-疫情学术进展


接口示例-疫情学术进展

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="疫情学术进展")
print(covid_163_df)
```

数据示例-疫情学术进展

```
                                                url3g  ...            stitle
0   http://3g.163.com/news/20/0313/01/F7IG6B4I0001...  ...               NaN
1   http://3g.163.com/news/20/0306/11/F71IP6280001...  ...  F71IP62800019NGP
2   http://3g.163.com/news/20/0303/11/F6PQGDCD0001...  ...  F6PQGDCD00019NGP
3   http://3g.163.com/news/20/0210/14/F51HPI890001...  ...  F51HPI8900019NGP
4   http://3g.163.com/news/20/0228/23/F6GRTAMN0001...  ...  F6GRTAMN00019NGP
..                                                ...  ...               ...
29  http://3g.163.com/news/20/0202/15/F4D23HC60001...  ...  F4D23HC600019NGP
30  http://3g.163.com/news/20/0202/14/F4CSKV890001...  ...  F4CSKV8900019NGP
31  http://3g.163.com/news/20/0202/17/F4D8C03S0001...  ...  F4D8C03S00019NGP
32  http://3g.163.com/news/20/0202/05/F4BUU2240001...  ...  F4BUU22400019NGP
33  http://3g.163.com/news/20/0202/05/F4BTHEQU0001...  ...  F4BTHEQU00019NGP
```

#### 实时资讯新闻播报

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="实时资讯新闻播报", 返回实时资讯新闻播报数据

输出参数-实时资讯新闻播报

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-实时资讯新闻播报


接口示例-实时资讯新闻播报

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="实时资讯新闻播报")
print(covid_163_df)
```

数据示例-实时资讯新闻播报
```
                         title  ...                                               link
0    新加坡新增新冠肺炎确诊病例14例 累计确诊226例  ...  https://news.163.com/20/0315/22/F7PT9IH100019B...
1        苏格兰新冠肺炎病毒检测呈阳性病例达153例  ...  https://news.163.com/20/0315/22/F7PT5PST00019B...
2         外媒：全球新冠肺炎死亡病例已超6000例  ...  https://news.163.com/20/0315/21/F7PRSOSN00019B...
3     法国数百“黄背心“无视禁令上街了 有人戴防护面罩  ...  https://news.163.com/20/0315/21/F7PRDBLK00019B...
4   荷兰已确诊新冠肺炎病例1135例 累计死亡20例    ...  https://news.163.com/20/0315/21/F7PQA54O000189...
..                         ...  ...                                                ...
45     英媒：因担心感染新冠病毒 英国女王离开白金汉宫  ...  https://news.163.com/20/0315/10/F7OJIAP200019B...
46    北京境外输入病例累计已达27例 首超外地来京病例  ...  https://news.163.com/20/0315/10/F7OJ5BR8000187...
47     英国医生：病毒太可怕 而我们没有中国那样的能力  ...  https://news.163.com/20/0315/09/F7OIQGNN000187...
48      古特雷斯第三次就疫情发表讲话：向新冠病毒宣战  ...  https://news.163.com/20/0315/09/F7OIC6S5000189...
49  7天确诊破5000 新冠如何在一周之内“闪袭“西班牙  ...  https://news.163.com/20/0315/09/F7OHPQQS000189...
```

#### 实时医院新闻播报

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="实时医院新闻播报", 返回实时医院新闻播报数据

输出参数-实时医院新闻播报

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-实时医院新闻播报


接口示例-实时医院新闻播报

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="实时医院新闻播报")
print(covid_163_df)
```

数据示例-实时医院新闻播报
```
                                           title  ...                                               link
0   宁夏回族自治区新型冠状病毒感染的肺炎医疗救治第一批定点医疗机构和设置发热门诊医疗机构名单  ...  https://news.163.com/20/0301/23/F6M1I3NF000189...
1                         湖南省新型冠状病毒感染的肺炎定点救治医院名单  ...  https://news.163.com/20/0301/23/F6M0VAAC000189...
2                      调整优化医院发热门诊 北京市76所医院保留发热门诊  ...  https://news.163.com/20/0301/22/F6LR1D52000189...
3                                四川省新冠肺炎救治定点医院名单  ...  http://sc.news.163.com/20/0228/08/F6F6M5QR0426...
4                        湖北公布新型肺炎医疗救治和发热门诊医疗机构名单  ...  https://news.163.com/20/0123/15/F3J7P4V600018A...
..                                           ...  ...                                                ...
25              黑龙江省卫健委公布130家新型肺炎定点医疗机构及513家发热门诊  ...  http://dy.163.com/v2/article/detail/F3HVO99705...
26                 吉林省设置发热门诊和新型冠状病毒感染的肺炎定点救治医疗机构  ...  http://dy.163.com/v2/article/detail/F3GK8OPS05...
27                  青海公布9家医院为新型冠状病毒感染的肺炎医疗救治定点医院  ...  http://dy.163.com/v2/article/detail/F3JLHHGO05...
28                       新疆公布新型冠状病毒感染的肺炎定点救治医院名单  ...  http://dy.163.com/v2/article/detail/F3JJU24T05...
29                          西藏公布新型冠状病毒感染救治定点医院名单  ...  http://dy.163.com/v2/article/detail/F3KTN6MQ05...
```

#### 前沿知识

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="前沿知识", 返回前沿知识数据

输出参数-前沿知识

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-前沿知识

接口示例-前沿知识

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="前沿知识")
print(covid_163_df)
```

数据示例-前沿知识
```
                           title  ...                                               link
0      钟南山:国内新冠疫情4月见顶，总感染规模约9.5万  ...  https://vip.open.163.com/mobile/activity/ncov/...
1   张文宏:上海已止住病例的指数增长，传播力比预期降低99%  ...  https://vip.open.163.com/mobile/activity/ncov/...
2         管轶:检测表明穿山甲可能是新冠病毒的中间宿主  ...  https://vip.open.163.com/mobile/activity/ncov/...
3  新冠病毒正式命名为SARS-Cov-2，是SARS姊妹病毒  ...  https://vip.open.163.com/mobile/activity/ncov/...
```

#### 权威发布

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="权威发布", 返回权威发布数据

输出参数-权威发布

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-权威发布

接口示例-权威发布

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="权威发布")
print(covid_163_df)
```

数据示例-权威发布
```
   title  ...                                               link
0    张文宏  ...  https://news.163.com/20/0315/17/F7PDEGB200018A...
1    张文宏  ...  https://news.163.com/20/0313/07/F7J5800Q000189...
2    钟南山  ...  https://news.163.com/20/0311/22/F7FM1PUI00018A...
3    李兰娟  ...  https://news.163.com/20/0310/18/F7CK07CV000189...
4    钟南山  ...  https://news.163.com/20/0309/14/F79KN0T4000189...
..   ...  ...                                                ...
26   钟南山  ...  https://news.163.com/20/0212/00/F554CHN4000189...
27   张文宏  ...  https://news.163.com/20/0206/16/F4NFU78S000189...
28   钟南山  ...  https://news.163.com/20/0131/17/F481L8JM000189...
29   李兰娟  ...  https://news.163.com/20/0123/16/F3JCMD5B00018A...
30   钟南山  ...           http://v.163.com/static/3/VK2EF0114.html
```

#### 滚动新闻

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="滚动新闻", 返回滚动新闻数据

输出参数-滚动新闻

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-滚动新闻

接口示例-滚动新闻

```
import gopup as gp
covid_163_df = gp.covid_163(indicator="滚动新闻")
print(covid_163_df)
```

数据示例-权威发布

```
                   title  ...                                               link
0        以色列总理接受新冠肺炎病毒检测  ...  https://news.163.com/20/0315/22/F7PSDT5C00019B...
1  16日起所有入境进京人员均需集中观察14天  ...  https://news.163.com/20/0315/16/F7P8HV3700019B...
2          意大利一市长患新冠肺炎病逝  ...  https://news.163.com/20/0315/15/F7P5SGAI00019B...
3    全球至少51名官员确诊 伊朗确诊28例  ...  https://news.163.com/20/0315/13/F7OVOG18000187...
4    襄阳：机关事业单位明日全面恢复正常上班  ...  https://news.163.com/20/0315/12/F7OQOBS7000189...
```

### 丁香园疫情数据

接口: covid_dxy

目标地址: http://3g.dxy.cn/newh5/view/pneumonia?scene=2&clicktime=1579615030&enterid=1579615030&from=groupmessage&isappinstalled=0

描述: 获取丁香园-新型冠状病毒肺炎-疫情数据-总入口

限量: 单次返回实时数据

输入参数 indicator

- 中国疫情分省统计详情
- 中国疫情分市统计详情
- 全球疫情分国家统计详情
- 中国疫情实时统计
- 国外疫情实时统计
- 全球疫情实时统计
- 中国疫情防控医院
- 实时播报
- 中国-新增疑似-新增确诊-趋势图
- 中国-现存确诊-趋势图
- 中国-现存疑似-趋势图
- 中国-治愈-趋势图
- 中国-死亡-趋势图
- 中国-非湖北新增确诊-趋势图
- 中国-湖北新增确诊-趋势图
- 中国-湖北现存确诊-趋势图
- 中国-非湖北现存确诊-趋势图
- 中国-治愈-死亡-趋势图
- 国外-国外新增确诊-趋势图
- 国外-国外累计确诊-趋势图
- 国外-国外死亡-趋势图
- 国外-重点国家新增确诊-趋势图
- 国外-日本新增确诊-趋势图
- 国外-意大利新增确诊-趋势图
- 国外-伊朗新增确诊-趋势图
- 国外-美国新增确诊-趋势图
- 国外-法国新增确诊-趋势图
- 国外-德国新增确诊-趋势图
- 国外-西班牙新增确诊-趋势图
- 国外-韩国新增确诊-趋势图

#### 中国疫情分省统计详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国疫情分省统计详情"

输出参数-中国疫情分省统计详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国疫情分省统计详情

接口示例-中国疫情分省统计详情

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="中国疫情分省统计详情")
print(covid_dxy_df)
```

数据示例-中国疫情分省统计详情
```
          地区 地区简称  现存确诊   累计确诊     治愈    死亡
0        湖北省   湖北  9604  67798  55095  3099
1        北京市   北京    84    452    360     8
2         香港   香港    67    155     84     4
3        广东省   广东    47   1361   1306     8
4         台湾   台湾    46     67     20     1
..       ...  ...   ...    ...    ...   ...
29       吉林省   吉林     0     93     92     1
30  新疆维吾尔自治区   新疆     0     76     73     3
31   宁夏回族自治区   宁夏     0     75     75     0
32       青海省   青海     0     18     18     0
33     西藏自治区   西藏     0      1      1     0
```

#### 中国疫情分市统计详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国疫情分市统计详情"
输出参数-中国疫情分市统计详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国疫情分市统计详情

接口示例-中国疫情分市统计详情

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="中国疫情分市统计详情")
print(covid_dxy_df)
```

数据示例-中国疫情分市统计详情
```
    cityName  currentConfirmedCount  ...  locationId  province
0         武汉                 9149.0  ...    420100.0       湖北省
1         孝感                  125.0  ...    420900.0       湖北省
2         鄂州                   62.0  ...    420700.0       湖北省
3         随州                   41.0  ...    421300.0       湖北省
4         荆州                   38.0  ...    421000.0       湖北省
..       ...                    ...  ...         ...       ...
423       宁东                    0.0  ...         0.0   宁夏回族自治区
424      石嘴山                    0.0  ...    640200.0   宁夏回族自治区
425       西宁                    0.0  ...    630100.0       青海省
426      海北州                    0.0  ...    632200.0       青海省
427       拉萨                    0.0  ...    540100.0     西藏自治区
```

#### 全球疫情分国家统计详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球疫情分国家统计详情"
输出参数-全球疫情分国家统计详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球疫情分国家统计详情

接口示例-全球疫情分国家统计详情

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="全球疫情分国家统计详情")
print(covid_dxy_df)
```

数据示例-全球疫情分国家统计详情
```
            id  ...                                     statisticsData
0    1130342.0  ...  https://file1.dxycdn.com/2020/0315/993/3402160...
1          NaN  ...  https://file1.dxycdn.com/2020/0315/383/3402160...
2    1130372.0  ...  https://file1.dxycdn.com/2020/0315/596/3402160...
3    1130344.0  ...  https://file1.dxycdn.com/2020/0315/812/3402160...
4    1130329.0  ...  https://file1.dxycdn.com/2020/0315/779/3402160...
..         ...  ...                                                ...
146  1130918.0  ...                                                NaN
147  1130920.0  ...                                                NaN
148  1130922.0  ...                                                NaN
149  1130332.0  ...  https://file1.dxycdn.com/2020/0315/813/3402160...
150  1130881.0  ...  https://file1.dxycdn.com/2020/0315/234/3402176...
```

#### 中国疫情实时统计

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国疫情实时统计"
输出参数-中国疫情实时统计

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国疫情实时统计

接口示例-中国疫情实时统计

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="中国疫情实时统计")
print(covid_dxy_df)
```

数据示例-中国疫情实时统计
```
                        info
数据发布时间   2020-03-16 19:30:19
现存确诊                   10002
累计确诊                   81099
境外输入                     123
累计治愈                   67879
                      ...
现存确诊较昨日                 -820
累计确诊较昨日                   51
累计治愈较昨日                  857
累计死亡较昨日                   14
现存重症较昨日                 -194
```

#### 国外疫情实时统计

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="国外疫情实时统计"
输出参数-国外疫情实时统计

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-国外疫情实时统计

接口示例-国外疫情实时统计

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="国外疫情实时统计")
print(covid_dxy_df)
```

数据示例-国外疫情实时统计

```
                           0
currentConfirmedCount  76189
confirmedCount         89793
suspectedCount             0
curedCount             10181
deadCount               3423
suspectedIncr              0
currentConfirmedIncr    9347
confirmedIncr          11091
curedIncr               1162
deadIncr                 582
```

#### 全球疫情实时统计

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球疫情实时统计"
输出参数-全球疫情实时统计

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球疫情实时统计

接口示例-全球疫情实时统计

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="全球疫情实时统计")
print(covid_dxy_df)
```

数据示例-全球疫情实时统计

```
                            0
currentConfirmedCount   86191
confirmedCount         170892
curedCount              78060
deadCount                6641
currentConfirmedIncr     8527
confirmedIncr           11142
curedIncr                2019
deadIncr                  596
```

#### 中国疫情防控医院

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国疫情防控医院"
输出参数-中国疫情防控医院

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国疫情防控医院

接口示例-中国疫情防控医院

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="中国疫情防控医院")
print(covid_dxy_df)
```

数据示例-中国疫情防控医院

```
   省级行政区   市级      机构／医院
0    湖北省  NaN        NaN
1    湖北省   武汉  定点医院/发热门诊
2    湖北省   荆门  定点医院/发热门诊
3    湖北省   宜昌  定点医院/发热门诊
4    湖北省   恩施       定点医院
..   ...  ...        ...
81    宁夏    /  定点医院/发热门诊
82    西藏    /  定点医院/发热门诊
83    新疆    /       定点医院
84    青海    /       定点医院
85    甘肃    /       定点医院
```

#### 实时播报

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="实时播报"
输出参数-实时播报

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-实时播报

接口示例-实时播报

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="实时播报")
print(covid_dxy_df)
```

数据示例-实时播报

```
                           title  ...                                          sourceUrl
0     伊朗新增1053例新冠肺炎，累计确诊升至14991例  ...      http://m.weibo.cn/2803301701/4483175407422772
1                   零死亡！宁夏确诊病例清零  ...      http://m.weibo.cn/2803301701/4483140900884657
2   北京3月16日0时至14时新增报告境外输入确诊病例6例   ...  http://wjw.beijing.gov.cn/xwzx_20031/xwfb/2020...
3                       捷克宣布全国隔离  ...      http://m.weibo.cn/2656274875/4483064778472648
4               好消息！贵州所有确诊病例全部治愈  ...      http://m.weibo.cn/2656274875/4483062924149409
```

#### 省份数据

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="湖北省"; 任意省份
输出参数-湖北省

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-湖北省

接口示例-湖北省

```
import gopup as gp
covid_dxy_df = gp.covid_dxy(indicator="湖北省")
print(covid_dxy_df)
```

数据示例-浙江省

```
        区域  现在确诊人数  确诊人数  疑似人数  治愈人数  死亡人数
0       丽水      10    28     0    18     0
1       湖州       2    12     0    10     0
2       杭州       1   182     0   181     0
3       嘉兴       1    45     0    44     0
4       温州       0   504     0   503     1
..     ...     ...   ...   ...   ...   ...
7       金华       0    55     0    55     0
8       绍兴       0    42     0    42     0
9   省十里丰监狱       0    36     0    36     0
10      衢州       0    14     0    14     0
11      舟山       0    10     0    10     0
```

#### 疫情趋势图

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国-新增疑似-新增确诊-趋势图"
输出参数-中国-新增疑似-新增确诊-趋势图

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|在本地输出图片

接口示例-中国-新增疑似-新增确诊-趋势图

```
import gopup as gp
gp.covid_dxy(indicator="中国-新增疑似-新增确诊-趋势图")
```


### 百度疫情数据

接口: covid_baidu

目标地址: https://voice.baidu.com/act/newpneumonia/newpneumonia/?from=osari_pc_1

描述: 获取百度-新型冠状病毒肺炎-疫情实时大数据报告

限量: 单次返回所有数据


#### 热门迁入地

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="热门迁入地", 返回全国迁徙城市热门

输出参数-热门迁入地

名称|类型|默认显示|描述
---|:---:|:---:|---
city_name|str|Y|城市名称
province_name|str|Y|省份
value|str|Y|迁入比例 = 该城市迁入人数 / 全国迁入总人数, https://qianxi.baidu.com/?from=shoubai#city=0
city_code|str|Y|各区县行政区划代码

接口示例-热门迁入地

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="热门迁入地")
print(covid_baidu_df)
```

数据示例-热门迁入地

```
   city_name province_name  value city_code
0        成都市           四川省   3.85    510100
1        北京市           北京市   3.32    110000
2        深圳市           广东省   3.09    440300
3        上海市           上海市   2.78    310000
4        广州市           广东省   2.72    440100
5        东莞市           广东省   2.17    441900
6        苏州市           江苏省   1.65    320500
7        重庆市           重庆市   1.65    500000
8        长沙市           湖南省   1.60    430100
9        昆明市           云南省   1.48    530100
10       沈阳市           辽宁省   1.41    210100
11       西安市           陕西省   1.40    610100
12       佛山市           广东省   1.33    440600
13       贵阳市           贵州省   1.32    520100
14       杭州市           浙江省   1.23    330100
15       郑州市           河南省   1.22    410100
16       南宁市       广西壮族自治区   1.22    450100
17       南京市           江苏省   1.20    320100
18       天津市           天津市   1.18    120000
19       合肥市           安徽省   1.09    340100
20       长春市           吉林省   1.07    220100
21      哈尔滨市          黑龙江省   0.98    230100
22       惠州市           广东省   0.97    441300
23       厦门市           福建省   0.96    350200
24       济南市           山东省   0.95    370100
25       青岛市           山东省   0.84    370200
26       中山市           广东省   0.83    442000
27       无锡市           江苏省   0.79    320200
28       太原市           山西省   0.75    140100
29       大连市           辽宁省   0.73    210200
```

#### 热门迁出地

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="热门迁出地", 返回全国迁徙城市热门

输出参数-热门迁出地

名称|类型|默认显示|描述
---|:---:|:---:|---
city_name|str|Y|城市名称
province_name|str|Y|省份
value|str|Y|迁入比例
city_code|str|Y|各区县行政区划代码


接口示例-热门迁出地

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="热门迁出地")
print(covid_baidu_df)
```

数据示例-热门迁入地

```
   city_name province_name  value city_code
0        重庆市           重庆市   1.68    500000
1        成都市           四川省   1.27    510100
2        南充市           四川省   1.07    511300
3        广州市           广东省   0.98    440100
4        邵阳市           湖南省   0.88    430500
5        北京市           北京市   0.87    110000
6        盐城市           江苏省   0.87    320900
7        深圳市           广东省   0.82    440300
8        毕节市           贵州省   0.82    520500
9        达州市           四川省   0.81    511700
10       衡阳市           湖南省   0.73    430400
11       梅州市           广东省   0.72    441400
12       茂名市           广东省   0.72    440900
13       阜阳市           安徽省   0.71    341200
14       周口市           河南省   0.69    411600
15       长沙市           湖南省   0.66    430100
16       西安市           陕西省   0.66    610100
17       上海市           上海市   0.66    310000
18       曲靖市           云南省   0.66    530300
19       南宁市       广西壮族自治区   0.65    450100
20       湛江市           广东省   0.64    440800
21       玉林市       广西壮族自治区   0.61    450900
22       合肥市           安徽省   0.61    340100
23       资阳市           四川省   0.61    512000
24       揭阳市           广东省   0.61    445200
25       广安市           四川省   0.59    511600
26       内江市           四川省   0.59    511000
27       永州市           湖南省   0.59    431100
28       遵义市           贵州省   0.58    520300
29       绵阳市           四川省   0.58    510700
```

#### 今日疫情热搜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="今日疫情热搜"

输出参数-今日疫情热搜

名称|类型|默认显示|描述
---|:---:|:---:|---
degree|str|Y|搜索量
query|str|Y|搜索内容
type|str|Y|类型
url|str|Y|网址

接口示例-今日疫情热搜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="今日疫情热搜")
print(covid_baidu_df)
```

数据示例-今日疫情热搜

```
     degree            query type  \
0  25779382         新型肺炎实时动态    2   
1   2626725          疫情拐点将出现    1   
2   1935775   疫情被列国际突发公共卫生事件    2   
3   1337020    湖北企业复工不早于2.13    2   
4   1009220   病毒在毛质衣物上存活时间更短    0   
5    905491            火神山直播    0   
6    893315      包机接海外湖北公民回家    3   
7    779037  省委书记检查防疫被村口大爷拦住    3   
                                                 url  
0  https://m.baidu.com/s?word=%E6%96%B0%E5%9E%8B%...  
1  https://m.baidu.com/s?word=%E7%96%AB%E6%83%85%...  
2  https://m.baidu.com/s?word=%E7%96%AB%E6%83%85%...  
3  https://m.baidu.com/s?word=%E6%B9%96%E5%8C%97%...  
4  https://m.baidu.com/s?word=%E7%97%85%E6%AF%92%...  
5  https://m.baidu.com/s?word=%E7%81%AB%E7%A5%9E%...  
6  https://m.baidu.com/s?word=%E5%8C%85%E6%9C%BA%...  
7  https://m.baidu.com/s?word=%E7%9C%81%E5%A7%94%...         
```

#### 防疫知识热搜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="防疫知识热搜", 返回防疫知识热搜数据

输出参数-防疫知识热搜

名称|类型|默认显示|描述
---|:---:|:---:|---
degree|str|Y|搜索量
query|str|Y|搜索内容
type|str|Y|类型
url|str|Y|网址

接口示例-防疫知识热搜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="防疫知识热搜")
print(covid_baidu_df)
```

数据示例-防疫知识热搜

```
    degree        query type  \
0  1802150     新型肺炎自查手册    0   
1   781468    新型冠状病毒的特征    0   
2   914125   n95口罩多久换一次    0   
3   801365    人的正常体温是多少    0   
4   599625  84消毒液对人体有害吗    3   
5   498645     钟南山示范摘口罩    3   
6   409385   戴口罩眼镜不起雾技巧    0   
7   109359    收快递会感染病毒吗    0   
                                                 url  
0  https://m.baidu.com/s?word=%E6%96%B0%E5%9E%8B%...  
1  https://m.baidu.com/s?word=%E6%96%B0%E5%9E%8B%...  
2  https://m.baidu.com/s?word=n95%E5%8F%A3%E7%BD%...  
3  https://m.baidu.com/s?word=%E4%BA%BA%E7%9A%84%...  
4  https://m.baidu.com/s?word=84%E6%B6%88%E6%AF%9...  
5  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...  
6  https://m.baidu.com/s?word=%E6%88%B4%E5%8F%A3%...  
7  https://m.baidu.com/s?word=%E6%94%B6%E5%BF%AB%...  
```

#### 热搜谣言粉碎

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="热搜谣言粉碎", 返回热搜谣言粉碎数据

输出参数-热搜谣言粉碎

名称|类型|默认显示|描述
---|:---:|:---:|---
degree|str|Y|搜索量
query|str|Y|搜索内容
type|str|Y|类型
url|str|Y|网址

接口示例-热搜谣言粉碎

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="热搜谣言粉碎")
print(covid_baidu_df)
```

数据示例-热搜谣言粉碎

```
   degree         query type  \
0  219570    洗热水澡预防新型肺炎    7   
1   85560     纸币会传播冠状病毒    7   
2   68568     全身喷洒酒精可消毒    7   
3   39528   武汉红十字会收取服务费    7   
4   37296     风油精涂人中防流感    7   
5    7224    超市买的东西必须消毒    7   
6    4032      香油滴鼻孔防传染    7   
7    6696  世卫组织认定中国为疫区国    7   
                                                 url  
0  https://m.baidu.com/s?word=%E6%B4%97%E7%83%AD%...  
1  https://m.baidu.com/s?word=%E7%BA%B8%E5%B8%81%...  
2  https://m.baidu.com/s?word=%E5%85%A8%E8%BA%AB%...  
3  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...  
4  https://m.baidu.com/s?word=%E9%A3%8E%E6%B2%B9%...  
5  https://m.baidu.com/s?word=%E8%B6%85%E5%B8%82%...  
6  https://m.baidu.com/s?word=%E9%A6%99%E6%B2%B9%...  
7  https://m.baidu.com/s?word=%E4%B8%96%E5%8D%AB%...  
```

#### 复工复课热搜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="复工复课热搜"

输出参数-复工复课热搜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-复工复课热搜

接口示例-复工复课热搜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="复工复课热搜")
print(covid_baidu_df)
```

数据示例-复工复课热搜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 热门人物榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="热门人物榜"

输出参数-热门人物榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-热门人物榜

接口示例-热门人物榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="热门人物榜")
print(covid_baidu_df)
```

数据示例-热门人物榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 历史疫情热搜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="历史疫情热搜"

输出参数-历史疫情热搜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-历史疫情热搜

接口示例-历史疫情热搜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="历史疫情热搜")
print(covid_baidu_df)
```

数据示例-历史疫情热搜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 搜索正能量榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="搜索正能量榜"

输出参数-搜索正能量榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-搜索正能量榜

接口示例-搜索正能量榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="搜索正能量榜")
print(covid_baidu_df)
```

数据示例-搜索正能量榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 游戏榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="游戏榜"

输出参数-游戏榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-游戏榜

接口示例-游戏榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="游戏榜")
print(covid_baidu_df)
```

数据示例-游戏榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 影视榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="影视榜"

输出参数-影视榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-影视榜

接口示例-影视榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="影视榜")
print(covid_baidu_df)
```

数据示例-影视榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 小说榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="小说榜"

输出参数-小说榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-小说榜

接口示例-小说榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="小说榜")
print(covid_baidu_df)
```

数据示例-小说榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 疫期飙升榜

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="疫期飙升榜"

输出参数-疫期飙升榜

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-疫期飙升榜

接口示例-疫期飙升榜

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="疫期飙升榜")
print(covid_baidu_df)
```

数据示例-疫期飙升榜

```
    degree describe  ... type                                                url
0  7536823           ...    1  https://m.baidu.com/s?word=%E7%BD%97%E9%A9%AC%...
1  6373462           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
2  5037203           ...    0  https://m.baidu.com/s?word=%E6%AD%A6%E6%B1%89%...
3  4037324           ...    0  https://m.baidu.com/s?word=%E6%88%88%E8%B4%9D%...
4  3647245           ...    0  https://m.baidu.com/s?word=%E6%A2%85%E8%A5%BF%...
5  2047481           ...    0  https://m.baidu.com/s?word=%E8%8B%B1%E5%9B%BD%...
6  1037482           ...    0  https://m.baidu.com/s?word=%E9%92%9F%E5%8D%97%...
7   703749           ...    0  https://m.baidu.com/s?word=%E5%9B%BD%E6%B0%91%...
```

#### 实时播报

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="实时播报"

输出参数-实时播报

名称|类型|默认显示|描述
---|:---:|:---:|---
bjh_na|str|Y|-
eventDescription|str|Y|新闻描述
eventTime|str|Y|新闻时间
eventUrl|str|Y|链接
homepageUrl|str|Y|链接
item_avatar|str|Y|-
siteName|str|Y|新闻来源

接口示例-实时播报

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="实时播报")
print(covid_baidu_df)
```

数据示例-实时播报

```
                                               bjh_na  ... siteName
0   {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...      环球网
1   {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...     人民日报
2   {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...    中国青年网
3   {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...     环球时报
4   {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...      环球网
..                                                ...  ...      ...
31  {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...     红星新闻
32  {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...  人民日报海外网
33  {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...      环球网
34  {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...  人民日报海外网
35  {'easyBrowse': '1', 'easyBrowseConfirm': '1', ...  ...      人民网
```

#### 中国分省份详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国分省份详情"

输出参数-中国分省份详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国分省份详情

接口示例-中国分省份详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="中国分省份详情")
print(covid_baidu_df)
```

数据示例-中国分省份详情

```
   confirmed  died  crued  ... curConfirmRelative icuDisable area
0          1            1  ...                  0          1   西藏
1         11           10  ...                  0          1   澳门
2         18           18  ...                  0          1   青海
3         67     1     20  ...                  6          1   台湾
4        155     4     84  ...                  4          1   香港
..       ...   ...    ...  ...                ...        ...  ...
29      1018     4   1014  ...                  0          1   湖南
30      1273    22   1250  ...                  0          1   河南
31      1361     8   1306  ...                  1          1   广东
32      1231     1   1216  ...                 -2          1   浙江
33     67798  3099  55094  ...               -826          1   湖北
```

#### 中国分城市详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="中国分城市详情"

输出参数-中国分城市详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-中国分城市详情

接口示例-中国分城市详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="中国分城市详情")
print(covid_baidu_df)
```

数据示例-中国分城市详情

```
     city confirmed died crued confirmedRelative curConfirm cityCode province
0      拉萨         1          1                 0          0      100       西藏
1      西宁        15         15                 0          0       66       青海
2     海北州         3          3                 0          0       67       青海
3     六盘水        10    1     9                 0          0      147       贵州
4    毕节地区        23         23                 0          0      206       贵州
..    ...       ...  ...   ...               ...        ...      ...      ...
434    黄冈      2907  125  2750                 0         32      271       湖北
435    孝感      3518  127  3266                 0        125      310       湖北
436    黄石      1015   38   950                 0         27      311       湖北
437    荆门       928   39   865                 0         24      217       湖北
438    鄂州      1394   57  1275                 0         62      122       湖北
```

#### 国外分国详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="国外分国详情"

输出参数-国外分国详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-国外分国详情

接口示例-国外分国详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="国外分国详情")
print(covid_baidu_df)
```

数据示例-国外分国详情

```
    confirmed died crued  ... curConfirm icuDisable      area
0           1             ...          1          1      坦桑尼亚
1           1             ...          1          1      利比里亚
2           1    1        ...          0          1  圭亚那合作共和国
3           1             ...          1          1       马约特
4           1             ...          1          1       巴哈马
..        ...  ...   ...  ...        ...        ...       ...
151       368    6    27  ...        335          1      澳大利亚
152       553         35  ...        518          1      马来西亚
153       823   25   144  ...        654          1        日本
154       243        105  ...        138          1       新加坡
155       147    1    37  ...        109          1        泰国
```

#### 国外分城市详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="国外分城市详情"

输出参数-国外分城市详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-国外分城市详情

接口示例-国外分城市详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="国外分城市详情")
print(covid_baidu_df)
```

数据示例-国外分城市详情

```
    province  city confirmed died crued
0         伊朗   德黑兰      2976           
1         伊朗    吉兰       684           
2         伊朗    库姆       888           
3         伊朗  伊斯法罕       902           
4         伊朗   法尔斯       232           
..       ...   ...       ...  ...   ...
105       日本    广岛         1           
106       日本    群马         5           
107       日本    福岛         2           
108       日本    佐贺         1           
109       日本    长崎         1 
```

#### 全球分洲详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球分洲详情"

输出参数-全球分洲详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球分洲详情

接口示例-全球分洲详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="全球分洲详情")
print(covid_baidu_df)
```

数据示例-全球分洲详情

```
  area  died crued confirmed confirmedRelative
0   亚洲   988  6661     27328              1673
1   欧洲  2347  3086     56831              6970
2   非洲     8    42       387                75
3  大洋洲     6    27       377                13
4  北美洲    73    71      4306               321
5  南美洲     6     1       511               152
6   其他     7   456       712                15
```

#### 全球分洲国家详情

名称|类型|必选|描述
---|:---:|:---:|---
indicator|str|Y|indicator="全球分洲国家详情"

输出参数-全球分洲国家详情

名称|类型|默认显示|描述
---|:---:|:---:|---
-|-|-|参见 数据示例-全球分洲国家详情

接口示例-全球分洲国家详情

```
import gopup as gp
covid_baidu_df = gp.covid_baidu(indicator="全球分洲国家详情")
print(covid_baidu_df)
```

数据示例-全球分洲国家详情

```
    confirmed died crued  relativeTime confirmedRelative  country province
0           6             1.584288e+09                 2   乌兹别克斯坦       亚洲
1           8             1.584202e+09                 2    哈萨克斯坦       亚洲
2          18             1.584202e+09                12      土耳其       亚洲
3           1             1.583683e+09                        蒙古国       亚洲
4          33             1.584202e+09                 7     塞浦路斯       亚洲
..        ...  ...   ...           ...               ...      ...      ...
151        45    2     1  1.584115e+09                        阿根廷      南美洲
152        75             1.584202e+09                14       智利      南美洲
153        37    2        1.584202e+09                 9     厄瓜多尔      南美洲
154       200             1.584202e+09                79       巴西      南美洲
155       712    7   456  1.584202e+09                15  钻石公主号邮轮       其他
```

### 疫情历史数据

接口: covid_hist_city; covid_hist_province

目标地址: https://github.com/norratek/Ncov2020HistoryData

描述: 获取新型肺炎统计数据颗粒细化到地市

限量: 单次返回所有细化到地市的所有数据(最好用代理速度比较快)

#### covid_hist_city

名称|类型|必选|描述
---|:---:|:---:|---
city|str|Y|city="武汉市"

输出参数-covid_hist_city

名称|类型|默认显示|描述
---|:---:|:---:|---
date|str|Y|时间（天）
country|str|Y|国家
countryCode|float|Y|国家代码
province|float|Y|省
provinceCode|float|Y|省代码
city|float|Y|市
cityCode|float|Y|市代码
confirmed|str|Y|确诊人数
suspected|str|Y|疑似人数
cured|str|Y|治愈人数
dead|str|Y|死亡人数


接口示例-covid_hist_city

```
import gopup as gp
covid_hist_city_df = gp.covid_hist_city(city="武汉市")
print(covid_hist_city_df)
```

数据示例-covid_hist_city

```
             date country countryCode  ... suspected  cured  dead
2      2019-12-01      中国          CN  ...         0      0     0
5      2019-12-02      中国          CN  ...         0      0     0
8      2019-12-03      中国          CN  ...         0      0     0
11     2019-12-04      中国          CN  ...         0      0     0
14     2019-12-05      中国          CN  ...         0      0     0
           ...     ...         ...  ...       ...    ...   ...
25699  2020-03-12      中国          CN  ...         0  34094  2430
26333  2020-03-13      中国          CN  ...         0  35197  2436
26980  2020-03-14      中国          CN  ...         0  36465  2446
27637  2020-03-15      中国          CN  ...         0  37643  2456
28302  2020-03-16      中国          CN  ...         0  38385  2469
```

#### covid_hist_province

名称|类型|必选|描述
---|:---:|:---:|---
province|str|Y|province="湖北省"

输出参数-covid_hist_province

名称|类型|默认显示|描述
---|:---:|:---:|---
date|str|Y|时间（天）
country|str|Y|国家
countryCode|float|Y|国家代码
province|float|Y|省
provinceCode|float|Y|省代码
city|float|Y|市
cityCode|float|Y|市代码
confirmed|str|Y|确诊人数
suspected|str|Y|疑似人数
cured|str|Y|治愈人数
dead|str|Y|死亡人数


接口示例-covid_hist_province

```
import gopup as gp
covid_hist_province_df = gp.covid_hist_province(province="湖北省")
print(covid_hist_province_df)
```

数据示例-covid_hist_province

```
             date country countryCode  ... suspected cured dead
1      2019-12-01      中国          CN  ...         0     0    0
2      2019-12-01      中国          CN  ...         0     0    0
4      2019-12-02      中国          CN  ...         0     0    0
5      2019-12-02      中国          CN  ...         0     0    0
7      2019-12-03      中国          CN  ...         0     0    0
           ...     ...         ...  ...       ...   ...  ...
28314  2020-03-16      中国          CN  ...         0   242    7
28315  2020-03-16      中国          CN  ...         0   529   22
28316  2020-03-16      中国          CN  ...         0   183    9
28317  2020-03-16      中国          CN  ...         0   477   15
28318  2020-03-16      中国          CN  ...         0    11    0
```

### 迁徙数据-百度

#### 迁入与迁出地详情

接口: migration_area_baidu

目标地址: https://qianxi.baidu.com/?from=shoubai#city=0

描述: 获取百度-百度地图慧眼-百度迁徙-迁入/迁出地数据接口

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

描述: 获取百度-百度地图慧眼-百度迁徙-迁徙规模

- 迁徙规模指数：反映迁入或迁出人口规模，城市间可横向对比
- 城市迁徙边界采用该城市行政区划，包含该城市管辖的区、县、乡、村

限量: 单次返回当前城市的去年和今年的迁徙规模数据, 查询参数中的 start_date 不要随意更改

输入参数

名称|类型|必选|描述
---|:---:|:---:|---
area|str|Y|area="武汉", 输入需要查询的省份或者城市, 都需要用全称, 比如 湖北省, 武汉市
indicator|str|Y|indicator="move_in", 返回迁入地详情, indicator="move_in", 返回迁出地详情
start_date|str|Y|start_date="20190112", 一般不要变化
end_date|str|Y|end_date="20200201", 往后查询如 20200202 之后

输出参数

名称|类型|描述
---|:---:|---
日期|索引|去年和今年的日期
迁徙规模指数|str|定义参见百度, 同 covid_baidu 定义

接口示例

```
import gopup as gp
migration_scale_baidu_df = gp.migration_scale_baidu(area="湖北省", indicator="move_out", start_date="20190112", end_date="20200201")
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