# 网易大神战绩查询gamedata

| 项目 | 说明 |
|------|------|
| **接口名称** | 获取所有比赛结果数据 |
| **请求地址** | `https://god.gameyw.netease.com/v1/app/gameData/d90/getAllMatchResultData` |
| **请求方法** | POST |
| **Content-Type** | application/json |

## 请求

```
POST /v1/app/gameData/d90/getAllMatchResultData?ts=1770639521&uf=0a3ac892a56f42b797b1009e64cedf6f00&ab=d80419e3b4088b74b1612376681c8ece9e&ef=3c2b68e114476d826d979ff23b8788a3fd HTTP/2
host: god.gameyw.netease.com
content-length: 77
sec-ch-ua-platform: "Android"
gl-nonce: ……
sec-ch-ua: "Android WebView";v="143", "Chromium";v="143", "Not A(Brand";v="24"
sec-ch-ua-mobile: ?1
gl-uid: ……
gl-token: ……
gl-version: 4.11.0
user-agent: Mozilla/5.0 (Linux; Android 16; 22127RK46C Build/BP2A.250605.031.A3; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/143.0.7499.34 Mobile Safari/537.36 GodlikeLite Godlike/4.11.0 (channel/lite_mi) UEPay/com.netease.godlikelite/android7.12.28
accept: application/json, text/plain, */*
gl-clienttype: 50
content-type: application/json
gl-source: URS
gl-deviceid: ……
origin: https://act.ds.163.com
x-requested-with: com.netease.godlikelite
sec-fetch-site: cross-site
sec-fetch-mode: cors
sec-fetch-dest: empty
referer: https://act.ds.163.com/
accept-encoding: gzip, deflate, br, zstd
accept-language: zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7
priority: u=1, i

{"roleId":"psrc000162800600120163","server":"163","latest":50,"modeId":"PVP"}
```
### URL Query 参数

| 参数名 | 类型 | 说明 |
|--------|------|------|
| ts | int | 时间戳 |
| uf | string | 加密参数 |
| ab | string | 加密参数 |
| ef | string | 加密参数 |

### 请求体 (JSON)

| 字段名 | 类型 | 说明 |
|--------|------|------|
| roleId | string | 角色ID |
| server | string | 163国服 |
| latest | int | 获取最近N场比赛 |
| modeId | string | 游戏模式 |

```json
{
    "roleId": "psrc000162800600120163",
    "server": "163",
    "latest": 50,
    "modeId": "PVP"
}
```

## 响应（JSON）

