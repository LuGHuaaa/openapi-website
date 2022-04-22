---
id: trade_definition
title: 交易命名词典
slug: trade-definition
---

## OrderType

* 说明：订单类型

| 枚举值 | 描述  |
|---- |-----|
|LO| 限价单                      |
| ELO     | 增强限价单                  |
| MO      | 市价单                      |
| AO      | 竞价市价单                  |
| ALO     | 竞价限价单                  |
| ODD     | 碎股单挂单                  |
| LIT     | 触价限价单                  |
| MIT     | 触价市价单                  |
| TSLPAMT | 跟踪止损限价单 (跟踪金额)   |
| TSLPPCT | 跟踪止损限价单 (跟踪涨跌幅) |
| TSMAMT  | 跟踪止损市价单 (跟踪金额) |
| TSMPCT  | 跟踪止损市价单 (跟踪涨跌幅) |



## OrderStatus

* 说明：订单状态

| 枚举值               | 描述              |
| -------------------- | ----------------- |
| NotReported          | 待提交            |
| ReplacedNotReported  | 待提交 (改单成功) |
| ProtectedNotReported | 待提交 (保价订单) |
| VarietiesNotReported | 待提交 (条件单)   |
| FilledStatus         | 已成交            |
| WaitToNew            | 已提待报          |
| NewStatus            | 已委托            |
| WaitToReplace        | 修改待报          |
| PendingReplaceStatus | 待修改            |
| ReplacedStatus       | 已修改            |
| PartialFilledStatus  | 部分成交          |
| WaitToCancel         | 撤销待报          |
| PendingCancelStatus  | 待撤回            |
| RejectedStatus       | 已拒绝            |
| CanceledStatus       | 已撤单            |
| ExpiredStatus        | 已过期            |
| PartialWithdrawal    | 部分撤单          |

## Market

* 说明：市场

| 枚举值 | 描述 |
| ------ | ---- |
| HK     | 港股 |
| US     | 美股 |

## WebSocket 推送通知

* WebSocket 推送通知字段说明

| 字段名            | 类型   | 注释                                                         |
| ----------------- | ------ | ------------------------------------------------------------ |
| side              | string | 买卖方向<br />Buy: 买入<br />Sell: 卖出                      |
| stock_name        | string | 公司名称                                                     |
| quantity          | string | 委托数量                                                     |
| symbol            | string | 订单标的                                                     |
| order_type        | string | 订单类型                                                     |
| price             | string | 委托价格                                                     |
| executed_quantity | string | 成交数量                                                     |
| executed_price    | string | 成交价格                                                     |
| order_id          | string | 订单 id                                                      |
| currency          | string | 结算货币                                                     |
| status            | string | 订单状态                                                     |
| submitted_at      | string | 下单时间，格式为时间戳 (秒)                                  |
| updated_at        | string | 最近更新时间                                                 |
| trigger_price     | string | 触发价格                                                     |
| msg               | string | 拒绝理由，备注信息                                           |
| tag               | string | 订单标记<br />Normal 普通订单<br />GTC 长期单<br />Grey 暗盘单 |
| trigger_status    | string | 条件单触发状态<br />NOT_ACTIVE 未激活 <br />DEACTIVE 已失效<br />ACTIVE 已激活 <br />RELEASED 已触发 |
| trigger_at        | string | 触发时间                                                     |
| tailing_amount    | string | 条件单跟踪金额                                               |
| tailing_percent   | string | 条件单跟踪涨跌幅                                             |
| limit_offset      | string | 指定价差                                                     |
| account_no        | string | 用户端账号                                                   |

### 示例

```JSON
{
	"side": "Buy",
	"stock_name": "腾讯控股",
	"quantity": "1000",
	"symbol": "700.HK",
	"order_type": "LO",
	"price": "213.2",
	"executed_quantity": "1000",
	"executed_price": "213.2",
	"order_id": "27",
	"currency": "HKD",
	"status": "NewStatus",
	"submitted_at": "1562761893",
	"updated_at": "1562761893",
	"trigger_price": "213.0",
	"msg": "Insufficient Qty - 1000",
	"tag": "Normal",
	"trigger_status": "NOT_ACTIVE",
	"trigger_at": "1562761893",
	"tailing_amount": "5",
	"tailing_percent": "0.01",
	"limit_offset": "0.01"
}
```