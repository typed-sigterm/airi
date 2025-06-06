<p align="center">
  <picture>
    <source
      width="250"
      srcset="./docs/public/logo-dark.png"
      media="(prefers-color-scheme: dark)"
    />
    <source
      width="250"
      srcset="./docs/public/logo-light.png"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img width="250" src="./docs/public/logo-light.png" />
  </picture>
</p>

<h1 align="center">Project AIRI</h1>

<p align="center">
  [<a href="https://discord.gg/TgQ3Cu2F7A">Discordサーバーに参加する</a>] [<a href="https:///airi.moeru.ai">試してみる</a>] [<a href="https://github.com/moeru-ai/airi/blob/main/README.zh-CN.md">文档</a>]
</p>

> [Neuro-sama](https://www.youtube.com/@Neurosama) に大きな影響を受けました

<img src="./docs/public/readme-image-pc-preview.png">

他のAI駆動のVTuberオープンソースプロジェクトとは異なり、アイリVTuberは開発初日から[WebGPU](https://www.w3.org/TR/webgpu/)、[WebAudio](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)、[Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers)、[WebAssembly](https://webassembly.org/)、[WebSocket](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket)などの多くのWeb技術をサポートしています。

これは、**アイリVTuberが現代のブラウザやデバイスで動作可能である**ことを意味し、モバイルデバイスでも動作します（PWAサポート済み）。これにより、私たち（開発者）はアイリVTuberの力を次のレベルに引き上げるための多くの可能性を持ちつつ、ユーザーがTCP接続や他の非Web技術を必要とする機能を有効にする柔軟性を残しています。例えば、Discordのボイスチャネルに接続したり、MinecraftやFactorioを友達と一緒にプレイすることができます。

> [!NOTE]
>
> 私たちはまだ開発の初期段階にあり、才能ある開発者を探しています。アイリVTuberを現実のものにするために私たちを助けてください。
>
> Vue.js、TypeScript、またはこのプロジェクトに必要な開発ツールに慣れていなくても大丈夫です。アーティスト、デザイナー、または最初のライブストリームを立ち上げる手助けをすることもできます。
>
> ReactやSvelte、Solidの大ファンであっても歓迎します。アイリVTuberに見たい機能を追加したり、実験したい機能を追加するためのサブディレクトリを開くことができます。
>
> 私たちが探している分野（および関連プロジェクト）：
>
> - Live2Dモデラー
> - VRMモデラー
> - VRChatアバターデザイナー
> - コンピュータビジョン
> - 強化学習
> - 音声認識
> - 音声合成
> - ONNXランタイム
> - Transformers.js
> - vLLM
> - WebGPU
> - Three.js
> - WebXR（@moeru-ai組織の[別のプロジェクト](https://github.com/moeru-ai/n3p6)もチェックしてください）
>
> **興味があるなら、ここで自己紹介してみませんか？ [Would like to join part of us to build Airi?](https://github.com/moeru-ai/airi/discussions/33)**

## 現在の進捗

可能なこと

- [x] 脳
  - [x] [Minecraft](https://www.minecraft.net)をプレイ
  - [x] [Factorio](https://www.factorio.com)をプレイ（進行中ですが、[PoCとデモが利用可能](https://github.com/moeru-ai/airi-factorio)）
  - [x] [Telegram](https://telegram.org)でチャット
  - [x] [Discord](https://discord.com)でチャット
  - [ ] メモリ
    - [x] ブラウザ内データベースサポート（DuckDB WASM | `pglite`）
    - [ ] メモリアラヤ（進行中）
  - [ ] ブラウザ内ローカル（WebGPU）推論
- [x] 耳
  - [x] ブラウザからの音声入力
  - [x] [Discord](https://discord.com)からの音声入力
  - [x] クライアント側の音声認識
  - [x] クライアント側の話し声検出
- [x] 口
  - [x] [ElevenLabs](https://elevenlabs.io/)音声合成
- [x] 体
  - [x] VRMサポート
    - [x] VRMモデルの制御
  - [x] VRMモデルのアニメーション
    - [x] 自動まばたき
    - [x] 自動視線追従
    - [x] アイドル時の目の動き
  - [x] Live2Dサポート
    - [x] Live2Dモデルの制御
  - [x] Live2Dモデルのアニメーション
    - [x] 自動まばたき
    - [x] 自動視線追従
    - [x] アイドル時の目の動き

## 開発

> このプロジェクトの詳細な開発手順については、[CONTRIBUTING.md](./CONTRIBUTING.md)を参照してください

```shell
pnpm i
```

### ドキュメントサイト

```shell
pnpm -F @proj-airi/docs dev
```

### ステージウェブ（[airi.moeru.ai](https://airi.moeru.ai)のフロントエンド）

```shell
pnpm -F @proj-airi/stage-web dev
```

### ステージたまごっち（アイリVTuberのElectronアプリ）

```shell
pnpm -F @proj-airi/stage-tamagotchi dev
```

## サポートされているLLM APIプロバイダー（[xsai](https://github.com/moeru-ai/xsai)によって提供）

- [x] [OpenRouter](https://openrouter.ai/)
- [x] [vLLM](https://github.com/vllm-project/vllm)
- [x] [SGLang](https://github.com/sgl-project/sglang)
- [x] [Ollama](https://github.com/ollama/ollama)
- [x] [Google Gemini](https://developers.generativeai.google)
- [x] [OpenAI](https://platform.openai.com/docs/guides/gpt/chat-completions-api)
  - [ ] [Azure OpenAI API](https://learn.microsoft.com/en-us/azure/ai-services/openai/reference)（PR歓迎）
- [x] [Anthropic Claude](https://anthropic.com)
  - [ ] [AWS Claude](https://learn.microsoft.com/en-us/azure/ai-services/openai/reference)（PR歓迎）
- [x] [DeepSeek](https://www.deepseek.com/)
- [x] [Qwen](https://help.aliyun.com/document_detail/2400395.html)
- [x] [xAI](https://x.ai/)
- [x] [Groq](https://wow.groq.com/)
- [x] [Mistral](https://mistral.ai/)
- [x] [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/)
- [x] [Together.ai](https://www.together.ai/)
- [x] [Fireworks.ai](https://www.together.ai/)
- [x] [Novita](https://www.novita.ai/)
- [x] [Zhipu](https://bigmodel.cn)
- [x] [SiliconFlow](https://cloud.siliconflow.cn/i/rKXmRobW)
- [x] [Stepfun](https://platform.stepfun.com/)
- [x] [Baichuan](https://platform.baichuan-ai.com)
- [x] [Minimax](https://api.minimax.chat/)
- [x] [Moonshot AI](https://platform.moonshot.cn/)
- [x] [Tencent Cloud](https://cloud.tencent.com/document/product/1729)
- [ ] [Sparks](https://www.xfyun.cn/doc/spark/Web.html)（PR歓迎）
- [ ] [Volcano Engine](https://www.volcengine.com/experience/ark?utm_term=202502dsinvite&ac=DSASUQY5&rc=2QXCA1VI)（PR歓迎）

## このプロジェクトから生まれたサブプロジェクト

- [Awesome AI VTuber](https://github.com/proj-airi/awesome-ai-vtuber): AI VTuberと関連プロジェクトのキュレーションリスト
- [`unspeech`](https://github.com/moeru-ai/unspeech): `/audio/transcriptions`と`/audio/speech`のためのユニバーサルエンドポイントプロキシサーバー、LiteLLMのように、任意のASRとTTSに対応
- [`hfup`](https://github.com/moeru-ai/hfup): HuggingFace Spacesへのデプロイとバンドルを支援するツール
- [`xsai-transformers`](https://github.com/moeru-ai/xsai-transformers): [xsAI](https://github.com/moeru-ai/xsai)のための実験的な[🤗 Transformers.js](https://github.com/huggingface/transformers.js)プロバイダー
- [WebAI: Realtime Voice Chat](https://github.com/proj-airi/webai-realtime-voice-chat): VAD + STT + LLM + TTSを使用してChatGPTのリアルタイム音声をゼロから実装する完全な例
- [`@proj-airi/drizzle-duckdb-wasm`](https://github.com/moeru-ai/airi/tree/main/packages/drizzle-duckdb-wasm/README.md): DuckDB WASMのDrizzle ORMドライバー
- [`@proj-airi/duckdb-wasm`](https://github.com/moeru-ai/airi/tree/main/packages/duckdb-wasm/README.md): `@duckdb/duckdb-wasm`の使いやすいラッパー
- [Airi Factorio](https://github.com/moeru-ai/airi-factorio): AiriがFactorioをプレイできるようにする
- [Factorio RCON API](https://github.com/nekomeowww/factorio-rcon-api): FactorioヘッドレスサーバーコンソールのRESTful APIラッパー
- [`autorio`](https://github.com/moeru-ai/airi-factorio/tree/main/packages/autorio): Factorio自動化ライブラリ
- [`tstl-plugin-reload-factorio-mod`](https://github.com/moeru-ai/airi-factorio/tree/main/packages/tstl-plugin-reload-factorio-mod): Factorioモッドの開発時にリロードをサポート
- [Velin](https://github.com/luoling8192/velin): Vue SFCとMarkdownを使用してLLMのための管理しやすい状態のプロンプトを書く
- [`demodel`](https://github.com/moeru-ai/demodel): さまざまな推論ランタイムからモデルやデータセットをデプロイ、バンドルするためのツール
- [`inventory`](https://github.com/moeru-ai/inventory): 中央集権的なモデルカタログとデフォルトプロバイダー設定のバックエンドサービス
- [MCP Launcher](https://github.com/moeru-ai/mcp-launcher): すべての可能なMCPサーバーのための簡単に使用できるMCPビルダー＆ランチャー、Ollamaのようにモデルのためのもの！
- [🥺 SAD](https://github.com/moeru-ai/sad): 自己ホストおよびブラウザで実行されるLLMのためのドキュメントとノート

```mermaid
%%{ init: { 'flowchart': { 'curve': 'catmullRom' } } }%%

flowchart TD
  Core("コア")
  Unspeech["unspeech"]
  DBDriver["@proj-airi/drizzle-duckdb-wasm"]
  MemoryDriver["[WIP] メモリアラヤ"]
  DB1["@proj-airi/duckdb-wasm"]
  ICONS["@proj-airi/lobe-icons"]
  UI("@proj-airi/stage-ui")
  Stage("ステージ")
  F_AGENT("Factorioエージェント")
  F_API["Factorio RCON API"]
  F_MOD1["autorio"]
  SVRT["@proj-airi/server-runtime"]
  MC_AGENT("Minecraftエージェント")
  XSAI["xsai"]

  subgraph Airi
    DB1 --> DBDriver --> MemoryDriver --> Memory --> Core
    ICONS --> UI --> Stage --> Core
    Core --> STT
    Core --> SVRT
  end

  STT --> |話す|Unspeech
  SVRT --> |Factorioをプレイ|F_AGENT
  SVRT --> |Minecraftをプレイ|MC_AGENT

  subgraph Factorioエージェント
    F_AGENT --> F_API -..- factorio-server
    subgraph factorio-server-wrapper
      subgraph factorio-server
        F_MOD1
      end
    end
  end

  subgraph Minecraftエージェント
    MC_AGENT --> Mineflayer -..- minecraft-server
    subgraph factorio-server-wrapper
      subgraph factorio-server
        F_MOD1
      end
    end
  end

  XSAI --> Core
  XSAI --> F_AGENT
  XSAI --> MC_AGENT
```

```mermaid
%%{ init: { 'flowchart': { 'curve': 'catmullRom' } } }%%

flowchart TD
  subgraph デプロイ＆バンドル
    direction LR
    HFUP["hfup"]
    HF[/"HuggingFace Spaces"\]
    HFUP -...- UI -...-> HF
    HFUP -...- whisper-webgpu -...-> HF
    HFUP -...- moonshine-web -...-> HF
  end

```

## 使用されているモデル

- [onnx-community/whisper-large-v3-turbo · Hugging Face](https://huggingface.co/onnx-community/whisper-large-v3-turbo)

## 類似プロジェクト

### オープンソースのもの

- [kimjammer/Neuro: A recreation of Neuro-Sama originally created in 7 days.](https://github.com/kimjammer/Neuro): 非常に完成度の高い実装
- [SugarcaneDefender/z-waif](https://github.com/SugarcaneDefender/z-waif): ゲーム、自律エージェント、プロンプトエンジニアリングに優れています
- [semperai/amica](https://github.com/semperai/amica/): VRM、WebXRに優れています
- [elizaOS/eliza](https://github.com/elizaOS/eliza): エージェントをさまざまなシステムやAPIに統合するための優れた例
- [ardha27/AI-Waifu-Vtuber](https://github.com/ardha27/AI-Waifu-Vtuber): Twitch APIの統合に優れています
- [InsanityLabs/AIVTuber](https://github.com/InsanityLabs/AIVTuber): 素晴らしいUIとUX
- [IRedDragonICY/vixevia](https://github.com/IRedDragonICY/vixevia)
- [t41372/Open-LLM-VTuber](https://github.com/t41372/Open-LLM-VTuber)
- [PeterH0323/Streamer-Sales](https://github.com/PeterH0323/Streamer-Sales)

### 非オープンソースのもの

- https://clips.twitch.tv/WanderingCaringDeerDxCat-Qt55xtiGDSoNmDDr https://www.youtube.com/watch?v=8Giv5mupJNE
- https://clips.twitch.tv/TriangularAthleticBunnySoonerLater-SXpBk1dFso21VcWD

## プロジェクトのステータス

![Repobeats analytics image](https://repobeats.axiom.co/api/embed/a1d6fe2c13ea2bb53a5154435a71e2431f70c2ee.svg 'Repobeats analytics image')

## 謝辞

- [pixiv/ChatVRM](https://github.com/pixiv/ChatVRM)
- [josephrocca/ChatVRM-js: A JS conversion/adaptation of parts of the ChatVRM (TypeScript) code for standalone use in OpenCharacters and elsewhere](https://github.com/josephrocca/ChatVRM-js)
- UIとスタイルのデザインは、[Cookard](https://store.steampowered.com/app/2919650/Cookard/)、[UNBEATABLE](https://store.steampowered.com/app/2240620/UNBEATABLE/)、および[Sensei! I like you so much!](https://store.steampowered.com/app/2957700/_/)の作品、[Ayame by Mercedes Bazan](https://dribbble.com/shots/22157656-Ayame)と[Wish by Mercedes Bazan](https://dribbble.com/shots/24501019-Wish)のアートワークに触発されました
- [mallorbc/whisper_mic](https://github.com/mallorbc/whisper_mic)
- [`xsai`](https://github.com/moeru-ai/xsai): LLMやモデルと対話するための多くのパッケージを実装しました。 [Vercel AI SDK](https://sdk.vercel.ai/)のように小さなものです。

## スター履歴

[![Star History Chart](https://api.star-history.com/svg?repos=moeru-ai/airi&type=Date)](https://www.star-history.com/#moeru-ai/airi&Date)
