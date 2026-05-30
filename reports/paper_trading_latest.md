# Live Paper Trading

- Generated: 2026-05-30T23:52:50.314800+00:00
- Dry run: False
- Latest executable books: 486
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 944
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
ef3cc2444550479d817893c9f7fd7ada favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
2d582f8ce0024408b77744c20a630510 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
156f0b629d4b42aebc480ed2a4b4cfa3 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
d80e6f5339194571b370901e482c8bef favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
a50c7d073c294521b0b30a3eab27db07 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
03499dec1e274db58973c2fd30858ef1 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
90f21038ad074c9992ec65304a699d3c favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
0320117efc1c477a889c643cb415f707 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
2eb6da08716f43d38960b5a3cbd5deaa  data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy     buy_yes_data_probe         0.57      0.565               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
835dc79a4bdf4c7b9fa02c4863ce8746  data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
9ec298be4f94428c835ffd239e18aaa1  data_collection_probe  72617304929419582091415328164327590812591322047048133931711341093980773468830             buy     buy_yes_data_probe         0.24      0.235               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
5fb32a150ab5461eadfb3a3e7f8d32c1    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.56      0.565               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
5dc380985245483692875e63eb728698    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
14f7eeae77e0449bb76fdb8a6f503d81    passive_queue_probe  72617304929419582091415328164327590812591322047048133931711341093980773468830             buy  buy_yes_passive_probe         0.23      0.235               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
5af0a0666bfc4478a4bd598fef89d3dd    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.44      0.435               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
79dab231e4a24c4484700aefbc0fc101    passive_queue_probe  35808719695016380591854385631017456061790359146170745619982098204617785016343            sell sell_yes_passive_probe         0.52      0.515               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
c4af419d16944bc591ba62275c734ee8    passive_queue_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy  buy_yes_passive_probe         0.48      0.485               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
64b00cb7fd174788a4fbe998d2f4c102    passive_queue_probe  36085831569567062276778049949933770604644781884292059937364072837957736538526             buy  buy_yes_passive_probe         0.52      0.525               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
309422091f544d1b9460e240339cf405    passive_queue_probe  13376028186724101887653406612446403060436811174785628829270034229284412706092             buy  buy_yes_passive_probe         0.47      0.475               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
72ddfaebd3b24abfa34acf4942113fb8    passive_queue_probe  27067287007835734603480979251913263202347932152446523710862265223338453264137            sell sell_yes_passive_probe         0.59      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
dba1b1d34ed948ea94cafa9d410e3213    passive_queue_probe  96245426081152539630687250907560097785488855843417898397615686917807604781341            sell sell_yes_passive_probe         0.42      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f1426f53747d49ef8d33ced0ef8349c5    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
4b7c17be66894015b5e8c38f20dc0542    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
f8f780316d984544b02d2fc08a62043a 2eb6da08716f43d38960b5a3cbd5deaa data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402  buy    0.570000     8.771930                5.0 0.064500                0.005000  same_run_order
52b941b89fb949bf98fa2fff9c525753 835dc79a4bdf4c7b9fa02c4863ce8746 data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917  buy    0.470000    10.638298                5.0 0.079500                0.005000  same_run_order
dabc54f8d84648119bf3df760f227f0d 9ec298be4f94428c835ffd239e18aaa1 data_collection_probe  72617304929419582091415328164327590812591322047048133931711341093980773468830  buy    0.248509    20.120000                5.0 0.112724                0.013509  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
