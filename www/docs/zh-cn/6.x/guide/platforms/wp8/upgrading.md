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

title: 升级 Windows Phone
---

# 升级 Windows Phone

本指南演示如何修改 Windows Phone 的专案，这两个版本 7 和 8，从Cordova的旧版本进行升级。 大多数这些说明适用于与旧集的前面的命令列工具创建的专案 `cordova` CLI 实用程式。 命令列介面资讯，请参阅如何更新的 CLI 版本。 以下部分显示了如何从非 CLI 专案升级。

## 从 3.1.0 升级到 3.2.0

为创建的Cordova CLI 的专案：

1.  更新 `cordova` CLI 版本。请参阅命令列介面。

2.  运行 `cordova platform update wp8` （或 `wp7` ，每添加到您的专案的平台）。

对于不使用 CLI Cordova创建的专案，请运行：

        bin\update <project_path>
    

## 从 3.0.0 升级到 3.1.0

为创建的Cordova CLI 的专案：

1.  更新 `cordova` CLI 版本。请参阅命令列介面。

2.  运行 `cordova platform update wp8` （或 `wp7` ，每添加到您的专案的平台）。

对于不使用 CLI Cordova创建的专案，请运行：

        bin\update <project_path>
    

## 从 2.9.0 升级到 CLI （3.0.0)

1.  创建新的 Apache Cordova 3.0.0 专案使用 CLI，Cordova，如所述的命令列介面。

2.  添加您的平台到Cordova专案中，例如：`cordova
platform add wp7 wp8`.

3.  该专案的内容复写 `www` 目录到 `www` 目录在您刚刚创建的Cordova专案的根目录。

4.  复制或覆盖任何本机资产从原始专案 （ `SplashScreen` ， `ApplicationIcon` 等等），这让确定要添加的任何新档 `.csproj` 档。 Windows 电话里面的专案生成 `platforms\wp7` 或 `platforms\wp8` 目录。

5.  使用Cordova CLI 工具来安装您需要的任何外挂程式。请注意 CLI 处理所有核心 Api 作为外挂程式，所以他们可能需要添加。只有 3.0.0 外挂程式是与 CLI 相容。

6.  生成并测试。

## 从 2.9.0 升级到 3.0.0 (非 CLI)

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 3.0.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  复制并覆盖任何闪屏或图示图像。

4.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

5.  生成并测试。

**注**： 所有核心 Api 从Cordova版本 3.0 中, 移除和作为外挂程式必须单独安装。 关于如何重新启用非 CLI 的工作流中的这些功能的详细资讯，请参阅使用 Plugman 到管理外挂程式。

## 从 2.8.0 升级到 2.9.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.9.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新的名称 `cordova.js` 的 HTML 标签，如果它仍在使用Cordova VERSION.js (应该是刚中`cordova.js`).

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们也添加到.csproj 档。

6.  生成并测试。

## 从 2.7.0 升级到 2.8.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.8.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova.js` 档。（注意档案名中的版本号的缺乏。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.6.0 升级到 2.7.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.7.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.7.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.5.0 升级到 2.6.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.6.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.6.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.4.0 升级到 2.5.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.5.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.5.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.3.0 升级到 2.4.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 或 WP8 2.4.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.4.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.2.0 升级到 2.3.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建新的 Apache Cordova WP7 2.3.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.3.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.1.0 升级到 2.2.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建新的 Apache Cordova WP7 2.2.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.2.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 2.0.0 升级到 2.1.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建新的 Apache Cordova WP7 2.1.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.1.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 1.9.0 升级到 2.0.0

有很大变化到 Apache Cordova 2.0.0 WP7 专案结构，使这升级有点更多涉及的其他人。 本质上这不是升级而建立一个新的专案和对现有原始程式码档的副本。

在 Visual Studio 的解决方案资源管理器视窗中：

1.  创建一个新的 Apache Cordova WP7 2.0 专案。

2.  将复制的内容你 `www` 目录到新的专案，并确保这些专案添加到 VS 专案。

3.  更新您的 html 代码，使用新的 `cordova-2.0.0.js` 档。

4.  复制并覆盖任何闪屏或图示图像。

5.  复制超过任何外挂程式从 `plugins` 目录到新专案，并确保他们还补充说到 VS 专案。

6.  生成并测试。

## 从 1.8.0 升级到 1.9.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.9.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.9.0.js` 档。

## 从 1.7.0 升级到 1.8.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.8.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.8.0.js` 档。

## 从 1.6.0 升级到 1.7.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.7.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.7.0.js` 档。

## 从 1.6.0 升级到 1.6.1

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.6.1.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.6.1.js` 档。

## 从 1.5.0 版升级到 1.6.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.6.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.6.0.js` 档。

## 从 1.4.0 升级到 1.5.0 版

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.5.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.5.0.js` 档。

## 从 1.3.0 升级到 1.4.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.4.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.4.0.js` 档。

## 从 1.2.0 升级到 1.3.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.3.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.3.0.js` 档。

## 从 1.1.0 升级到 1.2.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.2.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.2.0.js` 档。

## 从 1.0.0 升级到 1.1.0

在 Visual Studio 的解决方案资源管理器视窗中：

1.  删除 `GapLib/WP7CordovaClassLib.dll` 从您的专案。

2.  移除对的引用 `WP7CordovaClassLib` **的引用**的目录中。

3.  **引用**上按一下滑鼠右键，然后选择**增加参考**.

4.  导航到新分布和添加 `WP7CordovaClassLib.dll` 档。
    
    **注**： 您可以通过在引用上右击并选择**属性**查看 DLL 的版本.

5.  复制新 `cordova-1.1.0.js` 到您的专案。（请确定它被标记为内容）。

6.  更新您的 html 代码，使用新的 `cordova-1.1.0.js` 档。