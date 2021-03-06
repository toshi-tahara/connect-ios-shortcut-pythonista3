# ライブラリ
- numpy
- matplotlib
- eccodes
  > GPV気象情報のgrib2ファイル操作用

# メモ
- pip3でしかインストール出来ていないため，基本python3系を使用

# ターミナル
- cd
  - ディレクトリは1階層ずつ。
- ls
  - ディレクトリ内ファイルフォルダ一覧
- pwd
  - フォルダパス

# Git
- init
  - .gitフォルダ＝リポジトリを作成。プロジェクトのトップディレクトリに作成する。
- help
  - コマンド一覧表示
- config
  - 設定。ユーザー設定やリポジトリ設定，システム設定などがある。
  - editor設定は初回VSCODEでコマンドパレット→shell commandでcodeをインストール要
- add
  - ファイルをステージする。checkoutと同じ？
  - フォルダを引数にするとそのフォルダ以下をステージ （--folderなど）
  - git add . とすると全てをステージする。
  - git add -u では変更ファイルのみステージする。
- commit
  - 実行するとエディタでコメント入力をする。-vでdiff結果自動入力してくれるが，長い。
  - 保存→ステージ→コミット。次変更後保存→ステージ→コミットして変更をリポジトリに追加していく。
- status
  - HEADコミットとステージ，作業ツリーの差分を表示
  - git管理されていないファイルも対象で，その旨表示される。
- log
  - 履歴を表示。--onelineで一言表示。--allでブランチ全体の履歴。
- gitkでグラフィカル表示できるがmacはbrewで最新gitをインストールする必要あり
- diff
  - statusの差分を表示。引数でいろいろな比較ができる。
  - そのまま・・・作業ツリーとステージの差分
  - --stagedはHEADとステージの差
  - HEADは作業ツリーとHEADの差
  - コミットのハッシュ値やHEAD -1などで差分も出せる。
- checkout
  - コミットやステージの内容を作業ツリーに反映
  - **ブランチの切替にも使用**
- reset
  - 基本使わない。コミットをステージ・作業ツリーに反映する，HEADを旧版に戻すなど。
- branch
  - そのままだと現在のブランチを表示
  - 文字を追加するとその名称のブランチができる。
  - -dでブランチを削除。削除するブランチから移動する。ブランチ先端がなくなるだけで履歴はそのまま
- merge
  - 相手ブランチ名を入力してマージする。
  - --abortで中止
  - --no-ff 相手ブランチで早送りマージ。可能な場合はmergeでも自動実行するので覚えなくても良さそう。