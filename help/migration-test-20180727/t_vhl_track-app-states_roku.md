---
description: States are the different screens or views in your application. Each time a new state is displayed in your application, for example, when a user navigates from the home page to the video details screen, you should send a trackState call.
seo-description: States are the different screens or views in your application. Each time a new state is displayed in your application, for example, when a user navigates from the home page to the video details screen, you should send a trackState call.
seo-title: Track App States
title: Track App States
uuid: f8c147eb-9e33-4bc4-93d1-2af4a99c0073
index: y
internal: n
snippet: y
translate: y
---

# Track App States


>1. `trackState` is typically called each time a new screen is loaded.
>
>   ```
>   ADBMobile().trackState("State Name", {})
>   ```

>   The state name is reported in the `View State` variable in Adobe Mobile services, and a view is recorded for each `trackState` call. In other Analytics interfaces, `View State` is reported as `Page Name` and state views is reported as page views. 
>
>1. In addition to the `State Name`, you can send additional context data with each track action call:
>
>   ```
>   dictionary = { }
>   dictionary["myapp.login.LoginStatus"] = "logged in" 
>   ADBMobile().trackState("Home Screen", dictionary)
>   ```


>   >[!IMPORTANT]
>   >
>   >Context data values must be mapped to custom variables in Adobe Mobile services.
>   States are typically viewed by using a pathing report, so you can see how users navigate your app and which states are most commonly viewed.
>