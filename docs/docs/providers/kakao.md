---
id: kakao
title: Kakao
---

## Documentation

https://developers.kakao.com/product/kakaoLogin

## Configuration

https://developers.kakao.com/docs/latest/en/kakaologin/common

The "Authorized redirect URIs" used when creating the credentials must include your full domain and end in the callback path. For example;


![스크린샷 2023-11-28 오후 9 27 41](https://github.com/nextauthjs/next-auth/assets/66895208/7d4c2df6-45a6-4937-bb10-4b47c987bff4)

- **For production**: `https://{YOUR_DOMAIN}/api/auth/callback/kakao`
- **For development**: `http://localhost:3000/api/auth/callback/kakao`

## Options

The **Kakao Provider** comes with a set of default options:

- [Kakao Provider options](https://github.com/nextauthjs/next-auth/blob/v4/packages/next-auth/src/providers/kakao.ts)

You can override any of the options to suit your own use case.

## Example

```js
import KakaoProvider from "next-auth/providers/kakao";
...
providers: [
  KakaoProvider({
    clientId: process.env.KAKAO_CLIENT_ID,
    clientSecret: process.env.KAKAO_CLIENT_SECRET
  })
]
...
```

## Instructions

### Configuration

Create a provider and a Kakao application at `https://developers.kakao.com/console/app`. In the settings of the app under Kakao Login, activate web app, change consent items and configure callback URL.
