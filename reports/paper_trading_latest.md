# Live Paper Trading

- Generated: 2026-05-31T01:25:04.138031+00:00
- Dry run: False
- Latest executable books: 488
- Signals: 13
- Paper orders: 13
- Existing open orders rechecked: 1130
- Simulated fills: 1
- Lifecycle events: 27
- Rows appended: {'signals': 13, 'orders': 13, 'fills': 1, 'lifecycle_events': 27}
- Fill-probability gate used: False
- Fill-probability gate rejected orders: 0 / 0
- Fill-probability minimum: 0.02
- Live-LEV quarantine used: True
- Live-LEV quarantine dropped signals: 0 / 13
- Post-fill CLOB capture rows: 5 across 5 iterations

## Strategy Buckets

```text
              strategy  signals
favorite_longshot_bias        8
   passive_queue_probe        4
 data_collection_probe        1
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side              direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
0c8cf2bbf46a49a4a8681d7b687245b8 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
8fae9f1283ee41af82096e21bd7ada48 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
15b880e69bfa4d9b91b31b1a8c9188d7 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
920a7d50b544472b807f9a3fa7891669 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
9b896e9b75b94b8688c538ec02aa3beb favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
e82be127c858487cbb17f5da78a1f7d2 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
f4060b0f7c714e87988da0c8dc8966dd favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
03c661e98a2a49089fedb483984f34cd favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
25dd0c2584da4ec7bf445ce0edd05d5c  data_collection_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy     buy_yes_data_probe         0.42      0.415               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
ed0d3d4ea9444b52ab163de7a4e03798    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
9d44deb195574fa991f0ea918e6103c1    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
eb1c276a69a54a66bbf5f92d3e6227ef    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ed00a44c735c4713af881a9d4d620877    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                      token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
a5fe7a2e714841ca8d2db14e6c345ff8 25dd0c2584da4ec7bf445ce0edd05d5c data_collection_probe 77531852831940823906158779928459994173178439828904080507613540072180228176426  buy        0.42    11.904762                5.0    0.087                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
