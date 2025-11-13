# Metrics

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**distance_to_stop_loss_pct_notional** | **str** | distanceToStopLossUsd expressed as a percentage of notional. | [optional] 
**distance_to_stop_loss_usd** | **str** | The remaining buffer between the current drawdown (drawdownUsd) and the maximum permissible drawdown (drawdownCritValueNotional). | [optional] 
**drawdown_max_pct_notional** | **str** | The drawdown risk limit set as a percentage of notional. | [optional] 
**drawdown_max_usd** | **str** | The maximum permissible drawdown before breaching the drawdown risk limit. | [optional] 
**drawdown_pct_notional** | **str** | drawdownUsd expressed as a percentage of notional. | [optional] 
**drawdown_usd** | **str** | The difference between equity and the risk high water mark. | [optional] 
**equity** | **str** | The current equity capital supporting the notional allocation. | [optional] 
**equity_stop_loss** | **str** | The equity level at which the drawdown risk limit would be breached, calculated as riskHwm - drawdownCritValueNotional. | [optional] 
**gross_exposure_pct_notional** | **str** | grossExposureUsd expressed as a percentage of notional. | [optional] 
**gross_exposure_usd** | **str** | The total dollar value of unsigned notional exposures, calculated as [total notional long] + [total notional short]. | [optional] 
**net_exposure_pct_notional** | **str** | netExposureUsd expressed as a percentage of notional. | [optional] 
**net_exposure_usd** | **str** | The total dollar value of signed notional exposures, calculated as [total notional long] - [total notional short]. | [optional] 
**notional** | **str** | The internal risk allocation, serving as the reference amount for calculating risk limits, exposures, and returns, independent of actual equity. | [optional] 
**pnl_mtd_pct_notional** | **str** | Month-to-date gross return on notional. | [optional] 
**pnl_mtd_usd** | **str** | Month-to-date gross profit. | [optional] 
**pnl_qtd_pct_notional** | **str** | Quarter-to-date gross return on notional. | [optional] 
**pnl_qtd_usd** | **str** | Quarter-to-date gross profit. | [optional] 
**pnl_ytd_pct_notional** | **str** | Year-to-date gross return on notional. | [optional] 
**pnl_ytd_usd** | **str** | Year-to-date gross profit. | [optional] 
**risk_hwm** | **str** | The risk high water mark represents the highest equity level achieved. It is adjusted proportionally for capital movements and serves as the reference point for drawdown calculations. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

