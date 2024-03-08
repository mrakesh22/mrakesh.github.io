<!DOCTYPE html>
<html ng-app="myApp">
<head>
<title>Full Name Input with Default Values</title>
<script
src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></
script>
<style>
body {
font-family: sans-serif;
}
.container {
margin: 20px;
padding:
20px;
border: 1px solid #ccc;
}
label {
display: block;
margin-bottom:
5px;
}
input {
width: 100%;
padding: 5px;
border: 1px solid #ccc;
}
.fullName {
font-weight: bold;
}
</style>
</head>
<body>
<div class="container" ng-controller="myCtrl">
<h2>Full Name Input with Default Values</h2>
<label for="firstName">First Name:</label>
<input type="text" ng-model="firstName" id="firstName"
placeholder="Enter your first name" value="John">
<label for="lastName">Last Name:</label>
<input type="text" ng-model="lastName" id="lastName"
placeholder="Enter your last name" value="Doe">
<br>
<span class="fullName">Full Name: {{firstName + ' ' + lastName}}</span>
</div>
<script>

var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
$scope.firstName = "John";
$scope.lastName = "Doe";
});
</script>
</body>
</html>
