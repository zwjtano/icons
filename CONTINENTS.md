# 洲别地图图标

本批为六张地图轮廓手绘水彩图标：替换 `asia`，新增非洲、欧洲、北美洲、南美洲和大洋洲五项。
按用户要求，现有南极洲旗帜 `icons/antarctica.png`、对应名称和链接保持不变；不新增 `continent-antarctica`。
当前总合集 **499** 项、应用与通用图标 **241** 项、旗帜 **258** 项。

总合集固定按“应用 → 机场 → Emby → 六张洲地图 → 南极洲 → 其他国旗”排列；机场组为 airports.json 的全部 64 项（含 loon、surge、tag、wd），Emby 组含原 emby、omega、tudou-saha 和 Emby 专属订阅的 33 项，共 36 项；六张洲地图依次为亚洲、欧洲、非洲、北美洲、南美洲、大洋洲。其余应用、机场、Emby 和其余国旗各自按英文 ID 排序，今后新增图标也沿用此顺序；分组成员维护在 `icon-groups.json`。
`apps.json` 依次为其他应用 135 项、机场 64 项、Emby 36 项和六张洲地图；`flags.json` 仅将原南极洲条目移到首位，其余条目保留原顺序。
33 项 Emby 专属订阅条目的名称、URL、PNG、来源素材及专属订阅/索引/说明/预览文件逐字节保留；与原三项合并排序，但不扩充或改写 `emby.json`。
机场组完整保留新增 60 项及原 `loon`、`surge`、`tag`、`wd`。只对原四项现有“机场组 · ”名称追加 ` Airport`，在 airports.json/apps.json/icons.json 保持一致，其余 60 项名称与全部图片、URL 不变。
机场来源素材、索引、说明、预览、生成提示和 QA 元数据等现有文件由树哈希保护，不随本批改写。
所有旗帜条目的名称和 URL、旗帜集合名称与说明不变；`flags-index.json` 与原南极洲 PNG 逐字节不变。

参考底图：[Natural Earth 地理区域 GeoJSON](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_110m_geography_regions_polys.geojson)；[Natural Earth 陆地 GeoJSON](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_110m_land.geojson)。
底图由 Natural Earth 发布为公共领域资料，见[使用条款](https://www.naturalearthdata.com/about/terms-of-use/)；参考渲染后由内置图像工具制作水彩插画。
轮廓进行了适合小图识别的概略化处理；大洋洲包含澳大利亚、新西兰及太平洋岛屿的示意。

| ID | 中英文检索名 | 本次处理 |
| --- | --- | --- |
| `asia` | asia 亚洲 Asia | 替换地图图标，保留原名与文件名 |
| `europe` | europe 欧洲 歐洲 Europe | 新增地图图标 |
| `africa` | africa 非洲 Africa | 新增地图图标 |
| `north-america` | north-america 北美洲 North America 北美 | 新增地图图标 |
| `south-america` | south-america 南美洲 South America 南美 | 新增地图图标 |
| `oceania` | oceania 大洋洲 Oceania 澳大利亚洲 | 新增地图图标 |

六项归入 `apps.json` 的通用图标组；`icons.json.icons` 严格等于 `apps.json.icons + flags.json.icons`。
旗帜订阅只调整条目顺序；旗帜索引、其他 PNG 及历史流媒体目录保持不变。

地图轮廓为概略插画，不表示政治边界、领土归属或任何争议立场；图标不用于测绘或导航。
