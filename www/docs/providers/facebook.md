---
id: facebook
title: Facebook
---

## Documentation

https://developers.facebook.com/docs/facebook-login/manually-build-a-login-flow/

## Configuration

https://developers.facebook.com/apps/

The default requested scope is 'email', which is the absolute minimum permission required to use Facebook OAuth. To request different permissions, simply add a `scope` property to the configuration object with a single string of space-separated permissions. For example, `scope: 'instagram_basic user_friends'` This will overwrite the default scope, so if you still need email permissions, include `email` in the scope string.

## Example

```js
import Providers from `next-auth/providers`
...
providers: [
  Providers.Facebook({
    clientId: process.env.FACEBOOK_CLIENT_ID,
    clientSecret: process.env.FACEBOOK_CLIENT_SECRET
  })
}
...
```

:::tip
Production applications cannot use localhost URLs to sign in with Facebook. You need to use a dedicated development application in Facebook to use **localhost** callback URLs.
:::
