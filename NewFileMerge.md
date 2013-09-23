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
1. 切到 `b1`，將 `file.txt` 內容也改為：

		AAAAAAAA
		XXXXXXXX
1. 建立另一個純文字檔案 `file2.txt` ，加入 git 中，內容改為：

		AAAAAAAA
		BBBBBBBB

	並 commit（`bc1`）
1. 切到 `master`，要求與 `b1` 作 merge。
