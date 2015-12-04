Get Started with GeoBox.IO
--------------------------
This guide provides instructions to get you started collecting devices locations using GeoBox.IO. The guide covers the following topics:

* [Create a Locwise GeoBox.IO account](#Create-a-Locwise-GeoBox.IO-account)
* [Create your first GeoBox.IO application](#Create-your-first-GeoBox.IO-Application)
* Generate tracking API key
* Start tracking
* Adding Geofences
* Test the service

## Create a Locwise GeoBox.IO account <a id="Create-a-Locwise-GeoBox.IO-account"></a>
Locwise GeoBox.IO account is free, we recommend registering using your Gmail or Microsoft account
## Create your first GeoBox.IO Application
In order to get started with Locwise GeoBox.IO, first, you need to create a GeoBox.IO Application
GeoBox.IO Application is a logical entity which groups devices, geofences and events.
Any account may have several GeoBox.IO applications. 

![image](https://cloud.githubusercontent.com/assets/15333203/11377781/6e322598-92f0-11e5-8f37-f7059d0b07b4.png)
## Generate tracking API keys
Tracking is only possible when tracking messages contains a valid GeoBox.IO API key. 
GeoBox.IO API key is our way to identify who you are while using our infrastructure.
An application can have several different keys for different functionalities 
There are 2 types of GeoBox.IO API keys:
- Tracking API Key - Enables devices to report their location
- Management API Key - Enables interrogating devices location and managing system's geofences

Each of your GeoBox.IO applications has default API keys, you can always regenerate new API keys
Go to your Control Panel, choose one of your applications and click API Keys, choose the name of the API key you would like to generate, the following screen will pop-up, click Regenerate Key:

![image](https://cloud.githubusercontent.com/assets/15333203/11377889/1229757a-92f1-11e5-8182-5ff95da9a2c8.png)

 
##Start tracking

Add GeoBox.IO Javascript SDK to your application by adding the follow script

    <script type="text/javascript" src="http://locwisegridapi.azurewebsites.net/jsapi/v1/tracker" >/script>

Add the following lines to your HTML page:

    <script type="text/javascript">
    $(function () {
    var tracker = new LocwiseGrid.Tracker({
    apikey: "your api key",
    deviceid: "deviceid as you choose"
    });
    tracker.start();
    });
    </script>
