# Github Action Build OpenWRT Series
## 这是什么
这是一个使用Github Action编译OpenWRT相关的工具，你可以编译最新的OpenWRT或LEDE、或者编译单个包。
## 如何使用
**编译单个包**
1. 给个Star以表支持
2. Fork当前仓库
3. 在device文件夹中增加你设备的config，文件夹中默认包含`x86_64`、`Newifi3 D2`配置
4. 修改.github/workflows/build-openwrt-package.yml
   - `SDK_URL`修改为你的OpenWRT版本的SDK下载地址，可以在 https://downloads.openwrt.org/releases/ 中找到你的OpenWRT版本的SDK。如`https://downloads.openwrt.org/releases/22.03.2/targets/x86/64/openwrt-sdk-22.03.2-x86-64_gcc-11.2.0_musl.Linux-x86_64.tar.xz`
   - `CONFIG_FILE`修改为你的设备的配置文件。如`device/x86-64.config`
   - `PACKAGE_REPO`修改为你的包仓库地址。如`https://github.com/yichya/luci-app-xray.git`
   - `PACKAGE_NAME`修改为你的包名，可自定义。如`luci-app-xray`
   - `PACKAGE_BRANCH`修改为你的包的分支。如`master`
5. 选择仓库页面的Action，选择你的workflows，如`Build OpenWRT Package`，选择`Run workflow`，点击`Run workflow`即可运行编译。
6. 编译成功后，在Action的Workflow页面可以下载bin压缩包。
