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

title: 隐私指南
toc_title: 隐私管理
---

# 隐私指南

手机隐私是每个应用程式开发者必须解决的关键问题。 您的使用者期望将搜集他们的私人资讯，并由您的应用程式得到适当的处理。此外，有越来越多的现在有关于手机隐私惯例的法律要求司法管辖区。

本指南中的移动应用程式的隐私应被视为一*底漆*处理一些最重要的问题。 它概述了人们广泛接受的一些最佳做法，并提供到其他更详细的指南和参考参考。

*   **私隐政策**： 您的应用程式应包括私隐政策，解决什么样的资讯应用程式收集来自或关于您的使用者、 如何使用这些资讯，与谁它共用的和如何使用者可以在应用程式内私隐有关的选择等主题。以说明理解，你应该使用普通语言和避免技术术语。 你应该使您的隐私权原则可供使用者之前下载，如审查的 app 描述中的应用市场。 此外，应使您的隐私权原则可用在该应用程式本身的范围内。 有限的行动装置的显示大小创建用于向使用者显示私隐政策的挑战。 考虑发展一种*缩写形式*的政策，其中包括最重要的资讯，，然后在更多的细节感兴趣的人提供一个连结到"长表"政策。 几个小组正试图开发基于图示通信隐私惯例，你可能想要考虑一旦这些标准成熟的标准。

*   **敏感资讯的收集**： 敏感的个人资讯的应用程式的集合将引发重要隐私问题。 敏感的个人资讯的例子包括敏感的财务资讯，健康的资讯，并从或儿童的资讯。 它还包括从某些感应器和通常发现行动装置和平板电脑、 地理定位资讯、 连络人/电话簿、 麦克风/相机和存储的图片视频等的资料库收集的资讯。 请参见以下文档页的详细资讯：[相机][1]、[捕获][2]、[连络人][3]和[地理定位][4]。 一般情况下，您应该获得使用者的明确许可之前收集敏感资讯，如果可能的话，提供一种控制机制，使使用者可以轻松地更改许可权。 应用程式的作业系统可以说明在某些情况下提出只是时间的对话方块，要求使用者的许可权前集合。 在这些情况下，一定要利用任何机会，若要自订对话方块的框文本，以澄清如何应用程式使用，并且，如果适用，将共用此类资讯。

*   **避免使用者惊喜**： 如果应用程式收集或使用中可能向使用者根据您的应用程式 （例如，访问存储的图片的音乐播放机） 的主要目的令人惊讶的方式的资讯，你应该带类似的步骤作为敏感个人资讯的收集。 这就是，你强烈应考虑只是时间对话方块通知使用者有关集合或该资讯的使用，并提供一个相应的隐私控制项，如果合适的话，的使用。

*   **协力厂商资料收集或分享**： 如果你的应用程式收集到另一家公司 — — 提供的资讯，如一个社交网路平台或广告网路 （例如，如果您的应用程式会显示广告) — — 你应该告知该集合的使用者和共用。 至少，您的隐私权原则应该描述资讯收集和共用和，如果合适的话，为您的使用者提供控制能力或退出这种集合或共用。

*   **集合限制和安全**： 您的使用者委托他们的资讯与您的应用程式，他们期望你将会采取适当的安全防范措施来保护它。 避免个人资讯的安全妥协的最佳方法之一并不是在第一次的地方收集的资讯，除非您的应用程式具有集合的一个具体和合法的商业原因。 不会需要收集的资讯，确保你提供适当的安全控制，以保护该资讯，无论它存储在设备上或在您的后端伺服器上。 您还应开发这款应用和后端伺服器上实施适当的资料保留原则。

 [1]: cordova_camera_camera.md.html
 [2]: cordova_media_capture_capture.md.html
 [3]: cordova_contacts_contacts.md.html
 [4]: cordova_geolocation_geolocation.md.html

以下是一些其他有用手机隐私指南，开发人员：

*   加州总检察长[私隐去： 移动生态系统的建议][5]

*   民主与技术，隐私论坛，[为手机应用程式开发人员的最佳做法][6]的未来中心

*   CTIA 无线协会、[最佳做法和准则的位置基于服务][7]

*   联邦贸易委员会，[手机隐私披露： 建立信任通过透明度][8]

*   [应用隐私][9]网站隐私论坛的未来

 [5]: http://oag.ca.gov/sites/all/files/pdfs/privacy/privacy_on_the_go.pdf
 [6]: http://www.futureofprivacy.org/wp-content/uploads/Best-Practices-for-Mobile-App-Developers_Final.pdf
 [7]: http://www.ctia.org/business_resources/wic/index.cfm/AID/11300
 [8]: http://www.ftc.gov/os/2013/02/130201mobileprivacyreport.pdf
 [9]: http://www.applicationprivacy.org