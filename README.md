# LeanCloud Unity SDK


## 发布说明

目前 SDK 是通过服务端的 CI 进行构建以及发布版本，因此这个仓库不会包含源代码只是定期在 [Release](https://github.com/leancloud/unity-sdk/releases) 里面发布最新版本的。

## 版本号
版本号以日期+构建序列号组成，例如 v20170113.2 表示这个版本是 2017 年 1 月 13 号的当天的第 2 次 build。
建议大家一律下载最新版本即可，除非 Unity 自身存在版本兼容，否则 LeanCloud Unity SDK 一般意义上都支持所有版本的 Unity 开发，目前推荐 Unity 版本最好在 5.3 +。


### 已知问题
根据用户的反馈目前得知一些已知问题：

`UnityEditor.iOS.Extensions.Xcode.dll` 这个类库每一个版本的 Unity 都会不一样，但是根据社区反馈：

 - [FileNotFoundException when using Xcode API](http://answers.unity3d.com/questions/1148953/jenkins-failing-on-unityeditoriosextensionsxcode.html)
 - [Jenkins failing on UnityEditor.iOS.Extensions.Xcode](http://answers.unity3d.com/questions/1016975/filenotfoundexception-when-using-xcode-api.html)

 因此为了确保正常使用，你必须在项目里面显示的引用这个库到您的 Assets 文件夹下

 具体路径：

- Windows -假设您的 Unity 安装在 C 盘的，那么对应的路径如下： `C:\Program Files\Unity\Editor\Data\UnityExtensions\Unity\Advertisements\Editor\UnityEditor.iOS.Extensions.Xcode.dll`
- Mac OS - `/Applications/Unity/Unity.app/Contents/UnityExtensions/Unity/Advertisements/Editor/UnityEditor.iOS.Extensions.Xcode.dll`

注意，当前 SDK 为了让开发者迅速的体验 SDK，已经默认内置了一个 Unity v5.3 所包含 `UnityEditor.iOS.Extensions.Xcode.dll`，为了确保开发者不踩这个坑，最好还是引用您当前版本下 Unity 所对应的这个 dll 文件。


## Release Notes

#### 2017-01-17
1. Unity SDK 2.0 正式发布
2. 暂时下架了统计和推送相关的接口，之后的版本会补充



