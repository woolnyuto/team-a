# team-a
はじめにPython3の実行環境を構築してください。
環境構築の方法はしたの方に書きました。

## 実行方法

``` bash
# install buildtool(環境によりsudoで実行)
※python3の環境がない場合は下記の環境構築を行ってください。また、すでに"pipenv"をインストール済みの方はインストールを行わないでください。
$ brew install pipenv

# install dependencies
$ pipenv run python3 [ファイル名]

```

For detailed explanation on how things work, check out [Pipenv docs](https://pipenv-ja.readthedocs.io/ja/translate-ja/).

## Python3 Setup
原因は不明ですが、macのCommandLineToolsからインストールしたpython3ではウドかない場合がありますので下記の方法（pyenv + pipenv）で環境構築してください。pyenvは
``` bash
# homebrewのインストール
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# 正しくインストールできているか確認
$ brew doctor

# pyenvのインストールとPath(bash_profile or zshrc)
$ brew install pyenv
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile  
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile  
$ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile  
$ exec $SHELL -l

# python3のインストール(pyenv経由)
$ pyenv install 3.7.4
# pythonを適用
$ pyenv global 3.7.4  
# 確認  
$ python -V 
Python 3.7.4

# pipenvのインストール
$ brew install pipenv
$ echo 'eval "$(pipenv --completion)”' >> ~/.bash_profile
$ exec $SHELL -l

```
