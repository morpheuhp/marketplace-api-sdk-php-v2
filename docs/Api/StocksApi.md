# Swagger\Client\StocksApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStockProductBySku**](StocksApi.md#getStockProductBySku) | **GET** /products/{sku}/stocks | Get stock of the product
[**saveStockProductBySku**](StocksApi.md#saveStockProductBySku) | **POST** /products/{sku}/stocks | Save a newly created stock quantity of the product
[**updateStockProductBySku**](StocksApi.md#updateStockProductBySku) | **PUT** /products/{sku}/stocks | Update stock of the product


# **getStockProductBySku**
> \Swagger\Client\Model\InlineResponse2003 getStockProductBySku($client_id, $access_token, $sku)

Get stock of the product

Returns the current stock quantity of the product.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');
// Configure API key authorization: client_id
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('client_id', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('client_id', 'Bearer');

$api_instance = new Swagger\Client\Api\StocksApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku

try {
    $result = $api_instance->getStockProductBySku($client_id, $access_token, $sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StocksApi->getStockProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |

### Return type

[**\Swagger\Client\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **saveStockProductBySku**
> saveStockProductBySku($client_id, $access_token, $sku, $body)

Save a newly created stock quantity of the product

Saves a new stock quantity of a product with no previous stock set.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');
// Configure API key authorization: client_id
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('client_id', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('client_id', 'Bearer');

$api_instance = new Swagger\Client\Api\StocksApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body6(); // \Swagger\Client\Model\Body6 | Json to send a stock quantity.

try {
    $api_instance->saveStockProductBySku($client_id, $access_token, $sku, $body);
} catch (Exception $e) {
    echo 'Exception when calling StocksApi->saveStockProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body6**](../Model/\Swagger\Client\Model\Body6.md)| Json to send a stock quantity. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateStockProductBySku**
> updateStockProductBySku($client_id, $access_token, $sku, $body)

Update stock of the product

Updates the stock quantity of the product.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: access_token
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');
// Configure API key authorization: client_id
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('client_id', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('client_id', 'Bearer');

$api_instance = new Swagger\Client\Api\StocksApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body5(); // \Swagger\Client\Model\Body5 | Json to send a stock quantity.

try {
    $api_instance->updateStockProductBySku($client_id, $access_token, $sku, $body);
} catch (Exception $e) {
    echo 'Exception when calling StocksApi->updateStockProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body5**](../Model/\Swagger\Client\Model\Body5.md)| Json to send a stock quantity. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