```
HTTP/2 200
server: nginx
date: Mon, 09 Feb 2026 12:18:42 GMT
content-type: application/json;charset=UTF-8
vary: Origin
access-control-allow-origin: https://act.ds.163.com
access-control-allow-methods: GET,POST,PUT,DELETE,PATCH,HEAD,OPTIONS,CONNECT,TRACE
access-control-max-age: 3600
access-control-allow-headers: GL-ClientType,GL-Version,GL-CurTime,GL-DeviceId,GL-Token,GL-Uid,GL-Source,GL-CheckSum,GL-Nonce,GL-Gm-Sdk-Token,GL-UnisdkDeviceId,GL-Udid,GL-Channel,GL-ActiveSquareId,Content-Type,GL-X-XSRF-TOKEN,GL-Shield-Id,GL-Wx-Token
access-control-allow-credentials: true
vary: Accept-Encoding
content-encoding: br
ntes-trace-id: 8379555b1fc19a13:8379555b1fc19a13:0:1

{"result":"[{\"room_id\":\"1e4e880558c3412da15b516ed2ad8217\",\"role_name\":\"B站楠寻鸽\",\"battle_tid\":\"5000108\",\"group_id\":1.0,\"battle_logic_time\":300.0,\"total_live_time\":110.4541974067688,\"group_rank\":17.0,\"final_group_rank\":17.0,\"rank\":17.0,\"dead_times\":1.0,\"rescue_times\":0.0,\"ingame_score\":0.0,\"assist_count\":0.0,\"shield_damage\":887.0,\"real_damage\":0.0,\"damage\":887.0,\"damage_rank\":10.0,\"cure_hp\":0.0,\"cure_shield\":95.0,\"cure\":95.0,\"cure_rank\":3.0,\"kill_times\":0.0,\"skill_use_times\":2.0,\"device_hurt\":0.0,\"move_distance\":1102.0,\"chain_used_count\":3.0,\"chain_hit_count\":1.0,\"used_currency\":0.0,\"end_info\":[2.0,0.0,true],\"normal_hit_count\":10.0,\"reborn_count\":0.0,\"sum_used_item\":3.0,\"hero_id\":1000017.0,\"honor_title_info\":[],\"old_rank_score_list\":[],\"new_rank_score_list\":[],\"score_rank_list\":[],\"delta_value\":-141.0,\"born_position\":[851.08,80.34,1540.81],\"talent_skill_tid\":[3470120.0,3470123.0],\"soul_items_tids\":[3320010.0,3320010.0,3320011.0],\"weapon_proficiency\":[{\"experience_after\":1612.0,\"exp_delta\":78.0,\"weapon_type\":3910003.0,\"level_after\":4.0},{\"experience_after\":44.0,\"exp_delta\":15.0,\"weapon_type\":3910005.0,\"level_after\":2.0},{\"experience_after\":19.0,\"exp_delta\":32.0,\"weapon_type\":3910015.0,\"level_after\":5.0},{\"experience_after\":94.0,\"exp_delta\":7.0,\"weapon_type\":3910016.0,\"level_after\":3.0},{\"experience_after\":1255.0,\"exp_delta\":6.0,\"weapon_type\":3910018.0,\"level_after\":5.0}],\"be_killed_type\":{\"1\":1.0},\"shock_count\":0.0,\"be_rescued_count\":0.0,\"buy_count_info\":{},\"open_treasure_count\":6.0,\"dragon_info\":{\"bool_dragonkilling_success\":false,\"bool_dragonkilling_belaunched\":false,\"dragonkilling_round\":0.0,\"bool_dragonkilling_enter\":false},\"start_ts\":1.764339061E9,\"skill_use_times_per\":{\"1501500\":2.0},\"end_ts\":1.764339322E9,\"camp\":0.0,\"win_camp\":0.0,\"point_hold_score\":0.0,\"evaluation_score\":0.0,\"sub_battle_tid\":0.0,\"clan_war_team_score\":0.0,\"clan_war_rank\":0.0,\"weapon_damage_info\":{\"Dmg without weapon\":129.0,\"Katana\":758.0},\"kill_times_info\":{},\"head_shot_count_info\":{},\"moves_hit_count_info\":{\"T_Katana_bt\":4.0,\"T_Katana_pg\":4.0,\"蓄力\":4.0,\"非蓄\":5.0},\"moves_hit_damage_info\":{\"T_Katana_bt\":604.0,\"T_Katana_pg\":154.0,\"蓄力\":604.0,\"非蓄\":283.0},\"avg_rank_score\":2223.0,\"is_custom_room\":false,\"cur_player_num\":\"1\",\"role_id\":\"yZi21pIBk86GqxwDk860TaJiCyLEFmBKZj1wBebbEI_bDDYavuPtcPa9qNk\\u003d\"}]","code":200,"errmsg":"OK"}
```

| 字段名 | 类型 | 说明 |
|--------|------|------|
| code | int | 状态码 (200=成功) |
| errmsg | string | 错误信息 |
| result | string | 战斗数据JSON字符串 |


