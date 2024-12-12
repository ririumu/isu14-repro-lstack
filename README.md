LocalStack for ISUCON (WIP)
===

## Preface

ISUCON は伝統的に AWS で動いているので LocalStack で検証環境を作れないか。

## Howto

LocalStack は AWS の検証環境であり、本リポジトリは以下で動かせるようになっている。

* `poetry install` で必要なモジュールをインストール
* `poetry run localstack start` でスタート (初回は時間がかかる)
* `poetry run localstack status services` で locakstack の起動を確認
* `poetry run awslocal` は awscli に相当
* 例えば `aws s3 mb` は `poetry run awslocal s3 mb s3://foobar` 
* 同様に `aws s3 cp` は `poetry run awslocal s3 cp pyproject.toml s3://foobar/` 

## Task

* ISUCON の CFn テンプレートが展開できるか検証
