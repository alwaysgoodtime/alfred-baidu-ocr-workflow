# alfred-baidu-ocr-workflow

一个alfred的OCR workflow，可以将pdf书籍通过截图来识别为文字

代码来自mengbo的https://github.com/mengbo/baidu-ocr

本项目只是简单对其进行了alfred的移植。

环境依赖：测试平台为macOS, 需要装的软件有homebrew，pngpaste（图片转为base64编码）、jq（格式化返回值）、opencc（繁体转简体，可不使用，如果无需此功能，需修改workflow里的脚本）

## 使用指南：

1. 在百度智能云 => 产品服务 => 人工智能 => 文字识别 中创建应用，同时获取对应的API Key 和 Secret Key。

2. 将对应的API Key和Secret Key填入Environment Variables的AK与SK位置

   (Environment Variables在workflow右上角画[X]的位置)

3. 使用homebrew安装pngpaste、jq、opencc

   ~~~shell
   brew install pngpaste
   brew install jq
   brew install opencc
   ~~~

4. 在Alfred中输入OCR，按下回车，进行截图，文字如果识别成功，会自动放入剪贴板。（在过程中可能需要授予Alfred相应权限）

   