| 字段名 | 类型 | 说明 |
|--------|------|------|
| room_id | string | 房间唯一标识ID |
| role_name | string | 玩家游戏昵称 |
| battle_tid | string | 战斗类型ID |
| group_id | int | 队伍ID |
| battle_logic_time | float | 战斗逻辑时长(秒) |
| total_live_time | float | 总存活时间(秒) |
| group_rank | float | 队伍排名 |
| final_group_rank | float | 最终队伍排名 |
| rank | float | 个人最终排名 |
| dead_times | float | 死亡次数 |
| rescue_times | float | 救援次数 |
| ingame_score | float | 比赛内得分 |
| assist_count | float | 助攻次数 |
| shield_damage | float | 护甲伤害 |
| real_damage | float | 真实伤害 |
| damage | float | 总伤害值 |
| damage_rank | float | 伤害排名 |
| cure_hp | float | 治疗血量 |
| cure_shield | float | 治疗护盾 |
| cure | float | 总治疗量 |
| cure_rank | float | 治疗排名 |
| kill_times | float | 击杀数 |
| skill_use_times | float | 技能使用次数 |
| device_hurt | float | 装置伤害 |
| move_distance | float | 移动距离 |
| chain_used_count | float | 连击使用次数 |
| chain_hit_count | float | 连击命中次数 |
| used_currency | float | 使用货币数量 |
| end_info | array | 结束信息 [类型, 数值, 布尔值] |
| normal_hit_count | float | 普通攻击命中次数 |
| reborn_count | float | 重生次数 |
| sum_used_item | float | 使用物品总数 |
| hero_id | int | 英雄ID |
| honor_title_info | array | 荣誉称号信息 |
| old_rank_score_list | array | 旧段位分数列表 |
| new_rank_score_list | array | 新段位分数列表 |
| score_rank_list | array | 分数排名列表 |
| delta_value | float | 段位分变化值 |
| born_position | array | 出生点坐标 [X, Y, Z] |
| talent_skill_tid | array | 天赋技能ID列表 |
| soul_items_tids | array | 魂玉物品ID列表 |
| weapon_proficiency | array | 武器熟练度列表 |
| be_killed_type | object | 被击杀类型统计 |
| shock_count | float | 击晕次数 |
| be_rescued_count | float | 被救援次数 |
| buy_count_info | object | 购买统计信息 |
| open_treasure_count | float | 开启宝箱数量 |
| dragon_info | object | 屠龙信息 |
| start_ts | int | 开始时间戳 |
| skill_use_times_per | object | 技能使用次数详情 |
| end_ts | int | 结束时间戳 |
| camp | int | 阵营 |
| win_camp | int | 获胜阵营 |
| point_hold_score | float | 占点得分 |
| evaluation_score | float | 评价得分 |
| sub_battle_tid | int | 子战斗类型ID |
| clan_war_team_score | float | 公会战队伍得分 |
| clan_war_rank | float | 公会战排名 |
| weapon_damage_info | object | 武器伤害详情 |
| kill_times_info | object | 击杀方式详情 |
| head_shot_count_info | object | 爆头统计信息 |
| moves_hit_count_info | object | 招式命中次数详情 |
| moves_hit_damage_info | object | 招式伤害详情 |
| avg_rank_score | float | 平均段位分 |
| is_custom_room | bool | 是否为自定义房间 |
| cur_player_num | string | 当前玩家数量 |
| role_id | string | 角色唯一标识 |


### 解析

