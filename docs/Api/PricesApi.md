# Swagger\Client\PricesApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPriceProductBySku**](PricesApi.md#getPriceProductBySku) | **GET** /products/{sku}/prices | Get price of the product
[**savePriceProductBySku**](PricesApi.md#savePriceProductBySku) | **POST** /products/{sku}/prices | Save a newly created price of the product
[**updatePriceProductBySku**](PricesApi.md#updatePriceProductBySku) | **PUT** /products/{sku}/prices | Update price of the product


# **getPriceProductBySku**
> \Swagger\Client\Model\InlineResponse2002 getPriceProductBySku($client_id, $access_token, $sku)

Get price of the product

Returns the current list and sale prices of the searched product.

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

$api_instance = new Swagger\Client\Api\PricesApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku

try {
    $result = $api_instance->getPriceProductBySku($client_id, $access_token, $sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PricesApi->getPriceProductBySku: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **savePriceProductBySku**
> savePriceProductBySku($client_id, $access_token, $sku, $body)

Save a newly created price of the product

Saves a new list and/or sale price of a product with no previous price set.

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

$api_instance = new Swagger\Client\Api\PricesApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body4(); // \Swagger\Client\Model\Body4 | Json to send a price value.

try {
    $api_instance->savePriceProductBySku($client_id, $access_token, $sku, $body);
} catch (Exception $e) {
    echo 'Exception when calling PricesApi->savePriceProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body4**](../Model/\Swagger\Client\Model\Body4.md)| Json to send a price value. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updatePriceProductBySku**
> updatePriceProductBySku($client_id, $access_token, $sku, $body)

Update price of the product

Updates the list and/or sale price of the product.

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

$api_instance = new Swagger\Client\Api\PricesApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body3(); // \Swagger\Client\Model\Body3 | Json to send a price value.

try {
    $api_instance->updatePriceProductBySku($client_id, $access_token, $sku, $body);
} catch (Exception $e) {
    echo 'Exception when calling PricesApi->updatePriceProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body3**](../Model/\Swagger\Client\Model\Body3.md)| Json to send a price value. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

