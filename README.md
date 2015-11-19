Apache Cordova Parse Push Notifications
====================
# Overview #
Provides access to registering a device for Parse push notifications.

This fork (of cranberrygame's) contains numerous bug fixes.

[android, ios, wp8] [crodova cli] [xdk] [cocoon] [phonegap build service]

Requires parse account http://parse.com

# How to install #

## Cordova ##
```c
cordova plugin add https://github.com/skylordjason/cordova.plugin.parsepush
```

# Set up #

Set-up has not been commited.

# API #
```javascript
var applicationId = "REPLACE_THIS_WITH_YOUR_APPLICATION_ID";
var clientKey = "REPLACE_THIS_WITH_YOUR_CLIENT_KEY";

document.addEventListener("deviceready", function(){

	window.parsepushnotification.setUp(applicationId, clientKey);
	
	//registerAsPushNotificationClient callback (called after setUp)
	window.parsepushnotification.onRegisterAsPushNotificationClientSucceeded = function() {
		alert('onRegisterAsPushNotificationClientSucceeded');
	};
	window.parsepushnotification.onRegisterAsPushNotificationClientFailed = function() {
		alert('onRegisterAsPushNotificationClientFailed');
	};
	
	//subscribe callback
	window.parsepushnotification.onSubscribeToChannelSucceeded = function() {
		alert('onSubscribeToChannelSucceeded');
	};
	window.parsepushnotification.onSubscribeToChannelFailed = function() {
		alert('onSubscribeToChannelFailed');
	};	
	//unsubscribe callback
	window.parsepushnotification.onUnsubscribeSucceeded = function() {
		alert('onUnsubscribeSucceeded');
	};
	window.parsepushnotification.onUnsubscribeFailed = function() {
		alert('onUnsubscribeFailed');
	};	
}, false);

//
window.parsepushnotification.subscribeToChannel('Game');//parameter: channel

//
window.parsepushnotification.unsubscribe('Game');//parameter: channel
```
# Examples #

No examples are available.
