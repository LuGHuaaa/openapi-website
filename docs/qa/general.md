---
title: 通用问题
sidebar_position: 0
---

## Q1: 一定要开通真实账户才能调用 LongPort OpenAPI 吗？

A: 我们已提供了模拟账户，您可以用模拟账户来完成 OpenAPI 的行情和交易接口调试。

## Q2: 如何开通模拟账户调试？

A: 请访问 [开发者中心](https://open.longportapp.com/account/) 开启**模拟账户**并获得模拟账户对应的 App Key & Secret 以及 Access Token 等信息。

## Q3: 模拟调试的行情交易权限与真实账户相同吗？

A: 行情相同，交易不同。

模拟账户和真实账户共用 App Key & Secret，不同 Access Token。其中，行情权限与 App Key & Secret 关联，交易权限与 Access Token 关联，因此模拟账户和真实账户下，行情权限相同，交易权限与证券账号关联，可能会不同。

## Q4: 模拟调试支持哪些市场和品种的行情和交易

A: 行情：支持港股、美股、A 股通市场实时行情，其中，美股全美行情、港股 Level2 等高级行情也可通过在线行情商店购买对应行情权益后，通过 OpenAPI 获取行情数据。

交易：支持港美股股票、ETF、港股轮证交易，其中美股支持股票做空。美股 OTC、盘前盘后交易、期权交易在模拟账号下暂未支持。

## Q5: 接口调用频次及数量限制

A: 请访问 [频率限制](/docs/#rate-limit) 查看具体描述。

## Q6: 多个账户情况下，接口调用频次如何限制

A: 若客户持有多个证券账户，例如日内融或其他子账户，交易接口调用频次和数量限制按不同的证券账户统计和控制，行情接口则不受多账户影响，统一限制。

## Q7: 通过 LongPort OpenAPI 进行交易操作有额外收费吗

A: 通过 OpenAPI 接入进行行情查询、交易等，我们不会收取额外的费用。交易手续费、平台费、行情权限等账户相关的费用，请以 App 以及官网提供的信息为准。