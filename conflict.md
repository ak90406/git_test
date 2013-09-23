前期準備
--------
1. 建立一個 repo
1. 建立一個純文字檔案 `file.txt`，內容為：

		AAAAAAAA
		BBBBBBBB
	
1. 加入 git 中、並 commit（`baseC`）。
1. 建立一個名為 `b1` 的 branch。此時 `master` 與 `b1` 的 HEAD 同時指向 `baseC`。


測試 1
------
1. 切到 `master`，將 `file.txt` 內容改為：

		AAAAAAAA
		XXXXXXXX
	
	並 commit（`mc1`）
1. 切到 `b1`，將 `file.txt` 內容改為：

		AAAAAAAA
		ZZZZZZZZ
	
	並 commit（`bc1`）
1. 切到 `master`，要求與 `b1` 作 merge。

結果1
-----
1. merging時，git會提示發生conflict：

>Auto-merging file.txt  
>CONFLICT(content)：Merge conflict in file.txt  
>Automatic merge failed；fix conflicts and then commit the result.

1. 開啟`file.txt`後會看到：

>AAAAAAAA  
>＜＜＜＜＜＜HEAD  
>XXXXXXXX  
>＝＝＝＝＝＝  
>ZZZZZZZZ  
>＞＞＞＞＞＞b1  

1. 在`file.txt1`中，`＜＜＜＜＜＜HEAD`到`＝＝＝＝＝＝`為止，出現了XXXXXXXX，這是masrer commit上的內容。
1. 而`＝＝＝＝＝＝`到`＞＞＞＞＞＞b1`為止，所出現的ZZZZZZZZ，是branch commit上的內容。
1. git會用分隔符號來區分出`file.txt`在master commit上與branch commit上不一樣的內容，手動修改檔案conflict後存檔，再次回到git進行commit就會完成merge動作。
