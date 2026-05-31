# Live Paper Trading

- Generated: 2026-05-31T01:11:41.505820+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 1112
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
48db292ee83a4714bbbae0bdaa73fe7a favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
340da1b15448455d86b33a08c9775ace favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
7e14f2a8f1d942c7a727bf35ed6ed5b2 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
bb04067fead94c84b6175489f164e5ec favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
a4f1acf62b4c437982b0abc48e1fbb45 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
1d639f4585f04147abfbc7b8a88dc7f5 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
29169340bd1840398a8769a32129f543 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
c890c6f3cb934be79368f26502a81aae favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
cc7464c5aed74becbdc99b60b61d5934  data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
8069ddfab23e4df3a08e8d6fc692c102  data_collection_probe  12881849356844161973633098310214035614783586418054382638538783737761306601763             buy     buy_yes_data_probe         0.29      0.285               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
f0f6909f02f74895af28d5f03b3c4502  data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy     buy_yes_data_probe         0.42      0.415               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
0f5c564b3a484c4a86d800389ff962df    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f1a6983ecf2c4f58ae24ad7b8fe0b372    passive_queue_probe  12881849356844161973633098310214035614783586418054382638538783737761306601763            sell sell_yes_passive_probe         0.29      0.285               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
a846402646eb4e21bf5b5a32527340b3    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ab8088abebf242c99ec9214bfae4e869    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
d54879cfd7774aa7bc86a6ec80f02055    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f3ffd8be8e4345988fa19c681c797146    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
dbc38fed6b4949f8a9fd9c82b5308e3f    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
1ba038ea758e4d3898eac1fe69f81452    passive_queue_probe  20774972609562033466649635928456937284777449555135496361707158570943034147564             buy  buy_yes_passive_probe         0.71      0.715               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
1bd364d63a4c4f9a89b40cd9935d3537    passive_queue_probe  22550927216826323058125697426817377269508582698208790067897444185879261143156             buy  buy_yes_passive_probe         0.50      0.505               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
cb04e01b3cf5406da45266c0352d3fc8    passive_queue_probe 111717384248782787094361976174210153152989607372599454870190819408645062276501            sell sell_yes_passive_probe         0.50      0.495               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
904ee43c738f46e9add789f16561e418    passive_queue_probe  89482427291501472449331761687619022196978790718582858036252131762645152705581            sell sell_yes_passive_probe         0.55      0.545               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
fdce85e7bdcd47988635c4e39d92015b    passive_queue_probe  60849936685949154288916249085778855718942402683241688041583427950134958922785            sell sell_yes_passive_probe         0.46      0.455               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
ea84b93db778420b9b36af1709b4add9 cc7464c5aed74becbdc99b60b61d5934 data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917  buy        0.47    10.638298                5.0   0.0795                   0.005  same_run_order
449d39d39d144c08b2754eb3908c4c29 8069ddfab23e4df3a08e8d6fc692c102 data_collection_probe  12881849356844161973633098310214035614783586418054382638538783737761306601763  buy        0.29    17.241379                5.0   0.1065                   0.005  same_run_order
a762d03cb7634d87becb4981cf5d93c7 f0f6909f02f74895af28d5f03b3c4502 data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426  buy        0.42    11.904762                5.0   0.0870                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
