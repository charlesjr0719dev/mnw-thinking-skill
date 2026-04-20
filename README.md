# MNV Thinking Skill

> 密涅瓦思考專家——一個 Claude Code skill，當你帶著問題/決策/困惑來諮詢時，從 76 個密涅瓦思考角度（Habits of Cognition）中挑 2-4 個最合適的切入，跟你討論而不是教你。

## 這是什麼

**MNV 不是導師，是思考夥伴**。它的工作是：

1. **診斷**——你真正的問題（常常不是表面那個）
2. **挑角度**——從 76 個密涅瓦思考角度裡挑 2-4 個最貼題的
3. **討論**——用這些角度問你問題，**不給答案，給下一個該想的問題**

## 安裝（一行）

```bash
git clone https://github.com/charlesjr0719dev/mnv-thinking-skill.git ~/.claude/skills/MNV
```

完成。零設定、零路徑修改。

## 使用

在 Claude Code 對話中說以下任一句話即可觸發：

- 「問問 MNV」
- 「MNV 怎麼看」
- 「MNV 我想請教」
- 「用密涅瓦角度看」
- 「幫我用思考角度分析」

或直接丟一個需要思考框架協助的問題給 MNV。

## 結構

```
~/.claude/skills/MNV/
├── SKILL.md                    # MNV skill 主檔（Claude 自動讀取）
└── knowledge-base/
    ├── 密涅瓦思考習慣.md         # 主索引
    ├── 01-批判性思考.md         # 4 大類索引
    ├── 02-創意思考.md
    ├── 03-有效溝通.md
    ├── 04-有效互動.md
    └── HC/                      # 76 個思考角度個別筆記
        ├── 01-批判性思考/       # 5 子類
        ├── 02-創意思考/         # 3 子類
        ├── 03-有效溝通/         # 2 子類
        └── 04-有效互動/         # 4 子類
```

> 註：資料夾名稱沿用密涅瓦原始的 `HC`（Habits of Cognition）以保持與既有筆記的相容性。內文一律用「**思考角度**」這個更直觀的中文。

## 如何運作

當你觸發 MNV 後，Claude 會：

1. 讀 `SKILL.md` 了解 MNV 的工作流
2. 讀 `knowledge-base/密涅瓦思考習慣.md` 抓 76 個思考角度的地圖
3. 根據你的問題挑 2-4 個角度
4. 需要某個角度細節時才讀對應的個別筆記檔

## 範例對話

```
你：MNV 我在想要不要買新筆電

MNV：
診斷：你表面在問「要不要買」，但真正卡的是「不確定下游用途」。

建議從這 2 個角度切入：
- 🎯 效用 — 買了之後下一步具體要做什麼？
- ⚖️ 約束條件 — 預算、時間、現有設備能不能撐？

先想這個：
新筆電解決的是哪個現有設備做不到的事？如果列不出三件具體的事，就還沒到買的時候。
```

## ⚠️ Disclaimer

這是基於 [Minerva University](https://www.minerva.edu/) 的 **Habits of Cognition (HoCs) 框架**，由 AI 輔助整理的個人學習筆記。

- 內容為作者個人詮釋，不代表 Minerva 官方教材
- 原始 HoCs 框架版權歸 Minerva 大學所有
- 本 repo 僅供個人學習與思考輔助使用，請勿商用

如果你是 Minerva 大學的學生或校友，建議直接使用官方教材；本 repo 適合非 Minerva 背景但對思考工具有興趣的人快速建立思考框架。

## 客製化

想用你自己的話風格？直接 fork 這個 repo，改 `SKILL.md` 裡的「使用者」稱呼、語氣偏好、輸出格式，再 clone 你的 fork 即可。

## License

MIT — 詳見 [LICENSE](./LICENSE)

---

*Built with ❤️ for thinking better, not knowing more.*
