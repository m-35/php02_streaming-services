# 課題① 課題番号-プロダクト名
- 課題番号：PHP②課題アプリ（DB本番環境版）
- プロダクト名：スタートアップ企業広告動画配信サービスアプリの"種"
- キャッチフレーズ:「10月にはちゃんと咲きます🌸」

## ②課題内容（どんな作品か）
-【事前にお伝えしたいこと】
- ※前回提出課題ではできたログインのページ遷移ができなくなりました。（「https://snails.sakura.ne.jp/php02-m/login.php」）。
- ※登録したデータ一覧の表示は「https://snails.sakura.ne.jp/php02-m/script.php」からのリンクで確認できます。入力した情報はすべて反映表示できています
-【動作の内容】
- 1.アカウント情報を入力（「index.php」）
- 2.入力確認画面（「complete.php」）
- 3.ログイン画面 会社名とパスワードを入力（「login.php」）※現在未解決
- 4.データ表示＆動画アップロード画面（「script.php」「upload_video.php」）
※ご注意：課題のアカウント情報一覧はここです。
クリックで「selectall.php」に飛び表示されます。

## ③DEMO
- https://drive.google.com/file/d/13n9ScLNFzjuWNxdSOTAQETL_R05Pmkdn/view?usp=sharing
（※local接続時・ページ遷移OKバージョン）

## ④ 前回からの修正点
- PHP課題①のコードに講義後の「php02」のコードファイルをトレースして以下３点を追加・修正し連携させた。
- ⑴INSERT文を使った「insert.php」ファイルで、入力機能を明確にした。
- ⑵SELECT文を使った「selectall.php」ファイルで、表示機能を明確にした。
- ⑶入力フォームの項目数を増やし、装飾をcssで少し整えた

## ⑤難しかった点・今後トライしたいこと（又は機能）

- 【難しかった点】
- ⑴ データベースのテーブルの削除
- 講義で作成したlocalhostのデータベースは念のため上書きしないで、新規でデータベース（フォルダ）を作成した。
- テーブル設定がうまくいかず（長さとかでエラー）、作り直すためファイル削除を試みたが方法がなかなか見つからず苦戦した。
- ⑵ データ一覧「selectall.php」へのページ遷移
- 初期画面「insert.php」からheader関数で遷移しようとしたが、同ファイル内で既に使っており、条件分岐で別々にページ遷移できるのか試行錯誤して沼に沈んだ。
- 諦めて、遷移の起点ページを、動画データ取得ファイル「script.php」に設定したが、今度は動画アップロード機能が効かなくなり再び沈む。
- 最終的に、hrefでリンクを飛ばせばアップロード機能は干渉されなくなった。
- header関数とhrefの使い分けを今後学びたい。
- ⑶ Bootstlapの活用とstyles.css
- 入力フォームの装飾を、「php02」にあった
- Bootstlapでやろうとしたが使いこなせず通常のstyle.cssに方向転換した。
- その後、１つの「styles.css」で複数のphpファイルをまとめて装飾しようとしたがクラス設定等がうまくいかず、時間的余裕がなくなったので、やむなく各phpファイルにcssを直貼りした。見苦しいコードになっています。すみません。 
- ⑷ XAMMPの再インストール
- デプロイ直前に課題提出をしようとpcを立ち上げたところXAMMPのMySQLが接続できなくなった。
- チューターさんにslackで助言をもらい翌朝何とか再インストールできた。
- アンインストール直前にhtdocsフォルダだけコピーしておいたが、再インストール後コード通りにデータベースを作り直すのには神経を使った。
- MyySQLが切断された原因を調べたが、前日追い込みで長時間（6~7時間）連続で使用した際、コントロールパネルでQuitできないのをそのままにして、何度かPCのシャットダウンで済ませていたことが原因かもしれない。
- 再インストール後はXAMMPのコントロールパネルのプロパティで管理者設定を行った。マリアDB様に丁寧に接しなければ大事故になると学んだ。
- ⑸ DBにあげた後ログインページが動作しない
- Filezillaにつないでチェックしたところ、ログインページで入力クリックすると「このページは動作していませんsnails.sakura.ne.jp では現在このリクエストを処理できません。HTTP ERROR 500」とエラーが出る。
- エラーコード内容の範囲が広すぎて、ググったり、copilot先生に詰問したり、コントロールパネルのエラーログを見たり、コードを直したりと、提出直前の6時間程色々試したが今回は解決の目途が立たちませんでした。
- 根本的にsessionの使い方が理解できていないと思う。

- 【次回までにトライしたいこと】
- ⑴ログインページが動作しない事の解決
- ⑵入力項目の工夫
- 項目「資本金」は単位表記の体裁を整えたい。
- 項目「業種」はプルダウン選択できるようにしたい。
- ⑶出力データ表示の工夫
- 今回は手が回らなかったが、業種別や資本金別で表示できるようにしたい
  
- 【今後トライしたいこと】
- ⑷動画回りの工夫
- アカウントと動画の紐づけ
- 蓄積された動画の連続再生（ストリーミング的にするにはどうすればよいか）
- 動画評価機能や投げ銭的機能の追加

## ⑥ 感想など
- 今後も講義後のファイルをトレースして、学ぶ毎にプロダクトの機能を高めていきたいです。
- 課題提出時、MySQLが切断されて万事休すとなったのは、本当にしんどかった。チューター様本当に感謝です。
## 以上
