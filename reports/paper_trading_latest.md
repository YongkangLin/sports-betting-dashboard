# Live Paper Trading

- Generated: 2026-05-31T00:25:27.115236+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 1016
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
ca4b12069d834050a0bae7b0eb2bca5e favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
73c9533656f54d3fbcb2d1b1e41be255 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
4529ec3f4f154493a8caafd594cc0a31 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
1546ad2ca06541d89284b66732e72b5a favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
0af3894bc2d9456fb52a7fdc10f7550d favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
b1744518552a4af6a3181434df5b0c9f favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
c2f89731890c452d88d8625f46d283fa favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
2f7cc9c5b5ae4f799f5ba6df01c32f57 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
6b35295f0ad444b2b2b560fcbb8f9048  data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
cfd04be3f43a4e75b369dbf88255f6d0  data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy     buy_yes_data_probe         0.41      0.405               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
a2231400eaa64f33968196e535c076e1  data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951             buy     buy_yes_data_probe         0.43      0.425               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
c5cf7d6cb37d4d36afc0fc3b3e7a0d8a    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
e0b7ea33c9914999846966bb96b6d0cf    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.40      0.405               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
52b34122ba38475f9b8fe5e4d7aae2da    passive_queue_probe  60849936685949154288916249085778855718942402683241688041583427950134958922785            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
4c5c16f602f2423293624c3623a3383f    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
1338411466a14f38bbd097d594710b47    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
fa1ff06a9463494ebc95fff885d7960e    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
dba1af4dceab43308f2be04b1e95728b    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
49966b5630e44cf4bd0232a93b2ec04a    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
6577d22ba1cd4fe7a78f5913348de471    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.60      0.595               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f609dd52e6cb4326937c2ba8e561f611    passive_queue_probe  72419818697574778533704883644354227751046000265350681120987720656174039450133            sell sell_yes_passive_probe         0.78      0.775               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
c5fc367019fe418d90408743cd424d59    passive_queue_probe 104608192202170414626116005511925689996147684958374377871974005701322184899639            sell sell_yes_passive_probe         0.23      0.225               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
2ece71b20ca542a5b7c37187beabe326    passive_queue_probe  89482427291501472449331761687619022196978790718582858036252131762645152705581            sell sell_yes_passive_probe         0.54      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
1284d7a84c924cbaa731e82126c68f9a 6b35295f0ad444b2b2b560fcbb8f9048 data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917  buy        0.47    10.638298                5.0   0.0795                   0.005  same_run_order
54c84736b7234433952136544ecc7c17 cfd04be3f43a4e75b369dbf88255f6d0 data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402  buy        0.41    12.195122                5.0   0.0885                   0.005  same_run_order
e31fbf21960d4e75a9c3988b6ef50046 a2231400eaa64f33968196e535c076e1 data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951  buy        0.43    11.627907                5.0   0.0855                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
