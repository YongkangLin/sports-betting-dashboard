# Live Paper Trading

- Generated: 2026-05-30T23:28:56.521030+00:00
- Dry run: False
- Latest executable books: 482
- Signals: 19
- Paper orders: 19
- Existing open orders rechecked: 904
- Simulated fills: 3
- Lifecycle events: 41
- Rows appended: {'signals': 19, 'orders': 19, 'fills': 3, 'lifecycle_events': 41}
- Fill-probability gate used: False
- Fill-probability gate rejected orders: 0 / 0
- Fill-probability minimum: 0.02
- Live-LEV quarantine used: True
- Live-LEV quarantine dropped signals: 0 / 19
- Post-fill CLOB capture rows: 12 across 4 iterations

## Strategy Buckets

```text
              strategy  signals
favorite_longshot_bias        8
   passive_queue_probe        8
 data_collection_probe        3
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side              direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
f2fe87c891094c33b10222f180b71fb4 favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
8858b9d02cb34188b1d40acec79fa780 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
219897cfd6f44929a529041d91e66711 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
10c834808456479eb26ddc879df0a213 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
9a18d14fbc534933a5677d9ea22d19b0 favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
66de4cb1cc2f4f0395a65b12ab4efba0 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
bf3be9e875a64c88948f1d27aec3c159 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
0809f867c46c45c5bce91faa22c40ed4 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
86956cbc16c0400991c3a09139caa665  data_collection_probe 108059767755668016723872486265482838263029560661069487856940165158474295399516             buy     buy_yes_data_probe         0.57      0.565               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
8a0f03eee7c24d459767538308577bca  data_collection_probe  92697356862188157077056093577982118842855643840706001806047706558759246451741             buy     buy_yes_data_probe         0.47      0.465               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
bec0e87faefa49eca98252d89ce9b9df  data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy     buy_yes_data_probe         0.49      0.485               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
812133bf78f04a86bb6878d55e1cdf14    passive_queue_probe 108059767755668016723872486265482838263029560661069487856940165158474295399516             buy  buy_yes_passive_probe         0.56      0.565               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
3fc1103bd731414b80c88c6e23ef61bc    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
174fb049496c4bbf916a89fdecca0c57    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
3a7d202524484247883abcbe28988a99    passive_queue_probe   7720399120788946022974925663539915665145122195250033030972530633219689821345            sell sell_yes_passive_probe         0.76      0.755               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
7e5c51b021274a61b80b2d794883b659    passive_queue_probe  74170671452925195303534281944952981830841609487512036898317699936288275976259            sell sell_yes_passive_probe         0.68      0.675               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
626641a6f2f04b9bb0222e4629154d5a    passive_queue_probe 111883163922681763528989577126219325318778633437621543341927524705787440450096             buy  buy_yes_passive_probe         0.32      0.325               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
1e36cd84b9d74973b38892160c7e7848    passive_queue_probe  47062988043329943958165447317799962692984929028138399260987715699534752769142             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
a2c1802c427e4a5282600217b7d732c4    passive_queue_probe  25193652029001616183938966163098366729945775552098557037388001875010743350495            sell sell_yes_passive_probe         0.43      0.430               0.0       5.0       standard   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
e50b3cfa5d994ab7ae054fc3af9c81a8 86956cbc16c0400991c3a09139caa665 data_collection_probe 108059767755668016723872486265482838263029560661069487856940165158474295399516  buy    0.574257     8.706897                5.0 0.063861                0.009257  same_run_order
b10687b64a1440f2baaeeedab53c0dac 8a0f03eee7c24d459767538308577bca data_collection_probe  92697356862188157077056093577982118842855643840706001806047706558759246451741  buy    0.470000    10.638298                5.0 0.079500                0.005000  same_run_order
c2fc1b7604214fe9953e0b68d747251b bec0e87faefa49eca98252d89ce9b9df data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598  buy    0.490000    10.204082                5.0 0.076500                0.005000  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
