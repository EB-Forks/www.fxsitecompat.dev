---
date: "2015-08-30T22:50:24-04:00"
title: "このプロジェクトについて"
description: "Firefox のサイト互換性とは？ なぜそれがそれほど重要なのか？ その答えがここにあります。"
slug: "about"
---
## 概要

Firefox サイト互換性ワーキンググループは、情報源となるサイトのチェック、ドキュメントやツールの提供、ウェブ開発者とのエンゲージメント促進を通じて、Firefox の後方互換性とリグレッションに取り組んでいる独立したコミュニティイニシアチブです。クロスブラウザー互換性の改善については Mozilla の [Compatibility チーム](https://wiki.mozilla.org/Compatibility) が素晴らしい仕事をしていますが、Firefox 自体の互換性問題を集中的に扱っているスタッフがいないため、私たちがボランティアとして活動しています。私たちのミッションは以下の通りです。

* サイトの動作表示不良を未然に防ぐことによる Firefox ユーザー体験の改善
* 様々なチャンネルを通じたウェブ開発者との関係強化
* Firefox を何百万人ものユーザーのための一流ブランドと強固なウェブプラットフォームにすること

## 重要性

この HTML5 時代においてウェブの世界は急速に進化しています。Mozilla はリッチでモダンなウェブ技術の先駆者であり、Firefox は HTML、CSS、DOM、ECMAScript といった標準の仕様書に加えられた変更に遅れず付いて行こうとしています。また、標準化活動の一環として、Firefox は Netscape ブラウザーに由来する多くの古い非標準機能の廃止も進めています。それらの変更は、私たちがこのサイトで取り上げていますが、より良いウェブの世界のために必要なものです。

言うまでもなく、Mozilla が世界中のすべてのサイトに対して Firefox をテストすることは不可能あり、そのため Firefox のリリースにはあなたのウェブサイトやアプリの動作表示を損ねる可能性のある [リグレッション](https://www.fxsitecompat.dev/ja/statuses/regressed/) が含まれることもあります。理由の如何を問わず、サイトへの影響は Firefox からの顧客離反につながりますので、事前のリグレッション解決と変更点周知は Firefox エコシステムの成功にとって不可欠であると私たちは考えています。皆さんのような [ウェブ開発者の協力](https://www.fxsitecompat.dev/ja/contribute/) があれば、Firefox の大半のリグレッションはアルファもしくはベータサイクル中に発見、修正されるものと思います。

## 活動内容

私たちが焦点を当てている領域は 2 つあります。

* **後方互換性**: [Firefox Developer Edition](https://www.mozilla.org/firefox/developer/) より前に来る初期テスター向けビルドである [Firefox Nightly](https://nightly.mozilla.org/) を Mozilla が開発している間に、私たちは一連の [サイト互換性ドキュメント](https://www.fxsitecompat.dev/ja/docs/) を投稿し、後方互換性を失う変更点をウェブ開発者に告知します。その時点で、当該リリースの公開前にあなたのコードへ必要な変更を加えるための期間は少なくとも 8 週間あるはずです。
* **リグレッション**: 4 週間ごとに、Firefox の最終版が一般公開された後、私たちは時間をかけて [Firefox サポートフォーラム](https://support.mozilla.org/questions/firefox)、[Bugzilla](https://bugzilla.mozilla.org/)、Stack Overflow、Reddit といった各種チャンネルを監視し、リグレッションの発見に努めます。潜在的な問題が確認された場合、それを調査し、未報告の場合は Bugzilla へ報告し、Firefox 開発者に修正を促します。ウェブ開発者は、[Twitter](https://twitter.com/FxSiteCompat) で私たちをフォローすることで、問題点と、もしある場合はその回避策を知ることができます。

クロスブラウザー互換性や相互運用性について当サイトのブログで取り上げることもありますが、そうしたトピックは私たちの主な焦点からは外れます。その分野に関しては Mozilla の Compatibility チームが素晴らしい成果を上げており、彼らの活動もフォローすることをお勧めします。

## 参加者

このイニシアチブは長年 Mozilla に貢献している [Kohei Yoshino](https://mozillians.org/u/kohei.yoshino) が主導しています。彼は 2002 年以来のアクティブな Mozilla コミュニティメンバーであり、2004 年から 2012 年までフルタイム従業員として旧一般社団法人 Mozilla Japan に勤務した経験もあります。実のところ、一部の古いドキュメントは旧一般社団法人 Mozilla Japan の社内プロジェクトとして初めに日本語で書かれたものです。

参加はいつでも歓迎します。[協力](https://www.fxsitecompat.dev/ja/contribute/) ページであなたができることを見つけてください。質問やフィードバックがある場合は、私たちのソーシャルメディアのいずれか、もしくは [メール](mailto:kohei@fxsitecompat.dev) でいつでも気軽にご連絡ください。(日本語でも構いません)

## 謝辞

このプロジェクトは独立を保っていますが、部分的に Mozilla による支援を受けています。上に書いたように、初期のドキュメントは旧一般社団法人 Mozilla Japan 社内で作成されたものです。2018 年 1 月から 6 月まで、私たちの文書化作業は再び [Mozilla Corporation による資金提供を受けました](https://www.fxsitecompat.dev/ja/blog/2018/firefox-59-developer-edition-project-update-and-2-things-you-must-do-in-2018/)。

寄付やフィードバックの提供によってこのイニシアチブを支えてくれている個人の皆さんにも感謝します！
