# unlimit-sdktest
This is a simple unlimit sdk application with javascript vanilla to easy website embed function with gateFiSDK.

Notes: You need to open this html in an server side tech, like nodejs, apache, nginx, etc. To avoid CORS ERRORS.
Also, you need to add the updated unlimit sdk script in the html file. You can get it from the official repo https://cdn.jsdelivr.net/npm/@gatefi/js-sdk. And made a little changes to the sdk if you are not using the gateFiSDK.js from this repo.

If you are not using the sdk from this repo. You need to export GateFiDisplayModeEnum as follow in the last gateFiSDK.js.

``` javascript
// GateFiDisplayModeEnum.js
export const GateFiDisplayModeEnum = {
    Embedded: 'Embedded',
    // other display modes...
  };

```
Also after the export function in the sdk you have to change the 'this' variable for 'window'. 
``` javascript
exports?exports.gateFiSDK=t():e.gateFiSDK=t()}(this, 
``` 
change that for  
``` javascript
exports?exports.gateFiSDK=t():e.gateFiSDK=t()}(windows,  