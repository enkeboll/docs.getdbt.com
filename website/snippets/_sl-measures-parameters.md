| Parameter | Description |
| --- | --- | --- | 
| [`name`](/docs/build/measures#name) | Provide a name for the measure, which must be unique and can't be repeated across all semantic models in your dbt project. | Required | 
| [`description`](/docs/build/measures#description) | Describes the calculated measure. | Optional | 
| [`agg`](/docs/build/measures#description) | dbt supports the following aggregations: `sum`, `max`, `min`, `avg`, `median`, `count_distinct`, and `sum_boolean`. | Required | 
| [`expr`](/docs/build/measures#expr) | Either reference an existing column in the table or use a SQL expression to create or derive a new one. | Optional | 
| [`non_additive_dimension`](/docs/build/measures#non-additive-dimensions) | Non-additive dimensions can be specified for measures that cannot be aggregated over certain dimensions, such as bank account balances, to avoid producing incorrect results. | Optional |
| `agg_params` | Specific aggregation properties such as a percentile. | Optional |
| `agg_time_dimension` | The time field. Defaults to the default agg time dimension for the semantic model.  | Optional | 1.6 and higher |
| `create_metric` | Create a `simple` metric from a measure by setting `create_metric: True`. Specify its display name with `create_metric_display_name`. Available in dbt version 1.7 or higher. | Optional |
