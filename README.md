# food-recommend - 外卖推荐 Claude Code Skill

根据当天星期几和你想吃的品类，自动推荐外卖商家，避开黑名单，支持随时扩充。

## 安装

```bash
git clone git@github.com:songleo/food-recommend-skill.git ~/.claude/skills/food-recommend
```

重启 Claude Code 即可生效。

## 使用方式

| 你说的话 | 技能回复 |
|---|---|
| "今天吃什么好？" | 根据星期几优先推荐优惠商家，列出可选品类 |
| "想吃火锅" | 推荐豆米火锅、烧椒牛肉，附理由 |
| "把福茂源加入黑名单" | 确认已加入，后续推荐自动排除 |
| "添加炒饭新店'老王炒饭'，理由是分量大" | 写入配置文件并确认 |

## 自定义

直接编辑 `config.json`：

- `categories`：按品类添加商家和推荐理由
- `daily_promotions`：按星期几配置优惠活动
- `blacklist`：添加需要排除的商家名

修改后保存即可，无需改 `SKILL.md`。

## 文件结构

```
food-recommend/
├── SKILL.md      # 技能指令
└── config.json   # 商家/优惠/黑名单数据
```
