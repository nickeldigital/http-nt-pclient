# http_nt_pclient.GeneralApi

All URIs are relative to *NT_URL*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exchanges**](GeneralApi.md#exchanges) | **GET** /v1/exchanges/{site} | List exchanges for {site}.
[**exposures**](GeneralApi.md#exposures) | **GET** /v1/exposures | List exposures.
[**exposures_for_account**](GeneralApi.md#exposures_for_account) | **GET** /v1/exposures/{accountId} | List exposures for {accountId}.
[**fills**](GeneralApi.md#fills) | **GET** /v1/fills | List fills.
[**instruments**](GeneralApi.md#instruments) | **GET** /v1/instruments/{site}/{exchange} | List instruments for {site} and {exchange}.
[**limits**](GeneralApi.md#limits) | **GET** /v1/limits/{site}/{exchange}/{accountId} | Retrieve account limits for {accountId} on {site} and {exchange}.
[**positions**](GeneralApi.md#positions) | **GET** /v1/positions | List positions.
[**positions_for_account**](GeneralApi.md#positions_for_account) | **GET** /v1/positions/{accountId} | List positions for {accountId}.
[**risk**](GeneralApi.md#risk) | **GET** /v1/risk | Retrieve risk metrics.
[**sites**](GeneralApi.md#sites) | **GET** /v1/sites | List available Nickel Trader sites.

# **exchanges**
> list[str] exchanges(site)

List exchanges for {site}.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    site = 'site_example' # str | Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites). 
    try:
        # List exchanges for {site}.
        api_response = await api_instance.exchanges(site)
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->exchanges: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **site** | **str**| Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites).  | 

### Return type

**list[str]**

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exposures**
> list[ExposureDTO] exposures()

List exposures.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    try:
        # List exposures.
        api_response = await api_instance.exposures()
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->exposures: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ExposureDTO]**](ExposureDTO.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **exposures_for_account**
> list[ExposureDTO] exposures_for_account(account_id)

List exposures for {accountId}.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    account_id = 'account_id_example' # str | An exchange account id
    try:
        # List exposures for {accountId}.
        api_response = await api_instance.exposures_for_account(account_id)
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->exposures_for_account: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| An exchange account id | 

### Return type

[**list[ExposureDTO]**](ExposureDTO.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **fills**
> list[Trade] fills()

List fills.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    try:
        # List fills.
        api_response = await api_instance.fills()
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->fills: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Trade]**](Trade.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instruments**
> list[InstrumentSpecification] instruments(site, exchange)

List instruments for {site} and {exchange}.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    site = 'site_example' # str | Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites). 
    exchange = 'exchange_example' # str | Exchange, see [/v1/exchanges](#/General/exchanges)
    try:
        # List instruments for {site} and {exchange}.
        api_response = await api_instance.instruments(site, exchange)
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->instruments: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **site** | **str**| Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites).  | 
 **exchange** | **str**| Exchange, see [/v1/exchanges](#/General/exchanges) | 

### Return type

[**list[InstrumentSpecification]**](InstrumentSpecification.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **limits**
> list[LimitResponse] limits(site, exchange, account_id)

Retrieve account limits for {accountId} on {site} and {exchange}.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    site = 'site_example' # str | Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites). 
    exchange = 'exchange_example' # str | Exchange, see [/v1/exchanges](#/General/exchanges)
    account_id = 'account_id_example' # str | An exchange account id
    try:
        # Retrieve account limits for {accountId} on {site} and {exchange}.
        api_response = await api_instance.limits(site, exchange, account_id)
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->limits: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **site** | **str**| Instance of Nickel Trader used for the execution. One or more can be available. For the list of available sites, query [/v1/sites](#/General/sites).  | 
 **exchange** | **str**| Exchange, see [/v1/exchanges](#/General/exchanges) | 
 **account_id** | **str**| An exchange account id | 

### Return type

[**list[LimitResponse]**](LimitResponse.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **positions**
> list[PositionDTOV2] positions()

List positions.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    try:
        # List positions.
        api_response = await api_instance.positions()
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->positions: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[PositionDTOV2]**](PositionDTOV2.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **positions_for_account**
> list[PositionDTOV2] positions_for_account(account_id)

List positions for {accountId}.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    account_id = 'account_id_example' # str | An exchange account id
    try:
        # List positions for {accountId}.
        api_response = await api_instance.positions_for_account(account_id)
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->positions_for_account: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| An exchange account id | 

### Return type

[**list[PositionDTOV2]**](PositionDTOV2.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **risk**
> RiskResponse risk()

Retrieve risk metrics.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    try:
        # Retrieve risk metrics.
        api_response = await api_instance.risk()
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->risk: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RiskResponse**](RiskResponse.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sites**
> Sites sites()

List available Nickel Trader sites.

### Example
```python
import asyncio
import http_nt_pclient
from http_nt_pclient.rest import ApiException
from pprint import pprint

async def main():
    # Configure HTTP basic authorization: basicAuth
    api_instance = http_nt_pclient.GeneralApi()
    api_instance.api_client.configuration.username = 'API_KEY'
    api_instance.api_client.configuration.password = 'API_SECRET'
    api_instance.api_client.configuration.host = 'NT_URL'
    try:
        # List available Nickel Trader sites.
        api_response = await api_instance.sites()
        pprint(api_response)
    except ApiException as e:
        print(f"Exception when calling GeneralApi->sites: {e}\n")
    finally:
        # Explicitly close the session
        await api_instance.api_client.rest_client.pool_manager.close()

if __name__ == '__main__':
    asyncio.run(main())
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Sites**](Sites.md)

### Authorization

[basicAuth](../README.md#basicAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

