# Busybox
執行 `busybox --list`可以看到命令列表。

##ash
建立一個符合 POSIX 的一個簡單的shell
Shell：一個文字介面底下讓我們與系統溝通的一個工具介面

##awk
一種的文本處理工具，awk將文件作為紀錄序列處理，文件內容的每行都是一個記錄。每行內容都會被分割成一系列的域，因此，我們可以認為一行的第一個詞為第一個域，第二個詞為第二個。
EX：文件example中只有一行內容，內容為：```abc ABC .123``` ，則```$0```代表整行，```$1```代表```abc```，```$2```代表```ABC```，```$3```代表```.123```
 
Print:

```sh 
awk '{print $0,$1,$2,$3}' example
```

輸出結果：`abc ABC .123 abc ABC .123`
可以透過-F來修改域分隔符(預設為空格)

```sh 
awk -F"." '{print $0 "--" $1 "--" $2}' example
```
輸出結果：`abc ABC .123--abc ABC--123`

##cat
聯結一個或多個檔案，使用正規表示法輸出。

EX：
顯示README文件中的內容

`cat README`

將顯示的輸出指定到某個檔案
```sh
cat text1.txt > text2.txt
#以覆完全蓋的方式將text1.txt的內容覆蓋於text2.txt
cat text1.txt >> text3.txt
#以附加的方式將text1.txt的內容放在text3.txt的最後
```
