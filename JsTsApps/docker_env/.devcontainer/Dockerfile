# dev stage
FROM node:18-alpine AS dev
WORKDIR /webapp

# build stage
FROM node:18-alpine AS build
WORKDIR /webapp
COPY --from=dev /webapp /webapp
RUN ls
#RUN ["npm", "run", "build"]

# # runner stage
# FROM node:18-alpine AS runner
# WORKDIR /webapp

# # 実行ステージに必要なファイルのみをコピー
# COPY --from=build /webapp/package.json /webapp/package-lock.json ./
# COPY --from=build /webapp/.next ./.next
# COPY --from=build /webapp/public ./public
# COPY --from=build /webapp/next.config.js ./next.config.js

# # 本番環境用の依存関係のみをインストール
# RUN npm install --only=runner

# # ポートを公開
# EXPOSE 3000

# # Next.js アプリの起動
# CMD ["npm", "start"]
