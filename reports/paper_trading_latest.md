# Live Paper Trading

- Generated: 2026-05-30T19:11:38.030417+00:00
- Dry run: False
- Latest executable books: 458
- Signals: 23
- Paper orders: 23
- Existing open orders rechecked: 450
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
favorite_longshot_bias       20
 data_collection_probe        3
```

## Orders

```text
                        order_id               strategy                                                                       token_id            side          direction  limit_price  fair_prob  edge_after_costs  size_usd liquidity_tier            model_version         decision_version   status                           reason
a5a54c0b03764b3eae749766a5072006 favorite_longshot_bias  34087356637834874215866186174029680960921544181477195551838555754999852524900             buy   buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
0c470683e0024acba1fcdf1af7d43d1d favorite_longshot_bias  92816755304578259381356952331201491346619801385222002169623577619960501498008 buy_no_unmapped  fade_yes_longshot         0.10      0.085               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
60857d899a5145b99991178522e435a5 favorite_longshot_bias  34410262602501043362619334441585275150559497204102827166424758018496222749758             buy   buy_yes_favorite         0.86      0.875               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
c3690b38114e417bafa76bc206019a01 favorite_longshot_bias  28373857244897552580832317974647299355886409156928708887897777108710823384767             buy   buy_yes_favorite         0.83      0.845               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
bb61cc12a4334957b1143f2d846840e0 favorite_longshot_bias  87805459761728521377452139108789502581772464599578287932312318871969626781541             buy   buy_yes_favorite         0.91      0.925               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
7e32e14bd489418ca81b78c5e0a09c31 favorite_longshot_bias  61063196495177897320149021689096884765507615778300117379716677552436058501858             buy   buy_yes_favorite         0.89      0.900               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
113e5c7754e5470384900d1bb5caa62a favorite_longshot_bias  70728365344788038336906859116419100269131745032874464489754876440988496528613             buy   buy_yes_favorite         0.90      0.915               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
d3bcc38a217b4eb49331371a715bc6fb favorite_longshot_bias  95053469231206257302367310488868062905722206915369977028618527429805714894550             buy   buy_yes_favorite         0.80      0.815               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
18ade8eece374a50b64bb743da8e2e02 favorite_longshot_bias  39604648062103138938635849147125344136254605491936129690682936593009695489225 buy_no_unmapped  fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
8f118f6e1ab34d46927d0a057dccc3fa favorite_longshot_bias  72419818697574778533704883644354227751046000265350681120987720656174039450133             buy   buy_yes_favorite         0.78      0.795               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
005626a831ed4b3ea29116598a346ac2 favorite_longshot_bias  28556175293544815009471357755819019419359155078512947075831424259049941138231             buy   buy_yes_favorite         0.81      0.820               NaN       0.0       standard                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
1d899cc87ad14dad9b7ba96321c538d0 favorite_longshot_bias 110736410534465414356948717035097625452671622129462925235990458636828550672158             buy   buy_yes_favorite         0.82      0.835               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
b2363c684fb44a879130cb653909d953 favorite_longshot_bias  81690139337095758885065030014592134969111263965619602103558457247319033570523             buy   buy_yes_favorite         0.82      0.835               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
47d0262d9c4744faa28cb20fbb373279 favorite_longshot_bias  51480400198809553033812195396899360038782890842157585260103829390647846379581 buy_no_unmapped  fade_yes_longshot         0.14      0.125               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
5774edcf4c8b4cc0b43a397a1b5d2d94 favorite_longshot_bias  74816278703006137821091581096208461485183419732020348407085188944626016897967             buy   buy_yes_favorite         0.85      0.865               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
2a5a375d7ef84aa19702c6d1bf4777fc favorite_longshot_bias  10687872766195972048120830728022830196595594929036425689073380550668961448444 buy_no_unmapped  fade_yes_longshot         0.07      0.055               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
462c48aaed8547518628297f69a086f5 favorite_longshot_bias  66686559162383907003588692132495076592873723697442321757464590716644259797201             buy   buy_yes_favorite         0.80      0.815               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
d25f34e2482e49afa8088d4c2bddadf8 favorite_longshot_bias  45530349411000941238632218217444112062380366234248978106443901087488156777444             buy   buy_yes_favorite         0.78      0.795               NaN       0.0           deep                      NaN                      NaN rejected zero_liquidity_or_negative_kelly
5bd5ab0acdc54dfe95224dce026ed2b4 favorite_longshot_bias  58238770466755583420851558733211492909154562083056574063409657103994243041405 buy_no_unmapped  fade_yes_longshot         0.11      0.100               NaN       0.0       standard                      NaN                      NaN rejected        requires_no_token_mapping
5ef81a1967e24165ae9bd1b141002e9e favorite_longshot_bias  19111434165204331952645767337361409126785018569794816025396949145846822643714 buy_no_unmapped  fade_yes_longshot         0.09      0.075               NaN       0.0           deep                      NaN                      NaN rejected        requires_no_token_mapping
57cabbcf0a4547668334c14f78500320  data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598             buy buy_yes_data_probe         0.50      0.495               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
3333c8d84616408092f7fb3a6a40c97c  data_collection_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384             buy buy_yes_data_probe         0.58      0.575               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
10a3378611d8435c838468528098559a  data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951             buy buy_yes_data_probe         0.43      0.425               0.0       5.0           deep data-collection-probe-v1 data-collection-probe-v1     open              paper_order_created
```

## Fills

```text
                         fill_id                         order_id              strategy                                                                       token_id side  fill_price  fill_shares  fill_notional_usd  fee_usd  market_impact_slippage paper_fill_mode
3bc550c9ca9f4765a99f9f20487ef119 57cabbcf0a4547668334c14f78500320 data_collection_probe  79939935204329019739688977160933273128770637983122609367510311322486203217598  buy        0.50    10.000000                5.0   0.0750                   0.005  same_run_order
f83115e171fe4cfeb3e7228bad27c116 3333c8d84616408092f7fb3a6a40c97c data_collection_probe   1289553688365886122223508155872029305612490346519178960199078068818266883384  buy        0.58     8.620690                5.0   0.0630                   0.005  same_run_order
bf3633c2a12142e6a0e42b712365d263 10a3378611d8435c838468528098559a data_collection_probe 106023840862016965580036717455926555880264810085768284612278201213463621224951  buy        0.43    11.627907                5.0   0.0855                   0.005  same_run_order
```

## Gate

This remains paper trading only. Live capital should stay disabled until LEV and execution-adjusted ROI are positive over hundreds or thousands of logged fills.
