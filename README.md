## GitHub API Client

### Auth

You can create an Auth token on the [personal API tokens page](https://github.com/blog/1509-personal-api-tokens) or using [any other form of Auth provided by GitHub](https://developer.github.com/v3/#authentication).

Once you have a token, you can test out the API endpoint using cURL: 
`curl -H "Authorization: token <OAUTH-TOKEN>" https://api.github.com`

Going forward, using the Auth token in the HTTP header to authenticate future requests.

If you integrate this into an app without using cURL, you'll also need a [`User-Agent` header with your username](https://developer.github.com/v3/#user-agent-required) on GitHub, e.g.

`User-Agent: <USERNAME>`

### Endpoints

We're going to work around the endpoint that grabs your repositories.

`GET /repos/:owner/:repo`

[Here are the docs for the endpoint](https://developer.github.com/v3/repos/#get)
