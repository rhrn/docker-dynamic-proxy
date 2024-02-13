# Dynamic reverse proxy via URL

### Usage
#### Run
```
docker run --rm -p 8880:80 rhrn/dynamic-proxy
```
#### Local build
```
docker build -t  rhrn/dynamic-proxy:local .
```

### Examples
```
curl -i '127.0.0.1:8880/https://google.com/'
curl -i -X POST -d '{"x":72}' 'http://127.0.0.1:8880/https://dynproxy.requestcatcher.com/custom/url'
```

### Docker compose examples
- [mtu-proxy.yaml](examples/mtu-proxy.yaml)
- [secure-webhooks-by-path.yaml](examples/secure-webhooks-by-path.yaml)

### Test services
- https://webhook.site
- https://requestcatcher.com

### Why?
```
- Some services can't resolve DNS names.
- MTU bridge between diff networks
```

### Source
- https://github.com/rhrn/docker-dynamic-proxy
