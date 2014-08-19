instakids
==================
    ver 1.0 
    2014/08/16
    
    
> Start Over.


User Account & Access
------------------
------------------


### Get a Access Token
```
Before invoke any authorized API function,we must have a access token using Signin Method.
```


### Signin

###### URL:
<http://xxx.com/api/v1/account/signin>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Desc
:------------: | :-------------: | :------------: | ------------
Email | String  | - | 
Password | String  | - | 

###### Response:
{"success":true,"token":"abcd1234"}

------------------

### Signup
###### URL:
<http://xxx.com/api/v1/account/signin>

###### Http Method:
GET

###### Response Data Type
JSON

###### Parameters:

Prama | Type | Range | Desc
:------------: | :-------------: | :------------: | ------------
Email | String  | - | 
Password | String  | - | 

###### Response:
｛“success”:true,"errmsg",null,"data":{“token”:“abcd1234”}} 

### Signout

### Forgot Password

### Change Password



User Profile
------------------

### User Profile Object

### Get User Profile

### Update User Profile 

### Register Mobile Client Push Indentity


Shop
------------------
`We only have ONE shop for now`


### Shop Object

### Get Shop


Package
------------------

### Package Object


Order
------------------

### Order Object

### Get User OrderList

### Get Order

### Cancel Order

### Confirm Shiped(Finnish)

### Pay Order

### Refond Order



