# DeepSeek Harness

[English](README.md) | [中文](README.zh.md) | 繁體中文

DeepSeek Harness（`dsh`）是由 [DeepSeek AI](https://deepseek.com) 開發的開源 Agent Harness（智慧體／代理框架）。

它構建於**一切皆外掛**（Everything is a plugin）的架構之上，由 [Cordis](https://github.com/cordiverse/cordis) 驅動，其設計參見論文 [_A Programming Paradigm for Spatiotemporal Composability_](https://arxiv.org/abs/2608.25512)。

文件：[https://deepseek-harness.github.io/deepseek-harness/](https://deepseek-harness.github.io/deepseek-harness/)

## 開發者預覽

DeepSeek Harness 處於 *開發者預覽* 階段，正在快速反覆運算。**未來將出現破壞相容性的變更。**

執行本專案前，請閱讀[安全說明](SAFETY.zh-TW.md)。

<a id="run"></a>

## 執行

### 透過 `npm` 執行

安裝 `Node.js`，然後執行：

```sh
npx @deepseek-ai/dsh web
```

該指令預設會在 `http://127.0.0.1:3080` 啟動 Web UI，本機啟動時還會以預設瀏覽器開啟頁面。透過 SSH 啟動時只會輸出主機 URL，因為本機轉發位址由 SSH 用戶端或編輯器持有。傳入 `--no-open` 可僅執行伺服器而不開啟瀏覽器。詳見 [Web UI 指南](docs/user/guide/index.zh.md)。

<a id="run-from-source"></a>

### 從原始碼執行

如需從儲存庫原始碼執行：

```sh
git clone https://github.com/deepseek-ai/deepseek-harness.git
cd deepseek-harness
pnpm install
pnpm run build
pnpm dsh web
```

`pnpm run build` 會準備儲存庫產物。`pnpm dsh web` 會直接使用這些已建置產物，不會重新建置。

## 社群與支援

- 透過 [GitHub Discussions](https://github.com/deepseek-ai/deepseek-harness/discussions) 提交意見回饋或 Bug 回報。
- 為你的外掛儲存庫新增 [`dsh-plugin`](https://github.com/topics/dsh-plugin) 主題標籤，以便於被發現。
- 歡迎加入 DeepSeek Harness 企微群！掃描下方 QR Code 填寫問卷，小助手會定期發送入群邀請。
- 歡迎加入 <a href="https://discord.gg/4MrtZUhpxg">DeepSeek Harness Discord 社群</a>。

<table>
  <thead>
    <tr>
      <th align="center">入群問卷</th>
      <th align="center">微信公眾號</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><a href="https://trtgsjkv6r.feishu.cn/share/base/form/shrcnIt5twSVdLGD52KJBckGCgg"><img src="https://cdn.deepseek.com/harness/readme/community-wecom-survey.png" alt="DeepSeek Harness 入群問卷 QR Code" width="180" height="180"></a></td>
      <td align="center"><img src="https://cdn.deepseek.com/harness/readme/community-wechat-official-account.png" alt="DeepSeek Harness 團隊微信公眾號 QR Code" width="180" height="180"></td>
    </tr>
  </tbody>
</table>

## 參與貢獻

參見 [CONTRIBUTING.zh-TW.md](CONTRIBUTING.zh-TW.md)。

## 開發

請先閱讀[開發指南](docs/development.zh.md)與[架構文件](docs/architecture.zh.md)。

`pnpm run dev:web` 會在單一終端機中完成建置、啟動，並在原始碼修改時重建 client bundle；`make help` 列出 Web 與 Desktop 對應的 Make target。完整表格見開發指南的「應用程式指令」一節。

針對 Agent：請遵循 [AGENTS.md](AGENTS.md)。

## 引用

```bibtex
@misc{deepseek-harness2026,
  title={DeepSeek Harness: Everything is a Plugin},
  author={DeepSeek-AI},
  year={2026},
  publisher={GitHub},
  howpublished={\url{https://github.com/deepseek-ai/deepseek-harness}},
}
```

## 授權條款

[MIT](LICENSE)

第三方相依套件及其授權條款見 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
