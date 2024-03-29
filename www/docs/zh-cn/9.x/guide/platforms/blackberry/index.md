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

title: 黑莓平台指南
---

# 黑莓平台指南

本指南介绍了如何设置用于目标应用程式的版本 10 之前的黑莓平台 SDK 环境。 如果你想要的目标的最新版本，请参阅黑莓 10 平台指南。 请参阅下列特定于平台的详细资讯：

*   [黑莓手机配置](config.html)
*   [升级黑莓手机](upgrading.html)
*   [黑莓手机的外挂程式](plugin.html)
*   [黑莓手机的命令列工具](tools.html)

上面的命令列工具请参阅Cordova 3.0 以前的版本。关于当前介面的资讯，请参阅命令列介面。

## 要求和支援

此版本的黑莓手机不支援由 `cordova` 所述的命令列介面，而是由一组单独的命令列工具的实用程式。 从[cordova.apache.org][1]下载的Cordova分布.

 [1]: http://cordova.apache.org/#download

Cordova的黑莓手机依赖于[黑莓 WebWorks 框架][2]，这是可用于 Windows XP （32 位），Windows 7 （32 位和 64 位） 和 Mac (OS X 10.6.4+)。 WebWorks 应用程式可以*只*在以下黑莓平台上部署：

 [2]: https://bdsc.webapps.blackberry.com/html5

*   黑莓 OS 5.0 和更高
*   黑莓 PlayBook
*   黑莓 10 (QNX)

WebWorks 需要 JAVA 开发工具组 (JDK)。 对于 Windows，使用 32 位版本的[Oracle JDK][3]。 JAVA 中的预设安装的 Mac OS X 上最新支援版本 10.7，这需要[单独安装][4]。 它还要求 Apache Ant 在 Mac 上是 JAVA 安装的一部分安装。 Windows 版本，从[ant.apache.org][5].

 [3]: http://www.oracle.com/technetwork/java/javase/downloads/index.html#jdk
 [4]: http://support.apple.com/kb/DL1421
 [5]: http://ant.apache.org/bindownload.cgi

## 安装 SDK

下载并安装适当的 WebWorks SDK，为您的发展。可以从以下位置下载黑莓 PlayBook 和黑莓智慧手机 WebWorks Sdk。

