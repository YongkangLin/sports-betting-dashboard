# Live Paper Trading

- Generated: 2026-05-31T00:09:08.053924+00:00
- Dry run: False
- Latest executable books: 486
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 980
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
fd2a71c79d7544ca9a2169d50be2e209 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
af04fb681404458b9e5bf1b33124da5e favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
e6784069cd3247fcbc8a9820a28ebc26 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
64fabaabef0e4edf9019c01dce202175 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
f4a4f1215d3e4afd84ebbb1d40587273 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
c3884a6385134f8c9e41737dfcbad65a favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
2ca7fbd5e737496cbc0f3c1fb783ca2d favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
279dfc21f2b140b8bcaf21ea41b025d2 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
4baa627bc2fb475eafcd56fb4624b53b  data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
a9a601fbe00441f984de9505880a27d1  data_collection_probe  96245426081152539630687250907560097785488855843417898397615686917807604781341             buy     buy_yes_data_probe         0.41      0.405               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
79514977338543dca5cfffe62d253b8e  data_collection_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049             buy     buy_yes_data_probe         0.44      0.435               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
39d3ebf173cb4099b9590065dc63ff3d    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.56      0.565               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
9f8b70ee59a24f6fb4508ec53b69377b    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
2156f4284660464e96172d6ef6305a96    passive_queue_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy  buy_yes_passive_probe         0.46      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
dc17a47dbedc4e5f80cb10e40015e1a0    passive_queue_probe  96245426081152539630687250907560097785488855843417898397615686917807604781341            sell sell_yes_passive_probe         0.41      0.405               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ee46b64a7b024d0499c515b279bd0a5c    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.44      0.435               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
a013f2f2a1e14987bba496d96a80196d    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
f93041b3ec8f4f2e94e1359205fd88d6    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
6aa8a821a5f846b9ae8ef1be98a1fec0    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
e34de00368f74d5a8628eece0b8bdecc    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
8038f358ef624393979dff8c8eaa3f02    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
b5d75c8958434438b6ac4a95aca7592a    passive_queue_probe  35808719695016380591854385631017456061790359146170745619982098204617785016343            sell sell_yes_passive_probe         0.54      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
292b11d3db1b48559a1f7863528cd147    passive_queue_probe  36085831569567062276778049949933770604644781884292059937364072837957736538526             buy  buy_yes_passive_probe         0.51      0.515               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                      token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
0879179edf454efc9c081ed95f390905 4baa627bc2fb475eafcd56fb4624b53b data_collection_probe 79939935204329019739688977160933273128770637983122609367510311322486203217598  buy        0.47    10.638298                5.0   0.0795                   0.005  same_run_order
6f1ec1e714e849808f8da5ac77067a5d a9a601fbe00441f984de9505880a27d1 data_collection_probe 96245426081152539630687250907560097785488855843417898397615686917807604781341  buy        0.41    12.195122                5.0   0.0885                   0.005  same_run_order
bcd827abd2884b90ab4a90b2087f6d5c 79514977338543dca5cfffe62d253b8e data_collection_probe 57881479704847872943544095137157098030396673130860692546874262450849694058049  buy        0.44    11.363636                5.0   0.0840                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
