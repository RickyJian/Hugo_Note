# 頁面綁定 (Page Bundle)

是一種頁面資源(Page Resource)的分組方式

## Leaf Bundle

為 `content` 目錄中的任一層目錄，其中放著 `index.md` 檔案。

```
# 目錄結構參照 Hugo 官網
# https://gohugo.io/content-management/page-bundles/#examples-of-leaf-bundle-organization

content/
├── about
│   ├── index.md
├── posts
│   ├── my-post
│   │   ├── content1.md
│   │   ├── content2.md
│   │   ├── image1.jpg
│   │   ├── image2.png
│   │   └── index.md
│   └── my-other-post
│       └── index.md
│
└── another-section
    ├── ..
    └── not-a-leaf-bundle
        ├── ..
        └── another-leaf-bundle
            └── index.md
```

Leaf Bundle: `about`、`my-post`、`my-other-post`、 `another-leaf-bundle`

## Branch Bundle

為 `content` 目錄中的任一層目錄，其中放著 `_index.md` 檔案。

```
# 目錄結構參照 Hugo 官網
# https://gohugo.io/content-management/page-bundles/#examples-of-branch-bundle-organization
content/
├── branch-bundle-1
│   ├── branch-content1.md
│   ├── branch-content2.md
│   ├── image1.jpg
│   ├── image2.png
│   └── _index.md
└── branch-bundle-2
    ├── _index.md
    └── a-leaf-bundle
        └── index.md
```

Branch Bundle: `branch-bundle-1`、`branch-bundle-2`

----
# 參照

[Page Bundle](https://gohugo.io/content-management/page-bundles)
