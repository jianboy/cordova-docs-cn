---
license: >
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

title: menubutton
---

# menubutton

在使用者按功能表按钮时，将触发该事件。

    document.addEventListener("menubutton", yourCallbackFunction, false);
    

## 详细资讯

事件处理常式的应用覆盖的预设功能表按钮行为。

应用程式通常应使用 `document.addEventListener` 将一个事件拦截器附加一次 `[deviceready](events.deviceready.html)` 事件火灾。

## 支援的平台

*   亚马逊火 OS
*   Android 系统
*   黑莓 10

## 快速的示例

    document.addEventListener("menubutton", onMenuKeyDown, false);
    
    function onMenuKeyDown() {
        // Handle the back button
    }
    

## 完整的示例

    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
                          "http://www.w3.org/TR/html4/strict.dtd">
    <html>
      <head>
        <title>Menu Button Example</title>
    
        <script type="text/javascript" charset="utf-8" src="cordova.js"></script>
        <script type="text/javascript" charset="utf-8">
    
        // Wait for device API libraries to load
        //
        function onLoad() {
            document.addEventListener("deviceready", onDeviceReady, false);
        }
    
        // device APIs are available
        //
        function onDeviceReady() {
            // Register the event listener
            document.addEventListener("menubutton", onMenuKeyDown, false);
        }
    
        // Handle the menu button
        //
        function onMenuKeyDown() {
        }
    
        </script>
      </head>
      <body onload="onLoad()">
      </body>
    </html>