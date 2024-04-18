from [https://github.com/fatedier/frp](https://github.com/fatedier/frp)

构建指令
```bash
go install golang.org/x/mobile/cmd/gomobile@latest
gomobile init
go get golang.org/x/mobile/bind
gomobile bind -androidapi 21 ./cmd/frpc
```

项目根目录下生成如下产物 \
`frpclib.aar` \
`frpclib-sources.jar`

将`frpclib.aar`导入Android项目
```kotlin
implementation(files("libs/frpclib.aar"))
```

在Android中的使用
```kotlin
Frpclib.run(configFilePath)
```
