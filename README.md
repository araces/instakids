instakids
==================
    ver 1.0 
    2014/08/16
    
    
> Start Over.


User Account & Access
------------------


### Get a Access Token
```
Before invoke any authorize require API function,we must have a access token using Signin Method.
```
authorize SOP:

* sign in.
* sign in function response the access token.
* client keep the access token for authorize require api funcitons.

### Signin

###### URL:
<http://xxx.com/api/v1/account/signin>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
email | String  | - | `NO` | 
password | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{“token”:“abcd1234”}} 

------------------

### Signup
###### URL:
<http://xxx.com/api/v1/account/signup>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
email | String  | - | `NO` |
password | String  | | `NO` | 
devicetoken | String | | YES | 

###### Response:
｛“success”:true,"errmsg",null,"data":{“token”:“abcd1234”}} 

------------------


### Forgot Password
```
When user submit his email,we send a forgot password guide email to THE email address and user should following the instruction to complete that.
```
###### URL:
<http://xxx.com/api/v1/account/forgotpassword>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
email | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------

### Change Password
###### URL:
<http://xxx.com/api/v1/account/forgotpassword>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
email | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------


User Profile
------------------

### User Profile Object
###### Object Define:
Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
email | String  | - | `NO` |
createDate | DateTime  | - | `NO` |
name | String  | - | `NO` |
rank | unit  | - | `NO` |
credit | uint  | - | `NO` |
avator | String  | - | YES | full path url

###### Object raw json:
{"name":"ward","email":"abc@domain.com","createdate","2014-08-08","rank":2,"credit":200,"avator":"http://xxx.com/xx.jpg"}

------------------

### Get User Profile
###### URL:
<http://xxx.com/api/v1/account/getprofile>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
email | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{"name":"ward","email":"abc@domain.com","createdate","2014-08-08","rank":2,"credit":200,"avator":"http://xxx.com/xx.jpg"}} 

------------------

### Update User Profile 
###### URL:
<http://xxx.com/api/v1/account/updateprofile>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
email | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{"name":"ward","email":"abc@domain.com","createdate","2014-08-08","rank":2,"credit":200,"avator":"http://xxx.com/xx.jpg"}} 

------------------

### Register Mobile Client Push Indentity
###### URL:
<http://xxx.com/api/v1/account/registerDeviceToken>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
devicetoken | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------


Shop
------------------
`We only have ONE shop for now`


~~### Shop Object~~

~~### Get Shop~~


Package
------------------

### Package Object
###### Object Define:
Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
shopId | String  | - | `NO` |
packageId | String  | - | `NO` |
packageName | String  | - | `NO` |
createDate | DateTime  | - | `NO` |
price | Money  | - | `NO` |
pages | uint | - | `NO` |
desc | String  | - | `NO` |
images | String Array  | - | `NO` | aaa,bbb,ccc
packagetype | uint  | - | YES |

###### Object raw json:
{"name":"ward","email":"abc@domain.com","createdate","2014-08-08","rank":2,"credit":200,"avator":"http://xxx.com/xx.jpg"}

------------------

### GetPackages
###### URL:
<http://xxx.com/api/v1/account/getPackages>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
category | String  | - | `YES` |

###### Response:
｛“success”:true,"errmsg",null,"data":{"packages":{}}} 

------------------



ShopCart
------------------
`not avaliable in first release.`

Order
------------------

### Order Object
###### Order Object Define:
Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
orderId | String  | - | `NO` |
shopId | String  | - | `NO` |
userId | String  | - | `NO` |
createDate | DateTime  | - | `NO` |
status | unit  | - | `NO` |
amount | money | - | `NO` |
qty | uint  | - | `NO` |
orderProducts | JSON Array  | - | `NO` |
ordertype | uint  | - | YES |

###### OrderProduct Object Define:
Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
orderId | String  | - | `NO` |
createDate | DateTime  | - | `NO` |
status | unit  | - | `NO` |
orderProductId | String | - | `NO` |
qty | uint  | - | `NO` |
packageId | string  | - | `NO` |
packageName | string  | - | `NO` |
price | Money  | - | `NO` |

###### Object raw json:
{"name":"ward","email":"abc@domain.com","createdate","2014-08-08","rank":2,"credit":200,"avator":"http://xxx.com/xx.jpg"}

------------------


### Get User OrderList
###### URL:
<http://xxx.com/api/v1/account/getOrderList>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
startDate | String  | - | YES | eg:2014-08-18
endDate | String  | - | YES | eg:2014-08-20
status | unit  | - | YES |

###### Response:
｛“success”:true,"errmsg",null,"data":{"orders":{}}} 

------------------



### Get Order
###### URL:
<http://xxx.com/api/v1/account/getOrder>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
orderId | String  | - | `NO` | 

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------


### Cancel Order
###### URL:
<http://xxx.com/api/v1/account/cancelOrder>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
orderId | String  | - | `NO` | 

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------


### Confirm Shiped(Finnish)
###### URL:
<http://xxx.com/api/v1/account/finishOrder>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
orderId | String  | - | `NO` | 

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------

### Pay Order
```
Open a browser with the URL value in response json object for 3rd part online pay service step.
```
###### URL:
<http://xxx.com/api/v1/account/payOrder>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
orderId | String  | - | `NO` | 

###### Response:
｛“success”:true,"errmsg",null,"data":{""payment":{"url":"http://m.alipay.com/xxx"}}} 

------------------


### Refond Order
###### URL:
<http://xxx.com/api/v1/account/refondOrder>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
userId | String  | - | `NO` |
orderId | String  | - | `NO` | 

###### Response:
｛“success”:true,"errmsg",null,"data":{}} 

------------------


UploadPhoto
------------------
###### URL:
<http://xxx.com/api/v1/account/uploadPhoto>

###### Http Method:
POST

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Nullable | Desc
:------------ | :-------------: | :------------: | :------------: | ------------
token | String  | - | `NO` |
email | String  | - | `NO` |
localfilename | String  | - | `NO` |
file | Stream  | - | `NO` |
orderid | String  | - | `NO` |

###### Response:
｛“success”:true,"errmsg",null,"data":{"url":"http://xxx.com/abc.jpg","contentlength":2000}} 




