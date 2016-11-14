### tg-common-group ###
---

`tg-common-group` 是一個 `BaSH` 寫成的 Telegram 共同群組分析。依賴於 [jq](https://stedolan.github.io/jq/) 與 [telegram-cli](https://github.com/vysheng/tg)。

若要使用，安裝 jq，並編譯 telegram-cli，使用如下參數啟動 tg-cli：

```
telegram-cli -P 9009 --json
```

然後就可以使用 `./tg_common_groups` 查看共同群組了。

查詢一次過後，會生成 `cache` 文件夾。內有全部群組信息。 這時，可以使用 `tg_group_graph` 生成 mathematica 的 Graph 語句，繪製 成員-群組 關係網。

妳可以不使用任何參數調用 `tg_group_graph`。也可以為其指定來源群組。用法是：`tg_group_graph [src_group_name <your_user_id>]`，`src_group_name` 指定群組名稱。你可以在 `cache/` 裡邊看到它們。就是那段在 `.txt.json` 之前的字符。如果指定了來源組，也必須指定 `your_user_id`。是妳在 telegram 的數字 ID。

例：一個沒有限制來源組的關係網。

![一個沒有限制來源組的關係網](https://raw.githubusercontent.com/Nat-Lab/tg_common_groups/master/tg_net.png)

### Licence ###
MIT Licence
