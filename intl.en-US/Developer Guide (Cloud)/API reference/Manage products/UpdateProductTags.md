# UpdateProductTags {#reference_kw5_zrk_3gb .reference}

You can call this operation to update product tags.

## Restriction {#section_tx4_csk_3gb .section}

You can update a maximum of 10 tags each time you call this operation.

## Request parameters {#section_pqr_fsk_3gb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to UpdateProductTags.|
|ProductKey|String|Yes|The unique identifier of the product.|
|ProductTags|List<String\>|Yes|The tags that you want to update. A tag consists of a TagKey and a TagValue, which correspond to the key and value of the tag respectively. For more information, see the table [ProductInfo](#).**Note:** 

-   The TagKey must be unique.
-   The TagKey must already exists.

|
|Common request parameters|-|Yes|See [Common parameters](reseller.en-US/Developer Guide (Cloud)/API reference/Common parameters.md#).|

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|TagKey|String|Yes|The key of the tag.|
|TagValue|String|Yes|The value of the tag, which can contain Chinese characters, English letters, numbers, hyphens \(-\), underscores \(\_\), and dots \(.\), and cannot exceed 128 characters. A Chinese character is counted as two characters.|

## Response parameters {#section_hwv_5kk_3gb .section}

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|
|Code|String|The error code returned when the call fails. For more information about error codes, see [Error codes](reseller.en-US/Developer Guide (Cloud)/API reference/Error codes.md#).|
|InvalidProductTags|List<String\>|The invalid tags returned when the call fails.|

## Examples {#section_jyb_zqk_3gb .section}

**Sample request**

```
https://iot.cn-shanghai.aliyuncs.com/&Action=UpdateProductTags
&ProductKey=a1h7knJdld1
&ProductTag. 1. TagKey=first
&ProductTag. 1. TagValue=value1
&ProductTag. 2. TagKey=second
&ProductTag. 2. TagValue=value2
&Common request parameters
```

**Sample responses**

JSON format

```
{
  "RequestId": "92586B4B-FF78-494A-A22C-368E4293FBB7",
  "Success": true
}
```

XML format

```
<UpdateProductTagsResponse>
    <RequestId>57b144cf-09fc-4916-a272-a62902d5b207</RequestId>
    <Success>true</Success>
</UpdateProductTagsResponse>
```
