# ロボットシステム学第1回

上田 隆一

2018年9月21日@千葉工業大学



## 今日の内容

* 動機付け（なんでこの講義があるのか）



## ロボットシステム

* システム
    * 目的を遂行するための体系や組織
* ロボットシステム
    * 目的を遂行するために動く
    * 動くための様々な要素
        * センサ
        * アクチュエータ
        * 電気回路
        * 計算機（コンピュータ）
        * 外装
        * ・・・
    * 例: ルンバ、新幹線


## ロボットシステム開発の変化

* 一人で黙々と作る時代の終焉
    * 個人に関する終焉: 大学生から社会人へ
    * 時代としての終焉: インターネット上への知識の集積
* 開発のスピードの急激な変化
    * CAD、3Dプリンタ、ROS、各種サービスの無い時代と有る時代のスピードの違い

※ 注意: 一人で一通り作れることは相変わらず貴重。ただ、それだけだと広がりがない。


## 外のリソースを使う

* 分かりやすい例: オープンソース
    * SLAMや位置推定関係（ROSのgmappingやAMCL、他、次ページ）
    * マニピュレータ（Move It!）
        * 公式サイト
* Gitのホスティングサービス、CIサービス
* 個人的な見解では、人の作ったソフトを使いこなせた後に理屈をしっかり学ぶべき


## ROSでSLAM、ナビゲーション

* 例1: 小型ロボットのナビゲーション
    * 自己位置推定、SLAM、ナビゲーションに関してはプログラムを書いていない

<iframe width="560" height="315" src="https://www.youtube.com/embed/7xXnXHc0roA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

* 例2: RoboCup@Home
    * チーム結成から8ヶ月でハード、ソフトを組み上げ世界大会で善戦

<iframe width="560" height="315" src="https://www.youtube.com/embed/XozlE7fuTso" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>



## 変化の中心にあるもの

* プラットフォームの存在
    * 知識やソフト等を流通させるには、それらが適用できるモノが必要
    * ロボットは計算機だけの場合より多様だが存在
* プラットフォームの例
    * ハード: PC、Raspberry Pi、Arduinoとその互換品、各種規格品
    * ソフト: UNIX、Linux
    * サービス: GitHub
    * ロボット: TurtleBot、iCart-mini、HSR、・・・


## Raspberry Pi

* シングルボードコンピュータ
* 本講義で扱う
    * 特に講師が信者ということではない
    * 性能はともかく、プラットフォームとして非常に優秀
        * 使ったことがあっても、性能のことにしか目に行かない人は非常にまずい


## Raspberry Piについて詳しく

* イギリスで開発された教育用のシングルボードコンピュータ
* 開発の動機・歴史
    * 2006-2008年: 構想・試作
        * ケンブリッジ大の学生のコンピュータの腕が落ちてきた
            * 経験者と言ってもWord, Excel, HTMLくらい
            * （未ロボだと逆の人も多い）
        * 安価でハードの制御ができるようなシングルボードPCが作れないか？
    * 2009年: Raspberry Pi Foundation設立
        * Raspberry Piを販売（2016年に1000万台販売）


## 講義の目的

* 一つのシングルボードコンピュータで低レイヤーから高レイヤーまで一通り経験する
    * 低レイヤー: デバイスドライバ
    * 高レイヤー: インターネットとのやりとり
        * さらには著作権やライセンスまで
    * ラズパイで全部体験できる


## 講義の内容

全15回。シラバスから一部変更あり

* 第1週: イントロダクション（本講義）
* 第2週: ラズパイの操作
    * 通信等
* 第3週: マイコンの仕組み（3,4週は入れ替えで）
    * 低レイヤーを学習
* 第4週: オペレーティングシステム
    * プロセス、ファイルシステム
 
* 第5週: 電子回路とプログラミングI
    * GPIOをソフトウェアで操作
* 第6週: 電子回路とプログラミングII
    * 実習
* 第7週: ペリフェラル
    * 様々なデバイスの操作
* 第8週: ネットワーク
* 第9週: システム管理とデータ処理
* 第10週: オープンソースとライセンス
* 第11週: GitとGitHub
* 第12週: デバイスドライバ
     * Travis CIになるかも
* 第13週: ROSの役割と構造
* 第14週: ROSの利用
* 第15週: まとめ


## 講義で使う道具

* ノートPC
* Raspberry Pi
* Raspberry Piのアクセサリ（次のページ）
* 仮想マシン上 or ネイティブなUbuntu
    * Raspberry Piと繋がらないときの保険
* Ubuntu Server18.04 LTS
    * Desktop版でも良いけど重い

## ラズパイのアクセサリ

* USBケーブル（Type A-Micro B、あるいはType C-Micro B）
    * ノートPCからRaspberry Piに電源供給
* microSDカード
    * 16GBのものがおすすめ
    * 複数あるとよい
* LANケーブル
    * ノートPCとRaspberry Piを接続


## ウェブサイト等

