# QueryTopicReverseRouteTable {#reference_yj1_fjd_xdb .reference}

You can call this operation to query a source topic that is subscribed to by a specified topic. This is known as the reverse route table.

## Request parameters {#section_qdj_wl5_xdb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to QueryTopicReverseRouteTable.|
|Topic|String|Yes|The target topic, which receives messages.|

## Response parameters {#section_aw4_dm5_xdb .section}

|Name|Type|Description |
|:---|:---|:-----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean |Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|
|SrcTopics|List|The list of subscribed \(source\) topics returned when the call is successful.|

## Examples {#section_ok4_4m5_xdb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=QueryTopicReverseRouteTable
 &Topic=%2Fx7aWKW94bb8%2FtestDataToDataHub%2Fupdate
 &<Common request parameters>
```

**Response example**

```
{
    "RequestId":"FCC27691-9151-4B93-9622-9C90F30542EC",
    "Success":true,
    "SrcTopics":["/CXi4***/device1/get","/CXi4***/device4/get"]
}
```

