# Live Paper Trading

- Generated: 2026-05-31T00:47:51.992626+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 1064
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
818f9e1dd72d435baa1bd6ccf5449fb2 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
b5646c11ebf643f2a9a2029ee0ed5661 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
c06746c7ed1c4ca0ab46d498399e1bb7 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
c12280d950a34cfdb599a5ed6621105e favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
0b8ad3b2d47341e99d82ba6a1a5bc568 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
255a10588cd0423ab7fa3451c0d2ce0d favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
2ca873e3a4bb49039153294a72cc4468 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
9af1a312bcca4e8f881c7fc84953d35f favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
6910f9312b4d4c8abd7cce88e7d3a062  data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
bbcfb9050ed44fcbbc436e2d110c1b0a  data_collection_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049             buy     buy_yes_data_probe         0.59      0.585               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
46fc162e7a78479694f870c87928a615  data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy     buy_yes_data_probe         0.42      0.415               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
415df6db4a714db59ab00fd67038e205    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
b7a68bc3261846278798996818f906c6    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
295362ce2d2842ae91a70752690465f7    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
9d981a5ccedf4655893c3eba1b0ed477    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.59      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
364d70ba08f443058b847b5259bffb67    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
11db4085e5f34ff7bbe65a74ae056ed9    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
8acca9a564634a2580435f73f6e70a17    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
2abf50cf8e024b73a2c9b66c29fd8687    passive_queue_probe 111717384248782787094361976174210153152989607372599454870190819408645062276501            sell sell_yes_passive_probe         0.49      0.485               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
21a736acf80e409bade2f8331395f8e2    passive_queue_probe  22550927216826323058125697426817377269508582698208790067897444185879261143156             buy  buy_yes_passive_probe         0.51      0.515               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
64dd0cb83d8646a08f0e535fe102984a    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
7b4bef4b431447c1abbaf360f24e85e9    passive_queue_probe   7880351142136315614501292469773084645304166917637714889656093213004856481091            sell sell_yes_passive_probe         0.27      0.270               0.0       5.0       standard   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
38377e150eaa4e548c5bc498b08d9772    passive_queue_probe  11160356859053943773912991194819775861470205970326978922803344003995070350070             buy  buy_yes_passive_probe         0.73      0.730               0.0       5.0       standard   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
2dddf010fc034ca3b4263923cb94a874 6910f9312b4d4c8abd7cce88e7d3a062 data_collection_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917  buy        0.47    10.638298                5.0   0.0795                   0.005  same_run_order
48ccac1c0b084432a4beb5336393e1e4 bbcfb9050ed44fcbbc436e2d110c1b0a data_collection_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049  buy        0.59     8.474576                5.0   0.0615                   0.005  same_run_order
376db7ca2573468280ef9b66e818d292 46fc162e7a78479694f870c87928a615 data_collection_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402  buy        0.42    11.904762                5.0   0.0870                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
