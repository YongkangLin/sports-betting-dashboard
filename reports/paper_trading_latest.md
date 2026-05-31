# Live Paper Trading

- Generated: 2026-05-31T01:41:31.844744+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 21
- Paper orders: 21
- Existing open orders rechecked: 1142
- Simulated fills: 3
- Lifecycle events: 45
- Rows appended: {'signals': 21, 'orders': 21, 'fills': 3, 'lifecycle_events': 45}
- Fill-probability gate used: False
- Fill-probability gate rejected orders: 0 / 0
- Fill-probability minimum: 0.02
- Live-LEV quarantine used: True
- Live-LEV quarantine dropped signals: 0 / 21
- Post-fill CLOB capture rows: 12 across 4 iterations

## Strategy Buckets

```text
              strategy  signals
   passive_queue_probe       10
favorite_longshot_bias        8
 data_collection_probe        3
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side              direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
a48a1f54cc6443c3bb99aca3507601e8 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
6d9ef46794904be8884b98e49b6d38c3 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
b40e0574d1654ff586771176dc638eb5 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
4c81a620cb824f01bb2c36159ce76559 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
107f87f0df0e466cb969dc2c687e08fc favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
e1e560db3a6144f3834bf4057aeff460 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
c38c89d532144c4191ba0d234917336e favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
0f1646f0d5fe4457b1cbcfc40476d537 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
c00f6d508d41481596e2f5a10f6fbfa0  data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy     buy_yes_data_probe         0.42      0.415               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
37b616d53d424950ba30433e3afb5459  data_collection_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy     buy_yes_data_probe         0.54      0.535               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
2f28e53707d94131b933de3bef66aa11  data_collection_probe  72419818697574778533704883644354227751046000265350681120987720656174039450133             buy     buy_yes_data_probe         0.78      0.775               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
7cbb5b6fc50b4e378617104d953bb36d    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
d1c7fbc07bf640998cb6c38dab8341a8    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
87eb3c0863a84160b4e79c2a866a9b12    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
44defd70ad1a43619ec11fb6593cb613    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
12280e75306647eebb30a54624730eda    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
4c94a3feff164fc8aeb46ed7aea074ce    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f4809106e49f4d578d9a2f85944b2ce8    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
c40b83159cef487e89a021589089c1f6    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
6883d7f237454088b76318a73b33c7f6    passive_queue_probe  72419818697574778533704883644354227751046000265350681120987720656174039450133            sell sell_yes_passive_probe         0.78      0.775               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
a62add5557c341e39440a671d38a9cb5    passive_queue_probe 104608192202170414626116005511925689996147684958374377871974005701322184899639            sell sell_yes_passive_probe         0.23      0.225               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                      token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
82648c242a934d1183edc255346f0199 c00f6d508d41481596e2f5a10f6fbfa0 data_collection_probe 77531852831940823906158779928459994173178439828904080507613540072180228176426  buy        0.42    11.904762                5.0    0.087                   0.005  same_run_order
f7451c78b9aa40b5890307bf911618b0 37b616d53d424950ba30433e3afb5459 data_collection_probe 56936374719061521260071067724694755510656056657002561248979267332542463067862  buy        0.54     9.259259                5.0    0.069                   0.005  same_run_order
33e84f430e284547bd5f19b77d034eaf 2f28e53707d94131b933de3bef66aa11 data_collection_probe 72419818697574778533704883644354227751046000265350681120987720656174039450133  buy        0.78     6.410256                5.0    0.033                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
