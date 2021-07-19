# Cordova Plugin Push CVIng

Customized version of Cordova plugin Push for FCM/APNS push notification specific for Internal Project

## Forked from havesource/cordova-plugin-push
Thanks to: 
[![Build Status](https://travis-ci.org/havesource/cordova-plugin-push.svg)](https://travis-ci.org/havesource/cordova-plugin-push)

> Register and receive push notifications

# What is this?

This plugin offers support to receive and handle native push notifications with a **single unified API**.

This does not mean you will be able to send a single push message and have it arrive on devices running different operating systems. By default Android uses FCM and iOS uses APNS and their payloads are significantly different. Even if you are using FCM for both Android and iOS there are differences in the payload required for the plugin to work correctly. For Android **always** put your push payload in the `data` section of the push notification. For more information on why that is the case read [Notification vs Data Payload](https://github.com/havesource/cordova-plugin-push/blob/master/docs/PAYLOAD.md#notification-vs-data-payloads). For iOS follow the regular [FCM documentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref).

This plugin does not provide a way to determine which platform you are running on. The best way to do that is use the `device.platform` property provided by [cordova-plugin-device](https://github.com/apache/cordova-plugin-device).
