
# Background

ここ数年で通信(e.g.Bandwidth)やカメラ側の性能向上により、多くのビデオ解析ソリューションが開発されている。専用カメラも併売しているソリューションもあり、バルセロナを始めとしたトップクラブおよびユース・アカデミアで活用され始めている。

サッカーの動画分析は欧州で進んでいることを想定し、海外のビデオ分析ソリューションを調査することで、現状監督や分析官はツールを用いてどこまでできるのか把握することを試みた。

いくつかのツールはデモライセンスがあったので、Youtubeにある川崎フロンターレユース動画の解析も行った。

# Summary

- 動画解析ツールの殆どは、監督や分析官による動画分析（切り抜きや装飾）を、GUIで補助するレベルに留まっている。たとえると、WindowsMovieMakerやフォトショのレベル感。何があったのか、手動のタグ付けが前提であった。基本機能は下記と理解できた。
  - シーン分類の省力化：GUIによる手動だが直感的な動画タグ付け分類
  - 動画共有の効率化：モノによってはリアルタイムなチーム間の動画共有
  - プレゼン作成の省力化：静止画に対する矢印やコメント、スポットライト等のマニュアル加工  
  
- 一部の先端的解析ツールでは上記に加え、プレイヤーやフィールドのトラッキングを手動と自動で組み合わせ、位置や速度等を数クリックで計測可能な機能がリリースされ始めていた。複数カメラの同期も有している。ツールによる国際試合の解析結果は、オープンデータとして公開している事例もある。

- より高度な分析とされる、重要シーンの自動選定や戦術評価等は、未だどの製品でも十分に実装されていない。現状、論文や個人ブログに留まっていた。



# Feature Matrix


![](2022-06-04-13-21-16.png)

?:詳細解説がない

*:カメラ画像だけでは不可、他機器が必要

# Product Detail

## Hudi
専用カメラにより、撮影およびアプリへのアップロードをリアルタイムかつシームレスに実行。
![](2022-06-04-05-51-44.png)

コーチング時の動画レビューに用いられる。シーンのプレイリスト化は人力。
![](2022-06-04-05-50-09.png)

2次元化されたデータとして、ゲームチェンジとなったアクションの場所について自動レポート作成。
![](2022-06-04-05-47-52.png)
https://www.hudl.com/products/hudl

また、動画編集機能にも優れており、複数動画の同期や、GUIでビジュアルな解説を付与することも可能。
![](2022-06-04-05-56-38.png)

## Metrica
![](2022-06-04-06-52-26.png)
https://metrica-sports.com/

![](2022-06-04-07-50-56.png)


GUIベースで、トラックする選手をクリックするとスポットライトをあてて追跡できる。
![](2022-06-04-07-51-41.png)
![](2022-06-04-07-52-00.png)
![](2022-06-04-07-52-12.png)
![](2022-06-04-07-52-30.png)
![](2022-06-04-07-53-11.png)

選手は常にIDベースでトラックされている。
![](2022-06-04-07-56-11.png)

プレイヤーに関しては、常に2次元図が作成されている。
![](2022-06-04-07-57-02.png)

矢印も距離と共に描画可能。
![](2022-06-04-07-58-15.png)

速度も表示可能。
![](2022-06-04-08-00-34.png)

選手の過去未来の行動トレース結果の重畳表示も可能。
![](2022-06-04-08-03-02.png)
![](2022-06-04-08-05-21.png)

YoutubeのデータからManual Field Tracking をつかってみた
![](2022-06-04-08-39-59.png)
https://help.metrica-sports.com/hc/en-us/articles/5619193081236

割と誤検知も多いが、概ねうまく動いてくれている。速度が正しいのかは正直判別がつかなかった。ただ他にも、リンク（選手間の陣形）可視化機能もあり使いたいが、メモリを非常に喰うので直ぐフリーズしてしまった。
![](2022-06-04-09-06-27.png)


## SBG
70%のEuropeのPremier League™ で使用実績あり、チーム分析やスカウトへの活用が想定されている。複数カメラの同期や動画へのタグ/コメント機能、2次元化の機能を有する。一方、2次元化についてはセンサーも活用可能という記述から、カメラ画像のみから行っているか曖昧。
![](2022-06-04-07-20-41.png)
![](2022-06-04-07-20-53.png)
![](2022-06-04-07-21-02.png)
![](2022-06-04-07-22-59.png)
![](2022-06-04-07-23-08.png)
![](2022-06-04-07-23-23.png)
![](2022-06-04-07-23-49.png)
https://sbgsportssoftware.com/product/matchtracker-for-team

## FootballAnalysis
機械学習ベースであることを前面に出したプロダクト。
![](2022-06-04-07-18-15.png)

