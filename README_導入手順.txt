GYM READY PWA v2.0 / iPhone 17 / Windows 11
================================================
内容: index.html / sw.js / manifest.webmanifest / icons/*

【重要】ファイルを開くだけ(file://)ではオフラインPWAにはなりません。
HTTPS公開（GitHub Pagesなど）が必要です。初回はネット接続で開いてください。

【Windows 11: GitHub Pagesで無料公開】
1. GitHubで新規リポジトリを作る（例: gym-ready-pwa）。
2. このフォルダの index.html、sw.js、manifest.webmanifest、icons フォルダを
   リポジトリのルートにアップロードする。README.mdは任意。
3. Settings > Pages > Build and deployment > Source: Deploy from a branch
   Branch: main / (root) を指定してSave。
4. Pagesに出てきた https://ユーザー名.github.io/gym-ready-pwa/ を
   iPhoneのSafariで開く。デプロイ完了まで少し待つ場合があります。
5. Safariの共有メニュー > ホーム画面に追加 > 追加。
6. ホーム画面のGYM READYから一度オンラインで起動し、
   その後機内モードで起動できることを確認。

【注意】
* GitHub Pagesは通常公開URLです。コードと初期持ち物サンプルは一般に見えます。
  個人のチェック内容はアップロードされず、端末内(localStorage)に保存されます。
* Safariで開いた版とホーム画面版は、保存領域が別になる場合があります。
  データ移行はバックアップ保存と復元機能を使ってください。
* ホーム画面版の削除、サイトデータ消去、iOSのストレージ管理などで
  データが消える可能性があります。定期的にJSONバックアップを保存してください。
* 初回のオンライン読み込み・service workerのインストール完了までは
  オフライン起動を保証できません。
* キャッシュの更新は、オンラインでアプリを開き直すことで配信されます。
  旧画面が残る場合はアプリを終了して再度開いてください。
* オフライン保存は通信同期ではなく端末内の自動保存です。
* URLを公開したくない場合は別途非公開配信方式が必要です。
* このアプリはiPhoneの純正Swiftアプリではなくホーム画面追加型PWAです。

【ローカルで動作確認（Windows 11）】
Pythonが入っている場合はこのフォルダで python -m http.server 8000 を実行し、
PCのブラウザから http://localhost:8000/ で動作確認できます。
ただしiPhoneでのオフライン/PWA検証はHTTPSの公開URLで行ってください。

【後日Capacitor化】
index.htmlの画面と状態管理は再利用可能です。ネイティブ版では
sw.js/manifest.webmanifestは不要になることがあり、保存処理の移行を検討します。
