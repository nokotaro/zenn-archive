---
title: ZennとQiitaの記事をGitHubリポジトリで同時に管理する
private: false
tags:
  - github
  - zenn
  - zenncli
  - qiita
  - qiitacli
updated_at: '2025-01-14T00:51:53.497Z'
id: null
organization_url_name: null
slide: false
---

## はじめに

エンジニア向けの日本語記事共有プラットフォームといえば Qiita や Zenn などが挙げられます。

これまで私は読む側でしか使ってこなかったのですが、最近 [個人ブログ](https://nokotaro.hatenablog.com) で１日１記事を書く習慣をつけるように頑張っています。続けていく中で「技術記事についてはエンジニアが読んでくれるプラットフォームで公開したい」と思うようになりました。

そこで Qiita を使うか Zenn を使うか悩んだ末、結論として「QiitaもZennも使いたい！」という、なんともよくばりな考えにたどり着きました。

## 両方使おうと思ったきっかけ

過去に「[Zenn / Qiitaに投稿する同じ記事を一元管理するGitHubリポジトリを作りました](https://zenn.dev/ot07/articles/zenn-qiita-article-centralized)」という記事を読んだことがあり、その際は「ふーん」くらいにしか思ってなかったのですが、今回どのプラットフォームを使うか迷っていた際にこの記事の存在を思い出し、せっかくなので試してみることにしました。

<https://zenn.dev/ot07/articles/zenn-qiita-article-centralized>

ちなみに今回は先述の記事で紹介されている方法をもとに [C-naokiさん](https://c-naoki.vercel.app) が改良した [zenn-archive](https://github.com/C-Naoki/zenn-archive) を使って Qiita と Zenn の記事の一元管理化を試してみます。

こちらのツールついては、C-naokiさんご本人が書かれた [Zenn vs Qiitaを終わらせに来た](https://zenn.dev/naoki0103/articles/zenn-qiita-sync-workflow) の記事に、事前準備や使い方などの手順が詳細に書かれているのでそちらを参考にしてみてください。

<https://zenn.dev/naoki0103/articles/zenn-qiita-sync-workflow>

## 同時投稿ツールはほかにもある

この記事では省略しますが、

- [zenn-archive](https://github.com/C-Naoki/zenn-archive) - [(C-naokiさん)](https://c-naoki.vercel.app)
- [blog-project](https://github.com/SolitudeRA/blog-project) - [(SolitudeRAさん)](https://www.solitudera.com)
- [O.A.S.I.S](https://github.com/Sunwood-ai-labs/OASIS) - [(Makiさん)](https://hamaruki.com)

など類似ツールはいくつかありましたが、今回は [zenn-archive](https://github.com/C-Naoki/zenn-archive) を採用しました。

どのツールも大まかな流れとしては

- Zenn CLI で記事を管理するための markdownファイル を用意する
- 上記の markdownファイル を GitHub Actions で Qiita CLI用 に変換する

ということをやっています。

採用に至った基準や、実際に使用してみた感想、そのほか詰まったところなどは、個人ブログの[「ZennとQiitaの記事をGitHubリポジトリで一括管理する」](https://nokotaro.hatenablog.com/entry/2025/01/07/160253)の記事に書いてありますので、よければこちらも読んでくださると嬉しいです。

<https://nokotaro.hatenablog.com/entry/2025/01/07/160253>

## 実際に投稿された記事

実際にツールを使用し、Zenn と Qiita の両方に記事が投稿されるか確認しましたが、どちらも問題なく投稿されたことが確認できたので、今後はこちらのツールを活用し技術記事を公開していきたいなと思います。下にテスト用の記事を貼っておきます。

<https://zenn.dev/nokotaro/articles/zenn-qiita-sync-test>

<https://qiita.com/takenoko_0714/items/4c90a6f04c1bceb7c7ff>

もちろん、今あなたが読んでいるこの記事も、[zenn-archive](https://github.com/C-Naoki/zenn-archive) を使って同時投稿しています。画像添付や注釈表記などにも対応しているのですが、それはまた別の記事で試してみたいと思います。

というわけで、Zenn と Qiita の記事を、GitHubリポジトリで一元管理する方法の紹介でした。
