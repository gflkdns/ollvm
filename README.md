# ollvm

在原有ollvm基础上,增加控制流混淆,方法混淆,调用混淆,字符串混淆

这绝对是能节省你大量时间的一个仓库

mac平台编译好的ollvm混淆,只需下载解压到 /Users/username/Library/Android/sdk/ndk/21.1.6352462/toolchains/llvm/prebuilt/darwin-x86_64/ 目录即可然后覆盖即可

github有上传文件大小限制,去这个下载链接自取:https://download.csdn.net/download/qq_27512671/87768350

然后添加如下配置即可开启混淆:

```
    defaultConfig {
        minSdk 21
        consumerProguardFiles "consumer-rules.pro"
        ndkVersion "21.1.6352462"
        externalNativeBuild {
            cmake {
                cppFlags "-mllvm -sub -mllvm -sobf -mllvm -fla -mllvm -bcf"
            }
        }
    }
```
