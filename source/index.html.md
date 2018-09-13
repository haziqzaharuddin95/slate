---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - python
  - javascript
  - java
  - ruby
  - curl

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

---

# Introduction

Welcome to the Mahnee API! You can use our API to access Mahnee API endpoints, which would let users pay using Mahnee and making transaction of points from merchant to user easier.

# Code

We have language bindings in python, javascript, java, ruby, and curl! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

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

```curl
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

