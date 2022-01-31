# schweb-crawler-next: Schemas

這些 schema 是 schweb-crawler-next 會產生出的 JSON 資料格式。您可以據此產生對應語言的 type definition 。

## 直接產生 definition

### 依賴

- yaml2json-rs: <https://github.com/Nessex/yaml2json-rs>
  - 安裝： `cargo install yaml2json-rs-bin --bin yaml2json`

- jtd-codegen: <https://github.com/jsontypedef/json-typedef-codegen>
  - 安裝： `cargo install --git https://github.com/jsontypedef/json-typedef-codegen`

### 使用

見此：<https://jsontypedef.com/docs/implementations/>

```sh
yaml2json <JTD yml 檔案> | jtd-codegen - --root-name <JTD 根屬性的名稱 ...
```

比如可以：

```sh
# 先建立輸出資料夾
mkdir announcement-entry-response

# 產生檔案
yaml2json announcement-entry-response.jtd.yml | jtd-codegen - --root-name AnnouncementEntryResponse --typescript-out=./announcement-entry-response
```

## 授權

GPLv3

## 作者

pan93412
