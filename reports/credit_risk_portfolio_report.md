
# Portfolio Risk Report

The analyzed portfolio contains 1,000 borrowers and a total exposure proxy of 3,271,258.00.

The average predicted probability of default is 43.19%, while the observed default rate is 30.00%. Using an assumed LGD of 45%, the portfolio expected loss proxy is 732,747.35, equivalent to an expected loss rate proxy of 22.40%.

The largest expected loss contribution by supervised risk band comes from `high_risk`, which represents 64.65% of total expected loss proxy. The largest expected loss contribution by unsupervised segment comes from cluster `1`, which represents 69.36% of total expected loss proxy.

Anomalous borrower profiles represent 5.00% of the portfolio and account for 18.05% of expected loss proxy. The top 20 borrowers by expected loss proxy account for 14.96% of total expected loss proxy.

These results suggest that portfolio risk should be monitored through multiple lenses: predicted PD, exposure concentration, unsupervised risk clusters, and anomaly detection.


## Portfolio KPIs

| metric                    |            value |
|:--------------------------|-----------------:|
| number_of_borrowers       |   1000           |
| total_exposure_proxy      |      3.27126e+06 |
| average_exposure_proxy    |   3271.26        |
| average_predicted_pd      |      0.431864    |
| median_predicted_pd       |      0.400035    |
| observed_default_rate     |      0.3         |
| total_expected_loss_proxy | 732747           |
| expected_loss_rate_proxy  |      0.223996    |
| anomaly_rate              |      0.05        |
| exposure_hhi_by_borrower  |      0.00174384  |

## Risk Band Summary

| risk_band     |   borrowers |   observed_defaults |   observed_default_rate |   avg_predicted_pd |   median_predicted_pd |   exposure_proxy |   avg_exposure_proxy |   expected_loss_proxy |   anomaly_rate |   borrower_share |   exposure_share |   expected_loss_share |
|:--------------|------------:|--------------------:|------------------------:|-------------------:|----------------------:|-----------------:|---------------------:|----------------------:|---------------:|-----------------:|-----------------:|----------------------:|
| high_risk     |         322 |                 201 |               0.624224  |           0.785852 |             0.790463  |      1.30006e+06 |              4037.44 |              473755   |      0.0962733 |            0.322 |         0.397417 |             0.646546  |
| elevated_risk |         178 |                  58 |               0.325843  |           0.50268  |             0.503337  | 647615           |              3638.29 |              149564   |      0.0505618 |            0.178 |         0.197971 |             0.204114  |
| moderate_risk |         198 |                  26 |               0.131313  |           0.300811 |             0.309312  | 546772           |              2761.47 |               74844.4 |      0.030303  |            0.198 |         0.167144 |             0.102142  |
| low_risk      |         302 |                  15 |               0.0496689 |           0.098616 |             0.0963327 | 776816           |              2572.24 |               34584.1 |      0.013245  |            0.302 |         0.237467 |             0.0471979 |

## Cluster Summary

|   risk_cluster |   borrowers |   observed_defaults |   observed_default_rate |   avg_predicted_pd |   median_predicted_pd |   exposure_proxy |   avg_exposure_proxy |   expected_loss_proxy |   anomaly_rate |   avg_anomaly_score |   avg_duration_months |   avg_age |   borrower_share |   exposure_share |   expected_loss_share |
|---------------:|------------:|--------------------:|------------------------:|-------------------:|----------------------:|-----------------:|---------------------:|----------------------:|---------------:|--------------------:|----------------------:|----------:|-----------------:|-----------------:|----------------------:|
|              1 |         282 |                 120 |                0.425532 |           0.56244  |              0.590103 |      1.91397e+06 |              6787.12 |                508267 |      0.134752  |            0.246252 |               33.5461 |   36.1418 |            0.282 |         0.585087 |              0.693645 |
|              0 |         718 |                 180 |                0.250696 |           0.380579 |              0.334094 |      1.35729e+06 |              1890.37 |                224481 |      0.0167131 |            0.156719 |               15.9373 |   35.312  |            0.718 |         0.414913 |              0.306355 |

## Monitoring Flags

| flag                  |   borrowers |   borrower_share |   expected_loss_share |
|:----------------------|------------:|-----------------:|----------------------:|
| high_pd_high_exposure |         102 |            0.102 |              0.416035 |
| high_expected_loss    |         100 |            0.1   |              0.448718 |
| anomalous_elevated_pd |          28 |            0.028 |              0.129683 |