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

title: 亚马逊火 OS 外挂程式
---

# 亚马逊火 OS 外挂程式

按照有关的开发自订外挂程式概述 Android 外挂程式指南中提供的说明。

## 回声亚马逊火 OS 外挂程式示例

若要匹配的 JavaScript 介面*回波*特征描述的应用程式外挂程式，使用 `plugin.xml` 来注入 `feature` 到本地平台规范 `config.xml` 档：

    <platform name="amazon-fireos">
        <config-file target="config.xml" parent="/*">
            <feature name="Echo">
                <param name="android-package" value="org.apache.cordova.plugin.Echo"/>
            </feature>
        </config-file>
    </platform>
    

然后添加以下到 `src/org/apache/cordova/plugin/Echo.java` 档：

    package org.apache.cordova.plugin;
    
    import org.apache.cordova.CordovaPlugin;
    import org.apache.cordova.CallbackContext;
    
    import org.json.JSONArray;
    import org.json.JSONException;
    import org.json.JSONObject;
    
    /**
     * This class echoes a string called from JavaScript.
     */
    public class Echo extends CordovaPlugin {
    
        @Override
        public boolean execute(String action, JSONArray args, CallbackContext callbackContext) throws JSONException {
            if (action.equals("echo")) {
                String message = args.getString(0);
                this.echo(message, callbackContext);
                return true;
            }
            return false;
        }
    
        private void echo(String message, CallbackContext callbackContext) {
            if (message != null && message.length() > 0) {
                callbackContext.success(message);
            } else {
                callbackContext.error("Expected one non-empty string argument.");
            }
        }
    }
    

如果你想要重用的亚马逊火 OS 平台 Android 外挂程式代码然后修改通过指向 `android` 特定的原始档案。例如，

    <platform name="amazon-fireos">
        <config-file target="config.xml" parent="/*">
            <feature name="Echo">
                <param name="android-package" value="org.apache.cordova.plugin.Echo"/>
            </feature>
        </config-file>
        <source-file src="src/android/Echo.java" target-dir="src/org/apache/cordova/plugin" />
    </platform>
    

如果你想要编写自订的外挂程式的亚马逊火 OS 平台，然后创建一个名为资料夹 `amazon` 下你的外挂程式 src / 资料夹和修改通过为指向 `amazon` 特定的原始档案。 例如，

    <platform name="amazon-fireos">
        <config-file target="config.xml" parent="/*">
            <feature name="Echo">
                <param name="android-package" value="org.apache.cordova.plugin.Echo"/>
            </feature>
        </config-file>
        <source-file src="src/amazon/Echo.java" target-dir="src/org/apache/cordova/plugin" />
    </platform>
    

## 在你的外挂程式中使用亚马逊 web 视图

Cordova的亚马逊火 OS 使得使用的基于开放源码铬专案的自订亚马逊 web 视图。它是 GPU 加速和优化的流体性能上点燃火。

若要了解如何以最佳方式在您的专案中使用亚马逊 web 视图，查阅[亚马逊开发人员门户][1].

 [1]: https://developer.amazon.com/sdk/fire/IntegratingAWV.html