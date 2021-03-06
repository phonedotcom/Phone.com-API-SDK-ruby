# SwaggerClient::PaymentmethodsApi

All URIs are relative to *https://api.phone.com/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_account_payment_method**](PaymentmethodsApi.md#create_account_payment_method) | **POST** /accounts/{account_id}/payment-methods | Create an individual payment method.
[**delete_account_payment_method**](PaymentmethodsApi.md#delete_account_payment_method) | **DELETE** /accounts/{account_id}/payment-methods/{pm_id} | Delete an individual payment method.
[**get_account_payment_method**](PaymentmethodsApi.md#get_account_payment_method) | **GET** /accounts/{account_id}/payment-methods/{pm_id} | Show details of an individual payment method.
[**list_account_payment_methods**](PaymentmethodsApi.md#list_account_payment_methods) | **GET** /accounts/{account_id}/payment-methods | Get a list of payment methods for an account.
[**patch_account_payment_method**](PaymentmethodsApi.md#patch_account_payment_method) | **PATCH** /accounts/{account_id}/payment-methods/{pm_id} | Replace the status of an individual payment method.


# **create_account_payment_method**
> PaymentFull create_account_payment_method(account_id, data)

Create an individual payment method.

Create an individual payment method. See Account Payment Methods for more info on the properties.

### Example
```ruby
# load the gem
require 'swagger_client'
# setup authorization
SwaggerClient.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = SwaggerClient::PaymentmethodsApi.new

account_id = 56 # Integer | Account ID

data = SwaggerClient::CreatePaymentParams.new # CreatePaymentParams | Payment data


begin
  #Create an individual payment method.
  result = api_instance.create_account_payment_method(account_id, data)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PaymentmethodsApi->create_account_payment_method: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **Integer**| Account ID | 
 **data** | [**CreatePaymentParams**](CreatePaymentParams.md)| Payment data | 

### Return type

[**PaymentFull**](PaymentFull.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **delete_account_payment_method**
> DeleteEntry delete_account_payment_method(account_id, pm_id)

Delete an individual payment method.

Delete an individual payment method. See Account Payment Methods for more info on the properties.

### Example
```ruby
# load the gem
require 'swagger_client'
# setup authorization
SwaggerClient.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = SwaggerClient::PaymentmethodsApi.new

account_id = 56 # Integer | Account ID

pm_id = 56 # Integer | Payment Method ID


begin
  #Delete an individual payment method.
  result = api_instance.delete_account_payment_method(account_id, pm_id)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PaymentmethodsApi->delete_account_payment_method: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **Integer**| Account ID | 
 **pm_id** | **Integer**| Payment Method ID | 

### Return type

[**DeleteEntry**](DeleteEntry.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **get_account_payment_method**
> PaymentFull get_account_payment_method(account_id, pm_id)

Show details of an individual payment method.

Show details of an individual payment method. See Account Payment Methods for more info on the properties.

### Example
```ruby
# load the gem
require 'swagger_client'
# setup authorization
SwaggerClient.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = SwaggerClient::PaymentmethodsApi.new

account_id = 56 # Integer | Account ID

pm_id = 56 # Integer | Payment Method ID


begin
  #Show details of an individual payment method.
  result = api_instance.get_account_payment_method(account_id, pm_id)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PaymentmethodsApi->get_account_payment_method: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **Integer**| Account ID | 
 **pm_id** | **Integer**| Payment Method ID | 

### Return type

[**PaymentFull**](PaymentFull.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **list_account_payment_methods**
> ListPaymentMethods list_account_payment_methods(account_id, , opts)

Get a list of payment methods for an account.

Get a list of payment methods for an account. See Account Payment Methods for more info on the properties.

### Example
```ruby
# load the gem
require 'swagger_client'
# setup authorization
SwaggerClient.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = SwaggerClient::PaymentmethodsApi.new

account_id = 56 # Integer | Account ID

opts = { 
  filters_id: ["filters_id_example"], # Array<String> | ID filter
  sort_id: "sort_id_example", # String | ID sorting
  limit: 56, # Integer | Max results
  offset: 56, # Integer | Results to skip
  fields: "fields_example", # String | Field set
}

begin
  #Get a list of payment methods for an account.
  result = api_instance.list_account_payment_methods(account_id, , opts)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PaymentmethodsApi->list_account_payment_methods: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **Integer**| Account ID | 
 **filters_id** | [**Array&lt;String&gt;**](String.md)| ID filter | [optional] 
 **sort_id** | **String**| ID sorting | [optional] 
 **limit** | **Integer**| Max results | [optional] 
 **offset** | **Integer**| Results to skip | [optional] 
 **fields** | **String**| Field set | [optional] 

### Return type

[**ListPaymentMethods**](ListPaymentMethods.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



# **patch_account_payment_method**
> PaymentFull patch_account_payment_method(account_id, pm_id, opts)

Replace the status of an individual payment method.

Replace the status of an individual payment method. See Account Payment Methods for more info on the properties.

### Example
```ruby
# load the gem
require 'swagger_client'
# setup authorization
SwaggerClient.configure do |config|
  # Configure API key authorization: apiKey
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = SwaggerClient::PaymentmethodsApi.new

account_id = 56 # Integer | Account ID

pm_id = 56 # Integer | Payment Method ID

opts = { 
  data: SwaggerClient::PatchPaymentParams.new # PatchPaymentParams | Payment data
}

begin
  #Replace the status of an individual payment method.
  result = api_instance.patch_account_payment_method(account_id, pm_id, opts)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PaymentmethodsApi->patch_account_payment_method: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **Integer**| Account ID | 
 **pm_id** | **Integer**| Payment Method ID | 
 **data** | [**PatchPaymentParams**](PatchPaymentParams.md)| Payment data | [optional] 

### Return type

[**PaymentFull**](PaymentFull.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json



