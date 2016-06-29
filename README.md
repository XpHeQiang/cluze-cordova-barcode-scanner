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
    var codes = []; // this is for callback when finished mutilple scan
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
