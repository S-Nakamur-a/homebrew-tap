# homebrew-tap

S-Nakamur-a のツールの Homebrew tap。

## ccsessions

Claude Code の走行中セッションを macOS のメニューバーに**生き物の群れ**として
表示する常駐オーバーレイ → [S-Nakamur-a/ccsessions](https://github.com/S-Nakamur-a/ccsessions)

```sh
brew install S-Nakamur-a/tap/ccsessions
brew services start ccsessions
```

**入れただけでは何も起きない。** hook の配線は Claude Code のプラグインで行う
（`settings.json` の `hooks` セクションには触らない）。Claude Code の中で:

```
/plugin marketplace add S-Nakamur-a/ccsessions
/plugin install ccsessions@ccsessions-marketplace
```

導入状況の確認は `ccsessions doctor`、設定と顔作りの GUI は `ccsessions ui`。

ソースからビルドする formula なので Gatekeeper の確認も公証も要らない。
formula の原本と「なぜそう書いたか」は本体リポジトリの
[`packaging/homebrew/ccsessions.rb`](https://github.com/S-Nakamur-a/ccsessions/blob/main/packaging/homebrew/ccsessions.rb)
と [`docs/adr/0021-distribution.md`](https://github.com/S-Nakamur-a/ccsessions/blob/main/docs/adr/0021-distribution.md)。
