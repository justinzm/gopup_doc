## 新经济数据

### 千里马公司数据
接口: maxima_company

目标地址: https://www.itjuzi.com

描述: 获取国内千里马公司数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
- | - | - | -

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 公司名称 | str | - | - |
| 成立时间 | str | - | - |
| 总投资 | str | - | - |
| 所属行业 | str | - | - |
| 所属省份 | str | - | - |

接口示例

```
import gopup as gp
df_index = gp.maxima_company()
print(df_index)
```

### 独角兽公司数据
接口: nicorn_company

目标地址: https://www.itjuzi.com

描述: 获取国内独角兽公司数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
- | - | - | -

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 公司名称 | str | - | - |
| 成立时间 | str | - | - |
| 总投资 | str | - | - |
| 所属行业 | str | - | - |
| 所属省份 | str | - | - |

接口示例

```
import gopup as gp
df_index = gp.nicorn_company()
print(df_index)
```

### 倒闭公司数据
接口: death_company

目标地址: https://www.itjuzi.com

描述: 获取国内死亡公司数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
- | - | - | -

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 公司名称 | str | - | - |
| 成立时间 | str | - | - |
| 倒闭时间 | str | - | - |
| 存活天数 | str | - | - |
| 总投资 | str | - | - |
| 所属行业 | str | - | - |
| 所属省份 | str | - | - |

接口示例

```
import gopup as gp
df_index = gp.nicorn_company()
print(df_index)
```

### 特许经营许可
接口: death_company

目标地址: http://txjy.syggs.mofcom.gov.cn/

描述: 获取特许经营许可数据

输入参数

名称 | 类型 | 必须 | 描述
---|:---:|:---:|---
- | - | - | -

输出参数

| 名称 | 类型 | 默认显示 | 描述 |
---|:---:|:---:|---
| 特许人名称 | str | - | - |
| 备案时间 | str | - | - |
| 地址 | str | - | - |

接口示例

```
import gopup as gp
df_index = gp.franchise_china()
print(df_index)
```