# 玩家信息接口
## 请求地址

- 请求地址：`https://record.uu.163.com/api/naraka/auth/{name}/163`
- GET
- `name`：永劫无间ID，需要进行URL编码，例如使用`urllib.parse.quote`函数对ID进行编码后替换到URL中的`{name}`位置。

## 请求头

| 参数名称 | 示例值 | 说明 |
| --- | --- | --- |
| accept | application/json, text/plain, */* | 接受的响应内容类型 |
| accept-language | zh-CN,zh;q=0.9 | 接受的语言 |
| cache-control | no-cache | 缓存控制 |
| pragma | no-cache | 缓存控制 |
| priority | u=1, i | 优先级 |
| referer | https://record.uu.163.com/naraka/query | 请求来源页面地址 |
| sec-ch-ua-mobile | ?0 | 移动端标识 |
| sec-fetch-dest | empty | 请求目标类型 |
| sec-fetch-mode | cors | 请求模式 |
| sec-fetch-site | same-origin | 请求来源站点 |
| cookie | xxxxxxxx | 用户身份认证信息 |（网易uu加速器自备ck）
| user-agent | Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36 Edg/127.0.0.0 | 客户端标识 |

## 响应示例

```json
{
    "code": 1000,
    "msg": "ok",
    "data": {
        "_id": "67859ac5775e95ed58a36f6e",
        "role_id": "s3ri000007008100180163",
        "role_name": "\u4e0d\u821f\u6ee9\u5996\u59ec",
        "server_id": 163,
        "server_name": "\u56fd\u670d",
        "role_level": 157,
        "head_icon": 3430046,
        "head_icon_url": "https://g.fp.ps.netease.com/uut/file/611c6ee596dee48f6309f63c1aVIiWYu03",
        "game_time": 1431423,
        "update_time": "2025-01-14 06:59:17"
    }
}
```
| 字段名称 | 类型 | 说明 |
| --- | --- | --- |
| code | int | 状态码，1000表示成功 |
| msg | string | 消息描述 |
| data | object | 响应数据 |
| data._id | string | 角色ID |
| data.role_id | string | 角色ID（另一种格式） |
| data.role_name | string | 角色名称 |
| data.server_id | int | 服务器ID |
| data.server_name | string | 服务器名称 |
| data.role_level | int | 角色等级 |
| data.head_icon | int | 头像图标编号 |
| data.head_icon_url | string | 头像图标URL |
| data.game_time | int | 游戏时长 |
| data.update_time | string | 数据更新时间 |


# 战绩查询接口
## 请求信息
- `https://record.uu.163.com/api/naraka/battles`
- GET
### 请求头
| 参数 | 值 |
|------|----|
| accept | application/json, text/plain, */* |
| accept-language | zh-CN,zh;q=0.9 |
| cache-control | no-cache |
| pragma | no-cache |
| priority | u=1, i |
| sec-ch-ua-mobile | ?0 |
| sec-fetch-dest | empty |
| cookie | xxxxxxxxx |
| sec-fetch-mode | cors |
| referer | https://record.uu.163.com/naraka/?name={name}&server=163 |
| sec-fetch-site | same-origin |
| user-agent | Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36 Edg/127.0.0.0 |

