# MoooseMini ZMK Firmware

## Git操作ルール

- mainブランチに直接pushしない。作業はfeatureブランチで行い、PRを作成してマージする
- force push（--force, --force-with-lease）をしない
- ブランチやタグを削除しない
- git reset --hard をしない
- .github/ ディレクトリ内のワークフローファイルを変更しない
- 破壊的操作（リポジトリ削除、リリース削除等）を実行しない

## プロジェクト固有

- board: seeeduino_xiao_ble / shield: MoooseMini rgbled_adapter / snippet: studio-rpc-usb-uart
- pushまたはPR作成時にGitHub Actionsで自動ビルドされる
- ビルド成果物（.uf2）は `gh run download` で取得する
- 編集対象は config/MoooseMini.keymap と config/MoooseMini.conf
- boards/shields/ 以下のデバイス定義は変更しない

## 使用モジュール

config/west.yml で管理。各モジュールのREADMEに従って設定すること。

| モジュール | 作者 | 用途 | revision |
|-----------|------|------|----------|
| zmk-pmw3610-driver | badjeff | トラックボールセンサー(PMW3610)ドライバー | zmk-0.3 |
| zmk-layout-shift | kot149 | JISレイアウト対応（`&kp`をlayout-shift版に上書き） | v1 |
| zmk-scroll-snap | kot149 | スクロール方向を軸にスナップ | v1 |
| zmk-mouse-gesture | kot149 | マウスストロークをキー入力に変換 | v1 |
| zmk-listeners | ssbb | レイヤー/キーコードイベントでアクション実行 | v1 |
| zmk-rgbled-widget | caksoylar | RGB LEDでバッテリー/BT状態表示 | v0.3 |