```python
import json
from datetime import datetime
from typing import Any
def parse_battle_data(raw_data: dict) -> list[dict[str, Any]]:
    if raw_data["code"] != 200:
        raise Exception(f"请求失败: {raw_data['errmsg']}")
    battle_list = json.loads(raw_data["result"])
    parsed_result = []
    for battle in battle_list:
        start_time = datetime.fromtimestamp(battle["start_ts"]).strftime("%Y-%m-%d %H:%M:%S")
        end_time = datetime.fromtimestamp(battle["end_ts"]).strftime("%Y-%m-%d %H:%M:%S")
        battle_info = {
            "房间ID": battle["room_id"],
            "角色名": battle["role_name"],
            "战斗类型ID": battle["battle_tid"],
            "队伍ID": battle["group_id"],
            "战斗逻辑时长(秒)": battle["battle_logic_time"],
            "总存活时间(秒)": round(battle["total_live_time"], 2),
            "队伍排名": battle["group_rank"],
            "最终队伍排名": battle["final_group_rank"],
            "个人排名": battle["rank"],
            "死亡次数": battle["dead_times"],
            "救援次数": battle["rescue_times"],
            "比赛内得分": battle["ingame_score"],
            "助攻次数": battle["assist_count"],
            "护甲伤害": battle["shield_damage"],
            "真实伤害": battle["real_damage"],
            "总伤害": battle["damage"],
            "伤害排名": battle["damage_rank"],
            "治疗血量": battle["cure_hp"],
            "治疗护盾": battle["cure_shield"],
            "总治疗量": battle["cure"],
            "治疗排名": battle["cure_rank"],
            "击杀数": battle["kill_times"],
            "技能使用次数": battle["skill_use_times"],
            "装置伤害": battle["device_hurt"],
            "移动距离": battle["move_distance"],
            "连击使用次数": battle["chain_used_count"],
            "连击命中次数": battle["chain_hit_count"],
            "使用货币数量": battle["used_currency"],
            "结束信息": battle["end_info"],
            "普通攻击命中次数": battle["normal_hit_count"],
            "重生次数": battle["reborn_count"],
            "使用物品总数": battle["sum_used_item"],
            "英雄ID": battle["hero_id"],
            "荣誉称号信息": battle["honor_title_info"],
            "旧段位分数列表": battle["old_rank_score_list"],
            "新段位分数列表": battle["new_rank_score_list"],
            "分数排名列表": battle["score_rank_list"],
            "段位分变化值": battle["delta_value"],
            "出生点坐标": battle["born_position"],
            "天赋技能ID列表": battle["talent_skill_tid"],
            "魂玉物品ID列表": battle["soul_items_tids"],
            "武器熟练度": battle["weapon_proficiency"],
            "被击杀类型统计": battle["be_killed_type"],
            "击晕次数": battle["shock_count"],
            "被救援次数": battle["be_rescued_count"],
            "购买统计信息": battle["buy_count_info"],
            "开启宝箱数量": battle["open_treasure_count"],
            "屠龙成功": battle["dragon_info"]["bool_dragonkilling_success"],
            "屠龙发起": battle["dragon_info"]["bool_dragonkilling_belaunched"],
            "屠龙轮次": battle["dragon_info"]["dragonkilling_round"],
            "进入屠龙": battle["dragon_info"]["bool_dragonkilling_enter"],
            "开始时间": start_time,
            "结束时间": end_time,
            "技能使用详情": battle["skill_use_times_per"],
            "阵营": battle["camp"],
            "获胜阵营": battle["win_camp"],
            "占点得分": battle["point_hold_score"],
            "评价得分": battle["evaluation_score"],
            "子战斗类型ID": battle["sub_battle_tid"],
            "公会战队伍得分": battle["clan_war_team_score"],
            "公会战排名": battle["clan_war_rank"],
            "武器伤害详情": battle["weapon_damage_info"],
            "击杀方式详情": battle["kill_times_info"],
            "爆头统计信息": battle["head_shot_count_info"],
            "招式命中次数详情": battle["moves_hit_count_info"],
            "招式伤害详情": battle["moves_hit_damage_info"],
            "平均段位分": battle["avg_rank_score"],
            "是否自定义房间": battle["is_custom_room"],
            "当前玩家数量": battle["cur_player_num"],
            "角色ID": battle["role_id"]
        }
        parsed_result.append(battle_info)
    return parsed_result
if __name__ == "__main__":
    try:
        # raw_data = {...}
        battle_data = parse_battle_data(raw_data)
        for i, battle in enumerate(battle_data[:1]):
            print(f"\n=== 第{i+1}场战斗数据 ===")
            for key, value in battle.items():
                print(f"{key}: {value}")
    except Exception as e:
        print(f"解析失败: {e}")
```


