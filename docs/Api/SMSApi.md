# Swagger\Client\SMSApi

All URIs are relative to *https://api.smsfusion.com.au/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sendSMS**](SMSApi.md#sendSMS) | **GET** /sms/ | Send an SMS


# **sendSMS**
> \Swagger\Client\Model\SMSResult sendSMS($key, $num, $msg, $from, $deliverby, $dlrcb, $replycb, $replyemail, $validity, $cc)

Send an SMS

Send one or more SMS

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');

$api_instance = new Swagger\Client\Api\SMSApi();
$key = "key_example"; // string | API Key as generated from the <a href='https://www.smsfusion.com.au/admin/api/'>admin panel</a>
$num = array("num_example"); // string[] | Comma separated list of phone numbers or <a href='https://www.smsfusion.com.au/help/msisdn/'>MSDISDN</a>'s
$msg = "msg_example"; // string | Message content to send
$from = "from_example"; // string | MSISDN or vanity alphanumeric source number
$deliverby = "deliverby_example"; // string | UTC encoded time to send the SMS
$dlrcb = "dlrcb_example"; // string | HTTP or HTTPS callback URL for delivery reports. Timeout for callbacks is set to 30 seconds
$replycb = "replycb_example"; // string | HTTP or HTTPS callback URL for replies. Timeout for callbacks is set to 30 seconds
$replyemail = "replyemail_example"; // string | Email address to send replies to
$validity = 56; // int | Time in minutes to keep the SMS valid for
$cc = "cc_example"; // string | 2 character country code <a href='https://en.wikipedia.org/wiki/ISO_3166-2'>ISO 3166-2</a> for formatting local numbers internationally

try {
    $result = $api_instance->sendSMS($key, $num, $msg, $from, $deliverby, $dlrcb, $replycb, $replyemail, $validity, $cc);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->sendSMS: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**| API Key as generated from the &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/admin/api/&#39;&gt;admin panel&lt;/a&gt; |
 **num** | [**string[]**](../Model/string.md)| Comma separated list of phone numbers or &lt;a href&#x3D;&#39;https://www.smsfusion.com.au/help/msisdn/&#39;&gt;MSDISDN&lt;/a&gt;&#39;s |
 **msg** | **string**| Message content to send |
 **from** | **string**| MSISDN or vanity alphanumeric source number | [optional]
 **deliverby** | **string**| UTC encoded time to send the SMS | [optional]
 **dlrcb** | **string**| HTTP or HTTPS callback URL for delivery reports. Timeout for callbacks is set to 30 seconds | [optional]
 **replycb** | **string**| HTTP or HTTPS callback URL for replies. Timeout for callbacks is set to 30 seconds | [optional]
 **replyemail** | **string**| Email address to send replies to | [optional]
 **validity** | **int**| Time in minutes to keep the SMS valid for | [optional]
 **cc** | **string**| 2 character country code &lt;a href&#x3D;&#39;https://en.wikipedia.org/wiki/ISO_3166-2&#39;&gt;ISO 3166-2&lt;/a&gt; for formatting local numbers internationally | [optional]

### Return type

[**\Swagger\Client\Model\SMSResult**](../Model/SMSResult.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

