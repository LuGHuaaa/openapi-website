---
sidebar_position: 1
slug: /introduce
title: Longbridge Open API 简介
id: getting_started_introduce
---

# Longbridge Open API 简介
## 概述
### Open API 简介
Longbridge Open API 为有研发能力的投资者提供程序化行情交易接口，助力投资者根据自身投资策略搭建交易或行情策略分析工具。覆盖以下类别功能：
- 交易类 - 创建、修改、撤销订单，当日/历史订单及成交记录的查询等
- 行情类 - 实时行情报价、历史行情数的获取等
- 资产类 - 实时账户资产、持仓、现金查询等
- 实时订阅 - 提供行情实时报价以及订单状态实时变更信息推送

### 接口类型
Longbridge 提供接入底层服务的 Https/Websocket 接口以及封装在上层的 SDK（Python/C++）等多种接入方式，灵活选择。

### 系统流程
待补充

### 如何开通
第一步：登录 Longbridge App 或官网 [www.longbridgehk.com](www.longbridgehk.com) 完成长桥综合账户的开户（目前不支持长桥标准账户的接口服务）
第二步：登录 [www.longbridgeapp.com](www.longbridgeapp.com) 进入开发者平台，完成开发者认证即 Open API 权限申请，获取令牌

### 使用权限及限制
#### 交易类

|  | 股票 ETF   | 权证 | 期权 | 
|-------|-------|-----|----|
| 香港市场 |✔️|✔️||
| 美国市场 |✔️|✔️|✔️|

#### 行情类

<table>
    <tr>
        <td>市场</td>
        <td>标的</td>
        <td>权限获取方式</td>
    </tr>
    <tr>
        <td rowspan="2">港股市场</td>
        <td>证券类产品（含股票、ETFs、窝轮、牛熊、界内证）</td>
        <td rowspan="2">
            <ul>
            <li>中国大陆客户：请购买 <font color="red">港股 Lv2 实时行情 + 实时恒生指数-Open API（仅限大陆地区使用）</font></li>   
            <li>非中国大陆客户：请购买 <font color="red">港股 Lv2 实时行情 + 实时恒生指数-Open API（不限使用地区）</font></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>恒生指数</td>
    </tr>
    <tr>
        <td rowspan="3">美股市场</td>
        <td>证券类产品（含纽交所、美交所、纳斯达克上市的股票、ETFs）</td>
        <td rowspan="2">
            <ul>
            <li>Level 1：请购买 <font color="red">L1 Nasdaq Basic-Open API</font></li>    
            <li>Level 2：
                <ul>
                <li>非专业用户：请购买 <font color="red">L2+ Nasdaq TotalView-Open API（非专业用户）</font></li>
                <li>专业用户：请购买 <font color="red">L2+ Nasdaq TotalView-Open API（专业用户）</font></li>
                </ul>
            </li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>纳斯达克指数</td>
    </tr>
    <tr>
        <td>OPRA 期权</td>
        <td>
            <ul>
            <li>非专业用户：请购买 <font color="red">OPRA 期权实时行情-Open API（非专业用户）</font></li>
            <li>专业用户：请购买 <font color="red">OPRA 期权实时行情-Open API（专业用户）</font></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td rowspan="2">A 股市场</td>
        <td>证券类产品（含股票、ETFs）</td>
        <td rowspan="2">
            <ul>
            <li>中国大陆个人客户：免费获取 LV1 行情</li>   
            <li>非中国大陆客户/机构客户：暂不支持</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>指数</td>
    </tr>
</table>

### 使用费用
长桥不针对接口服务额外收取开通或使用费用，只需开通长桥综合账户及 Open API 服务权限后即可免费使用。实际交易产生佣金费用或高级行情产品费用参考[官网收费](https://longbridgehk.com/zh-CN/rate)说明或咨询线上客服。