# Third-party notices

未使用 Qwerty Learner 代码或数据。未使用 OpenEtymology 完整生产 SQLite 词典。

应用原创代码与原创 SVG 许可证见根目录 `LICENSE`（MIT）。第三方数据按各自来源和下列许可分别适用；不得把全部资源笼统写成 MIT 或 CC0。

## 运行时

- react, react-dom: MIT
- dexie: Apache-2.0
- pixi.js 8.21.0: MIT
- howler 2.2.4: MIT

## 开发

- vite: MIT
- @vitejs/plugin-react: MIT
- typescript: Apache-2.0
- vitest: MIT
- oxlint: MIT
- fake-indexeddb: Apache-2.0 / MIT
- @types/react, @types/react-dom, @types/node, @types/howler: MIT

## 字体

- Space Grotesk：SIL Open Font License 1.1，本地 WOFF2，用于拉丁界面与数字。
- Fraunces：SIL Open Font License 1.1，本地 WOFF2，用于大号英文词核。
- 中文界面使用系统字体栈：`-apple-system, BlinkMacSystemFont, "PingFang SC", "Noto Sans SC", "Microsoft YaHei", sans-serif`。
- 禁止远程 Google Fonts 与运行时 CDN。

## 音频

- Kenney Interface Sounds / Impact Sounds / Sci-Fi Sounds：CC0 1.0，仅选用个别官方文件，不整包塞入应用。
- 单词发音继续使用设备系统 `speechSynthesis`，优先美式英语；不把角色台词做成机器 TTS。
- 现有 Web Audio 程序化层仍可作为开发回退，不得冒充最终 Kenney 采样。

每项部署音频必须能从 manifest 追溯：文件 → 来源 → 版本 → 许可证 → SHA-256 → 用途。详见 `docs/ASSET_LICENSES.md` 与 `src/v5/audio/audioManifest.ts`。

## 数据

课程词库数据采用多来源组合，各字段保留其来源和适用许可：

- FrequencyWords / OpenSubtitles2018-derived frequency content：CC BY-SA 4.0，仅用于排序；FrequencyWords 生成器代码为 MIT，本应用未再分发该代码。
- Open English WordNet 2025：CC BY 4.0，用于词性、义项、定义和现有例句。
- ECDICT 1.0.28：MIT，Copyright (c) 2017 Linwei；用于词性匹配的中文释义片段和词形。
- CMUdict：BSD-style redistribution terms with CMU notice；用于美式发音标注。
- CEFR-J / Open Language Profiles A1-B2：须引用数据集；允许免费研究和商业用途；版权归 Tono Laboratory at TUFS。引用：The CEFR-J Wordlist Version 1.5. Compiled by Yukio Tono, Tokyo University of Foreign Studies.
- Octanove Vocabulary Profile C1/C2：CC BY-SA 4.0。
- CEFR 等级仅在来源记录确实提供时附加；不把 CEFR-J 条款扩展到 Octanove，也不把 Octanove 的 CC BY-SA 套用到 CEFR-J。

来源版本及原文证据保存在交付记录中；课程清单逐字段记录来源、许可和修订版本。

正式专八学习内容派生自 OpenEtymology 公开词书：

- 仓库: https://github.com/openetymology/OpenEtymology
- 文件: `TEM8/TEM8.txt`, `TEM8/TEM8.epub`
- 代码许可证: Apache-2.0
- 数据许可证: CC BY-SA 4.0
- 本应用派生词包同样按 CC BY-SA 4.0 保留署名
- 处理方式: EPUB/XHTML 确定性解析、精确词形匹配、固定章节、可学习资格筛选
- 完整生产词典数据库未包含、未授权

## 开源参考

见 `docs/OPEN_SOURCE_REVIEW.md`。未引入 simple-keyboard、Monkeytype、kbsim、Thock、`@pixi/react` 或 `pixi-filters` 依赖。
