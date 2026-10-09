# hakobus-types

バスの時刻表を返す、読み取り専用の小さな API の OpenAPI の定義です。[Funmary](https://github.com/funmary-app/funmary) は、この定義を実装したサーバーの基底 URL を渡すと、「バス」のタブを出せます。

このリポジトリにあるのは定義だけです。サーバーも、データも、取得の処理も入っていません。

## 定義

- [openapi.yaml](openapi.yaml)
- `GET /health`: サーバーが動いているか
- `GET /v1/timetable`: すべての停留所、系統、運行日、便。形は GTFS-JP に合わせてある

## 実装するとき

この定義のサーバーは、だれでも作れます。載せるデータを配る権利があるかは、実装する人が確かめてください。

定義の検査は `npx @redocly/cli lint openapi.yaml` でできます。応答の形は、定義のスキーマと見比べてください。

## ライセンス

次の 2 つのライセンスのどちらかを選んで使えます(SPDX の式では `BSD-3-Clause OR Apache-2.0`)。Funmary と同じです。

- BSD 3-Clause License ([LICENSE-BSD-3-CLAUSE](LICENSE-BSD-3-CLAUSE))
- Apache License, Version 2.0 ([LICENSE-APACHE-2.0](LICENSE-APACHE-2.0))