### 请求参数（Params）
| 参数 | 类型 | 描述 |
|------|------|------|
| page | int | 查询页码，默认为1 |
| page_size | int | 每页显示的记录数，默认为10 |
| name | str | 玩家ID，需进行URL编码 |
## 响应（JSON）
### 响应示例（参数为不舟滩妖姬）
```json
{
  "code": 1000,
  "msg": "ok",
  "data": [
    {
      "_id": "67859e22b7fd7e383427be3b",
      "role_id": "s3ri000007008100180163",
      "room_id": "216499208",
      "server_id": 163,
      "hero_id": 1000004,
      "hero_icon_url": "https://g.fp.ps.netease.com/uut/file/610a7338143cfa94649dcf4bVSUIdYg803",
      "game_mode": 1,
      "begin_time": 1736808467,
      "begin_rank_score": 1288,
      "round_rank_score": 29,
      "kill": 5,
      "damage": 11690,
      "rescue": 0,
      "rank": 7,
      "scene": 2,
      "update_time": "2025-01-14 07:13:38"
    },
    {
      "_id": "67859e22b7fd7e383427be3c",
      "role_id": "s3ri000007008100180163",
      "room_id": "216498737",
      "server_id": 163,
      "hero_id": 1000004,
      "hero_icon_url": "https://g.fp.ps.netease.com/uut/file/610a7338143cfa94649dcf4bVSUIdYg803",
      "game_mode": 1,
      "begin_time": 1736807819,
      "begin_rank_score": 1274,
      "round_rank_score": 14,
      "kill": 3,
      "damage": 7913,
      "rescue": 0,
      "rank": 25,
      "scene": 3,
      "update_time": "2025-01-14 07:13:38"
    },
    ...
  ]
}
```
| 字段 | 类型 | 描述 |
|------|------|------|
| code | int | 状态码，用于标识请求的处理结果，1000表示成功，其他值表示不同的错误情况 |
| msg | str | 消息描述，对状态码的具体说明，如“ok”表示请求成功 |
| data | list | 战绩数据列表，包含玩家的多条战绩记录 |
| data._id | str | 战绩记录ID，用于唯一标识一条战绩记录 |
| data.role_id | str | 角色ID，代表玩家在游戏中的角色标识，可用于区分不同角色的战绩 |
| data.room_id | str | 房间ID，表示玩家参与比赛的房间编号，可用于查询同一房间的其他玩家战绩 |
| data.server_id | int | 服务器ID，163为国服 |
| data.hero_id | int | 英雄ID，对应游戏中不同的英雄角色：1000001:"土御门胡桃"<br>1000003:"宁红夜"<br>1000004: "迦南"<br>1000005: "特木尔"<br>1000006: "火狗"<br>1000007: "天海"<br>1000009: "呆呆姬"<br>1000010: "崔三娘"<br>1000011: "岳山"<br>1000013: "无尘"<br>1000015: "顾清寒"<br>1000016: "武田信忠"<br>1000017: "殷紫萍"<br>1000018: "沈妙"<br>1000020: "1000020"<br>1000021: "1000021"<br>1000022: "1000022"<br>1000023: "1000023"<br>1000024: "魏青"<br> |
| data.hero_icon_url | str | 英雄图标URL |
| data.game_mode | int | 游戏模式，不同的数字代表不同的游戏模式，具体映射关系如下：<br>0: "全部"<br>1: "天选单排"<br>2: "天选三排"<br>3: "无尽试炼"<br>4: "天人单排"<br>5: "天人三排"<br>6: "匹配单排"<br>7: "匹配三排"<br>9: "匹配双排"<br>10: "无尽试炼双排"<br>11: "无尽试炼三排"<br>12: "天选双排"<br>13: "天人双排" |
| data.begin_time | int | 比赛开始时间戳，表示比赛开始的精确时间，可用于计算比赛的具体日期和时间 |
| data.begin_rank_score | int | 比赛开始时的段位分数，反映玩家在比赛开始时的段位水平，段位分数越高，表示玩家的段位越高 |
| data.round_rank_score | int | 当前轮次的段位分数变化，表示玩家在该轮比赛中段位分数的增减情况，正值表示段位分数增加，负值表示段位分数减少 |
| data.kill | int | 击杀数，玩家在比赛中击杀敌人的数量，是衡量玩家战斗能力的重要指标之一 |
| data.damage | int | 造成伤害，玩家在比赛中对敌人造成的总伤害值，反映了玩家在比赛中的输出能力 |
| data.rescue | int | 救援数，玩家在比赛中救援队友的次数，体现了玩家的团队协作精神和支援能力 |
| data.rank | int | 排名，玩家在该场比赛中的最终排名，排名越靠前，表示玩家在比赛中的表现越好 |
| data.scene | int | 场景类型，不同的数字代表游戏中的不同场景，具体映射关系如下：<br>1: "聚窟洲"<br>2: "火罗国"<br>3: "龙隐洞天" |
| data.update_time | str | 更新时间，表示该战绩记录最后查询的时间 |

# 特定某局具体战绩查询

## 请求信息
- `https://record.uu.163.com/api/naraka/battle/detail/{room_id}`
- GET

### 请求参数
- **room_id**（路径参数）：房间号，会在战绩查询响应体返回。

