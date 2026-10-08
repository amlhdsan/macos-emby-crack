# macos-emby-crack
macOS 破解 emby 官方客户端（也适用于 iOS）

目前（26/10/8）仍旧有效

方法：

1. 首先 App Store 下载 ShadowRocket 软件，此处建议 3 刀买下，因为 iOS 也能非常方便地进行使用并破解，二者方法几乎相同。
2. 打开 ShadowRocket，点击左侧「配置」，「本地文件」下会显示「default.conf」（此处任意 .conf 文件都可以）。
3. 右键（iOS 上是长按），点击「编辑纯文本」，并在文件末尾（最下方）加上：
   ```
   [Script]
   EmbyPremiere = type=http-response,script-path=https://gitlab.com/iptv-org/embypublic/-/raw/master/Script/EmbyPremiere.js,pattern=^https?:\/\/mb3admin.com\/admin\/service\/registration\/validateDevice,max-size=131072,requires-body=true,timeout=10,enable=true
   [MITM]
   hostname = mb3admin.com
   ```
4. 点击保存
5. 再次右键，点击「编辑配置」，点击「HTTPS」解密，打开「HTTPS 解密」，此时，系统会提示进行证书安装。

对于 iOS 用户，请移步[文章](https://embywiki.feverss.cloud/use-on-various-devices/use-on-ios/use-official-client/shi-yong-shadowrocket-po-jie)，讲的很详细。

对于 macOS 用户，点击安装证书，首先会下载证书，会使用默认浏览器下载「ca.cer」证书，双击打开，完成系统验证，然后，在 spotlight 搜索中找到 app（或者在『应用程序』中，『实用工具』文件夹内有）『钥匙串访问』，打开之后，左边选择「系统（system）」，最右边「证书（certificates）」，下面会显示一个带有红叉叉的，名字为「Shadowrocket+日期+时间」的一个证书，双击，展开「信任』一栏，将「使用此证书时」选项后，选择「始终信任」，然后完成系统验证即可完成安装。

回到小火箭界面，已经显示「系统信任』，即可回到主界面。然后点击主界面「未连接」右面的开关，系统会提示「添加 VPN 配置」，点击同意即可。

现在打开 emby，已经完成破解。
