# Flutter环境搭建

1. 安装配置JDK

2. 安装AS，注意配置Android SDK目录

3. 安装Flutter SDK

   1. 下载，[下载地址](https://storage.googleapis.com/flutter_infra/releases/stable/windows/flutter_windows_v1.12.13+hotfix.8-stable.zip)

      ```powershell
      https://storage.googleapis.com/flutter_infra/releases/stable/windows/flutter_windows_v1.12.13+hotfix.8-stable.zip
      ```

   2. 安装，解压到没有权限要求的、没有空格的目录下

   3. 配置bin目录到path环境下

4. 配置Flutter国内镜像源

   ```powershell
   PUB_HOSTED_URL=https://pub.flutter-io.cn
   FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
   ```

   复制KEY-VALUE到环境变量中

5. 运行flutter doctor，可能会出现如下，最重要的是Android toolchain：

   ```powershell
   C:\Users>flutter doctor
   Doctor summary (to see all details, run flutter doctor -v):
   [√] Flutter (Channel stable, v1.12.13+hotfix.8, on Microsoft Windows [Version 10.0.1832.657], locale zh-CN)
   
   [!] Android toolchain - develop for Android devices (Android SDK version 29.0.3)
       ! Some Android licenses not accepted.  To resolve this, run: flutter doctor --android-licenses
   [√] Android Studio (version 3.5)
   [!] IntelliJ IDEA Ultimate Edition (version 2018.3)
       X Flutter plugin not installed; this adds Flutter specific functionality.
       X Dart plugin not installed; this adds Dart specific functionality.
   [!] Connected device
       ! No devices available
   
   ! Doctor found issues in 3 categories.
   
   C:\Users>
   ```

   这样解决运行，然后输入Y：

   ```powershell
   flutter doctor --android-licenses
   ```

   最后这样即可：

   ```powershell
   Doctor summary (to see all details, run flutter doctor -v):
   [√] Flutter (Channel stable, v1.12.13+hotfix.8, on Microsoft Windows [Version 10.0.18362.657], locale zh-CN)
   
   [√] Android toolchain - develop for Android devices (Android SDK version 29.0.3)
   [√] Android Studio (version 3.5)
   [!] IntelliJ IDEA Ultimate Edition (version 2018.3)
       X Flutter plugin not installed; this adds Flutter specific functionality.
       X Dart plugin not installed; this adds Dart specific functionality.
   [!] Connected device
       ! No devices available
   
   ! Doctor found issues in 2 categories.
   ```

   

6. 给开发工具AS或者VS CODE安装dart  flutter插件，配置Flutter SDK路径。

7. 完毕，注意Flutter项目名称，不能驼峰命名。