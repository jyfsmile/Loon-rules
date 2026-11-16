# loon-rules

Loon 分流规则集，按类别分类存放。私有仓库。

## 目录

| 目录 | 说明 | 状态 |
| --- | --- | --- |
| `rules/rex/` | Rex App（`.rex` 首页包）相关：Pornhub / Beeg / PimpBunny / YesPorn / 4KPorno | 已有 `rex.list` |
| `rules/streaming/` | 流媒体类 | 待补充 |
| `rules/apple/` | Apple 相关，如 APNs 推送 | 待补充 |
| `rules/direct/` | 直连类 | 待补充 |
| `rules/reject/` | 广告 / 拦截类 | 待补充 |

## Loon 里怎么用

每个 `.list` 都是远程规则集（不带策略组）：

1. Loon → 配置 → 规则 → 添加远程规则
2. URL 填对应文件的 raw 地址，例如 Rex：
   `https://raw.githubusercontent.com/jyfsmile/Loon-rules/main/rules/rex/rex.list`
3. 策略选你的代理策略组（如节点选择），保存即可

也可以把 `.list` 里的规则逐行粘到本地配置的 `[Rule]` 里，末尾加上 `,你的策略组名`，放在 `FINAL` 之前。

## 新增规则集

- 一个类别一个目录，一个规则集一个 `.list` 文件
- 文件头用 `#` 写清来源、用途、更新日期
- 只放 `DOMAIN-SUFFIX` / `DOMAIN` / `DOMAIN-KEYWORD` 这类域名规则，不放 IP 段（除非必要）
- 改完在 README 的表格里更新状态
