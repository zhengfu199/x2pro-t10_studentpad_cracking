# 解锁Bootloader教程
## 注意事项
目前只能在Linux下进行解锁，如果解锁，数据100%会消失，请做好觉悟再看下面的教程
## 文件下载
### 在whhhhh的网盘上，具体是在“破解文件”文件夹里有个“[小白勿用]Unlock Bootloader.zip”，将其下载下来备用
## 详细步骤
### 你得先在开发者模式打开“OEM解锁”，然后将设备重启到bootloader模式下，请执行以下命令
```adb reboot bootloader```
### 给定制的fastboot赋权，不然无法正常进行后面的步骤
```chmod +x ./fastboot```
### 进行get_identifier_token
```./fastboot oem get_identifier_token```
### 得到identifier_token之后，我们就可以进行真正的解锁了
```chmod +x ./signidentifier_unlockbootloader.sh
./signidentifier_unlockbootloader.sh 这里填上你得到的identifier_token(一串数字，如果是两行的就拼接为一行) rsa4096_vbmeta.pem signature.bin
./fastboot flashing unlock_bootloader signature.bin
```
### 然后回过去关注平板，按音量下键进行解锁
### 自此，解锁过程结束
### telegram channel（防失连群）：https://t.me/+rCs1ouVhrUU1YTFl
### The Guide was written in 2023/3/2 by laohua2333
