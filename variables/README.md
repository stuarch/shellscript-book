#學習使用shell
實作shellVariable.sh
使用echo
```shell
echo "This is a test!"
```
執行結果
This is a test!

建立變數
```shell
shvar="This is a test"
echo $shvar
```
執行結果
This is a test

編輯紀錄
```shell
ll $lastdir
```

假設要使用shell的程序執行的任務
```shell
allfiles=*
echo $allfiles
```
執行結果
印出所有目錄裡的檔案
shellVariable.sh

更改檔名
```shell
shvar="shellVariable.sh"
apple="123.sh"
mv $shvar $apple
```
執行結果
將檔案名稱shellVariable.sh更改成123.sh
