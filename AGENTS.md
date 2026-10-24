# 图标仓库维护约定

## 发布

使用 GitHub API 创建发布提交和 Release。保留未涉及的文件和现有图片链接。

## 订阅顺序

- `icons.json` 固定为应用及通用图标在前、国家及地区旗帜在后。
- 应用组逐项采用 `apps.json` 的顺序，旗帜组逐项采用 `flags.json` 的顺序。
- 总合集固定按“应用 → 机场 → Emby → 六张洲地图 → 南极洲 → 其他国旗”排列；机场组为 airports.json 的全部 64 项（含 loon、surge、tag、wd），Emby 组含原 emby、omega、tudou-saha 和 Emby 专属订阅的 33 项，共 36 项；六张洲地图依次为亚洲、欧洲、非洲、北美洲、南美洲、大洋洲。其余应用、机场、Emby 和其余国旗各自按英文 ID 排序，今后新增图标也沿用此顺序；分组成员维护在 `icon-groups.json`。
- `icon-groups.json.order` 固定为 `apps`、`airports`、`emby`、`continents`、`antarctica`、`flags`。
- `apps` 与 `flags` 为各订阅扣除显式分组成员后的剩余项；应用组末尾依次放机场、Emby、六洲，旗帜组首项为原 `antarctica`。
- 机场组严格采用 `airports.json.icons` 的全部 URL 文件名 ID，当前为 64 项（含用户指定的 Loon、Surge、TAG、WD），在 `icon-groups.json.airports` 按 ID 排序；保留“机场组 · ”名称前缀及原图、原别名。按用户用途分组，客户端也可由用户明确指定加入机场组。
- 新增 Emby 服务图标时将其 ID 写入 `emby` 数组并按 ID 排序；当前包含 `emby`、`omega`、`tudou-saha` 及 `emby.json` 的 33 个 URL 文件名 ID，共 36 项；专属订阅保持原 33 项。
- `continents` 固定为 `asia`、`europe`、`africa`、`north-america`、`south-america`、`oceania`；`antarctica` 引用现有旗帜 ID，不另建图标。
- 显式分组成员必须存在且互不重复；全部分组必须覆盖所有订阅条目且仅覆盖一次。README 预览行采用相同顺序。
- 普通应用、机场、Emby 和其余旗帜各自按图片 URL 文件名的英文 ID 升序排列；六洲固定顺序、南极洲固定在旗帜首位，不得跨组统一排序。
- 总合集的 `icons` 数组必须严格等于 `apps.json.icons + flags.json.icons`。
- 今后新增或更新图标也必须保持此规则，不得再对总合集跨组统一排序。
- 条目仅使用 `name` 和 `url`；中英文检索词写入 `name`，不为别名创建重复条目。

## 文档与校验

README 保持中文，保留总合集、应用、机场、Emby、国旗五个可以直接复制的完整订阅地址。更新计数与预览后，校验总合集分组顺序、分类完整性、重复 ID、图片真实透明通道和线上链接。
