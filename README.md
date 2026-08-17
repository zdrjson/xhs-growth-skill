# xhs-growth

一个给 Claude Code / Claude Agent 用的 Skill：小红书起号、定位、爆款内容、涨粉节奏与变现的实操方法论。

方法论蒸馏自 **[@yanliudreamer](https://x.com/yanliudreamer/articles)**（小红书 *Dreamer妍妍*，19.8 万粉）公开发表的 5 篇小红书系列长文。本仓库不收录原文，只整理其中可执行的判断与操作，原文请读作者主页。

## 内容

| 文件 | 覆盖 |
|---|---|
| `xhs-growth/SKILL.md` | 入口：按用户所处阶段路由到对应参考 |
| `references/01-positioning.md` | 定位、人设、垂直度、8 个起号误区 |
| `references/02-cold-start.md` | 推荐逻辑、封面标题公式、第一条与前 10 条、执行细节 |
| `references/03-viral-content.md` | 爆款公式、四段结构、会爆的 5 种类型、写前三问 |
| `references/04-rhythm-0-10k.md` | 内容储备节奏、三件事循环、0→1万粉四阶段排期与内容配比 |
| `references/05-monetization-ip.md` | 变现四层结构、个人IP如何长出来、长期主义 |
| `references/00-sources.md` | 出处、作者背景、结论的适用边界 |

## 安装

```bash
git clone https://github.com/zdrjson/xhs-growth-skill.git
cp -r xhs-growth-skill/xhs-growth ~/.claude/skills/
```

之后在 Claude Code 里问"我的小红书怎么起号 / 为什么没流量 / 这周发什么"就会触发。

## 适用边界

作者的经验建立在**知识 / 职场 / AI 类个人 IP** 赛道，且本人有硅谷大厂与哈佛背书。带货号、纯生活号、无背书素人套用时需要打折——尤其"广告报价 ≈ 粉丝数 1/10"这类数字是该品类行情，不是通用标准。

## License

方法论版权归原作者 [@yanliudreamer](https://x.com/yanliudreamer) 所有，本仓库为学习整理，非商业用途。整理部分以 MIT 提供。
