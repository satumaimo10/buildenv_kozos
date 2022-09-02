# buildenv_kozos
このリポジトリは、書籍[12ステップで作る 組込みOS自作入門](http://kozos.jp/books/makeos/)の開発環境構築を補助する目的で提供される、非公式のリポジトリです。

このリポジトリは、H8/3069F向けのビルドツール(binutils-2.19.1, gcc-3.4.6)をDockerコンテナとして提供します。

## 使い方
### コンテナのビルド・実行
```bash
docker-compose up -d
```

### コンテナ内のビルドツール使用
コンテナの内部に入ることで、コンテナの提供するビルドツールを使用できます。
```bash
docker exec -it (container_name) bash
```

### コンテナの終了
```bash
docker-compose down
```

## workspaceについて
docker-composeを使用した場合、コンテナとディレクトリworkspaceは自動的にマウントされます。

永続化したいデータ、ホストOSで使用したいデータはworkspaceに配置するようにしてください。
