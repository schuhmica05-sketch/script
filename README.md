# script

**把已确定的商业短视频选题，写成 3 条获客导向、可直接拍摄的完整口播。适用于短视频脚本、商业文案与获客内容。**

An Agent Skill / AI Skill for commercial short-video script writing and customer-acquisition copywriting, turning a validated topic into three shoot-ready scripts.

工作版本 V0.2，以中文为主，也跟随用户语言。适合实体商家、创始人 IP、专家型个人、专业服务和高客单业务。以真实项目材料为基础，帮助观众形成新的判断，并增加进一步了解业务的理由。

核心原则：**结构负责稳定，内容负责惊喜。** Skill 负责守住选题、事实和论证方向，不把正文写成检查表；具体语言、节奏、故事和情绪留给生成时自由发挥。

## 它做什么

```text
topic output → one main purpose → structure routing
→ free writing → light quality gate → 3 scripts
```

在七种结构中选择适合当前材料的论证方式。有明显优解时，同结构写三条实质不同的稿；没有唯一优解时，用三种合适结构各写一条。结构只负责信息怎样推进，正文不按“开头/证据/金句/购买理由”逐项填空。写完后只检查跑题、编造、重复、用户收获和商业推进。默认只给文案 A、B、C，可以自然结束，不必私信、评论或领资料。

## 它不做什么

- 不重新选题，也不擅自替换用户已经确定的题目。
- 不保证爆款、客咨、成交或经营效果。
- 不虚构案例、客户原话、数据、疗效、法律结论或领取资料。
- 不替代拍摄、剪辑、发布、销售承接，不自动接入业务系统。

## 最小用法

在支持本地 Agent Skills 的宿主中加载此目录的 `SKILL.md`，保持 `references/` 与 `agents/` 的相对路径。文件夹名称为 `script`，无脚本、MCP、API Key 或额外运行依赖。审核期间可明确指定本地 `SKILL.md` 路径试用；审核后再按宿主的技能安装方式放入技能目录。本包未验证各宿主的自动发现行为。

```text
请用 $script 根据下面的 topic 输出写3条获客型短视频文案：

选题：……
实际讲什么：……
依据／待补素材：……
```

也可原样粘贴 `topic` 的 `### 01｜选题表达`、`**实际讲什么：**`、`**依据／待补素材：**`。已有项目、受众、案例和表达习惯无需重复填写。没经过 `topic` 的固定选题，只要事实足够，也能使用。

事实足够即出稿。只有会改变正文的核心缺口才补问，通常 1—3 个问题；缺失会导致承诺无法成立时先说明，不用编造凑足三稿。尚未执行的体验或演示保持结果开放。

## 与 topic 组合

```text
real business info → $topic → topic output → $script → 3 complete scripts
```

`topic` 决定什么值得讲，`script` 决定怎么讲。两者独立，`script` 不需要自动调用或修改 `topic`。

## 证据与边界

V0.2 是可用工作版，不是已证明跨所有行业有效的算法。校准案例反映制作说明中的专家可拍性信号，不代表本包独立复核或真实发布获客效果。康养内容保留主观体感与服务过程；风险内容帮助确认身份、行为和事实，不能凭文案结构给出确定医学或法律结论。

## 文件说明

- [SKILL.md](SKILL.md)：输入契约、判断流程、路由、写作、质量门槛和输出边界。
- [references/judgment-guide.md](references/judgment-guide.md)：七种母结构及关键写作判断。
- [references/calibration-cases.md](references/calibration-cases.md)：四组校准案例及方法证据限制。
- [agents/openai.yaml](agents/openai.yaml)：界面名称、描述和默认调用提示。
- [LICENSE](LICENSE)：MIT 许可证。

## 许可证

采用 [MIT License](LICENSE)。
