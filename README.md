# 巴厘岛行程小助手 🏝️

2026 年 9 月 25 日 – 10 月 4 日，巴厘岛 9 天 7 晚双人行程的随身页面。

**在线访问：** `https://<你的用户名>.github.io/bali-trip/`

---

## 页面

| 页面 | 地址 | 内容 |
|---|---|---|
| **行程小助手**（推荐） | [`index.html`](index.html) | 倒计时 + 实时天气 + 可导航地图 + 每日流程 + 紧急电话 + 航班/入境/餐食/清单速查 |
| 完整攻略 | [`guide.html`](guide.html) | 住宿、餐食、SPA、入境手续、携带物品与药品清单的完整版 |
| 自订速查卡 | [`self-booking.html`](self-booking.html) | Yoga Barn / Udara 等需自己预订的项目 |

`index.html` 是**单文件自包含**的——Leaflet 地图引擎已内联，**断网也能正常打开**（底图会灰掉，但节点、动线、倒计时、流程全部可用）。

---

## 行程概览

```
9/25  北京 PEK 15:45 ──CA969──▶ 新加坡 SIN 21:55
9/26  SIN 06:20 ──SQ934──▶ 巴厘岛 DPS 08:55
      └ 乌布 Alila Ubud ×2 晚（Yoga Barn 疗愈课）

9/27  Tukad Cepung 瀑布 + Bali Pulina 咖啡庄园
9/28  阿勇河漂流 ──▶ Amed 武吉瑟加拉 ×1 晚
9/29  Amed 浮潜 + 体验深潜（日式沉船 / Jemeluk 湾）
9/30  Udara Bali 音疗 09:30 ──▶ Canggu Potato Head ×2 晚
      └ 下午 La Brisa 日落晚餐

10/1  转场乌鲁瓦图 LXR（局部海景泳池别墅）×2 晚
10/2  Melasti 沙滩 + 情人崖
10/3  返程日：库塔洋人街 ──▶ 情人崖 Kecak 火舞 ──▶ 金巴兰
10/4  DPS 01:10 ──KE434──▶ 首尔 ICN 09:25
      ICN 14:40 ──OZ335──▶ 北京 PEK 15:50
```

**住宿**：乌布 Alila Ubud 2 晚 · Amed 武吉瑟加拉 1 晚 · Canggu Potato Head 2 晚 · 乌鲁瓦图 LXR 2 晚

---

## 使用说明

### 手机上离线使用
1. Safari / Chrome 打开在线地址；
2. 「分享」→「添加到主屏幕」；
3. 之后点图标即可打开，已缓存的页面断网也能看。

### 几个功能要点
- **⏳ 倒计时**：所有时间点固定按 **GMT+8** 解析（巴厘岛 WITA 与北京同时区），跨时区打开不会算错；勾选完成状态存在本机浏览器。
- **📍 我的位置**：需 **HTTPS** 环境才允许浏览器定位——用线上地址打开即可，本地文件双击打开会被浏览器拒绝。
- **🧭 地点导航**：地图标记和流程里的地名都可点，直接唤起 Google Maps 导航（需联网）。
- **🌤️ 实时天气**：每次打开自动拉取 Open-Meteo 数据（需联网），最多预报未来 16 天。

### 入境手续提醒
中国护照走**落地签 VoA**，出发前需办 3 个网上申报（**只认 `.go.id` 域名**）：

1. **eVOA 电子落地签** — `evisa.imigrasi.go.id`，IDR 500K/人
   - ⚠️ 主目的选 `General, Family, or Social`、次目的选 `Tourism, Family Visit, and Transit`，才会跳出 **B1 Tourist (Visa On Arrival)**
   - ⚠️ 别选 `Work and Holiday`（那是 B30 工作度假签，需印尼担保人，必被拦）
2. **All Indonesia 入境申报** — `allindonesia.imigrasi.go.id`，免费，抵达前 72h
3. **Love Bali 入岛税** — `lovebali.baliprov.go.id`，IDR 150K/人

---

## 本地开发

纯静态站点，无需构建。改完 `index.html` / `guide.html` 直接提交即可。

```bash
# 本地预览
python -m http.server 8080
# 打开 http://localhost:8080
```

> 注意：仓库根目录下的 `index.html` 是**工作目录里 `bali-plan-携程方案3.html` 的副本**，改了源文件需要同步过来。

---

## 隐私

本仓库包含个人行程信息（住宿、航班、日期）。若需公开访问，建议在仓库 Settings → General → Danger Zone 中确认可见性；或改用私有仓库 + 仅自己可见的部署方式。
