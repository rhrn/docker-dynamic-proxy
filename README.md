# Dynamic reverse proxy via URL

### Usage
* Run
```
docker run --rm -p 8880:80 rhrn/dynamic-proxy
```

* Examples
```
curl -i '127.0.0.1:8880/https://google.com/'
curl -i -X POST -d '{"x":72}' 'http://127.0.0.1:8880/https://dynproxy.requestcatcher.com/custom/url'
```

### Test services
- https://webhook.site
- https://requestcatcher.com

### Why?
```
Some services can't resolve DNS names.
So, the proxy can route an trafic on various services based on domain names.
```
