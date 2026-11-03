# manju-storyboard · AI 漫剧分镜制作 Skill

**版本**：v2.1.4 ｜ **形态**：自包含 Markdown 技能包（6 个 `.md`，无脚本、无外部依赖）
**用途**：把小说原文直接转成可复制投喂 AI 视频工具的分镜提示词。

> ⚠️ 本包是**独立体系**，与 `manju-pipeline-v6.5.8` / `manju-pipeline-v8` / `manju-pipeline-v6.6` **互不兼容**，
> 规则、术语、references 全部自带，不依赖任何外部真源。不要混用两者的规程。

## 四条铁律

1. **不留人不拍** — 0 秒炸弹开局，每 10 秒段必须有功能，爽点/对抗/反转/钩子段段相扣。
2. **没意义不拍** — 每个镜头开拍前必须答上「拍它有什么意义、观众买不买单」，答不出就淘汰。
3. **提示词 = 实时画面** — 运镜、动作、台词、人物关系同时态推进，全部是镜头能捕捉的语言。
4. **连续性压倒一切** — 0.5s 承接、屏幕站位、180° 轴线、景别起幅，让一堆碎片剪起来像一个人拍的。

## 核心能力

留人节奏模型（0 秒炸弹 + 10 秒功能段）｜拍摄准入制｜台词四问（4.5 字/秒净语速）｜并行时长模型｜
整秒收敛｜0.5s 首帧承接｜180° 轴线 + ASCII 俯视图｜AI 可视化语言规范｜受控词表。

## 文件结构

```
manju-storyboard/
├── SKILL.md                    # 主控文件：输入契约、执行铁律、S0a→S6 阶段流程（24.5 KB）
├── CHANGELOG.md                # 语义化版本沿革与逐条修订依据（10.8 KB）
└── references/
    ├── checklist.md            # 逐镜头卡查表（含「段」三义辨析表）（10.1 KB）
    ├── example.md              # 完整实例：炸弹表 + 分镜 + 纯台词清单（12.2 KB）
    ├── templates.md            # 各类交付物模板（7.8 KB）
    └── vocabulary.md           # 受控词表（6.6 KB）
```

## 怎么用

1. 读 `SKILL.md`（入口，含输入契约与失败处理）；
2. 写作时按需查 `references/checklist.md`（逐镜过检）与 `references/templates.md`（交付物格式）；
3. 拿不准格式就先照 `references/example.md` 仿写；
4. 术语歧义看 `references/vocabulary.md` 与 checklist 开头的三义辨析表。

把整个目录放进你的 agent 技能目录（例如 `~/.workbuddy/skills/manju-storyboard/`），或在会话中直接投喂 `SKILL.md` + 所需 `references/`。

## 来源与维护

- 原始包为微信分发的 `.skill` 文件（2026-10-25 收到），经 7 轮修订后定为 v2.1.4：搬正 S4/S5/S6、补卡六、拆运镜「拉」、补整秒收敛、术语三义辨析。
- 逐条修订依据见 `CHANGELOG.md`。
- 仓库由 DSH 侧（郑月漓）经 GitHub REST API 发布，2026-11-04。
