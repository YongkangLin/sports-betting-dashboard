# Live Paper Trading

- Generated: 2026-05-31T01:18:43.168075+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 17
- Paper orders: 17
- Existing open orders rechecked: 1124
- Simulated fills: 3
- Lifecycle events: 37
- Rows appended: {'signals': 17, 'orders': 17, 'fills': 3, 'lifecycle_events': 37}
- Fill-probability gate used: False
- Fill-probability gate rejected orders: 0 / 0
- Fill-probability minimum: 0.02
- Live-LEV quarantine used: True
- Live-LEV quarantine dropped signals: 0 / 17
- Post-fill CLOB capture rows: 12 across 4 iterations

## Strategy Buckets

```text
              strategy  signals
favorite_longshot_bias        8
   passive_queue_probe        6
 data_collection_probe        3
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side              direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
3a4c1a069670497dbc565e123e2f9af5 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
f1fd74942eb74a5ebb21a2961fe81743 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
48785dfcb3d34a3aaf97d9b39236f009 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
a1096a7e16a84bc1b4f61aa4a45dfe03 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
1b64f7487b254ab98c327de6f6c59bb7 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
a84d3d232c2d41078d5f4b0f87eb9dff favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
807e1434e50e4cd5a18493cf828024da favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
664a371661df45309785eea01962c7ad favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
c2af9f2ec9c34da197ba90343834fdeb  data_collection_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy     buy_yes_data_probe         0.58      0.575               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
5fd925fce26b482b80aac0f83b1ec91f  data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951             buy     buy_yes_data_probe         0.43      0.425               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
7752d077941d4f469efc40a574287d19  data_collection_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy     buy_yes_data_probe         0.59      0.585               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
401494baf2744b58a90001feb61d8f10    passive_queue_probe  12881849356844161973633098310214035614783586418054382638538783737761306601763            sell sell_yes_passive_probe         0.29      0.285               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
56c5a486f7e5422384f23c246df8be18    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
cc2d02893a5b4f24aed96d130f2e3cb0    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
3cdd7c48cfc2430b9bc890479c3d9deb    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
132ade6f20504135a4b0ed307138f3ab    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ad7bc6011f0443b99e8471bb10d17c3f    passive_queue_probe  20774972609562033466649635928456937284777449555135496361707158570943034147564             buy  buy_yes_passive_probe         0.71      0.715               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
9d214239ec554d8b9ddc291964412e79 c2af9f2ec9c34da197ba90343834fdeb data_collection_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384  buy        0.58     8.620690                5.0   0.0630                   0.005  same_run_order
8df1f90df4d446b6a020b63e7654e167 5fd925fce26b482b80aac0f83b1ec91f data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951  buy        0.43    11.627907                5.0   0.0855                   0.005  same_run_order
b10e0c32e53f404984a49bfad174c240 7752d077941d4f469efc40a574287d19 data_collection_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952  buy        0.59     8.474576                5.0   0.0615                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
