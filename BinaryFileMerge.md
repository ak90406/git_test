前期準備
--------
1. 建立一個 repo
1. 建立一個圖片檔案 `file.jpg`，隨手畫一個`Ｏ`。
1. 加入 git 中、並 commit（`baseC`）。
1. 建立一個名為 `b1` 的 branch。此時 `master` 與 `b1` 的 HEAD 同時指向 `baseC`。


測試 1
------
1. 切到 `b1`，將 `file.jpg` ，抹去原本的`Ｏ`，改畫成`Ｘ`，並 commit（`bc1`）。
1. 切到 `master`，要求與 `b1` 作 merge。

結果 1
-----
1. git 在merge過後只留下`Ｏ`圖案的`file.jpg`，即只會留下head所指的branch（在這邊是`master`）的 Binary檔案
