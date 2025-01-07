# Microsoft aoai-realtime-audio-sdk rtclient-0.5.1 サンプルプログラム集

このリポジトリは、Microsoft社のaoai-realtime-audio-sdkのrtclient-0.5.1を使用したサンプルプログラム集です。音声認識とAIによる応答を体験できる複数のサンプルプログラムと、それらを動作させるためのスクリプト、設定ファイルなどを含んでいます。


## サンプルプログラムの説明

このサンプルプログラム集には、以下の3つのPythonサンプルプログラムが含まれています。

- **`low_level_sample.py`**:  SDKの基本的な機能を確認するためのサンプルプログラムです。音声データの読み込み、送信、受信の基本的な流れを検証できます。
- **`client_sample.py`**:  入力音声に対して、Azure OpenAIのモデルを用いてテキスト応答を生成し、音声として出力するサンプルプログラムです。音声認識とテキスト生成、音声合成の連携を確認できます。
- **`client_sample_no_vad.py`**:  システムプロンプトを与えて入力音声に対して応答するサンプルプログラムです。音声活性検出(VAD)を使用しないため、継続的な音声入力に対応します。


## ファイルの説明

このリポジトリには、サンプルプログラムの動作に必要なファイルが含まれています。

- **`.env.example`**: Azure OpenAIのエンドポイント、APIキー、使用するモデルのデプロイ名を設定するためのサンプルファイルです。このファイルを`.env`としてコピーし、必要事項を入力して使用します。
- **`createvenv.bat`**: Pythonの仮想環境を`venv`フォルダに作成するためのバッチファイルです。(Windowsコマンドプロンプト用)
- **`activate.bat`**: `createvenv.bat`で作成した`venv`環境に入るためのバッチファイルです。(Windowsコマンドプロンプト用)  PowerShellでは`activate`コマンドで仮想環境に入ります。
- **`deactivate.bat`**: Pythonの仮想環境`venv`から抜けるためのバッチファイルです。(Windowsコマンドプロンプト用) PowerShellではPowerShellを終了することで仮想環境から抜けます。
- **`do_low_level_sample.bat`**: `low_level_sample.py`を実行するためのバッチファイルです。
- **`do_client_sample.bat`**: `client_sample.py`を実行するためのバッチファイルです。
- **`do_client_sample_no_vad.bat`**: `client_sample_no_vad.py`を実行するためのバッチファイルです。
- **`download-wheel.ps1`**:  pypi.orgリポジトリに登録されていない`rtclient-0.5.1-py3-none-any.whl`をダウンロードするPowerShellスクリプトです。
- **`download-wheel.sh`**:  pypi.orgリポジトリに登録されていない`rtclient-0.5.1-py3-none-any.whl`をダウンロードするUnixシェルスクリプトです。
- **`requirements.txt`**: サンプルプログラムの動作に必要なPythonパッケージをリストアップしたファイルです。`pip install -r requirements.txt`でインストールできます。
- **`test_instructions_for_LMM.txt`**: `client_sample_no_vad.py`で使用されるサンプル命令です。(興奮気味に話す)
- **`test_instructions_for_LMM_soccer.txt`**: `client_sample_no_vad.py`で使用されるサンプル命令です。(サッカー中継のように話す)
- **`test_instructions_for_LMM_soccer_ja.txt`**: `client_sample_no_vad.py`で使用されるサンプル命令です。(サッカー中継のように日本語で話す)
- **`output/`**: サンプルプログラムの実行結果が出力されるフォルダです。


## インストール手順

1. **Python仮想環境の作成**: `createvenv.bat`を実行して、`venv`フォルダにPython仮想環境を作成します。
2. **Python仮想環境へのアクティブ化**: PowerShellで`activate`コマンドを実行するか、コマンドプロンプトで`activate.bat`を実行して、仮想環境をアクティブにします。
3. **rtclient-0.5.1のダウンロード**: `download-wheel.ps1`を実行して、`rtclient-0.5.1-py3-none-any.whl`をダウンロードします。
4. **rtclient-0.5.1のインストール**:  `pip install rtclient-0.5.1-py3-none-any.whl`を実行して、ダウンロードした`rtclient`を仮想環境にインストールします。
5. **依存パッケージのインストール**: `pip install -r requirements.txt`を実行して、必要なPythonパッケージを仮想環境にインストールします。
6. **.envファイルの設定**: `.env.example`を`.env`にコピーし、Azure OpenAIのエンドポイント、APIキー、モデルのデプロイ名を入力します。


## 実行方法

1. **`low_level_sample.py`の実行**: `do_low_level_sample.bat`を実行します。実行結果は`output`フォルダに出力されます。
2. **`client_sample.py`の実行**: `do_client_sample.bat`を実行します。実行結果は`output`フォルダに出力されます。
3. **`client_sample_no_vad.py`の実行**: `do_client_sample_no_vad.bat`を実行します。このサンプルは`test_instructions_for_LMM_soccer_ja.txt`ファイルを読み込んで使用します。実行結果は`output`フォルダに出力されます。