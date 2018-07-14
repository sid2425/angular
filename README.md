<!DOCTYPE html>
<html ng-app="myApp">
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>
    <div ng-controller="cat">
        Operand 1<input ng-model="fname" type="text">
        Operand 2<input ng-model="lname" type="text">
        <select>
            <option ng-click="sum()">sum</option>
            <option ng-click="minus()">subtract</option>
            <option ng-click="mul()">multiply</option>
            <option ng-click="div()">div</option>
        </select>
        Result:<label ng-bind="Result"></label>
    </div>
    <script>
    var app=angular.module("myApp",[]);
    app.controller("cat",function($scope)
    {
       $scope.fname=0;
       $scope.lname=0;
       $scope.Result=0; 
       $scope.sum=function()
       {
        $scope.Result=$scope.fname+$scope.lname;
       };
       $scope.minus=function()
       {
        $scope.Result=$scope.fname-$scope.lname;
       };
       $scope.mul=function()
       {
        $scope.Result=$scope.fname*$scope.lname;
       };
       $scope.div=function()
       {
        $scope.Result=$scope.fname/$scope.lname;
       };
    
});
    </script>
</body>