### 请求头
| 参数名称 | 参数值 | 说明 |
| --- | --- | --- |
| accept | application/json, text/plain, */* | 指定响应内容的类型 |
| accept-language | zh-CN,zh;q=0.9 | 指定请求的语言 |
| cache-control | no-cache | 禁用缓存 |
| pragma | no-cache | 禁用缓存 |
| cookie | xxxxxxxx | 包含用户身份认证等信息的 cookie |
| priority | u=1, i | 指定请求的优先级 |
| referer | https://record.uu.163.com/naraka/detail?id={room_id} | 指定请求的来源页面 |
| sec-ch-ua-mobile | ?0 | 指定是否为移动设备发起的请求 |
| sec-fetch-dest | empty | 指定请求的目的地类型 |
| sec-fetch-mode | cors | 指定请求的模式为跨源资源共享 |
| sec-fetch-site | same-origin | 指定请求的来源站点与目标站点相同 |
| user-agent | Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/127.0.0.0 Safari/537.36 Edg/127.0.0.0 | 指定请求的客户端浏览器信息 |

## 响应示例
```json
{
    "code": 1000,
    "msg": "ok",
    "data": {
        "_id": "6785a39ae2f93b6d63e8886f",
        "role_id": "s3ri000007008100180163",
        "room_id": "105726889",
        "role_name": "\u4e0d\u821f\u6ee9\u5996\u59ec",
        "server_id": 163,
        "server_name": "\u56fd\u670d",
        "role_level": 156,
        "head_icon": 3430046,
        "head_icon_url": "https://g.fp.ps.netease.com/uut/file/611c6ee596dee48f6309f63c1aVIiWYu03",
        "grade_id": 5020021,
        "grade_icon_url": "https://g.fp.ps.netease.com/uut/file/611e031b143cfa2fe8a99797sxJD02e703",
        "grade_name": "\u9ec4\u91d1\u2164",
        "honor_titles": [
            "\u960e\u738b",
            "1135"
        ],
        "game_mode": 2,
        "begin_time": 1686662029,
        "hero_id": 1000009,
        "hero_icon_url": "https://g.fp.ps.netease.com/uut/file/610a73385e6027355c431e05LAiKhobe03",
        "rank": 8,
        "begin_rank_score": 2000,
        "round_rank_score": 8,
        "kill": 5,
        "damage": 8622,
        "cure": 5123,
        "rescue": 1,
        "total_live_time": 719,
        "move_distance": 3592,
        "shield_damage": 2323,
        "shield_cure": 3788,
        "head_shot": 0,
        "shock": 0,
        "reborn": 0,
        "used_currency": 17000,
        "used_skill": 31,
        "chain_used": 3,
        "souls": [
            {
                "soul_name": "\u5927\u9b42\u7389\u2022\u4f53\u529b",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93da4ae863b8be8a463eAfpSZWcE03",
                "soul_id": 3320001
            },
            {
                "soul_name": "\u5927\u9b42\u7389\u2022\u653b\u51fb",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93dc4ae863b8be8a46463f2aKEI003",
                "soul_id": 3320011
            },
            {
                "soul_name": "\u5c0f\u9b42\u7389\u2022\u8fd1\u6297",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93ee4ae863b664881d05uUTmosuf03",
                "soul_id": 3320050
            },
            {
                "soul_name": "\u5927\u9b42\u7389\u2022\u653b\u51fb",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93dc4ae863b8be8a46463f2aKEI003",
                "soul_id": 3320011
            },
            {
                "soul_name": "\u5927\u9b42\u7389\u2022\u4f53\u529b",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93da4ae863b8be8a463eAfpSZWcE03",
                "soul_id": 3320001
            },
            {
                "soul_name": "\u6d41\u5929\u96f7",
                "soul_icon_url": "https://g.fp.ps.netease.com/uut/file/612c93eba7f25261daa4d63c67kr4RRi03",
                "soul_id": 3325310
            }
        ],
        "weapons": [
            {
                "weapon_name": "\u957f\u5251",
                "weapon_icon_url": "https://g.fp.ps.netease.com/uut/file/611c6f8296dee4324c500cb7uIiqOzhE03",
                "real_damage": 1715,
                "kill_times": 2,
                "weapon_type": "101"
            },
            {
                "weapon_name": "\u53cc\u5200",
                "weapon_icon_url": "https://uu.fp.ps.netease.com/file/62b56ec79d15dc3f936ae371KkPXEhHc04",
                "real_damage": 16,
                "kill_times": 0,
                "weapon_type": "118"
            },
            {
                "weapon_name": "\u68cd",
                "weapon_icon_url": "https://uu.fp.ps.netease.com/file/637d8fffc664ed22e9b300baeiiyGRYD04",
                "real_damage": 1283,
                "kill_times": 1,
                "weapon_type": "120"
            },
            {
                "weapon_name": "\u592a\u5200",
                "weapon_icon_url": "https://g.fp.ps.netease.com/uut/file/611c6f83143cfa42defc1628MioLHksD03",
                "real_damage": 1555.1525423728813,
                "kill_times": 1,
                "weapon_type": "102"
            }
        ],
        "teammates": [],
        "opponents": [],
        "scene": 2,
        "update_time": "2025-01-14 07:44:46"
    }
}
```