*   \[黑莓 PlayBook SDK\](HTTPs://developer.blackberry.com/html5/download/#playbook) 和[Adobe Air SDK][6]

*   \[黑莓智慧手机 SDK\]() HTTPs://developer.blackberry.com/html5/download/#smartphones

 [6]: http://www.adobe.com/devnet/air/air-sdk-download.html

## 登记册的签名金钥

如果您希望发布黑莓应用程式商店上的应用程式或在实际设备上，您会需要注册一套免费的代码签名金钥。 要这样做，请完成[黑莓键订单表单][7]。 一旦您收到你签署的钥匙，他们需要进行设置。 请参阅[黑莓 HTML5/WebWorks 网站][8]的资讯。

 [7]: https://www.blackberry.com/SignedKeys
 [8]: https://developer.blackberry.com/html5/documentation/signing_setup_bb10_apps_2008396_11.html

## 安装Cordova

下载并解压缩[Cordova][1]的最新副本.

## 设立了一个新的专案

*   打开一个命令列终端并导航到您解压缩Cordova。

*   那里是Cordova支援每个平台的目录。导航到 `blackberry` 目录。

*   `blackberry`目录中包含几个子目录。 `example`目录中包含一个完整的Cordova专案。 复制 `example` 目录到您的电脑上的另一个位置和导航到那里。

*   编辑 `project.properties` 档，以指定您使用的 WebWorks SDK。 例如，下面是黑莓 PlayBook，黑莓智慧手机 (OS5-7） 或黑莓 10 (QNX) 的各自设置：
    
        playbook.bbwp.dir=C:\\Program Motion\\BlackBerry WebWorks SDK 中 Files\\Research 为 TabletOS 2.1.0.6\\bbwp blackberry.bbwp.dir=C:\\Program Motion\\BlackBerry WebWorks Packager 在 Files\\Research qnx.bbwp.dir=C:\\Program 档 (86) \\Research In Motion\\BlackBerry 10 WebWorks SDK 1.0.2.9
        

这些参数对应于参数指定在生成您的专案时。首次运行这些命令，它们生成一个"HelloWorld"应用程式：

        Cordova/生成 playbook Cordova/生成黑莓Cordova/生成 qnx
    

和 SDK，您还需要注册的代码签名金钥和调试标记。 签名金钥允许您分发通过黑莓应用程式。 调试标记使您可以测试黑莓手机模拟器或设备上未签名的应用程式。 您不需要创建和安装调试标记自己 ；如果你提供的金钥库的密码，生成脚本创建，并为您安装调试标记。 若要设置签名金钥，请转到黑莓手机网站来得到它，确保保留您指定的密码。 然后运行 `blackberry-signer` 实用套装程式含的 SDK。 黑莓手机提供了更多的资讯在这里：

*   [注册您的代码签名金钥][9]

*   [设置您的电脑代码签名][10]

*   [设置您的 SDK 环境的综合指南][11]

 [9]: https://www.blackberry.com/SignedKeys/codesigning.html
 [10]: http://developer.blackberry.com/html5/documentation/set_up_for_signing.html
 [11]: http://developer.blackberry.com/native/documentation/bb10/com.qnx.doc.native_sdk.quickstart/topic/set_up_your_environment.html

## 部署到模拟程式

在 Windows 上，黑莓智慧手机模拟器，才可用。 黑莓 PlayBook 模拟器需要 VMWare 播放机 (Windows) 或 VMWare 融合 (Mac OS X）。 WebWorks SDK 提供了一个预设模拟器，但额外的模拟程式都[可以通过黑莓手机][12].

 [12]: http://us.blackberry.com/developers/resources/simulators.jsp

从专案目录中，键入 `./cordova/run <target>` ，更换 `<target>` 或 `qnx` ， `playbook` ，或 `blackberry` 。 请注意对于黑莓 10 和行动手册，必须已经启动模拟程式虚拟映射。

请参阅下列内容的详细资讯：

*   [黑莓 PlayBook][13]

*   [黑莓智慧手机][14]

 [13]: https://developer.blackberry.com/html5/documentation/using_the_tablet_simulator_1866980_11.html
 [14]: https://developer.blackberry.com/html5/documentation/run_your_app_on_smartphone_sim_1876976_11.html

对于黑莓 Playbook 编辑 `project.properties` 档以自订 `playbook.sim.ip` 和 `playbook.sim.password` 的属性。 可通过**设置**应用程式主画面上模拟程式的 IP 位址。 启用**的安全和隐私 → 发展模式**选项，以显示该位址。 此外可以在**安全和隐私**选项卡中设置密码。

对于黑莓智慧手机，编辑 `project.properties` 档以自订 `blackberry.sim.dir` 和 `blackberry.sim.bin` 的属性。 您需要在 Windows 上，例如指定目录路径时逃脱的路径分隔符号：`C:\\Program
Files\\BlackBerry\\Simulator`.

一旦该模拟程式已安装并运行，运行任一以下操作以安装到主画面的应用程式：

        Cordova/运行 playbook Cordova/运行黑莓
    

如果设备连接到您的电脑是否提示您时，回答否。

**注：**上黑莓 OS 5，该应用程式安装在 `Downloads` 目录。

## 将部署到设备

要将您的应用程式部署到一个设备，它必须连接，和您必须注册为代码签名金钥，如上文所述。 也、 要部署应用程式对黑莓 PlayBook**设置 → 安全 → 发展模式**必须启用选项。

在黑莓 PlayBook 上编辑 `project.properties` 档和修改以下以反映该设备的 IP 和密码作为配置上面，一直以来与您设置的签名私密金钥密码：

从专案目录中，键入 `./cordova/run <target>` ，更换 `<target>` 或 `qnx` ， `playbook` ，或`blackberry`.

在黑莓智慧手机 (OS5-7），指定 `blackberry.sigtool.password` 属性作为签名的私密金钥密码。

然后从该专案的目录，运行你会在模拟程式中查看该应用程式的命令之一：

        Cordova/运行 playbook Cordova/运行黑莓
    

如果设备连接到您的电脑是否提示您时，回答是。

**注：**上黑莓 OS 5，该应用程式安装在 `Downloads` 目录。

## 附加资讯

下面的文章可能说明您解决常见的问题，开发的黑莓 WebWorks 框架生成的应用程式时：

*   [黑莓 WebWorks 发展陷阱][15]

*   [包装 WebWorks 应用程式的最佳做法][16]

 [15]: http://supportforums.blackberry.com/t5/Web-and-WebWorks-Development/Common-BlackBerry-WebWorks-development-pitfalls-that-can-be/ta-p/624712
 [16]: https://bdsc.webapps.blackberrycom/html5/documentation/ww_developing/bestpractice_compiling_ww_apps_1873324_11.html