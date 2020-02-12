# 頁面內容

Hugo 檔案定義的資料稱為 `frot matter`。Hugo 專案中版面結構與資料是分開的，當在頁面渲染時才會將資料與網頁布局做綁定。

## 檔案結構

可以使用三種檔案型態定義 `front matter`—`yaml`、`toml`及`json`。

### YAML

```yaml
---
title: "Yaml"
date: 2020-02-09T23:02:19+08:00
draft: true
---

YAML front matter
```

[yaml 介紹](https://zh.wikipedia.org/wiki/YAML)

### TOML

```toml
+++
title= "Toml"
date= "2020-02-09T23:53:20+08:00"
draft= "true"
+++

TOML front matter
```

[toml 介紹](https://zh.wikipedia.org/zh-tw/TOML)

### JSON

```json
{
    "title": "JSON",
    "date": "2020-02-09T23:53:20+08:00",
    "draft": "true"
}

[JSON 介紹](https://zh.wikipedia.org/wiki/JSON)

JSON front matter
```

## 檔案內容

## 參數

### 預設參數

------
# 參考

[Front Matter](https://gohugo.io/content-management/front-matter/)