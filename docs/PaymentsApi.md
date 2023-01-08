# \PaymentsApi

All URIs are relative to *https://api.dev.neem.io/neem*

Method | HTTP request | Description
------------- | ------------- | -------------
[**InitiateWalletPayment**](PaymentsApi.md#InitiateWalletPayment) | **Post** /api/v1/wallets/payment-initiate/{walletId} | Make Payments
[**WalletBillInquiry**](PaymentsApi.md#WalletBillInquiry) | **Get** /api/v1/wallets/bill/inquiry/{walletId} | Bill Inquiry
[**WalletBillPayment**](PaymentsApi.md#WalletBillPayment) | **Post** /api/v1/wallets/bill/payment/{walletId} | Bill Payment
[**WalletPaymentInquiry**](PaymentsApi.md#WalletPaymentInquiry) | **Get** /api/v1/wallets/payment-inquiry/{walletId} | Payment Inquiry



## InitiateWalletPayment

> map[string]interface{} InitiateWalletPayment(ctx, walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).Body(body).Execute()

Make Payments

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := int32(56) // int32 | 
    xNeemId := "1234" // string |  (optional)
    xNeemPartnerId := int32(1234) // int32 |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.PaymentsApi.InitiateWalletPayment(context.Background(), walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `PaymentsApi.InitiateWalletPayment``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `InitiateWalletPayment`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `PaymentsApi.InitiateWalletPayment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **int32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiInitiateWalletPaymentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemId** | **string** |  | 
 **xNeemPartnerId** | **int32** |  | 
 **body** | **map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## WalletBillInquiry

> map[string]interface{} WalletBillInquiry(ctx, walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).EndToEndIdentification(endToEndIdentification).ProductId(productId).ConsumerNumber(consumerNumber).Execute()

Bill Inquiry

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    xNeemId := "1234" // string |  (optional)
    xNeemPartnerId := int32(1234) // int32 |  (optional)
    endToEndIdentification := "endToEndIdentification_example" // string |  (optional)
    productId := "productId_example" // string |  (optional)
    consumerNumber := "consumerNumber_example" // string |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.PaymentsApi.WalletBillInquiry(context.Background(), walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).EndToEndIdentification(endToEndIdentification).ProductId(productId).ConsumerNumber(consumerNumber).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `PaymentsApi.WalletBillInquiry``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `WalletBillInquiry`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `PaymentsApi.WalletBillInquiry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiWalletBillInquiryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemId** | **string** |  | 
 **xNeemPartnerId** | **int32** |  | 
 **endToEndIdentification** | **string** |  | 
 **productId** | **string** |  | 
 **consumerNumber** | **string** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## WalletBillPayment

> map[string]interface{} WalletBillPayment(ctx, walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).Body(body).Execute()

Bill Payment

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := int32(56) // int32 | 
    xNeemId := "1234" // string |  (optional)
    xNeemPartnerId := int32(1234) // int32 |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.PaymentsApi.WalletBillPayment(context.Background(), walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `PaymentsApi.WalletBillPayment``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `WalletBillPayment`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `PaymentsApi.WalletBillPayment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **int32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiWalletBillPaymentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemId** | **string** |  | 
 **xNeemPartnerId** | **int32** |  | 
 **body** | **map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## WalletPaymentInquiry

> map[string]interface{} WalletPaymentInquiry(ctx, walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).EndToEndIdentification(endToEndIdentification).PaymentScheme(paymentScheme).Amount(amount).Currency(currency).CreditorIdentification(creditorIdentification).CreditorName(creditorName).CreditorInstitutionIdentification(creditorInstitutionIdentification).CreditorSecondaryIdentification(creditorSecondaryIdentification).ExtendedProperties(extendedProperties).Execute()

Payment Inquiry

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    xNeemId := "1234" // string |  (optional)
    xNeemPartnerId := int32(1234) // int32 |  (optional)
    endToEndIdentification := "endToEndIdentification_example" // string |  (optional)
    paymentScheme := "paymentScheme_example" // string |  (optional)
    amount := "amount_example" // string |  (optional)
    currency := "currency_example" // string |  (optional)
    creditorIdentification := "creditorIdentification_example" // string |  (optional)
    creditorName := "creditorName_example" // string |  (optional)
    creditorInstitutionIdentification := "creditorInstitutionIdentification_example" // string |  (optional)
    creditorSecondaryIdentification := "creditorSecondaryIdentification_example" // string |  (optional)
    extendedProperties := []map[string]interface{}{map[string]interface{}(123)} // []map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.PaymentsApi.WalletPaymentInquiry(context.Background(), walletId).XNeemId(xNeemId).XNeemPartnerId(xNeemPartnerId).EndToEndIdentification(endToEndIdentification).PaymentScheme(paymentScheme).Amount(amount).Currency(currency).CreditorIdentification(creditorIdentification).CreditorName(creditorName).CreditorInstitutionIdentification(creditorInstitutionIdentification).CreditorSecondaryIdentification(creditorSecondaryIdentification).ExtendedProperties(extendedProperties).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `PaymentsApi.WalletPaymentInquiry``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `WalletPaymentInquiry`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `PaymentsApi.WalletPaymentInquiry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiWalletPaymentInquiryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemId** | **string** |  | 
 **xNeemPartnerId** | **int32** |  | 
 **endToEndIdentification** | **string** |  | 
 **paymentScheme** | **string** |  | 
 **amount** | **string** |  | 
 **currency** | **string** |  | 
 **creditorIdentification** | **string** |  | 
 **creditorName** | **string** |  | 
 **creditorInstitutionIdentification** | **string** |  | 
 **creditorSecondaryIdentification** | **string** |  | 
 **extendedProperties** | **[]map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