## interplay sports
ハイエンドにみえたが、デモ版をいじると実際は滅茶苦茶に古いツールで、機械学習により自動化された機能はほぼなく残念。
![](2022-06-04-07-16-58.png)
![](2022-06-04-07-17-14.png)
https://interplay-sports.com/trial-versions/　　
https://interplay-sports.com/wp-content/uploads/2016/09/Interplay-sports_UserGuide_Soccer_PRO.pdf  



## Pixellot
バルセロナで使われている録画カメラ。
![](2022-06-04-07-02-06.png)
https://www.pixellot.tv/products/pixellot-air/

## iSportsAnalysis
Youtube動画をアップロードしデモ版をつかってみた。動画を見ながら事前に作ったボタンの押下時間でスムーズにタグ付けを行い、コメントを残し、共有するツール。2次利用のためにExcel出力が可能。ただ確かにこれを続けるのは結構つらい。
![](2022-06-04-06-48-22.png)
![](2022-06-04-06-50-05.png)
![](2022-06-04-06-56-04.png)

## Chyron CoarchPaint
スポーツやゲームの動画編集に特化したプロダクト。ビジュアルな矢印や円を描くために用いられる。
![](2022-06-04-05-58-43.png)


## Longomatch
動画編集とコメント共有が主機能で、機械学習的要素はなし。
![](2022-06-04-06-51-33.png)

## Once
動画編集とコメント共有が主機能で、機械学習的要素はなし。ビジュアルな描画が訴求点。
![](2022-06-04-06-22-31.png)
https://once.de/once-pro-free-trial/

動画を見ながらタグ付けを実施する。
![](2022-06-04-08-10-54.png)
各静止画に対してビジュアルを加えてプレゼンテーションを作る形態。
![](2022-06-04-08-19-09.png)


## CoachLogic
動画編集とコメント共有が主機能で、機械学習的要素はなし。
![](2022-06-04-06-29-47.png)
https://www.coach-logic.com/football-video-analysis

## Performasports
![](2022-06-04-06-41-58.png)
自動か手動かわからないが”FastpassAnalaysis”を購入すると48時間以内に多くのリストされたKPIに関するレポートを生成可能。
![](2022-06-04-07-05-37.png)
![](2022-06-04-07-04-44.png)
https://www.performasports.com/first-pass-video-analysis


## YouTubeCoder by FC Python
Youtubeを見ながら全選手の位置とイベントをクリックベースで構造化データに落とすツール。無料版。つらい。
https://fcpythonvideocoder.netlify.app/

# Ref highlight tools (論文系は別MDでまとめ)
- BIHUB and Pixellot develop new automated recording system for Barça Academy and Youth Football
  https://www.fcbarcelona.jp/ja/club/news/2051982/bihub-and-pixellot-develop-new-automated-recording-system-for-barca-academy-and-youth-football


- A New Way Of Classifying Team Formations In Football (2019)
   
    https://www.sportperformanceanalysis.com/article/tag/Football


- Football's video analysis revolution: From the top clubs to the masses
  ![](2022-06-04-06-21-54.png)
    https://www.skysports.com/football/news/11095/12133219/footballs-video-analysis-revolution-from-barcelona-to-the-masses


- THE FIGURE OF THE ANALYST AND THE IMPORTANCE OF VIDEO ANALYSIS IN FOOTBALL
  ![](2022-06-04-06-23-30.png)
  ![](2022-06-04-06-23-58.png)
    https://soccerinteraction.com/the-figure-of-the-analyst-and-the-importance-of-video-analysis-in-football


- How to Create an Effective Football(Soccer) Analysis Video
  
  https://www.udemy.com/course/how-to-create-an-effective-football-soccer-analysis-video/

- COACHES PERCEPTIONS OF THE USE OF VIDEO ANALYSIS
  https://www.researchgate.net/publication/262299780_COACHES_PERCEPTIONS_OF_THE_USE_OF_VIDEO_ANALYSIS




# DUST
  
- 比較的安価な動画解析ツールの多くは、監督や分析官による手作業を完全に自動化しておらず、下記が主な機能であった。
  - シーン分類の省力化：GUIによる手動だが直感的な動画タグ付け分類
  - 動画共有の効率化：モノによってはリアルタイムなチーム間の動画共有
  - プレゼン作成の省力化：静止画に対する矢印やコメント、スポットライト等のマニュアル加工　　

　　
- 高価な解析ツールの中には、機械学習等による差別化が図られていた。一方、シーンの自動抽出はいずれも手動であった。また実際の動画では特に選手のトラッキングにやや誤検知もありGUI上の手動補正が可能となっていた。
  - 2次元図への変換/プレイヤー追従は、手動と自動のハイブリッド
  - GUIベースでプレイヤー追従/移動速度/過去未来の動き等の可視化項目を選択
  - 専用ビューワーにて複数カメラの自動同期再生

![](2022-06-04-11-18-36.png)
![](2022-06-04-11-19-10.png)
![](2022-06-04-11-20-51.png)

