# ollvm

mac平台编译好的ollvm混淆,只需下载解压到 /Users/username/Library/Android/sdk/ndk/21.1.6352462/toolchains/llvm/prebuilt/darwin-x86_64/ 目录即可然后覆盖即可

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
