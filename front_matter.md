# 頁面內容

Hugo 中版面結構與資料是分開的，當在頁面渲染時才會將資料與網頁布局做綁定。在 Hugo 裡我們將此稱為 `front matter` ，我們可以使用三種檔案型態定義我們的 `front matter` ，分別為 `yaml` 、 `toml` 及 `json`。

此章節只做 `front matter` 的介紹及使用，若要實際是出來還需要 `page resource` 和 `template` 的結合

## 檔案結構

檔案又分為上下兩部

* 上半部： 變數區，可在此區塊設定頁面所要使用的變數，變數又分為 `使用者定義` 及 `系統預設`
* 下半部： 內容區，在此區域所設定的內容可使用 `頁面資源{{.Content}}` 做綁定，另外此區域也能綁定 `shortcodes`

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

在此只介紹常用系統變數，若要詳細了解可參閱 [front matter variable](https://gohugo.io/content-management/front-matter/#front-matter-variables)

* title

    頁面標題

* date

    頁面日期

* draft

    此變數必為 `true`、`false`，當為 `true` 時 hugo 不會顯示此頁面，若要讓此頁面顯示必須使用 `hugo server -D`

### 使用者定義

當變數定義好後必須綁定 `page resources {{.Params}}` 才可將自定義變數顯示出來。

```yaml
---
title: "User_defined"
date: 2020-02-17T23:35:27+08:00
draft: true
id: "01234567890"
---

user defined front matter, the `id` is self defined front matter. it will show below this sentence.
```

------
# 參考

[Front Matter](https://gohugo.io/content-management/front-matter/)