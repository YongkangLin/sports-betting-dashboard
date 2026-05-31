# Live Paper Trading

- Generated: 2026-05-31T00:36:18.714805+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 1040
- Simulated fills: 3
- Lifecycle events: 49
- Rows appended: {'signals': 23, 'orders': 23, 'fills': 3, 'lifecycle_events': 49}
- Fill-probability gate used: False
- Fill-probability gate rejected orders: 0 / 0
- Fill-probability minimum: 0.02
- Live-LEV quarantine used: True
- Live-LEV quarantine dropped signals: 0 / 23
- Post-fill CLOB capture rows: 12 across 4 iterations

## Strategy Buckets

```text
              strategy  signals
   passive_queue_probe       12
favorite_longshot_bias        8
 data_collection_probe        3
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side              direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
a206ec5a2bce475c89686a1d5461e5f0 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
a91eb44e05874259865a051be96d1d1f favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
9868af0491734039872c3dc100496bc5 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
58feafefa2c74d2ca4aa8bc296639f15 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
325e2627b7b84b0c8996461a3d58aae7 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
3aeae702775e44e3a10fd358c05648ba favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
d235a70a6570432eba1ff170283c6230 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
767db04d89774d408f99dd238c8c10ed favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
53742f7e41cd4f6fbca685523bbd4080  data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
0f95c88ad27a4c4787613002f550c471  data_collection_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy     buy_yes_data_probe         0.59      0.585               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
04f35ac58f204f61b21bb80f778f2c4a  data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy     buy_yes_data_probe         0.42      0.415               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
88c4e8a9b69d4c9b8a039a9a78e47404    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
111b9b92023a4516b4d6cb3a2c048603    passive_queue_probe  60849936685949154288916249085778855718942402683241688041583427950134958922785            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
6ae41cdc268f464f80d2b5da37f7bca3    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
12faccd4b02c4a968cf36429411d1caa    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
c0c203c19b4d4d58a41fdcdac9484724    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
e6ca45b7dde14bd58b25407d7e46f4a0    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
d1f50f766ac4493fa3bd098260119a85    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
e35477536f8f48bf8fad5047bc7e7dbb    passive_queue_probe  89482427291501472449331761687619022196978790718582858036252131762645152705581            sell sell_yes_passive_probe         0.54      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ccd1a8fba10f44598847992c1121dadd    passive_queue_probe 104608192202170414626116005511925689996147684958374377871974005701322184899639            sell sell_yes_passive_probe         0.23      0.225               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
3d41a471da6645bea26e0768d462eb60    passive_queue_probe  72419818697574778533704883644354227751046000265350681120987720656174039450133            sell sell_yes_passive_probe         0.78      0.775               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
31759ecc23f645639f78ad1d23f74834    passive_queue_probe  11160356859053943773912991194819775861470205970326978922803344003995070350070             buy  buy_yes_passive_probe         0.73      0.730               0.0       5.0       standard   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f6ee5931d2f141538ad95aed2d43ac7c    passive_queue_probe   7880351142136315614501292469773084645304166917637714889656093213004856481091            sell sell_yes_passive_probe         0.27      0.270               0.0       5.0       standard   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
647e12c44e65403bbe5c533b29af4ede 53742f7e41cd4f6fbca685523bbd4080 data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917  buy        0.47    10.638298                5.0   0.0795                   0.005  same_run_order
ec67b3fe40514b4d86a1e548bf5c5c4e 0f95c88ad27a4c4787613002f550c471 data_collection_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952  buy        0.59     8.474576                5.0   0.0615                   0.005  same_run_order
7a7734e8aceb4423a2f233343ec6aa78 04f35ac58f204f61b21bb80f778f2c4a data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426  buy        0.42    11.904762                5.0   0.0870                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
