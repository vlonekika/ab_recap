# ab_recap
some ab recap notebooks


## A/B Test Duration Optimization Study

`ab_part1.ipynb`

This research explores the paradoxical relationship between test duration and statistical power in A/B testing. Using real-world streaming platform data, we demonstrate how longer observation periods can unexpectedly reduce test sensitivity despite larger sample sizes. The analysis reveals that extended timeframes introduce behavioral variance from irregular users, ultimately diminishing detection capability for meaningful effects.

Our findings challenge conventional "longer-is-better" testing approaches and provide framework for optimizing experiment duration based on user engagement patterns.


`ab_part2.ipynb`

This notebook systematically evaluates the performance of different statistical approaches on the `cart_added_cnt` metric using historical user data. Key analyses include:

- **Rank Transformation vs Mann-Whitney Test:** applying rank-based t-tests and comparing with non-parametric Mann-Whitney results. Both methods show equivalent p-values for skewed discrete metrics.
- **CUPED Adjustment:** implementing CUPED on original, log-transformed, and rank-transformed metrics. We assess variance reduction, correctness, and t-test power, highlighting the impact of distribution skewness on detectability.
- **Bucketing (Post-Aggregation) Analysis:** evaluating how qcut-based binning affects variance, effective sample size, correctness, and power. Demonstrates limitations of bucketing for discrete metrics with many ties.
- **Post-Stratification:** stratifying by sex and age groups to test for variance reduction and power improvement. Shows minimal effect on discrete metrics with weak correlation to stratifying features.

The study provides practical insights into how transformation, variance reduction, and stratification techniques influence statistical test sensitivity, offering guidance for designing more robust A/B experiments.