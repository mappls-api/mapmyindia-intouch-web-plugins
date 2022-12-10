[<img src="https://about.mappls.com/images/mappls-logo.svg" height="60"/> </p>](https://about.mappls.com/api/)
# mapmyindia-intouch-web-plugins V1

## InTouch Live Location Tracking Widget
In this tutorial, we are going to see an easy to integrate InTouch Live location Tracking widget powered by Mappls from MapmyIndia. Using this widget, you will be able to view the vehicles live locaiton on Map.

### 3 Step process to integrate InTouch Live location tracking widget in any Web App

1. #### Step 1
    Inside the <head> section of HTML of web page, or wherever else you find more suitable, include the following MapmyIndia javascript code.
    ```html
    <script src="https://cdn.mapmyindia.com/Intouch/sdk/v1.0/intouch-sdk.js"></script>
    ```
2. #### Step 2
    Inside the <body> section of HTML of web page, define a div into which the InTouch Live location Tracking widget from MapmyIndia needs to be loaded.
    ```html
     <div id="mapdiv"></div>
    ```

3. #### Step 3 
    To load up the InTouch live location Tracking widget from MapmyIndia, call the following javascript code **AFTER** the Intouch live location Tracking javascript file (as defined in step 1) has loaded.
    ```js
    <script type="text/javascript" defer=defer>
    var intouchSdk = new IntouchSdk();
    function deviceDataCallback(data) {
        console.log(data);
    }

    function updateToken() {
        console.log("tokenUpdated");
        intouchSdk.updateAccessToken("<Enter the oAuth Token without Bearer word>"); // While adding the token Don't use Bearer word, since it is being internally added.
    }

    intouchSdk.initialize(mapdiv, "<Enter the Map Access Token>", "<Enter the oAuth Token without Bearer word>", updateToken); // For Map access token Use the Map API Rest key

    var deviceObj = {};
    // deviceObj.customIconUrl = "";
    deviceObj.iconType = 'car';// Allowed types are "bike", "car", "bus", "truck", "men".
    deviceObj.deviceId = {Device Id}; // Enter the Device Id for which you want to see the Tracking. 
    deviceObj.bindPopUp = true;
    intouchSdk.trackDevice(deviceObj, deviceDataCallback);
    </script>

#### That’s it - all done!

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
    var intouchSdk = new IntouchSdk();
    function deviceDataCallback(data) {
        console.log(data);
    }

    function updateToken() {
        console.log("tokenUpdated");
        intouchSdk.updateAccessToken("token-generated-from-CI-and-CS");
    }

    intouchSdk.initialize(mapdiv, "provided-map-api-key-here", "token-generated-from-CI-and-CS", updateToken);

    var deviceObj = {};
    // deviceObj.customIconUrl = "";
    deviceObj.iconType = 'car';
    deviceObj.deviceId = 1002537;
    deviceObj.bindPopUp = true;
    intouchSdk.trackDevice(deviceObj, deviceDataCallback);
</script>

</html>
```
### Intouch Live Tracking sample Widget Image
        
![Live Tracking widget](https://user-images.githubusercontent.com/59359484/158617366-5e814961-0a7a-44e4-bf2b-981af94fc92d.png)

        
<br>

For any queries and support, please contact: 

[<img src="https://about.mappls.com/images/mappls-logo.svg" height="40"/> </p>](https://about.mappls.com/api/)
Email us at [apisupport@mappls.com](mailto:apisupport@mappls.com)


![](https://www.mapmyindia.com/api/img/icons/support.png)
[Support](https://about.mappls.com/contact/)
Need support? contact us!

<br></br>
<br></br>

[<p align="center"> <img src="https://www.mapmyindia.com/api/img/icons/stack-overflow.png"/> ](https://stackoverflow.com/questions/tagged/mappls-api)[![](https://www.mapmyindia.com/api/img/icons/blog.png)](https://about.mappls.com/blog/)[![](https://www.mapmyindia.com/api/img/icons/gethub.png)](https://github.com/Mappls-api)[<img src="https://mmi-api-team.s3.ap-south-1.amazonaws.com/API-Team/npm-logo.one-third%5B1%5D.png" height="40"/> </p>](https://www.npmjs.com/org/mapmyindia) 



[<p align="center"> <img src="https://www.mapmyindia.com/june-newsletter/icon4.png"/> ](https://www.facebook.com/Mapplsofficial)[![](https://www.mapmyindia.com/june-newsletter/icon2.png)](https://twitter.com/mappls)[![](https://www.mapmyindia.com/newsletter/2017/aug/llinkedin.png)](https://www.linkedin.com/company/mappls/)[![](https://www.mapmyindia.com/june-newsletter/icon3.png)](https://www.youtube.com/channel/UCAWvWsh-dZLLeUU7_J9HiOA)




<div align="center">@ Copyright 2022 CE Info Systems Ltd. All Rights Reserved.</div>

<div align="center"> <a href="https://about.mappls.com/api/terms-&-conditions">Terms & Conditions</a> | <a href="https://about.mappls.com/about/privacy-policy">Privacy Policy</a> | <a href="https://about.mappls.com/pdf/mapmyIndia-sustainability-policy-healt-labour-rules-supplir-sustainability.pdf">Supplier Sustainability Policy</a> | <a href="https://about.mappls.com/pdf/Health-Safety-Management.pdf">Health & Safety Policy</a> | <a href="https://about.mappls.com/pdf/Environment-Sustainability-Policy-CSR-Report.pdf">Environmental Policy & CSR Report</a>

<div align="center">Customer Care: +91-9999333223</div>
