# Swagger\Client\ProductsApi

All URIs are relative to *https://api-sandbox.netshoes.com.br/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getProductBySku**](ProductsApi.md#getProductBySku) | **GET** /products/{sku} | Get product by sku
[**getProducts**](ProductsApi.md#getProducts) | **GET** /products | Get list of products
[**getStatusProductBySku**](ProductsApi.md#getStatusProductBySku) | **GET** /products/{sku}/status | Get product status
[**saveProduct**](ProductsApi.md#saveProduct) | **POST** /products | Create a new product.
[**updateProduct**](ProductsApi.md#updateProduct) | **PUT** /products/{sku} | Update a product.
[**updateProductStatusBySku**](ProductsApi.md#updateProductStatusBySku) | **PUT** /products/{sku}/status | Update product status. Only sandbox


# **getProductBySku**
> \Swagger\Client\Model\InlineResponse200Items getProductBySku($client_id, $access_token, $sku, $expands)

Get product by sku

Returns the product associated with the searched sku.

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$expands = "expands_example"; // string | Expand response relationships, for instance if you need to access product images use 'images', to access product attributes use 'attributes' and to access images and attributes use 'images,attributes'.

try {
    $result = $api_instance->getProductBySku($client_id, $access_token, $sku, $expands);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->getProductBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **expands** | **string**| Expand response relationships, for instance if you need to access product images use &#39;images&#39;, to access product attributes use &#39;attributes&#39; and to access images and attributes use &#39;images,attributes&#39;. | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200Items**](../Model/InlineResponse200Items.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProducts**
> \Swagger\Client\Model\InlineResponse200 getProducts($client_id, $access_token, $page, $size, $expands)

Get list of products

Returns all products associated to the seller.

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$page = 0; // int | Number of the page in pagination. The starting page number is zero.
$size = 20; // int | Define the size of the returned list of products.
$expands = "expands_example"; // string | Expand response relationships, for instance if you need to access product images use 'images', to access product attributes use 'attributes' and to access images and attributes use 'images,attributes'.

try {
    $result = $api_instance->getProducts($client_id, $access_token, $page, $size, $expands);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->getProducts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **page** | **int**| Number of the page in pagination. The starting page number is zero. | [optional] [default to 0]
 **size** | **int**| Define the size of the returned list of products. | [optional] [default to 20]
 **expands** | **string**| Expand response relationships, for instance if you need to access product images use &#39;images&#39;, to access product attributes use &#39;attributes&#39; and to access images and attributes use &#39;images,attributes&#39;. | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStatusProductBySku**
> \Swagger\Client\Model\InlineResponse2001 getStatusProductBySku($client_id, $access_token, $sku)

Get product status

Returns the current status of a product.

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku

try {
    $result = $api_instance->getStatusProductBySku($client_id, $access_token, $sku);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->getStatusProductBySku: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **saveProduct**
> saveProduct($client_id, $access_token, $body)

Create a new product.

Creates a new product. Cannot set flavor and color on the same product

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$body = new \Swagger\Client\Model\Body(); // \Swagger\Client\Model\Body | Product json to create a new product.

try {
    $api_instance->saveProduct($client_id, $access_token, $body);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->saveProduct: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **body** | [**\Swagger\Client\Model\Body**](../Model/\Swagger\Client\Model\Body.md)| Product json to create a new product. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateProduct**
> updateProduct($client_id, $access_token, $sku, $body)

Update a product.

Updates a product. Cannot set flavor and color on the same product

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body1(); // \Swagger\Client\Model\Body1 | Product json to create a new product.

try {
    $api_instance->updateProduct($client_id, $access_token, $sku, $body);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->updateProduct: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body1**](../Model/\Swagger\Client\Model\Body1.md)| Product json to create a new product. |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateProductStatusBySku**
> \Swagger\Client\Model\InlineResponse2001 updateProductStatusBySku($client_id, $access_token, $sku, $body)

Update product status. Only sandbox

Update product status for Sandbox operations

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

$api_instance = new Swagger\Client\Api\ProductsApi();
$client_id = "client_id_example"; // string | The APP Token used to authenticate.
$access_token = "access_token_example"; // string | The Access Token used to authenticate.
$sku = "sku_example"; // string | Product's Sku
$body = new \Swagger\Client\Model\Body2(); // \Swagger\Client\Model\Body2 | Json to update status.

try {
    $result = $api_instance->updateProductStatusBySku($client_id, $access_token, $sku, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->updateProductStatusBySku: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **string**| The APP Token used to authenticate. |
 **access_token** | **string**| The Access Token used to authenticate. |
 **sku** | **string**| Product&#39;s Sku |
 **body** | [**\Swagger\Client\Model\Body2**](../Model/\Swagger\Client\Model\Body2.md)| Json to update status. |

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[access_token](../../README.md#access_token), [client_id](../../README.md#client_id)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

