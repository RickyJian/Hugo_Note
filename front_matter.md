# 頁面內容

Hugo 中版面結構與資料是分開的，當在頁面渲染時才會將資料與網頁布局做綁定。在 Hugo 裡我們將此稱為 `front matter` ，我們可以使用三種檔案型態定義我們的 `front matter` ，分別為 `yaml` 、 `toml` 及 `json` 。

## 檔案結構

檔案又分為上下兩部

* 上半部： 變數區，可在此區塊設定頁面所要使用的變數，變數又分為 `使用者定義` 及 `系統預設`
* 下半部： 內容區，在此區域所設定的內容可使用 `系統預設變數{{.Content}}` 做綁定，另外此區域也能做 `shortcodes` 的設定

### YAML

變數區的開頭與結尾須用 `---` 做包覆

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

變數區的開頭與結尾須用 `+++` 做包覆

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

變數區的開頭用 `{` 結尾用 `}` 做包覆

```json
{
    "title": "JSON",
    "date": "2020-02-09T23:53:20+08:00",
    "draft": "true"
}

JSON front matter
```

[JSON 介紹](https://zh.wikipedia.org/wiki/JSON)

## 變數

### 預設變數

## 內容

### shortcodes

------
# 參考

[Front Matter](https://gohugo.io/content-management/front-matter/)