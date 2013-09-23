準備工作
------
1. 建立一個repo
1. 建立三個純文字文件：`A.txt`、`B.txt`、`C.txt`，個別輸入

          A.txt：FileA
          
          B.txt：FileB
          
          C.txt：FileC

加入repo中並commit為`BasicC`

1. 建立一個branch`B1`，此時`master`和`B1`的HEAD都指向`BasicC`

測試1
--------
1. 切換HEAD到`B1`上，刪除`A.txt`檔案，並commit為`b1c`
1. 回到master，刪除`B.txt`檔案，並commit為`mc`
1. 合併兩個branch

結果1
-----
1. 在刪除`A.txt`及`B.txt`時，要先輸入`git add --all`，之後才能commit。
1. 將`B1`merge到`master`後，`A.txt`及`B.txt`都被刪除了，git顯示：

>Removing A.txt  
Merge made by the 'recursive' strategy.  
A.txt | 1-  
1 file changed, 1 deletion(-)  
delete mode 100644 A.txt
