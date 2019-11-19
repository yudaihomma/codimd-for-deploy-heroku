# codimd-for-deploy-heroku

## 概要
- よくcodimdのherokuワンクリックデプロイメントが使えなくなるので自分で立てる用

## deploy
`$ docker build ./ -t イメージ名`

`$ heroku login`

`$ heroku container:login`

`$ heroku container:push web`

`$ heroku container:release web`

## herokuの環境変数
herokuコンソールでSettings -> Config Vars

```
CMD_ALLOW_ORIGIN GrowiのURI
CMD_CSP_ENABLE false
DATABASE_URL heroku-postgresの接続名
GROWI_URI GrowiのURI
HMD_ALLOW_ORIGIN GrowiのURI
```
