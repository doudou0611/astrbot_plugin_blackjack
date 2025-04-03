# 欢乐21点游戏插件
# 这是kjqwdw的修改版本，改变了发牌策略，现在初始牌通过私聊发送，而不是在群发
   原作者：kjqwdw
   原项目：https://github.com/kjqwdw/astrbot_plugin_game_sy

一个基于 AstrBot 的多人21点游戏插件，支持2-4人同时游戏。

## 游戏规则

1. 2-4人即可开始游戏
2. A可以算1点或11点
3. JQK都算10点
4. 其他牌按面值计算
5. 超过21点爆牌
6. 未爆牌者中点数最大者获胜

## 指令列表

- `/hj create` - 创建游戏房间
- `/hj join` - 加入游戏
- `/hj start` - 开始游戏（仅房主可用）
- `/hj hit` - 要牌
- `/hj stand` - 停牌
- `/hj help` - 显示帮助信息

## 游戏流程

1. 群内任意成员使用 `/hj create` 创建游戏房间
2. 其他玩家使用 `/hj join` 加入游戏
3. 当人数达到2-4人时，房主可以使用 `/hj start` 开始游戏
4. 游戏开始后，每位玩家轮流进行操作：
   - 使用 `/hj hit` 要牌
   - 使用 `/hj stand` 停牌
5. 当所有玩家都停牌或爆牌后，游戏结束并显示结果

## 安装方法

1. 将插件文件夹 `astrbot_plugin_game_sy` 复制到 AstrBot 的 plugins 目录下
2. 重启 Bot 或使用重载插件命令

## 注意事项

- 游戏需要在群聊中进行
- 每个群同时只能进行一局游戏
- 游戏中途可以使用 `/hj quit` 退出
- 如果房主退出，游戏将自动结束

## 版本历史

- v1.0.0: 初始版本
  - 支持基础的21点游戏功能
  - 支持2-4人游戏
  - 实现基本的游戏流程控制

## 机器人玩家

当玩家人数不足时，可以添加机器人玩家参与游戏：

- 使用 `/hj addbot` 添加一个机器人玩家
- 机器人玩家会自动进行游戏
- 机器人的策略：
  - 点数 ≤ 11：必定要牌
  - 点数 12-16：70%概率要牌
  - 点数 ≥ 17：停牌
- 每个房间最多可以添加3个机器人

