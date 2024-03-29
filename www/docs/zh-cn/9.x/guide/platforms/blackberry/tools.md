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

title: 黑莓手机的命令列工具
---

# 黑莓手机的命令列工具

`cordova`命令列实用程式是一个高级别的工具，允许您在一次跨几个平台生成的应用程式。 旧版本的Cordova框架提供了特定于每个平台的命令列工具集。 若要使用它们作为 CLI 的替代，您需要从[cordova.apache.org][1]下载此版本的Cordova。 下载档案中包含单独的档案，为每个平台。 展开您想要的目标平台。 这里描述的工具，通常可用在顶级 `bin` 目录中，否则为咨询**自述**档，了解有关更多详细的指示。

 [1]: http://cordova.apache.org

## 创建一个专案

运行 `create` 命令，指定的现有路径的专案、 反向域式包识别码和应用程式的显示名称。这里是 Mac 和 Windows 的语法：

    $ /path/to/cordova-blackberry-webworks/bin/create /path/to/my_new_project com.example.project_name ProjectName
    $ /path/to/cordova-blackberry-webworks/bin/create.bat /path/to/my_new_project com.example.project_name ProjectName
    

**注：**黑莓平台忽略套装软体名称的预留位置 ( `com.example.project_name` )，但它已仍需使用的跨平台的工具。

## 生成专案

对于黑莓手机的专案，请确保您自订 `project.properties` 在Cordova专案的根目录中的档。 你需要提供你的黑莓手机签名金钥的密码，这样做并指定黑莓 WebWorks SDK 和黑莓模拟程式的可执行档的位置。

    $ /path/to/my_new_project/cordova/build <platform>
    $ /path/to/my_new_project/cordova/build.bat <platform>
    

## 启动模拟程式

对于黑莓手机的专案，请确保您自订 `project.properties` Cordova专案目录的根目录中的档。 你需要提供你的黑莓手机签名金钥的密码，这样做并指定黑莓 WebWorks SDK 和黑莓模拟程式的可执行档的位置。

    $ /path/to/my_new_project/cordova/run <platform>
    

然后选择 '否' 时提示您：

    你有一个黑莓设备连接到您的电脑吗？(y/n) $ /path/to/my_new_project/cordova/run < 平台 >
    

然后选择 '否' 时提示您：

    你有一个黑莓设备连接到您的电脑吗？(y /) n
    

## 日志记录

不幸的是，流直接从设备日志是目前不支援的。 然而，黑莓手机提供了内置 Web 检查器支援 Playbook 和黑莓智慧手机设备运行黑莓 OS 7.0 及以上。 您还可以访问您的应用程式日志 (包括对任何调用 `console.log` ） 在您的设备，在按住 ALT 键从主画面和键入 lglg 键上。