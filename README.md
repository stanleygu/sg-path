# Node.js Path service for angular

Use the [node.js path module](http://nodejs.org/api/path.html) in Angular.

Convenient for dealing with URLs.

# Installation

* Using bower, `bower install --save stanleygu/sg-path`
* Add the module in your angular app definition:
```
angular.module('myApp', ['stanleygu.path']);
```

# Example Usage

Getting repository info from Github API

```
angular.module('myApp')
  .controller('myCtrl', function ($scope, $http, sgPath) {
    var baseUrl = 'https://api.github.com';
    var route = 'repos';
    var user = 'angular';
    var repo = 'angular.js'
    
    $http
      .get(sgPath.join(baseUrl, route, user, repo)
      .success(function(data){
        $scope.repositoryInfo = data;
      });
  });
```


