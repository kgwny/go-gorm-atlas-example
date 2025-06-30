# go-gorm-atlas-example

## セットアップ

### atlas インストール
```
curl -sSf https://atlasgo.sh | sh
```

### atlas バージョン確認
```
atlas version
```

### go mod 初期化
```
go mod init my-app
```

### gorm のインストール
```
go get -u gorm.io/gorm
```

### mysql ドライバーのインストール
```
go get -u gorm.io/driver/mysql
```

### atlas のインストール
```
go get -u ariga.io/atlas/sql/migrate
```

### golang-migrate のインストール
```
go get -u github.com/golang-migrate/migrate/v4
```

### atlas-provider-gorm のインストール
```
go get -u ariga.io/atlas-provider-gorm
```

## atlas と gorm によるマイグレーション
構造体を基にしてマイグレーションファイルを生成する
migrations ディレクトリが作成される
```
atlas migrate diff --config file://atlas.hcl --env gorm
```
