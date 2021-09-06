# mapmyindia-intouch-web-plugins

## InTouch Live Location Tracking Widget
Easy to integrate InTouch Live location Tracking widget by MapmyIndia. Using this widget you will be able to view the vehicles live locaiton on Map.

### 3 Step process to integrate InTouch Live location tracking widget in any Web App

1. #### Step 1
    Inside the <body> section of HTML of web page, define a div into which the InTouch Live location Tracking widget from MapmyIndia needs to be loaded.
    ```html
     <div id="mapdiv"></div>
    ```

2. #### Step 2
    Inside the <head> section of HTML of web page, or wherever else you find more suitable, include the following MapmyIndia javascript code.
    ```html
    <script src="https://cdn.mapmyindia.com/Intouch/sdk/v1.0/intouch-sdk.js"></script>
    ```
3. #### Step 3 
    To load up the InTouch live location Tracking widget from MapmyIndia, call the following javascript code **AFTER** the Intouch live location Tracking javascript file (as defined in step 2) has loaded.
    ```js
    var intouchObj = {};  
    //intouchObj.customIconUrl = "";
    intouchObj.iconType = 'car'; // Allowed types are "bike", "car", "bus", "truck", "men".
    intouchObj.mapKey = "Enter the Map Access Token"; // Use the Map API Rest key
    intouchObj.deviceId ={Device Id}; // Enter the Device Id for which you want to see the Tracking. 
    intouchObj.access_token = "Enter the oAuth Token without Bearer word"; // While adding the token Don't use Bearer word, since it is being internally added.
    intouchObj.bindPopUp = true;
    var intouchSdk = new IntouchSdk();
    intouchSdk.trackDevice(mapdiv, intouchObj);
    ```
    That’s it - all done!

## Sample Code
```html
<html>
<head>
  <script src="https://cdn.mapmyindia.com/Intouch/sdk/v1.0/intouch-sdk.js"></script>
</head>

<body>
  <div id="mapdiv"></div>
</body>
<script type="text/javascript" defer=defer>
  var intouchObj = {};  
  // intouchObj.customIconUrl = "";
  intouchObj.iconType = 'bus';
  intouchObj.mapKey = "9a5cf885c506836aca535c22c98fa23";
  intouchObj.deviceId = 323123;
  intouchObj.access_token = "6ed72323a62-93a6-4437-bb9e-56";
  intouchObj.bindPopUp = true;
  var intouchSdk = new IntouchSdk();
  intouchSdk.trackDevice(mapdiv, intouchObj);

</script>

</html>
```


For any queries and support, please contact: 

[<img src="https://www.mapmyindia.com/images/logo.png" height="40"/> </p>](https://www.mapmyindia.com/api)
Email us at [apisupport@mapmyindia.com](mailto:apisupport@mapmyindia.com)


![](https://www.mapmyindia.com/api/img/icons/support.png)
[Support](https://www.mapmyindia.com/api/index.php#f_cont)
Need support? contact us!

<br></br>
<br></br>

[<p align="center"> <img src="https://www.mapmyindia.com/api/img/icons/stack-overflow.png"/> ](https://stackoverflow.com/questions/tagged/mapmyindia-api)[![](https://www.mapmyindia.com/api/img/icons/blog.png)](http://www.mapmyindia.com/blog/)[![](https://www.mapmyindia.com/api/img/icons/gethub.png)](https://github.com/MapmyIndia)[<img src="https://mmi-api-team.s3.ap-south-1.amazonaws.com/API-Team/npm-logo.one-third%5B1%5D.png" height="40"/> </p>](https://www.npmjs.com/org/mapmyindia) 



[<p align="center"> <img src="https://www.mapmyindia.com/june-newsletter/icon4.png"/> ](https://www.facebook.com/MapmyIndia)[![](https://www.mapmyindia.com/june-newsletter/icon2.png)](https://twitter.com/MapmyIndia)[![](https://www.mapmyindia.com/newsletter/2017/aug/llinkedin.png)](https://www.linkedin.com/company/mapmyindia)[![](https://www.mapmyindia.com/june-newsletter/icon3.png)](https://www.youtube.com/user/MapmyIndia/)




<div align="center">@ Copyright 2021 CE Info Systems Pvt. Ltd. All Rights Reserved.</div>

<div align="center"> <a href="https://www.mapmyindia.com/api/terms-&-conditions">Terms & Conditions</a> | <a href="https://www.mapmyindia.com/about/privacy-policy">Privacy Policy</a> | <a href="https://www.mapmyindia.com/pdf/mapmyIndia-sustainability-policy-healt-labour-rules-supplir-sustainability.pdf">Supplier Sustainability Policy</a> | <a href="https://www.mapmyindia.com/pdf/Health-Safety-Management.pdf">Health & Safety Policy</a> | <a href="https://www.mapmyindia.com/pdf/Environment-Sustainability-Policy-CSR-Report.pdf">Environmental Policy & CSR Report</a>

<div align="center">Customer Care: +91-9999333223</div>
