# CG Kit

## Table of Contents
* [Introduction](#introduction)
* [Getting Started](#getting-started)
* [Supported Environments](#supported-environments)
* [Result](#result)
* [License](#license)
## Introduction
　　CGKit sample code encapsulates APIs of the Vulkan. It provides many sample programs for your reference or usage.<br>
　　The following describes heads files of sample code.<br>

　　1. [SDK DOWNLOAD](https://developer.huawei.com/consumer/en/doc/development/HMSCore-Library-V5/sdk-download-0000001050441521-V5) |--cgsdk-vulkanframework headers<br>
Folder or File|Description
----|----
　　include/CGRenderingFramework/Application:|Head file of plantform apis.<br>
　　include/CGRenderingFramework/Core:|Head file of instantiate apis.<br>
　　include/CGRenderingFramework/Log:|Head file of log system apis.<br>
　　include/CGRenderingFramework/Math:|Head file of math apis.<br>
　　include/CGRenderingFramework/nolhmann:|Head file of json apis.<br>
　　include/CGRenderingFramework/Rendering:|Head file of rendering apis.<br>
　　include/CGRenderingFramework/Resource:|Head file of rendering resource apis.<br>
　　include/CGRenderingFramework/Scene:|Head file of rendering scene apis.<br>
　　include/CGRenderingFramework/Utils:|Head file of param apis.<br>
  
　　2. cgsdk-vulkanframework libs<br>
  Folder or File|Description
----|----
　　libs/arm64-v8a/libcgkit.so:|64 bit<br>
　　libs/armeabi-v7a/libcgkit.so:|32 bit<br>

　　3. cgsdk-plugin-base libs<br>
   Folder or File|Description
----|----
　　libs/arm64-v8a/libPluginInterface.so:|64 bit<br>
　　libs/armeabi-v7a/libPluginInterface.so:|32 bit<br>

　　4. cgsdk-plugin-offlinesuperresolution headers in lib/cgsdk-plugin/cgsdk-plugin-offlinesuperresolution<br>
   Folder or File|Description
----|----
　　pkg-for-cgsdk/include:|Head file of OSRPlugin apis.<br>
  
　　5. cgsdk-plugin-offlinesuperresolution resources in /lib/cgsdk-plugin/cgsdk-plugin-offlinesuperresolution<br>
   Folder or File|Description
----|----
　　pkg-for-cgsdk/assets:|Resource file of OSRPlugin.<br>
  
　　6. cgsdk-plugin-offlinesuperresolution libs in Software/lib/cgsdk-plugin/cgsdk-plugin-offlinesuperresolution<br>
   Folder or File|Description
----|----
　　pkg-for-cgsdk/libs/arm64-v8a/libcgkit_plugin_offlineSupRes.so:|64 bit

## Getting Started
　　1. Check whether the Android studio development environment is ready. Open the sample code project directory with file "build.gradle" in Android Studio. Run TestApp on your device or simulator which have installed latest Huawei Mobile Service(HMS).<br><br>
　　2. Register a [HUAWEI account](https://developer.huawei.com/consumer/en/).<br><br>
　　3. Create an app, generate a signing certificate and configure the app information in AppGallery Connect.<br>
   　　See details: [HUAWEI CGKit Development Preparation](https://developer.huawei.com/consumer/en/doc/development/HMSCore-Guides/environment-req-0000001050200019)<br><br>
　　4. To build this demo, please first import the demo in the Android Studio (3.5+).<br><br>
　　5. Configure the sample code:<br>
　　　(1) Change the value of applicationid in the app-level build.gradle file of the sample project to the package name of your app.<br>
　　　(2) Add signing certificate(.jks) to the root directory, and change the value of signingConfigs in the app-level build.gradle file of the sample project.<br>
　　　(3) Create your own models and materials according to [CG Development Guide](https://developer.huawei.com/consumer/en/doc/development/HMSCore-Guides/demo-data-process-0000001050200023).<br>
　　　(4) Add Rendering Framework SDK, cgsdk-plugin-base SDK and cgsdk-plugin-offlinesuperresolution SDK to following direcotories.<br><br>
    　　　　[Rendering Framework SDK]<br>
    　　　　Add include directory in SDK to your own project(src/cpp/include).<br>
    　　　　Add libs/arm64-v8a/libcgkit.so in SDK to your own project(libs/arm64-v8a).<br>
    　　　　Add libs/armeabi-v7a/libcgkit.so in SDK to your own project(libs/armeabi-v7a).<br><br>
    　　　　[cgsdk-plugin-base SDK]<br>
    　　　　Add libs/arm64-v8a/libPluginInterface.so in SDK to your own project(libs/arm64-v8a).<br>
    　　　　Add libs/armeabi-v7a/libPluginInterface.so in SDK to your own project(libs/libPluginInterface-v7a).<br><br>
    　　　　[cgsdk-plugin-offlinesuperresolution SDK]<br>
    　　　　Add pkg-for-cgsdk/include/OSRPluginCommon.h in SDK to your own project(src/main/cpp/include/OSRPlugin).<br>
    　　　　Add pkg-for-cgsdk/assets/ie_data.bin in SDK to your own project(src/main/assets/resource).<br>
    　　　　Add pluginList directory in SDK to your own project(src/main/assets).<br>
    　　　　Add libs/arm64-v8a/libcgkit_plugin_offlineSupRes.so in SDK to your own project(OSRPlugin/arm64-v8a).<br>
    
　　6. Run the sample on your Android device or emulator for vulkan rendering demo.<br><br>
　　7. Run the sample on your Android device or emulator for offlinesuperresolution plugin demo:<br>
   　　　(1) Run run.bat in app/src/main/assets/resource directory.<br>
   　　　(2) Dobule tap screen.<br>
   　　　(3) Pull the result file form directory /sdcard/Android/data/${package}/files, using command:<br>
    　　　　`adb pull /sdcard/Android/data/com.hisi.CGRenderFrameworkDemo/files/output_ie_sync.ppm.`<br>

## Supported Environments
　　1. Devices with Android 8.0 or later.<br>
　　2. Devices with Vulkan1.0 or Vulkan1.1.<br>

## Result
　　<img src="CGRenderResult.jpg" width="30%" height="30%">
## License
　　The sample of CGKit has obtained the [Apache 2.0 license.](http://www.apache.org/licenses/LICENSE-2.0).
