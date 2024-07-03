# Fetchとpullはどう違うのか

```markdown
# GitのFetchとPullの違い

## 1. Fetch（フェッチ）

Fetchは、リモートリポジトリから最新の変更を取得しますが、ローカルの作業ブランチには直接反映しません。

### 特徴:
- リモートの変更を安全に確認できる
- ローカルの作業に影響を与えない
- 変更を確認してから統合するかどうか決められる

### 使用例:
```bash
git fetch origin
```

## 2. Pull（プル）

Pullは、Fetchの後に自動的にマージを行う操作です。リモートの変更をローカルの作業ブランチに直接反映します。

### 特徴:
- リモートの変更を即座にローカルに反映
- Fetchとマージを一度に行う
- 競合が発生する可能性がある

### 使用例:
```bash
git pull origin main
```

## 3. 主な違い

- 安全性: Fetchの方が安全
- 即時性: Pullの方が即時的
- 制御: Fetchの方が細かい制御が可能

## 4. 使い分け

- 変更を確認してから統合したい場合: Fetch
- 迅速に最新の状態に更新したい場合: Pull
- チーム開発で慎重に進めたい場合: Fetch
- 個人開発で素早く同期したい場合: Pull

## 5. ワークフロー例

### Fetchを使用する場合:
1. `git fetch origin`
2. `git log --oneline --decorate --graph --all` で変更を確認
3. 問題なければ `git merge origin/main`

### Pullを使用する場合:
1. `git pull origin main`
```