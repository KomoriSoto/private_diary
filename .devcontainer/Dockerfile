FROM python:3.11

ENV PYTHONUNBUFFERED 1

RUN mkdir /code

# WORKDIR： フォルダcodeへ移動（なければフォルダcodeを作成）し、それを作業ディレクトリとして指定
WORKDIR /code

# ローカルPCのrequirements.txtを、コンテナ内部のフォルダcodeへコピー。今回はコピー先を絶対パス表記で指定している
COPY requirements.txt /code/

# フォルダcode下において、pipコマンドを実行
RUN pip install -r requirements.txt

# Dockerfileと同じフォルダ（.devcontainer）にあるデータをcodeフォルダ内部へコピー
COPY . /code/