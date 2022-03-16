# Alloy Proxy
A web proxy for use in combating web filters.
## Deploy on Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/herokuhabataku/alloy/tree/master)
## Deploy on vercel(only SSL)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fherokuhabataku%2Falloy)
## Running locally

```sh
git clone https://github.com/titaniumnetwork-dev/alloyproxy.git
cd alloyproxy
node server.js
```

## Options in config.json
```json
{
    "port": "8080",
    "ssl": false,
    "prefix": "/web/",
    "localAddresses": [],
    "blockedHostnames": []
}
```

`"port": "8080"` = Sets HTTP server port of web proxy.

`"ssl": "false"` = Sets HTTP server SSL.

`"prefix": "/web/"` = Sets the overall prefix of the web proxy.

`"localAddresses": [ "0.0.0.0" ]` = Allows you to choose which IP to make the request from. If there are multiple IP's then the IP chosen will be randomized.

`"blockedHostnames": [ "example.org", "example.com" ]` = If the hostname of the proxy URL matches any of the URL hostnames listed in the array, the request to the server will be cancelled.
