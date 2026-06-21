
# Stress Testing Report

The base scenario estimates total expected loss at 732,747.35, equivalent to an expected loss rate of 22.40%.

Under the adverse scenario, total expected loss rises to 1,182,948.50, representing a multiplier of 1.61 times the base expected loss.

Under the severe scenario, total expected loss rises to 1,564,056.07, equivalent to an expected loss rate of 45.54%. This represents a multiplier of 2.13 times the base expected loss.

In the severe scenario, the largest cluster-level contribution to expected loss comes from risk cluster `1`, with an expected loss share of 67.96%. The largest risk-band contribution comes from `high_risk`, with an expected loss share of 56.73%.

These results indicate that the portfolio should be monitored through both broad credit deterioration assumptions and targeted deterioration in high-risk segments, anomalous profiles, and high-exposure borrowers.


## Stress Scenarios

| scenario       |   pd_multiplier |   lgd |   ead_multiplier |   high_risk_band_pd_addon |   high_risk_cluster_pd_addon |   anomaly_pd_addon | description                                                               |
|:---------------|----------------:|------:|-----------------:|--------------------------:|-----------------------------:|-------------------:|:--------------------------------------------------------------------------|
| base           |            1    |  0.45 |             1    |                      0    |                         0    |               0    | Current model estimate with base LGD assumption.                          |
| mild_stress    |            1.15 |  0.5  |             1    |                      0.02 |                         0.01 |               0.01 | Moderate deterioration in borrower risk and recovery assumptions.         |
| adverse_stress |            1.3  |  0.55 |             1.03 |                      0.05 |                         0.03 |               0.03 | Adverse credit environment with stronger deterioration in risky profiles. |
| severe_stress  |            1.55 |  0.65 |             1.05 |                      0.08 |                         0.05 |               0.05 | Severe stress with broad PD deterioration and higher loss severity.       |

## Portfolio Stress Summary

| scenario       | description                                                               |   total_ead |   average_pd |   median_pd |   lgd |   total_expected_loss |   expected_loss_rate |   expected_loss_increase_vs_base |   expected_loss_multiplier_vs_base |
|:---------------|:--------------------------------------------------------------------------|------------:|-------------:|------------:|------:|----------------------:|---------------------:|---------------------------------:|-----------------------------------:|
| base           | Current model estimate with base LGD assumption.                          | 3.27126e+06 |     0.431864 |    0.400035 |  0.45 |      732747           |             0.223996 |                                0 |                            1       |
| mild_stress    | Moderate deterioration in borrower risk and recovery assumptions.         | 3.27126e+06 |     0.501633 |    0.474524 |  0.5  |      941249           |             0.287733 |                           208502 |                            1.28455 |
| adverse_stress | Adverse credit environment with stronger deterioration in risky profiles. | 3.3694e+06  |     0.559323 |    0.56881  |  0.55 |           1.18295e+06 |             0.351086 |                           450201 |                            1.6144  |
| severe_stress  | Severe stress with broad PD deterioration and higher loss severity.       | 3.43482e+06 |     0.620917 |    0.702619 |  0.65 |           1.56406e+06 |             0.455353 |                           831309 |                            2.13451 |

## Risk Band Stress Summary

