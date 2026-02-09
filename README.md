<h1 align="center">永劫无间（端手游） - API 收集整理</h1>
<p align="center" class="shields">
    <a href="https://github.com/njmxye/NarakaBladepoint-API-collect/issues" style="text-decoration: none;">
        <img src="https://img.shields.io/github/issues/njmxye/NarakaBladepoint-API-collect.svg?style=flat&color=red" alt="GitHub issues"/>
    </a>
    <a href="https://github.com/njmxye/NarakaBladepoint-API-collect/stargazers" style="text-decoration: none;">
        <img src="https://img.shields.io/github/stars/njmxye/NarakaBladepoint-API-collect.svg?style=flat&color=yellow" alt="GitHub stars"/>
    </a>
    <a href="https://github.com/njmxye/NarakaBladepoint-API-collect/network" style="text-decoration: none;">
        <img src="https://img.shields.io/github/forks/njmxye/NarakaBladepoint-API-collect.svg?style=flat&color=blue" alt="GitHub forks"/>
    </a>
    <a href="https://github.com/njmxye/NarakaBladepoint-API-collect/actions" style="text-decoration: none;">
        <img src="https://img.shields.io/github/actions/workflow/status/njmxye/NarakaBladepoint-API-collect/vuepress-deploy.yml?style=flat" alt="Build status"/>
    </a>
    <a href="https://github.com/njmxye/NarakaBladepoint-API-collect/blob/master/LICENSE" style="text-decoration: none;">
        <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg?style=flat" alt="GitHub license"/>
    </a>
</p>

![当前在线](https://img.shields.io/badge/dynamic/json?url=https://steamcharts.com/app/1203220/chart-data.json&query=$[-1][1]&label=Steam当前在线&color=4CAF50&suffix=人)

![24小时峰值](https://img.shields.io/badge/dynamic/json?url=https://steamcharts.com/app/1203220/chart-data.json&query=$[?(@[0]>=(Date.now()-86400000))][*][1]|max&label=24h峰值&color=FF9800&suffix=人)

![历史峰值](https://img.shields.io/badge/dynamic/json?url=https://steamcharts.com/app/1203220/chart-data.json&query=$[*][1]|max&label=历史峰值&color=E91E63&suffix=人)



##### 声明

- **请勿滥用，本项目仅用于学习和测试！请勿滥用，本项目仅用于学习和测试！请勿滥用，本项目仅用于学习和测试！**
- 利用本项目提供的接口、文档等造成不良影响及后果与本人无关
- 由于本项目的特殊性，可能随时停止开发或删档
- 欢迎有兴趣者参与接口的维护更新，提交新接口请按格式增加。
- **上传任何信息时请注意脱敏，删去jwt、敏感 cookies 等可能泄漏个人信息的数据（例如 `token`等）**

<!-- 请在表尾添加新行 -->
| 名称  |  作者  | 备注  |
|-------| ----- |------ |
| （未完成）[白泽百科（端游）](docs/bzbkdy.md) | [@楠寻](https://github.com/njmxye) | 提供游戏内玩法介绍，玩法搜索，捏脸数据，征神之路，兵器攻略，英雄手册，战绩查询，举报等功能…… |
| （已完成）[战绩查询（网易uu加速器）](docs/vjixuu163.md) | [@楠寻](https://github.com/njmxye) | 提供不是很准确的战绩查询（主接口崩了的时候备用） |
| （未完成）[战绩查询（网易大神）](docs/vjixdu.md) |  | 战绩查询主接口（还没开始搞） |
<!-- 请在此处添加新行-->

```html

<iframe 
    src="https://steamcharts.com/app/1203220#app-title" 
    scrolling="no" 
    style="width:690px;height:175px;overflow:hidden;pointer-events:none;"
></iframe>


```