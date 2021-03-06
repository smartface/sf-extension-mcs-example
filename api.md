<a name="MCS"></a>

## MCS
Creates new instace of MCS

**Kind**: global class  

* [MCS](#MCS)
    * [new MCS(options)](#new_MCS_new)
    * _instance_
        * [.autoFlushEventsStarted](#MCS+autoFlushEventsStarted)
        * [.setAuthorization(options)](#MCS+setAuthorization)
        * [.login(options, callback)](#MCS+login)
        * [.logout()](#MCS+logout)
        * [.registerDeviceToken(options, callback)](#MCS+registerDeviceToken)
        * [.deregisterDeviceToken(options, callback)](#MCS+deregisterDeviceToken)
        * [.sendAnalytic(options, [callback])](#MCS+sendAnalytic)
        * [.sendBasicEvent(eventName, [callback])](#MCS+sendBasicEvent)
        * [.storeBasicEvent(eventName)](#MCS+storeBasicEvent)
        * [.flushEvents([callback])](#MCS+flushEvents)
        * [.startAutoFlushEvents([period])](#MCS+startAutoFlushEvents)
        * [.stopAutoFlushEvents()](#MCS+stopAutoFlushEvents)
        * [.getCollectionList(callback)](#MCS+getCollectionList)
        * [.getItemListInCollection(options, callback)](#MCS+getItemListInCollection)
        * [.getItem(options, callback)](#MCS+getItem)
        * [.storeItem(options, callback)](#MCS+storeItem)
        * [.deleteItem(options, callback)](#MCS+deleteItem)
        * [.createRequestOptions(options)](#MCS+createRequestOptions) ⇒ <code>object</code>
        * [.getAppPolicies(callback)](#MCS+getAppPolicies)
        * [.getDeviceLocationsByName(options, callback)](#MCS+getDeviceLocationsByName)
        * [.getDeviceLocationsById(options, callback)](#MCS+getDeviceLocationsById)
        * [.getPlaceByName(options, callback)](#MCS+getPlaceByName)
        * [.getPlaceById(options, callback)](#MCS+getPlaceById)
        * [.getAssetByName(options, callback)](#MCS+getAssetByName)
        * [.getAssetById(options, callback)](#MCS+getAssetById)
        * [.getLocationList(options, callback)](#MCS+getLocationList)
    * _inner_
        * [~loginCallback](#MCS..loginCallback) : <code>function</code>
        * [~registerDeviceTokenCallback](#MCS..registerDeviceTokenCallback) : <code>function</code>
        * [~deregisterDeviceTokenCallback](#MCS..deregisterDeviceTokenCallback) : <code>function</code>
        * [~sendAnalyticCallback](#MCS..sendAnalyticCallback) : <code>function</code>
        * [~sendBasicEventCallback](#MCS..sendBasicEventCallback) : <code>function</code>
        * [~getCollectionListCallback](#MCS..getCollectionListCallback) : <code>function</code>
        * [~getItemListInCollectionCallback](#MCS..getItemListInCollectionCallback) : <code>function</code>
        * [~getItemCallback](#MCS..getItemCallback) : <code>function</code>
        * [~storeItemCallback](#MCS..storeItemCallback) : <code>function</code>
        * [~deleteItemCallback](#MCS..deleteItemCallback) : <code>function</code>
        * [~getAppPoliciesCallback](#MCS..getAppPoliciesCallback) : <code>function</code>
        * [~getDeviceLocationsByNameCallback](#MCS..getDeviceLocationsByNameCallback) : <code>function</code>
        * [~getDeviceLocationsByIdCallback](#MCS..getDeviceLocationsByIdCallback) : <code>function</code>
        * [~getPlaceByNameCallback](#MCS..getPlaceByNameCallback) : <code>function</code>
        * [~getPlaceByIdCallback](#MCS..getPlaceByIdCallback) : <code>function</code>
        * [~getAssetByNameCallback](#MCS..getAssetByNameCallback) : <code>function</code>
        * [~getAssetByIdCallback](#MCS..getAssetByIdCallback) : <code>function</code>

<a name="new_MCS_new"></a>

### new MCS(options)

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | init object |
| options.baseUrl | <code>string</code> | MCS Base URL |
| options.backendId | <code>string</code> | MCS BackendId |
| options.androidApplicationKey | <code>string</code> | MCS Android Client Key |
| options.iOSApplicationKey | <code>string</code> | MCS iOS Client Key |
| options.anonymousKey | <code>string</code> | MCS Basic Anonymous Key |

<a name="MCS+autoFlushEventsStarted"></a>

### mcS.autoFlushEventsStarted
**Kind**: instance property of [<code>MCS</code>](#MCS)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| gets | <code>boolean</code> | calling flushEvents periodically is active or not |

<a name="MCS+setAuthorization"></a>

### mcS.setAuthorization(options)
Sets API authorization header value. Compared to login, this does not check

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | authorization options |
| options.username | <code>string</code> | MCS Username |
| options.password | <code>string</code> | MCS Password |

<a name="MCS+login"></a>

### mcS.login(options, callback)
login to MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | login options |
| options.username | <code>string</code> | MCS Username |
| options.password | <code>string</code> | MCS Password |
| callback | [<code>loginCallback</code>](#MCS..loginCallback) | for login |

**Example**  
```js
result:
  {
    "id": "295e450a-63f0-41fa-be43-cd2dbcb21598",
    "username": "joe",
    "email": "joe@example.com",
    "firstName": "Joe",
    "lastName": "Doe",
    "links": [
      { "rel": "canonical", "href": "/mobile/platform/users/joe" },
      { "rel": "self", "href": "/mobile/platform/users/joe" }
    ]
  }
```
<a name="MCS+logout"></a>

### mcS.logout()
Logs out authenticated user, using Anonymous Key if provided

**Kind**: instance method of [<code>MCS</code>](#MCS)  
<a name="MCS+registerDeviceToken"></a>

### mcS.registerDeviceToken(options, callback)
Register device push notification token to MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | push notification options |
| options.packageName | <code>string</code> | Application package name |
| options.version | <code>string</code> | Application version |
| callback | [<code>registerDeviceTokenCallback</code>](#MCS..registerDeviceTokenCallback) | for registerDeviceToken |

**Example**  
```js
result:
  {
    "id": "8a8a1eff-83c3-41b4-bea8-33357962d9a7",
    "user": "joe",
    "notificationToken": "03767dea-29ac-4440-b4f6-75a755845ade",
    "notificationProvider": "APNS",
    "mobileClient": {
      "id": "com.oracle.myapplication",
      "version": "1.0",
      "platform": "IOS"
    },
    "modifiedOn": "2015-05-05'T'12:09:33.281'Z"
  }
```
<a name="MCS+deregisterDeviceToken"></a>

### mcS.deregisterDeviceToken(options, callback)
Deregister device push notification token from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | push notification options |
| options.packageName | <code>string</code> | Application package name |
| callback | [<code>deregisterDeviceTokenCallback</code>](#MCS..deregisterDeviceTokenCallback) | for deregisterDeviceToken |

<a name="MCS+sendAnalytic"></a>

### mcS.sendAnalytic(options, [callback])
Send Analytic Event to MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  
**See**: [Oracle Docs](https://docs.oracle.com/en/cloud/paas/mobile-cloud/mcsra/op-mobile-platform-analytics-events-post.html)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | Analytic options |
| [options.deviceId] | <code>string</code> | can override what is set by the mcs lib |
| [options.sessionId] | <code>string</code> | can override what is set by the mcs lib |
| options.body | <code>object</code> | Event json array |
| [callback] | [<code>sendAnalyticCallback</code>](#MCS..sendAnalyticCallback) | for sendAnalytic |

<a name="MCS+sendBasicEvent"></a>

### mcS.sendBasicEvent(eventName, [callback])
Send Analytic Event to MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| eventName | <code>string</code> | Event name |
| [callback] | [<code>sendBasicEventCallback</code>](#MCS..sendBasicEventCallback) | for sendBasicEvent |

<a name="MCS+storeBasicEvent"></a>

### mcS.storeBasicEvent(eventName)
stores basic events to be sent later. Similar to sendBasicEvent

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type |
| --- | --- |
| eventName | <code>string</code> | 

<a name="MCS+flushEvents"></a>

### mcS.flushEvents([callback])
Sends stored events

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| [callback] | [<code>sendBasicEventCallback</code>](#MCS..sendBasicEventCallback) | for sendBasicEvent |

<a name="MCS+startAutoFlushEvents"></a>

### mcS.startAutoFlushEvents([period])
Starts calling flushEvents periodically

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [period] | <code>number</code> | <code>15000</code> | in miliselcods |

<a name="MCS+stopAutoFlushEvents"></a>

### mcS.stopAutoFlushEvents()
Stops calling flushEvents periodically

**Kind**: instance method of [<code>MCS</code>](#MCS)  
<a name="MCS+getCollectionList"></a>

### mcS.getCollectionList(callback)
Get all collections list from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| callback | [<code>getCollectionListCallback</code>](#MCS..getCollectionListCallback) | for getCollectionList |

<a name="MCS+getItemListInCollection"></a>

### mcS.getItemListInCollection(options, callback)
Get item list in collection from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>string</code> \| <code>object</code> | MCS collection id |
| options.collectionId | <code>string</code> | MCS collection id |
| callback | <code>getItemListInCollectionCallback</code> | for getItemListInCollection |

<a name="MCS+getItem"></a>

### mcS.getItem(options, callback)
Get item data from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | Analytic options |
| options.collectionId | <code>string</code> | MCS collection Id |
| options.itemId | <code>string</code> | MCS item Id |
| callback | [<code>getItemCallback</code>](#MCS..getItemCallback) | for getItem |

<a name="MCS+storeItem"></a>

### mcS.storeItem(options, callback)
Store item to MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | Analytic options |
| options.collectionId | <code>string</code> | MCS collection Id |
| options.itemName | <code>string</code> | item full name |
| options.base64EncodeData | <code>string</code> | item base64 encode data |
| options.contentType | <code>string</code> | item content type |
| callback | [<code>storeItemCallback</code>](#MCS..storeItemCallback) | for storeItem |

<a name="MCS+deleteItem"></a>

### mcS.deleteItem(options, callback)
Delete item data from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | Analytic options |
| options.collectionId | <code>string</code> | MCS collection Id |
| options.itemId | <code>string</code> | MCS item Id |
| callback | [<code>deleteItemCallback</code>](#MCS..deleteItemCallback) | for deleteItem |

<a name="MCS+createRequestOptions"></a>

### mcS.createRequestOptions(options) ⇒ <code>object</code>
Create api request options for MCS Custom API

**Kind**: instance method of [<code>MCS</code>](#MCS)  
**Returns**: <code>object</code> - httpRequestOption to be used in Smartface request  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| options | <code>object</code> |  | Request options |
| options.apiName | <code>string</code> |  | MCS Api Name |
| options.endpointPath | <code>string</code> |  | MCS Endpoint path |
| [options.version] | <code>string</code> | <code>&quot;\&quot;1.0\&quot;&quot;</code> | API version, by default 1.0 |

<a name="MCS+getAppPolicies"></a>

### mcS.getAppPolicies(callback)
Get application policies from MCS

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| callback | [<code>getAppPoliciesCallback</code>](#MCS..getAppPoliciesCallback) | for getAppPolicies |

<a name="MCS+getDeviceLocationsByName"></a>

### mcS.getDeviceLocationsByName(options, callback)
Get Device Location List by Name

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.name | <code>string</code> |  |
| callback | [<code>getDeviceLocationsByNameCallback</code>](#MCS..getDeviceLocationsByNameCallback) | for getDeviceLocationsByName |

<a name="MCS+getDeviceLocationsById"></a>

### mcS.getDeviceLocationsById(options, callback)
Get Device Location List by Id

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.id | <code>string</code> |  |
| callback | [<code>getDeviceLocationsByIdCallback</code>](#MCS..getDeviceLocationsByIdCallback) | for getDeviceLocationsById |

<a name="MCS+getPlaceByName"></a>

### mcS.getPlaceByName(options, callback)
Get Places List by Name

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.name | <code>string</code> |  |
| callback | [<code>getPlaceByNameCallback</code>](#MCS..getPlaceByNameCallback) | for getPlaceByName |

<a name="MCS+getPlaceById"></a>

### mcS.getPlaceById(options, callback)
Get Places List by Id,

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.id | <code>string</code> |  |
| callback | [<code>getPlaceByIdCallback</code>](#MCS..getPlaceByIdCallback) | for getPlaceById |

<a name="MCS+getAssetByName"></a>

### mcS.getAssetByName(options, callback)
Get Asset List by Name

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.name | <code>string</code> |  |
| callback | [<code>getAssetByNameCallback</code>](#MCS..getAssetByNameCallback) | for getAssetByName |

<a name="MCS+getAssetById"></a>

### mcS.getAssetById(options, callback)
Get Asset List by Id

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.id | <code>string</code> |  |
| callback | [<code>getAssetByIdCallback</code>](#MCS..getAssetByIdCallback) | for getAssetById |

<a name="MCS+getLocationList"></a>

### mcS.getLocationList(options, callback)
Get Location List Base Function

**Kind**: instance method of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.key | <code>string</code> |  |
| options.value | <code>string</code> |  |
| options.pathStr | <code>string</code> |  |
| options.isQuery | <code>string</code> |  |
| callback | <code>MCS~getLocationListCallback</code> | for getLocationList |

<a name="MCS..loginCallback"></a>

### MCS~loginCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | json result |

<a name="MCS..registerDeviceTokenCallback"></a>

### MCS~registerDeviceTokenCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | json result |

<a name="MCS..deregisterDeviceTokenCallback"></a>

### MCS~deregisterDeviceTokenCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..sendAnalyticCallback"></a>

### MCS~sendAnalyticCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | json result |

**Example**  
```js
result:
 {"message": "1 events accepted for processing."}
```
<a name="MCS..sendBasicEventCallback"></a>

### MCS~sendBasicEventCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | json result |

**Example**  
```js
result:
 {"message": "1 events accepted for processing."}
```
<a name="MCS..getCollectionListCallback"></a>

### MCS~getCollectionListCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>Array.&lt;object&gt;</code> | array for collections |
| result[].id | <code>string</code> | collection id |
| result[].description | <code>string</code> | collection description |

<a name="MCS..getItemListInCollectionCallback"></a>

### MCS~getItemListInCollectionCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>Array.&lt;object&gt;</code> |  |
| result[].id | <code>string</code> | item id |
| result[].name | <code>string</code> | item name |
| result[].contentType | <code>string</code> | item contentType |
| result[].createdBy | <code>string</code> | item createdBy |
| result[].createdOn | <code>string</code> | item createdOn |
| result[].modifiedBy | <code>string</code> | item modifiedBy |
| result[].modifiedOn | <code>string</code> | item modifiedOn |

<a name="MCS..getItemCallback"></a>

### MCS~getItemCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | base64 encoded file data |

<a name="MCS..storeItemCallback"></a>

### MCS~storeItemCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | json result |

**Example**  
```js
{
    "id": "947119e5-b45c-498b-a643-dca279b24f07",
    "name": "947119e5-b45c-498b-a643-dca279b24f07",
    "user": "8c8f1a5a-e56b-494b-9a99-f03d562c1ee7",
    "contentLength": 59,
    "contentType": "text/plain",
    "eTag": "\"1\"",
    "createdBy": "mobileuser",
    "createdOn": "2015-06-24T02:59:08Z",
    "modifiedBy": "mobileuser",
    "modifiedOn": "2015-06-24T02:59:08Z",
    "links": [
      {
        "rel": "canonical",
        "href": "/mobile/platform/storage/collections/technicianNotes/objects/947119e5-b45c-498b-a643-dca279b24f07?user=8c8f1a5a-e56b-494b-9a99-f03d562c1ee7"
      },
      {
        "rel": "self",
        "href": "/mobile/platform/storage/collections/technicianNotes/objects/947119e5-b45c-498b-a643-dca279b24f07"
      }
    ]
  }
```
<a name="MCS..deleteItemCallback"></a>

### MCS~deleteItemCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> | info message |

<a name="MCS..getAppPoliciesCallback"></a>

### MCS~getAppPoliciesCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getDeviceLocationsByNameCallback"></a>

### MCS~getDeviceLocationsByNameCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getDeviceLocationsByIdCallback"></a>

### MCS~getDeviceLocationsByIdCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getPlaceByNameCallback"></a>

### MCS~getPlaceByNameCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getPlaceByIdCallback"></a>

### MCS~getPlaceByIdCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getAssetByNameCallback"></a>

### MCS~getAssetByNameCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

<a name="MCS..getAssetByIdCallback"></a>

### MCS~getAssetByIdCallback : <code>function</code>
**Kind**: inner typedef of [<code>MCS</code>](#MCS)  

| Param | Type | Description |
| --- | --- | --- |
| err | <code>string</code> | Error |
| result | <code>string</code> |  |

