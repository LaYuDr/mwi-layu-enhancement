# 强化助手

银河奶牛（Milky Way Idle）的本地 Tampermonkey 辅助插件，当前正式版本使用 V3 界面。

## 功能

- 中文 / English 双语界面，默认跟随游戏语言，也可手动选择。

- 强化路线、期望消耗、工时费和利润计算。
- 强化方案显示期望时间与强化次数，始终按单件显示，不随计划数量变化；时间仅计强化耗时。
- 强化与制造经验预估，显示当前和预计进度、跨级提示及对应技能图标。
- 物品收藏、自定义分区、等级与参考售价管理。
- 材料汇总、备料车、库存缺口和预算。
- 紧凑的底子来源选择栏，可自行选择采购或自制；+0 采购报价缺失时自动使用有效的自制成本，同物品保护与材料清单同步按实际来源计算；显示所选方案相对另一方案每小时多赚或少赚的预计差额。
- 官方行情、本人挂单及已观察到的成交记录。
- 紧凑的价格纵表合并市场深度与收益，显示真实买卖挂单量、本人同价订单队列，以及左一上方和右一下方各三个价格档位；保留实际非标准价格。
- 打开游戏市场、制作或强化页面，并预填相关参数。
- 本地设置备份与恢复；界面随游戏容器宽度调整。

不会自动开始强化、制作、购买或出售。计算结果是估算，实际游戏操作由玩家确认。没有逐笔成交价和时间的数据不会冒充真实成交记录。

## 安装与更新

[从 Greasy Fork 安装](https://greasyfork.org/zh-CN/scripts/599358)

需要先安装 Tampermonkey。安装后刷新游戏；同一插件的正式版、开发加载器、独立 V3 试用版只启用一个。正式脚本已包含运行时代码，无需启动本地服务。

更新由 Tampermonkey 的更新设置控制，也可在其管理面板手动检查更新。作者在 GitHub 更新正式脚本后，由 Greasy Fork 已配置的同步方式拉取；同步和客户端检查可能有延迟。

支持 `www.milkywayidle.com` 与 `www.milkywayidlecn.com`。同一浏览器和游戏域名下沿用原主版本的 `mwi-layu:*` 数据；独立 V3 试用版的隔离数据不自动合并。浏览器、游戏域名和角色作用域按现有规则隔离。

## 语言设置 / Language

在「设置与备份 → Language / 语言」选择「跟随游戏 / Follow game」「中文」或「English」，点击「应用语言 / Apply language」即可生效。偏好保存在当前浏览器与站点，并包含在本地备份中。

切换语言会重建插件界面，不刷新游戏；请先保存其他设置及未提交输入，临时价格模拟会重置。自定义分区名称保持原文。英文物品名称优先使用游戏官方词典，缺失时使用游戏物品数据或可读的 HRID 名称。

The interface follows the game language by default. To override it, open **Settings & backup → Language**, choose **English** or **中文**, then click **Apply language**. Save other settings and unfinished inputs first: changing language rebuilds the plugin interface and resets temporary price simulations. Your custom group names remain unchanged. All game actions and trades still require manual confirmation.

## 隐私与许可

玩家数据保存在本地浏览器，不上传到 GitHub 或 Greasy Fork；游戏行情请求使用官方来源。此仓库只分发完整用户脚本、更新元数据与说明，不包含玩家数据、备份或本地开发加载器。

项目代码采用 MIT；第三方组件与署名见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)，同样包含在用户脚本中。

反馈问题请使用 [GitHub Issues](https://github.com/LaYuDr/mwi-layu-enhancement/issues)，不要附带密码、账号凭据或完整玩家备份。

## 可选使用量统计

默认关闭。在 Tampermonkey 菜单点击本插件的「使用量统计 [已关闭]」，阅读说明并确认开启；再次点击可关闭。只上报插件 ID、版本和随机安装标识的 SHA-256 摘要，不读取硬件编号、账号、角色、聊天、资产或交易，不发送 Cookie。网络服务仍能接收到来源 IP。

接收方为柆雨的雨云中转 `https://ukpyedhl.cn-hk1.rainapp.top`。未同步记录暂存在服务器，电脑保存并确认后删除队列；电脑上的历史统计及备份永久保留。关闭只停止后续上报，不删除已保存统计。

分别统计本插件累计上报安装数与北京时间每日活跃安装数，不等于物理设备数、人数或全部下载量；只计主动开启并成功上报的安装。重装或清除脚本存储可能产生新安装标识。每天最多记录一次成功上报，失败退避重试，不补造离线历史。开发加载器不参与生产统计。
