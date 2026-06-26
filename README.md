# ちさの相談室 / lien — 恋愛・復縁の電話相談 SEOサイト

復縁・恋愛の電話相談（ちさの相談室／結城ちさ）の集客用 静的サイト。
当面のCTAはココナラ（https://coconala.com/services/4283448 ）へ誘導。

## 構成
- `index.html` … LP（強み・悩み・流れ・料金・プロフィール・FAQ・記事一覧・CTA）
- `articles/` … SEO記事
  - `fukuen-denwa-soudan.html` 復縁したいとき／まず整理すべき5つ
  - `kidoku-suru.html` 既読スルーは脈なし？追わない理由と次の一手
  - `block-fukuen.html` ブロックされたら復縁は無理？
- `styles.css` / `sitemap.xml` / `robots.txt`

## SEO方針
- 激戦の「電話相談」正面ではなく、ロングテール＋独自性で狙う：
  「復縁 電話相談」「既読スルー 脈なし」「ブロック 復縁」「既婚者 恋愛相談 電話」「元キャバ嬢 恋愛相談」
- 記事を増やすほど資産になる。テーマ案：既婚者・不倫の整理／別れるか迷う／依存しやすい恋愛／マッチングアプリの進め方 等。
- 各ページの title・description・canonical・OGP は記入済み。記事を足したら sitemap.xml に追記。

## 公開前にやること（重要）
1. **ドメイン/公開URLを決める**。全ファイルの `https://oshiro17.github.io/chisa-soudan` を実URLへ一括置換：
   - `index.html`（canonical / og:url）、各 `articles/*.html`（canonical）、`sitemap.xml`、`robots.txt`
2. **OGP画像**を用意して `og:image` を追加すると、SNSシェアの見栄えが上がる。
3. 公開後、**Google Search Console** にサイト登録＋ sitemap.xml を送信（インデックス促進）。
4. **Googleビジネス プロフィール**やSNS（Instagram等）からの導線も併設すると初速が出る。

## デプロイ（資格サイトと同じGitHub Pages方式が手軽・無料）
1. このフォルダを git 初期化し、GitHubの新規リポジトリへ push
2. リポジトリ設定 → Pages → main / root を公開
3. 独自ドメインを使う場合は `CNAME` ファイルを追加し、DNSを設定（資格サイトと同手順）

## 将来：自前の「1分課金」電話相談（Phase 2）
ココナラ手数料を外して自前で1分課金にする場合は、Twilio（番号秘匿＋通話時間計測）＋Stripe（カード事前登録→通話後に従量課金）＋常時稼働のバックエンドが必要。本サイトのCTAを自前の予約・課金導線へ差し替える。
