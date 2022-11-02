# Docker + Actix + Yew + Surreal DB Full Stack Template

## 👨‍💻 Project Structure

Contains 3 sub-projects

1. api: actix web server
2. client: Yew frontend
3. database: surreal
4. types: json serializable structures used to communicate the frontend and backend.

# Dockerized workflow

1. Install docker
2. Run one of the supported make commands

```
make test
make up
make down
make build
```

# OAuth2

This template supports OAuth2 via yew-auth, to configure client_id and other secrets, read the docker-compose

Copy `docker/.env-sample` to `docker/.env` and fill in the variables. Assuming that you want to use Google as your OAuth provider, you will need to generate OAuth 2.0 credentials using a Google Cloud developer account.

Once you have a Google Cloud developer account, you can generate the values for the `OAUTH_CLIENT_ID` and `OAUTH_SECRET` variables using the following steps: [Setting up OAuth 2.0](https://support.google.com/cloud/answer/6158849?hl=en). As part of registering your web app with Google Cloud to associate with the OAuth credentials, you will need to configure your app to request the following scopes: `email`, `profile`, and `openid`.
