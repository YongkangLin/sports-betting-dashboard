# Live Paper Trading

- Generated: 2026-05-30T23:58:45.416541+00:00
- Dry run: False
- Latest executable books: 486
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 956
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
deb503a7c6374b76a21282c44b73e269 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
305a18c67c5748818701030cd9a8defe favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy       buy_yes_favorite         0.89      0.905               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
7c50653fcee44b7db8d9fcf5c9901d85 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
ebc259f5cd89492c89f1a1820d8199c8 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy       buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
7c991c47ad284bc8a12a12af6b6ceacb favorite_longshot_bias 104267490818682702307686644262312954209143243276446662224187931447432098298393             buy       buy_yes_favorite         0.93      0.945               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
58bad88eb85149b7b6ecb86080c5b8ca favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped      fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
0188613511724686be313b560f0c9964 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped      fade_yes_longshot         0.11      0.095               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
b3140ce40e3d46ffaf16a6542c3cadce favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy       buy_yes_favorite         0.92      0.930               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
9f0b30ca1c214ecda14bb3aa5570824d  data_collection_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049             buy     buy_yes_data_probe         0.44      0.435               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
d9bdee5253e94de2bad813b40f4955fa  data_collection_probe  35808719695016380591854385631017456061790359146170745619982098204617785016343             buy     buy_yes_data_probe         0.52      0.515               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
55e69698b0c44b009f72a9952a1da6c5  data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy     buy_yes_data_probe         0.49      0.485               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
2dece72c07f04eecbd8777b5fa52e226    passive_queue_probe  42873895851018051543725096590620321074907558861463383603249689629727937903402             buy  buy_yes_passive_probe         0.56      0.565               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
de959fec3566443fa829bc75458ae2f4    passive_queue_probe 105863550463546431611528463561144881659177878192488543485430376912976176829917            sell sell_yes_passive_probe         0.47      0.465               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
116c3f7f1f2849f9a99ea0db0e6115c1    passive_queue_probe  57881479704847872943544095137157098030396673130860692546874262450849694058049            sell sell_yes_passive_probe         0.44      0.435               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
2b39de2825ad4607ae738035d51cc9f1    passive_queue_probe  35808719695016380591854385631017456061790359146170745619982098204617785016343            sell sell_yes_passive_probe         0.52      0.515               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
cd83bd90d11e424f8d161dc5a7f58564    passive_queue_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy  buy_yes_passive_probe         0.48      0.485               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
164d43ac41b14e9bae87fc89ead22694    passive_queue_probe  27067287007835734603480979251913263202347932152446523710862265223338453264137            sell sell_yes_passive_probe         0.59      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
114f5a3f1b69483787785d70c7aaaa43    passive_queue_probe  96245426081152539630687250907560097785488855843417898397615686917807604781341            sell sell_yes_passive_probe         0.42      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
5dce6ea80e4c4d6ba247e79697160bcc    passive_queue_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy  buy_yes_passive_probe         0.57      0.575               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
47380a3e398440aa8ed5e3178dfa48a5    passive_queue_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951            sell sell_yes_passive_probe         0.43      0.425               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
3b1ccc4d00e34ca68e97655a391b2543    passive_queue_probe  19181795497624344761636476310807127966421666504143793580642769392931259470952             buy  buy_yes_passive_probe         0.58      0.585               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
ccf81fb7aead498ea0ca8a0c6fa1e2ee    passive_queue_probe  77531852831940823906158779928459994173178439828904080507613540072180228176426             buy  buy_yes_passive_probe         0.41      0.415               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
1fd574647de64b2e8595db90168b304c    passive_queue_probe  56936374719061521260071067724694755510656056657002561248979267332542463067862             buy  buy_yes_passive_probe         0.53      0.535               0.0       5.0           deep   passive-queue-probe-v1   passive-queue-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                      token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
df337675edbd426083a4581191c796de 9f0b30ca1c214ecda14bb3aa5570824d data_collection_probe 57881479704847872943544095137157098030396673130860692546874262450849694058049  buy        0.44    11.363636                5.0   0.0840                   0.005  same_run_order
3a3e1638901e4b76bc6e61c5e5469134 d9bdee5253e94de2bad813b40f4955fa data_collection_probe 35808719695016380591854385631017456061790359146170745619982098204617785016343  buy        0.52     9.615385                5.0   0.0720                   0.005  same_run_order
c723ec9e6c7349598102098f18fca290 55e69698b0c44b009f72a9952a1da6c5 data_collection_probe 79939935204329019739688977160933273128770637983122609367510311322486203217598  buy        0.49    10.204082                5.0   0.0765                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
