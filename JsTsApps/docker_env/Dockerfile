FROM node:18-alpine AS dev
WORKDIR /app

# TypeScriptとcreate-next-appをインストール
RUN npm install -g typescript create-next-app

# Next.jsアプリケーションを作成
RUN npx create-next-app@latest my-app --typescript

# 作成したNext.jsアプリケーションのディレクトリに移動
WORKDIR /app/my-app

# 必要なパッケージのインストール
RUN npm install

# Dockerイメージのポートを公開（必要に応じて）
EXPOSE 3000

# コンテナ起動時にshellに入る
CMD /bin/sh