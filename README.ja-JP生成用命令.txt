このプロジェクトはMicrosoft社のaoai-realtime-audio-sdkのrtclient-0.5.1を使用したサンプルプログラム集です
このサンプルプログラム集のREADME.ja-JP.mdを以下のサンプルプログラムの説明、ファイルの説明、インストール手順、実行方法を参考に日本語で作成してください。


# サンプルプログラムの説明
low_level_sample.py:動作を確認するためのサンプルプログラムです。
client_sample.py:入力音声に対して応答するサンプルプログラムです。
client_sample_no_vad.py:instructions(システムプロンプトを与えて入力音声に対して応答するサンプルプログラムです。

# ファイルの説明
.env.example:Azure OpenAIのエンドポイント、APIキー、gpt-4o-realtime-previewのデプロイ名を設定するファイルのサンプルです。このファイルを.envにコピーして使用します。
createvenv.bat:Pythonの仮想環境をvenvフォルダに作成するコマンドプロンプト用バッチファイルです
activate.bat:createvenv.batで作成したvenv環境に入るコマンドプロンプト用バッチファイルです。Powershellではactivateと入力することで仮想環境に入れます。
deactivate.bat:Pythonの仮想環境venvから抜けるコマンドプロンプト用バッチファイルです。PowershellではPowershellを終了して抜けます。
do_low_level_sample.bat:do_low_level_sample.pyを実行するコマンドライン用バッチファイルです。
do_client_sample.bat:client_sample.pyを実行するコマンドライン用バッチファイルです。
do_client_sample_no_vad.bat:do_client_sample_no_vad.pyを実行するコマンドライン用バッチファイルです。
download-wheel.ps1:pypi.orgリポジトリに登録されていないrtclient-0.5.1-py3-none-any.whlをダウンロードするPowerShellツールです。ダウンロード後、pip install rtclient-0.5.1-py3-none-any.whlでPython仮想環境にインストールします。
download-wheel.sh:pypi.orgリポジトリに登録されていないrtclient-0.5.1-py3-none-any.whlをダウンロードするUnix Shellツールです。ダウンロード後、pip install rtclient-0.5.1-py3-none-any.whlでPython仮想環境にインストールします。
requirements.txt:low_level_sample.py,client_sample.py,client_sample_no_vad.pyの動作に必要なPythonパッケージを導入するための定義ファイルです。pip install -r requirements.txtでPython仮想環境にインストールします。
test_instructions_for_LMM.txt:client_sample_no_vad.pyで使用するサンプル命令です。興奮気味に話す
test_instructions_for_LMM_soccer.txt:client_sample_no_vad.pyで使用するサンプル命令です。サッカー中継のように話す
test_instructions_for_LMM_soccer_ja.txt:client_sample_no_vad.pyで使用するサンプル命令です。サッカー中継のように日本語で話す

#インストール手順
1.Python仮想環境を作成する
  createvenv.batコマンドでvenvというサブフォルダが作成されます。
2.Python仮想環境に入る
  Powershellならばactivate、コマンドプロンプトならばactivate.batコマンドでPython仮想環境に入ります
2.依存パッケージのrtclient-0.5.1をダウンロードする
  pypi.orgに登録が無いrtclient-0.5.1をdownload-wheel.ps1ツールでダウンロードします。
3.依存パッケージのrtclient-0.5.1をPython仮想環境にインストールする
  pip install rtclient-0.5.1-py3-none-any.whlでPython仮想環境にインストールします。
4.依存パッケージをPython仮想環境にインストールする
  pypi.orgにあるい依存パッケージをpip install -r requirements.txtでPython仮想環境にインストールします。
5..envファイルをコピーする
　.env.exampleファイルを.envファイルにコピーします。
6..envファイルにAzure OpenAIエンドポイント、APIキー、モデルのデプロイ名を入力します。

#実行方法
1.do_low_level_sample.pyの実行
  do_low_level_sample.batを起動します。起動するとoutputフォルダに結果ファイルが格納されます。
2.do_client_sample.pyの実行
  do_client_sample.batを起動します。起動するとoutputフォルダに結果ファイルが格納されます。
3.do_client_sample_no_vad.pyの実行
  do_client_sample_no_vad.batァイルが格納されます。
  test_instructions_for_LMM_soccer_ja.txtファイルを読み取るようにしてあります。

  