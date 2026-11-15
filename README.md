# モデルとデータの図鑑（公開用）

このリポジトリは、Webページを公開するためだけの置き場所です。中身（台帳）と書き出しのプログラムは、非公開のリポジトリ `research-catalog` にあります。

- 公開の流れ：`.github/workflows/pages.yml` が、毎朝6時（日本時間）と、このリポジトリの main が変わったときに、`research-catalog` を読み取り専用の鍵（Secret `CATALOG_TOKEN`）で読み込み、`scripts/build_site.py` でページを書き出して GitHub Pages に公開します。
- 手で公開し直すとき：Actions → pages → Run workflow。
- 鍵の期限が切れると更新が止まります（ページは残ります）。期限前に Fine-grained token を作り直し、Settings → Secrets and variables → Actions の `CATALOG_TOKEN` を更新してください。
- このリポジトリに置いた HTML（`index.html` など）は公開に使われません。公開されるのは毎回書き出したページです。
