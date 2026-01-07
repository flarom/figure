# VRM Viewer with VRMA Animation

[English](README.md) | [日本語](README-jp.md)

Three.jsとthree-vrmライブラリを使用して構築された、VRMA（VRMアニメーション）サポート付きのWebベースVRM（Virtual Reality Model）ビューアーです。

## 🎮 ライブデモ

**[デモを試す →](https://tk256ailab.github.io/vrm-viewer/)**

## 特徴

- 📱 **レスポンシブデザイン**: デスクトップとモバイルデバイスで動作
- 🎭 **VRMモデルサポート**: VRM 1.0モデルの読み込みと表示
- 🎬 **VRMAアニメーション**: カスタムVRMAアニメーションファイルの再生
- 🎮 **インタラクティブコントロール**: アニメーションの再生、一時停止、停止
- 🎨 **モダンUI**: 清潔でグラデーションベースのインターface
- ⚡ **高速パフォーマンス**: 最適化されたレンダリングとアニメーション

## デモ

`index.html`をWebブラウザで開くとデモを確認できます。ビューアーには以下が含まれています：

- サンプルVRMモデル（sample.vrm）
- 11種類のVRMAアニメーション例：
  - **Angry**: 怒り感情のアニメーション
  - **Blush**: 照れる感情のアニメーション
  - **Clapping**: 拍手するアニメーション
  - **Goodbye**: さよならの手振りアニメーション
  - **Jump**: ジャンプ動作のアニメーション
  - **LookAround**: 周りを見回すアニメーション
  - **Relax**: リラックスポーズのアニメーション
  - **Sad**: 悲しい感情のアニメーション
  - **Sleepy**: 眠そうな感情のアニメーション
  - **Surprised**: 驚いた感情のアニメーション
  - **Thinking**: 考え込むポーズのアニメーション

## プロジェクト構造

```
vrm_viewer/
├── index.html              # メインビューアーアプリケーション
├── VRM/
│   └── sample.vrm     # サンプルVRMモデル
├── VRMA/
│   ├── Angry.vrma          # 怒り感情のアニメーション
│   ├── Blush.vrma          # 照れる感情のアニメーション
│   ├── Clapping.vrma       # 拍手するアニメーション
│   ├── Goodbye.vrma        # さよならの手振りアニメーション
│   ├── Jump.vrma           # ジャンプ動作のアニメーション
│   ├── LookAround.vrma     # 周りを見回すアニメーション
│   ├── Relax.vrma          # リラックスポーズのアニメーション
│   ├── Sad.vrma            # 悲しい感情のアニメーション
│   ├── Sleepy.vrma         # 眠そうな感情のアニメーション
│   ├── Surprised.vrma      # 驚いた感情のアニメーション
│   └── Thinking.vrma       # 考え込むポーズのアニメーション
├── README.md               # 英語版ドキュメント
└── README-jp.md           # このファイル
```

## クイックスタート

### 方法1: GitHub Pages（推奨）

1. **このリポジトリをGitHubにフォークまたはアップロード**
2. **GitHub Pagesを有効化**：
   - リポジトリのSettingsに移動
   - 「Pages」セクションまでスクロール
   - 「Source」で「Deploy from a branch」を選択
   - ブランチを「main」、フォルダを「/ (root)」に設定
   - 「Save」をクリック
3. **デモにアクセス** `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/`

### 方法2: ローカル開発

1. **このリポジトリをクローンまたはダウンロード**
2. **ローカルWebサーバーを起動**（ファイル読み込みに必要）：
   ```bash
   # Pythonを使用
   python -m http.server 8000
   
   # Node.jsを使用
   npx serve .
   
   # PHPを使用
   php -S localhost:8000
   ```
3. **ブラウザを開き** `http://localhost:8000` にアクセス
4. **VRMモデルを読み込み**（ページ読み込み時に自動実行）
5. **VRMAボタンでアニメーションを選択**
6. **再生、一時停止、停止ボタンで再生をコントロール**

## 使用方法

### VRMモデルの読み込み

ビューアーは`index.html`で指定されたVRMモデルを自動的に読み込みます。独自のモデルを使用するには：

1. `.vrm`ファイルを`VRM/`ディレクトリに配置
2. `index.html`の`VRM_MODEL_URL`変数を更新

### VRMAアニメーションの再生

1. VRMモデルの読み込みが完全に完了するまで待機
2. VRMAアニメーションボタンのいずれかをクリックしてアニメーションを選択（Angry、Blush、Clapping、Goodbye、Jump、LookAround、Relax、Sad、Sleepy、Surprised、Thinking）
3. 再生コントロールを使用してアニメーションを管理

### カメラ操作

- **回転**: 左クリックしながらドラッグでモデルを中心にカメラを回転
- **並行移動**: 右クリックしながらドラッグでカメラを水平/垂直方向に移動
- **ズーム**: マウスホイールでズームイン/アウト

### コントロール

- **VRMAアニメーションボタン**: 異なるアニメーションの選択と読み込み
- **再生**: アニメーション再生の開始または再開
- **一時停止**: 現在のアニメーションの一時停止/再開
- **停止**: アニメーションの停止とデフォルトポーズへのリセット

## 技術詳細

### 依存関係

- [Three.js](https://threejs.org/) - 3Dグラフィックスライブラリ
- [@pixiv/three-vrm](https://github.com/pixiv/three-vrm) - VRMモデルサポート
- [@pixiv/three-vrm-animation](https://github.com/pixiv/three-vrm-animation) - VRMAアニメーションサポート

### アニメーション仕様

- **フォーマット**: glTFバイナリ形式のVRMA（VRMアニメーション）ファイル
- **ヒューマノイドボーン**: VRM 1.0ヒューマノイド仕様と互換
- **フレームレート**: 線形補間による60 FPS
- **継続時間**: 可変（含まれるアニメーションは4-12秒）

### ブラウザ互換性

- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 14+
- ✅ Edge 80+

## カスタマイズ

### 新しいアニメーションの追加

1. VRMAアニメーションファイルを作成または取得
2. `VRMA/`ディレクトリに配置
3. `index.html`の`VRMA_ANIMATION_URLS`配列を更新
4. HTMLに対応するボタンを追加

### スタイリング

インターフェースは簡単なテーマ設定のためにCSSカスタムプロパティを使用。主要な変数：

- 背景色とグラデーション
- ボタンスタイルとホバー効果
- コントロールパネルの外観
- レスポンシブブレークポイント

## ライセンス

このプロジェクトはデモンストレーション目的です。使用するVRMモデルとアニメーションについて適切な権利を持っていることを確認してください。

## 貢献

1. リポジトリをフォーク
2. フィーチャーブランチを作成
3. 変更を加える
4. 十分にテスト
5. プルリクエストを提出

## 謝辞

- [three-vrm](https://github.com/pixiv/three-vrm) - Three.js用VRMサポート
- [Three.js](https://threejs.org/) - 3Dグラフィックス基盤
- VRMコンソーシアム - VRMフォーマット仕様
