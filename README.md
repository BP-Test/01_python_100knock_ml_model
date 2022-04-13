# Objective

This is a repository to implement codes introduced in the following book:'[「Python実践機械学習システム100本ノック」](https://www.shuwasystem.co.jp/book/9784798063416.html)'

## Objective Phases
1. First Stage
   1. Learn from examples to implement variety of minimal viable products in the streams of advanced analytics.
   2. Aut]
2. The next objective is to come up with quick-win strategies + implementation that can be done in current working environment. adapt the learning from the book to real business, especially in my current working environment to speed up and automate redundant processes that sucks up important resources of the company.

Such as follows:

1. Automation of redundant processes.
2. Applying simple but robust ML model on frequent refreshed datasets.
3. Building dashboard using python to rack core KPI
4. Build docker container to run jobs sustainably.
5. advanced analytics Although the aim is to trace over the courses, I will work on the following things.
6. Make codes more efficient.
7. Optimize the running time of codes.
8. Turn redundant codes into functions.
9. Use classes if necessary.


# Citation from Preface

分析結果や技術が理解されない状況に直面する。
残念ながら、それは殆どの現場で起きてしまう。
現場に理解されるためには、技術だけでは不十分で、運用を意識し、小さな成果を継続的に生み出すための最小限の仕組み化が必要です。
最小限の仕組みでも、小さな成果を上げ続けていくことで、少しずつ見方を増やし、文化の醸成に繋がっていきます。
# Intro of the book

あなたの分析結果や技術は、社内で十分に理解されていますか？ もし理解されていないのなら、小規模でも継続的にデータ分析や機械学習を回す「仕組み」が必要です。本書は、大好評の『Python実践データ分析100本ノック』の続編として、実際のビジネス現場を想定した100の例題を解くことで、現場の視点と応用力が身に付くよう設計した問題集です。データ活用プロジェクトを立ち上げ、社内にきっちり定着化させるための最初の一歩です！

# Remarks from the Author

この度は、「Python実践機械学習システム100本ノック」を手にとっていただきありがとうございます。

ダウンロードファイルには、
本章とDockerファイルの二つが含まれています。

【本章】
本章には、章ごとにフォルダが準備されています。
それぞれのフォルダには、
　①ソースコードであるJupyter Notebookファイル(.ipynb)と
　②サンプルデータファイル
が含まれています。

①のJupyter Notebookファイルは、各章ごとに2種類存在し、
１つは問題であるノックのみのファイル、
もう１つはノックに加えて解答であるサンプルコードも記載されているファイルとなります。
＊解答を含むファイルはファイル名に _answer が付いています。

②のサンプルデータは、1～4章まではそのまま利用できる形になっていますが、
5章以降は、使用データから適宜配置し利用してください。

【Google Colaboratoryの利用】
Google Colaboratoryを利用する場合は、
本章フォルダをGoogleDriveにアップロードして使用します。
その際に、マイドライブ直下に「MLSys_100Knocks」等の作業フォルダを作成することをお勧めします。
アップロードが完了したら、各章のJupyter Notebookファイルを右クリックし、
「アプリで開く」から「Google Colaboratory」を選択してください。
ファイルが開いたら、上部のコメントアウトされている部分を有効にし、実行してください。
なお、ライブラリのバージョンは、Google Colaboratoryに準拠する形を取っています。

※重要
Google Colaboratoryでの動作も確認はしていますが、
本書に掲載した結果等は、WindowsPCのJupyter Notebookで実行したものとなります。
他の動作環境(MacやGoogle Colaboratory)を用いると、結果が異なる可能性があるのでご留意ください。

現在では、6章のデータ読み込みの際に、
globでのファイル取得の順番が異なることから、
機械学習の結果が若干、本書と変わってくることが確認されています。
もし気になる方は、ノック51に「tbl_order_paths = sorted(tbl_order_paths)」を追加してください。


【Docker環境について】
Docker環境を利用する場合は、
お使いのパソコンに「Docker」と「Docker-Compose」が必要となります。

※重要
すでにDocker（及びDocker-Compose）を利用している方を対象としておりますので、
Dockerの環境構築についてのお問い合わせはご容赦願います。
（上記内容が不明な場合や、うまく構築出来ない場合は、
　上記Jupyter NotebookかGoogle Colaboratoryをご利用下さい）

１．ダウンロードしたサンプルソースを任意のフォルダに展開して下さい。
２．Terminal /　Windows Powershell等を起動し、カレントディレクトリを
　　docker-compose.yamlがあるフォルダに変更して下さい。
３．「docker-compose build」を行い、ビルドを実行してください。
　　注意：　初回ビルドはある程度時間が掛かります。
　　　　　　　エラーで失敗する可能性がありますが、--no-cache等を試して下さい。
４．ビルドが完了したら「docker-compose up -d」を行い、コンテナを起動してください。
　　注意：　他のプログラムやコンテナでポート3333を利用している場合は、
　　　　　　　.envファイルの「JUPYTER_NB_PORT=3333」を任意のポート番号に変更して起動しなおして下さい。
５．「./jupyter_notebook/codes」フォルダの中に、【本章】のソース・データ一式をコピーして配置して下さい。
　　　codes
      |- 1章
      |- ・・・
      |- 10章　　　　
６．ブラウザにて「localhost:3333」にアクセスして、Notebook画面が表示されれば準備は完了です。


本書のコードよりもエレガントなコードを常に模索していきましょう！

100本ノック、是非、楽しんでください！