| risk_band     |   borrowers |        total_ead |   avg_pd |   total_expected_loss |   observed_default_rate | scenario       |   expected_loss_share |   ead_share |
|:--------------|------------:|-----------------:|---------:|----------------------:|------------------------:|:---------------|----------------------:|------------:|
| elevated_risk |         178 | 647615           | 0.50268  |              149564   |               0.325843  | base           |             0.204114  |    0.197971 |
| high_risk     |         322 |      1.30006e+06 | 0.785852 |              473755   |               0.624224  | base           |             0.646546  |    0.397417 |
| low_risk      |         302 | 776816           | 0.098616 |               34584.1 |               0.0496689 | base           |             0.0471979 |    0.237467 |
| moderate_risk |         198 | 546772           | 0.300811 |               74844.4 |               0.131313  | base           |             0.102142  |    0.167144 |
| elevated_risk |         178 | 647615           | 0.601733 |              200103   |               0.325843  | mild_stress    |             0.212593  |    0.197971 |
| high_risk     |         322 |      1.30006e+06 | 0.903075 |              598470   |               0.624224  | mild_stress    |             0.635825  |    0.397417 |
| low_risk      |         302 | 776816           | 0.115097 |               45593.2 |               0.0496689 | mild_stress    |             0.048439  |    0.237467 |
| moderate_risk |         198 | 546772           | 0.348356 |               97084   |               0.131313  | mild_stress    |             0.103144  |    0.167144 |
| elevated_risk |         178 | 667043           | 0.714439 |              271669   |               0.325843  | adverse_stress |             0.229654  |    0.197971 |
| high_risk     |         322 |      1.33906e+06 | 0.972167 |              722501   |               0.624224  | adverse_stress |             0.610763  |    0.397417 |
| low_risk      |         302 | 800120           | 0.133267 |               61365.3 |               0.0496689 | adverse_stress |             0.0518749 |    0.237467 |
| moderate_risk |         198 | 563175           | 0.398326 |              127414   |               0.131313  | adverse_stress |             0.107709  |    0.167144 |
| elevated_risk |         178 | 679996           | 0.873515 |              400057   |               0.325843  | severe_stress  |             0.255782  |    0.197971 |
| high_risk     |         322 |      1.36506e+06 | 1        |              887288   |               0.624224  | severe_stress  |             0.567299  |    0.397417 |
| low_risk      |         302 | 815657           | 0.161298 |               90872.3 |               0.0496689 | severe_stress  |             0.0581004 |    0.237467 |
| moderate_risk |         198 | 574111           | 0.478378 |              185839   |               0.131313  | severe_stress  |             0.118819  |    0.167144 |

## Cluster Stress Summary

|   risk_cluster |   borrowers |   total_ead |   avg_pd |   total_expected_loss |   observed_default_rate |   anomaly_rate | scenario       |   expected_loss_share |   ead_share |
|---------------:|------------:|------------:|---------:|----------------------:|------------------------:|---------------:|:---------------|----------------------:|------------:|
|              0 |         718 | 1.35729e+06 | 0.380579 |       224481          |                0.250696 |      0.0167131 | base           |              0.306355 |    0.414913 |
|              1 |         282 | 1.91397e+06 | 0.56244  |       508267          |                0.425532 |      0.134752  | base           |              0.693645 |    0.585087 |
|              0 |         718 | 1.35729e+06 | 0.442545 |       290403          |                0.250696 |      0.0167131 | mild_stress    |              0.308529 |    0.414913 |
|              1 |         282 | 1.91397e+06 | 0.652077 |       650846          |                0.425532 |      0.134752  | mild_stress    |              0.691471 |    0.585087 |
|              0 |         718 | 1.39801e+06 | 0.494767 |       369075          |                0.250696 |      0.0167131 | adverse_stress |              0.311995 |    0.414913 |
|              1 |         282 | 1.97139e+06 | 0.723688 |       813874          |                0.425532 |      0.134752  | adverse_stress |              0.688005 |    0.585087 |
|              0 |         718 | 1.42515e+06 | 0.55591  |       501153          |                0.250696 |      0.0167131 | severe_stress  |              0.320419 |    0.414913 |
|              1 |         282 | 2.00967e+06 | 0.78643  |            1.0629e+06 |                0.425532 |      0.134752  | severe_stress  |              0.679581 |    0.585087 |

## Top Severe Stress Borrowers

