# ZMK MoooseMini ファームウェア

## Git操作ルール

- mainブランチに直接pushしない。作業はfeatureブランチで行い、PRを作成してマージする
- force push（--force, --force-with-lease）をしない
- ブランチやタグを削除しない
- git reset --hard をしない
- .github/ ディレクトリ内のワークフローファイルを変更しない

## ビルド

- board: seeeduino_xiao_ble
- shield: MoooseMini rgbled_adapter
- snippet: studio-rpc-usb-uart
- pushまたはPR作成時にGitHub Actionsで自動ビルドされる
- ビルド成果物（.uf2）は `gh run download` で取得する

## キーマップ編集

- 編集対象は config/MoooseMini.keymap と config/MoooseMini.conf
- boards/shields/ 以下のデバイス定義は変更しない