* [講義のサイト](https://lab.ueda.tech/?page_id=3451)
* 連絡: 人に見られてもいい内容はTwitterで[@ryuichiueda](https://twitter.com/ryuichiueda)
* レポート提出: メールでレポート提出の予定
    * 追って連絡

## テスト・レポート等

* 課題は2回
    * 配点: 各20点（＋α）
* テストは1回
    * 配点: 60点
* 出席
    * 遅刻、早退は0.5回とカウント

* この講義資料にプルリクくれて私がマージしたら加点します。


## 参考図書

* 初心者の人はこれを購入のこと
    * [福田: これ１冊でできる！ラズベリー・パイ　超入門 改訂第4版、ソーテック社, 2017.](https://www.amazon.co.jp/dp/480071172X)
* Linuxの操作
    * 初心者向け
        * [Piro（結城洋志）: シス管系女子, 日経BP, 2015.](https://www.amazon.co.jp/dp/4822224961)
    * 中級者〜
        * [上田: シェルプログラミング実用テクニック, 技術評論社, 2015.](https://www.amazon.co.jp/dp/4774173444)
* デバドラ関係
    * [Corbet 他(著), 山崎 他(翻訳): Linuxデバイスドライバ 第3版, オライリージャパン, 2005.](https://www.amazon.co.jp/dp/4873112532)
    * デバイスドライバのリファレンス
    * ちょっと古い
    * [英語ならネット上に](http://www.makelinux.net/ldd3/)
* OS
    * [Tanenbaum: オペレーティングシステム 第3版, ピアソンエデュケーション, 2007.](https://www.amazon.co.jp/dp/4894717697)
        * 中古が出回っている
    * [Bovet: 詳解 Linuxカーネル 第3版, オライリー・ジャパン, 2007.](https://www.amazon.co.jp/dp/487311313X)
    * https://www.amazon.co.jp/%E8%A9%A6%E3%81%97%E3%81%A6%E7%90%86%E8%A7%A3-Linux%E3%81%AE%E3%81%97%E3%81%8F%E3%81%BF-%E5%AE%9F%E9%A8%93%E3%81%A8%E5%9B%B3%E8%A7%A3%E3%81%A7%E5%AD%A6%E3%81%B6OS%E3%81%A8%E3%83%8F%E3%83%BC%E3%83%89%E3%82%A6%E3%82%A7%E3%82%A2%E3%81%AE%E5%9F%BA%E7%A4%8E%E7%9F%A5%E8%AD%98-%E6%AD%A6%E5%86%85-%E8%A6%9A/dp/477419607X/ref=sr_1_6?s=books&ie=UTF8&qid=1537491750&sr=1-6&keywords=%E6%8A%80%E8%A1%93%E8%A9%95%E8%AB%96%E7%A4%BE%E3%80%80%E3%82%AA%E3%83%9A%E3%83%AC%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0

## 宿題: Raspberry Piのセットアップ

* Raspberry Piを入手してRaspbianをインストールのこと
    * 初心者向けの指示: [NOOBS](https://www.raspberrypi.org/downloads/noobs/)を使ってRaspbianをインストールのこと
        * 手順: [拙ブログ](https://b.ueda.tech/?post=20180905_raspi)
        * 他の情報
            * ネット上に山のように情報
            * 「これ1冊で・・・」に詳しい解説
    * 諸注意
        * デスクトップ環境は使いません
        * ギブアップしてもケアしますから講義には来てください。
        * 慣れている人はUbuntuでもよい

## Raspberry Piの入出力

![](https://lab.ueda.tech/wp-content/uploads/2016/08/raspberrypi.png)

* 上図: Raspberry Pi 2 Model B

* 電源入力: MicroUSB
* ディスプレイへ出力: HDMI
* ストレージ: microSDカード
* 有線LANポート
* USBポート
* **40ピンのブロック**
    * 「GPIOピン」と呼ばれる
* 他: 専用カメラの取り付け端子等


## GPIOピンの構成

* Raspberry Pi 2からRaspberry Pi 3 B+まで変わってない
* 配置（Model Bのもの）: http://pinout.xyz
    * 電源: 3.3V、5V
    * GND
    * GPIOピン: 27
        * うち何本かがI2C、SPI、UARTも使える
    * I2C ID EEPROM用ピン
* A/D変換機能は付いていない


## CPU・メモリ・ストレージ

* Raspberry Pi 3 B+
    * CPU: 1.4GHz Cortex-A53 ARMv8 64bit（4コア）
    * DRAM: 1GB DDR2 450MHz
    * ストレージ: microSD
         * 細かい規格の制限や相性等に注意
         * 16GBまではトラブルが少ない


## Raspberry Piのソフトウェア

* Linuxが標準
    * Raspbian
    * Ubuntu
* ロボットのコントローラとしてのLinux
    * 欠点: マイコンのように単純なリアルタイム制御ができない
    * 長所: 開発時、運用時にインターネットとシームレスに接続
    * これから講義でいろいろやります

## 次回

* 教室でRaspberry Piを使います
    * ノートPCにLANケーブルで接続してSSHから操作