|     |   actual_default | risk_band     |   risk_cluster |   ensemble_anomaly_flag |   credit_amount |   duration_months |   age_years |   base_pd |   severe_pd |   base_expected_loss |   severe_expected_loss |
|----:|-----------------:|:--------------|---------------:|------------------------:|----------------:|------------------:|------------:|----------:|------------:|---------------------:|-----------------------:|
| 915 |                1 | high_risk     |              1 |                       1 |           18424 |                48 |          32 |  0.648542 |    1        |              5376.93 |               12574.4  |
|  95 |                1 | high_risk     |              1 |                       1 |           15945 |                54 |          58 |  0.989257 |    1        |              7098.17 |               10882.5  |
| 818 |                0 | high_risk     |              1 |                       1 |           15857 |                36 |          43 |  0.956704 |    1        |              6826.71 |               10822.4  |
| 887 |                1 | high_risk     |              1 |                       0 |           15672 |                48 |          23 |  0.797578 |    1        |              5624.84 |               10696.1  |
| 917 |                1 | high_risk     |              1 |                       1 |           14896 |                 6 |          68 |  0.998459 |    1        |              6692.87 |               10166.5  |
| 374 |                1 | high_risk     |              1 |                       1 |           14782 |                60 |          60 |  0.975232 |    1        |              6487.14 |               10088.7  |
| 236 |                1 | high_risk     |              1 |                       1 |           14555 |                 6 |          23 |  0.957341 |    1        |              6270.34 |                9933.79 |
|  63 |                1 | high_risk     |              1 |                       0 |           14421 |                48 |          25 |  0.883607 |    1        |              5734.12 |                9842.33 |
| 378 |                1 | high_risk     |              1 |                       1 |           14318 |                36 |          57 |  0.970408 |    1        |              6252.44 |                9772.04 |
| 744 |                0 | elevated_risk |              1 |                       1 |           14179 |                39 |          30 |  0.568885 |    1        |              3629.8  |                9677.17 |
| 714 |                1 | high_risk     |              1 |                       0 |           14027 |                60 |          27 |  0.971069 |    1        |              6129.53 |                9573.43 |
| 637 |                0 | elevated_risk |              1 |                       0 |           15653 |                60 |          21 |  0.493764 |    0.895334 |              3478    |                9565.01 |
| 373 |                0 | elevated_risk |              1 |                       1 |           13756 |                60 |          63 |  0.559897 |    1        |              3465.88 |                9388.47 |
| 381 |                1 | high_risk     |              1 |                       1 |           12976 |                18 |          38 |  0.804642 |    1        |              4698.46 |                8856.12 |
|  87 |                1 | high_risk     |              1 |                       1 |           12612 |                36 |          47 |  0.828142 |    1        |              4700.04 |                8607.69 |
|  18 |                1 | high_risk     |              1 |                       1 |           12579 |                24 |          44 |  0.858046 |    1        |              4857.01 |                8585.17 |
| 615 |                0 | high_risk     |              1 |                       1 |           12204 |                48 |          48 |  0.772545 |    1        |              4242.66 |                8329.23 |
| 272 |                0 | high_risk     |              1 |                       1 |           12169 |                48 |          36 |  0.909605 |    1        |              4981.04 |                8305.34 |
| 274 |                1 | high_risk     |              1 |                       0 |           11998 |                30 |          34 |  0.97017  |    1        |              5238.04 |                8188.64 |
| 105 |                1 | elevated_risk |              1 |                       1 |           11938 |                24 |          39 |  0.538894 |    1        |              2894.99 |                8147.69 |
| 832 |                1 | high_risk     |              1 |                       0 |           11816 |                45 |          29 |  0.945908 |    1        |              5029.58 |                8064.42 |
| 395 |                0 | high_risk     |              1 |                       0 |           11760 |                39 |          32 |  0.865624 |    1        |              4580.88 |                8026.2  |
| 333 |                1 | elevated_risk |              1 |                       1 |           11590 |                48 |          24 |  0.567338 |    1        |              2958.95 |                7910.18 |
| 736 |                1 | high_risk     |              1 |                       0 |           11560 |                24 |          23 |  0.738149 |    1        |              3839.85 |                7889.7  |
| 763 |                1 | elevated_risk |              1 |                       1 |           12680 |                21 |          30 |  0.461954 |    0.896028 |              2635.91 |                7754.32 |