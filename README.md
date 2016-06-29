# This is a cordova plugin which support Andorid only at the moment
this plugin support sigle & mutiple scan, and it is very quick.

# How to use
###1. Download###
<code>cordova plugin add https://github.com/garyganyang/cluze-cordova-barcode-scanner.git</code>

###2. Integrate with Ionic###
```js
/* Single Scan*/
    $scope.cameraBarcode = function () {
        window.BarcodeScanner.singleScan(function (result) {
            $scope.$apply();
            $scope.barcode = result;
        }, function (e) {
            console.log(e);
        });
    };
```
```js
/* Mutiple Scan*/
    var codes = ['6928393400082']; // this is for re-scan, if you call pass this to multipleScan() you can keep scanning
    $scope.camera = function () {
        window.BarcodeScanner.multipleScan(function (result) {
            $scope.$apply();
            iangular.forEach(result, function (each) {
              console.log(each);
            })
        }, function (e) {
            console.log(e);
        }, codes);
    };
```
![](http://i.imgur.com/VhBWCTX.jpg)
![](http://i.imgur.com/pJNGRUR.jpg)
