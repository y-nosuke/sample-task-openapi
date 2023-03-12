# sample task openapi

## openapigenerator のインストール

```bash
# go
docker run --rm -it -v c:/root/opt/sample-task-openapi:/local openapitools/openapi-generator-cli:latest generate \
     -i local/openapi.yaml \
     -g go-echo-server \
     -p packageVersion=0.0.1 \
     -o local/out/go-echo-server

# spring
docker run --rm -it -v c:/root/opt/sample-task-openapi:/local openapitools/openapi-generator-cli:latest generate \
     -i local/openapi.yaml \
     -g spring \
     -p packageVersion=0.0.1 \
     -o local/out/spring

# typescript-axios
docker run --rm -it -v c:/root/opt/sample-task-openapi:/local openapitools/openapi-generator-cli:latest generate \
     -i local/openapi.yaml \
     -g typescript-axios \
     -p packageVersion=0.0.1 \
     -o local/out/typescript-axios
```

## 静的ドキュメント作成

```bash
docker run --rm -it -v c:/root/opt/sample-task-openapi:/data ghcr.io/redocly/redoc/cli:latest build openapi.yaml
```

## 参考

- [OpenAPI Specification](https://swagger.io/specification/)
- [OAI/OpenAPI-Specification](https://github.com/OAI/OpenAPI-Specification)
- [OpenAPI Generator](https://openapi-generator.tech/)
- [OpenAPITools/openapi-generator](https://github.com/OpenAPITools/openapi-generator)
- [OpenAPITools/openapi-generator](https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator-gradle-plugin)
- [Swagger Data Types](https://swagger.io/docs/specification/data-models/data-types/)
- [Redocly/redoc](https://github.com/Redocly/redoc/pkgs/container/redoc%2Fcli)

- [俺的【OAS】との向き合い方 (爆速で OpenAPI と友達になろう)](https://tech-blog.optim.co.jp/entry/2020/04/13/100000)
- [OpenAPI によるスキーマファースト開発の実施サンプルと Cloud Run について](https://tech-blog.optim.co.jp/entry/2019/04/17/174000)
- [SpringBoot×OpenAPI 入門　〜Generation gap パターンで作る OpenAPI〜](https://qiita.com/haruto167/items/219bb0b0167804d0c922)
- [OpenAPI と TypeScript で作る！チーム開発に適した Web アプリケーションの作り方](https://blog.5thfloor.co.jp/2019/06/26/webapp-development-with-openapi-and-typescript/)
- [OpenAPI3 を使ってみよう！Go 言語でクライアントとスタブの自動生成まで！](https://techblog.zozo.com/entry/openapi3/go)
- [平静を保ち、コードを生成せよ 〜 OpenAPI Generator 誕生の背景と軌跡 〜 / gunmaweb34](https://speakerdeck.com/akihito_nakano/gunmaweb34)
