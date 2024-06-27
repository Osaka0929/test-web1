

## 開始

自分のRepositoryにForkする。(右上Forkボタン、"Create fork")

```bash
git clone git@github.com:<あなたのユーザー名>/test-web1.git
pnpm install
pnpm dev
```

[http://localhost:3000](http://localhost:3000) を開く。

## 課題1

Next.jsとChakra UIを使用して、`src/pages/index.tsx`のみを編集して、以下のようなページを作ってください。



https://github.com/tips-toyama/test-web1/assets/17561618/2a23c718-a48c-4b9f-b375-9294a0e923fe



どちらもすでにインストールされています。

### 使用するAPI

`https://pokeapi.co/api/v2/pokemon/<ID>`(ID 25がピカチュウ)

取得したJSONの中の、`json.name`が名前(英語)、`json.sprites.front_default`が画像です。

# 課題2

Next.jsとChakra UIを使用して、`src/pages/login.tsx`のみを編集して、以下のようなページを作ってください。

どちらもすでにインストールされています。

### 使用するAPI

POST https://api.we.tips/v1/login

```json
{
    "id": "<ID>",
    "password": "<パスワード>"
}
```

でリクエストすると、

```json
{
    "accessToken": "<Access Token>",
    "expiresIn": 86400,
    "expiresAt": 1719574844,
    "refreshToken": "<Refresh Token>",
    "requiresUpdate": false,
    "userData": {
        "success": true,
        "username": "<ID>",
        "attributes": {
            "sub": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
            "email_verified": "true",
            "admin": true,
            "id": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
            "role": "teacher",
            "email": "test@example.com",
            "displayName": "<お名前>",
            "director": [
                "<チームの名前>",
                "<チームの名前>"
            ]
        }
    }
}
```

と帰ってきます。
