# 目錄類型

`content` 目錄結構分為兩種 `Leaf Bundle` 和 `Branch Bundle`。

網頁路徑與 `content` 中的資料節路徑相對應。

## Leaf Bundle

**單一**結構目錄層。

此目錄中存在的檔案皆為單一頁面所應用資源，不可嵌套任何目錄。若在此目錄定義 `index.md` 則為此目錄的主頁面。

在此目錄中不可定義 `_index.md` 檔案。

```command
# 此目錄結構參照 example/content_directory/content

content/ # root directory
│
├── dir1
│   ├── _index.md
│   ├── dir2
│   │   ├── _index.md
│   │   └── third.md
│   ├── dir3 # Leaf Bundle
│   │   ├── forth.md
│   │   └── index.md # main page
│   └── second.md
└── first.md
```

## Branch Bundle

**列表**結構目錄層。

除了 `content` 中底層目錄及第一層目錄為預設列表結構，若要將目錄定義為列表結構，必須在目錄中定義 `_index.md` 檔案。可在使用 `_index.md` 做料表結構的設定。

```command
# 此目錄結構參照 example/content_directory/content

content/ # root directory, default branch bundle
│
├── dir1 # fist level directory, default branch direcory
│   ├── _index.md # branch bundle setting file
│   ├── dir2 # second level directory, branch bundle
│   │   ├── _index.md
│   │   └── third.md
│   ├── dir3
│   │   ├── forth.md
│   │   └── index.md
│   └── second.md
└── first.md
```

-----
# 參考

[Page Bundle](https://gohugo.io/content-management/page-bundles/)

# 範例

[目錄類型](example/content_directory)