---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript
  - python
  - java
  - ruby
  - c

---

# Introduction

Welcome to the Mahnee API! You can use our API to access Mahnee API endpoints, which would let users pay using Mahnee and making transaction of points from merchant to user easier.

# Flow of Transaction

By implementing this API, you, as merchant, will have the opportunity to implement payment using Mahnee for your customers of your online merchant shop.

When customers opt for paying by Mahnee, they will be prompt to fill in their email (used for Mahnee account). After the transaction is done, the points 

(NOTE: it is up to you, the merchant, to make sure that the customer is a registered Mahnee User)

# Code

We have language bindings in python, javascript, java, ruby, and curl! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

## Example Code

Copy the example code at the side and replace the following variables as follows:

Variable | Description 
-------- | -----------
your_special_id | your special id received by Mahnee
yourusername@gmail.com | your username used for Mahnee business account
password | your password for your Mahnee business account

```javascript
$http.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded;charset=utf-8';
$http.default.headers.post["Authorization"] = "your_special_id";
$http.post("https://join.mahnee.com/api/getAuth", $.param({
  "username" : "yourusername@gmail.com",
  "password" : "password",
  "company_code" : 3
})).then(function(result){
  if(result['status'] == 'success'){
      $http.defaults.headers.post["Authorization"] = result['hash'];
      $http.post("https://join.mahnee.com/api/givePoint", $.param({
      "username" : "yourusername@gmail.com",
      "password" : "password",
      "company_code" : 3,
      "receiver_email" : "people_youwant_give_point_to@gmail.com",
      "type" : "big",
      "point_original" : "109.99"
      })).then(function(result){
        if(result['status'] == 'success'){

        } else if(result['status'] == 'fail'){
          // insufficient_balance
          // expired_auth
          // invalid_auth
          // invalid_owner
          // invalid_password
          // invalid_username
        }
      });
  } else if(result['status'] == 'fail'){
    // invalid_username
    // invalid_password
    // invalid_owner
    // invalid_auth
    // expired_auth
  }
});
```

```python
$http.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded;charset=utf-8';
$http.default.headers.post["Authorization"] = "your_special_id";
$http.post("https://join.mahnee.com/api/getAuth", $.param({
  "username" : "yourusername@gmail.com",
  "password" : "password",
  "company_code" : 3
})).then(function(result){
  if(result['status'] == 'success'){
      $http.defaults.headers.post["Authorization"] = result['hash'];
      $http.post("https://join.mahnee.com/api/givePoint", $.param({
      "username" : "yourusername@gmail.com",
      "password" : "password",
      "company_code" : 3,
      "receiver_email" : "people_youwant_give_point_to@gmail.com",
      "type" : "big",
      "point_original" : "109.99"
      })).then(function(result){
        if(result['status'] == 'success'){

        } else if(result['status'] == 'fail'){
          // insufficient_balance
          // expired_auth
          // invalid_auth
          // invalid_owner
          // invalid_password
          // invalid_username
        }
      });
  } else if(result['status'] == 'fail'){
    // invalid_username
    // invalid_password
    // invalid_owner
    // invalid_auth
    // expired_auth
  }
});
```

```java
$http.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded;charset=utf-8';
$http.default.headers.post["Authorization"] = "your_special_id";
$http.post("https://join.mahnee.com/api/getAuth", $.param({
  "username" : "yourusername@gmail.com",
  "password" : "password",
  "company_code" : 3
})).then(function(result){
  if(result['status'] == 'success'){
      $http.defaults.headers.post["Authorization"] = result['hash'];
      $http.post("https://join.mahnee.com/api/givePoint", $.param({
      "username" : "yourusername@gmail.com",
      "password" : "password",
      "company_code" : 3,
      "receiver_email" : "people_youwant_give_point_to@gmail.com",
      "type" : "big",
      "point_original" : "109.99"
      })).then(function(result){
        if(result['status'] == 'success'){

        } else if(result['status'] == 'fail'){
          // insufficient_balance
          // expired_auth
          // invalid_auth
          // invalid_owner
          // invalid_password
          // invalid_username
        }
      });
  } else if(result['status'] == 'fail'){
    // invalid_username
    // invalid_password
    // invalid_owner
    // invalid_auth
    // expired_auth
  }
});
```

```ruby
$http.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded;charset=utf-8';
$http.default.headers.post["Authorization"] = "your_special_id";
$http.post("https://join.mahnee.com/api/getAuth", $.param({
  "username" : "yourusername@gmail.com",
  "password" : "password",
  "company_code" : 3
})).then(function(result){
  if(result['status'] == 'success'){
      $http.defaults.headers.post["Authorization"] = result['hash'];
      $http.post("https://join.mahnee.com/api/givePoint", $.param({
      "username" : "yourusername@gmail.com",
      "password" : "password",
      "company_code" : 3,
      "receiver_email" : "people_youwant_give_point_to@gmail.com",
      "type" : "big",
      "point_original" : "109.99"
      })).then(function(result){
        if(result['status'] == 'success'){

        } else if(result['status'] == 'fail'){
          // insufficient_balance
          // expired_auth
          // invalid_auth
          // invalid_owner
          // invalid_password
          // invalid_username
        }
      });
  } else if(result['status'] == 'fail'){
    // invalid_username
    // invalid_password
    // invalid_owner
    // invalid_auth
    // expired_auth
  }
});
```

```c
$http.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded;charset=utf-8';
$http.default.headers.post["Authorization"] = "your_special_id";
$http.post("https://join.mahnee.com/api/getAuth", $.param({
  "username" : "yourusername@gmail.com",
  "password" : "password",
  "company_code" : 3
})).then(function(result){
  if(result['status'] == 'success'){
      $http.defaults.headers.post["Authorization"] = result['hash'];
      $http.post("https://join.mahnee.com/api/givePoint", $.param({
      "username" : "yourusername@gmail.com",
      "password" : "password",
      "company_code" : 3,
      "receiver_email" : "people_youwant_give_point_to@gmail.com",
      "type" : "big",
      "point_original" : "109.99"
      })).then(function(result){
        if(result['status'] == 'success'){

        } else if(result['status'] == 'fail'){
          // insufficient_balance
          // expired_auth
          // invalid_auth
          // invalid_owner
          // invalid_password
          // invalid_username
        }
      });
  } else if(result['status'] == 'fail'){
    // invalid_username
    // invalid_password
    // invalid_owner
    // invalid_auth
    // expired_auth
  }
});
```

## Explanation by Parts

## Possible Errors

Below are the errors that might arise in 

### Error 1
1. insufficient_balance
2. expired_auth
3. invalid_auth
4. invalid_owner
5. invalid_password
6. invalid_username

### Error 2

1. invalid_username
2. invalid_password
3. invalid_owner
4. invalid_auth
5. expired_auth








