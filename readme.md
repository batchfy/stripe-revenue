# Stripe 统计商品营收

根据每个月 payout（银行实际到账）统计每个商品的营收。

## 用法

`python revenue.py --year 2025 --month 03`

`--year` 和 `--month` 都是可选参数，如果不填，默认当前年月。


## 基本逻辑

1. 查到一个月所有的银行到账（payout）
2. 在每一个 payout 里面，查询所有包含的交易，包括收款，退款，续订等等
3. 根据每一个交易，找到对应的商品，然后累计每一个商品的营收。
