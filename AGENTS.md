# Local Codex Agent Rules — pcr-tool

対象: 上流由来のPCR Toolリポジトリ（既存開発ブランチを保護）。

## Loop Engineering（2026-11-17）
- [固有の開発・試験ループ](docs/LOOP_ENGINEERING.md)、[Codex再開指示](prompts/CODEX_LOOP.md)を先に読む。
- README等の既存仕様・停止指示を尊重。1起動1件の小タスクを現状→仮説→実装→テスト→評価→次タスクとする。
- READYなしでも未完了を確認するが、存在しない課題は作らない。外部操作や本番変更の承認を迂回しない。


## progress-collection対応（2026-11-17）
- `progress.md` を監視と既存Codexへの指示候補の正本として登録。実機で既存 `PROGRESS.md` がある場合は二重作成しない。
- 開発ループ終了時に、実装差分・検証証拠・状態/次タスクを更新する。未完了の根拠がなければNO_TASK。
- 実際の指示送信はホスト/既存thread/権限が確認された場合のみ。監視だけをPASSとしない。