| weapon_type | 武器名称 |
|-------------|----------|
| 3910003 |  |
| 3910005 |  |
| 3910015 |  |
| 3910016 |  |
| 3910018 |  |


```
=== 第1场战斗数据 ===
房间ID: 1e4e880558c3412da15b516ed2ad8217
角色名: B站楠寻鸽
战斗类型ID: 5000108
队伍ID: 1.0
战斗逻辑时长(秒): 300.0
总存活时间(秒): 110.45
队伍排名: 17.0
最终队伍排名: 17.0
个人排名: 17.0
死亡次数: 1.0
救援次数: 0.0
比赛内得分: 0.0
助攻次数: 0.0
护甲伤害: 887.0
真实伤害: 0.0
总伤害: 887.0
伤害排名: 10.0
治疗血量: 0.0
治疗护盾: 95.0
总治疗量: 95.0
治疗排名: 3.0
击杀数: 0.0
技能使用次数: 2.0
装置伤害: 0.0
移动距离: 1102.0
连击使用次数: 3.0
连击命中次数: 1.0
使用货币数量: 0.0
结束信息: [2.0, 0.0, True]
普通攻击命中次数: 10.0
重生次数: 0.0
使用物品总数: 3.0
英雄ID: 1000017
荣誉称号信息: []
旧段位分数列表: []
新段位分数列表: []
分数排名列表: []
段位分变化值: -141.0
出生点坐标: [851.08, 80.34, 1540.81]
天赋技能ID列表: [3470120.0, 3470123.0]
魂玉物品ID列表: [3320010.0, 3320010.0, 3320011.0]
武器熟练度: [{'experience_after': 1612.0, 'exp_delta': 78.0, 'weapon_type': 3910003.0, 'level_after': 4.0}, {'experience_after': 44.0, 'exp_delta': 15.0, 'weapon_type': 3910005.0, 'level_after': 2.0}, {'experience_after': 19.0, 'exp_delta': 32.0, 'weapon_type': 3910015.0, 'level_after': 5.0}, {'experience_after': 94.0, 'exp_delta': 7.0, 'weapon_type': 3910016.0, 'level_after': 3.0}, {'experience_after': 1255.0, 'exp_delta': 6.0, 'weapon_type': 3910018.0, 'level_after': 5.0}]
被击杀类型统计: {'1': 1.0}
击晕次数: 0.0
被救援次数: 0.0
购买统计信息: {}
开启宝箱数量: 6.0
屠龙成功: False
屠龙发起: False
屠龙轮次: 0.0
进入屠龙: False
开始时间: 2025-11-28 16:51:01
结束时间: 2025-11-28 16:55:22
技能使用详情: {'1501500': 2.0}
阵营: 0.0
获胜阵营: 0.0
占点得分: 0.0
评价得分: 0.0
子战斗类型ID: 0.0
公会战队伍得分: 0.0
公会战排名: 0.0
武器伤害详情: {'Dmg without weapon': 129.0, 'Katana': 758.0}
击杀方式详情: {}
爆头统计信息: {}
招式命中次数详情: {'T_Katana_bt': 4.0, 'T_Katana_pg': 4.0, '蓄力': 4.0, '非蓄': 5.0}
招式伤害详情: {'T_Katana_bt': 604.0, 'T_Katana_pg': 154.0, '蓄力': 604.0, '非蓄': 283.0}
平均段位分: 2223.0
是否自定义房间: False
当前玩家数量: 1
角色ID: yZi21pIBk86GqxwDk860TaJiCyLEFmBKZj1wBebbEI_bDDYavuPtcPa9qNk
```
