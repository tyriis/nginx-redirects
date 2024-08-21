# nginx-redirect

## setup

```console
docker-compose up
```

## test cases

```console
❯ curl -I -H "Host: test.com" http://127.0.0.1:8080/some/path
```

```plaintext
HTTP/1.1 301 Moved Permanently
Server: nginx/1.27.1
Date: Wed, 21 Aug 2024 07:40:23 GMT
Content-Type: text/html
Content-Length: 169
Connection: keep-alive
Location: http://www.test.com/some/path
```

---

```console
curl -I http://127.0.0.1:8080/some/path
```

```plaintext
HTTP/1.1 301 Moved Permanently
Server: nginx/1.27.1
Date: Wed, 21 Aug 2024 07:39:24 GMT
Content-Type: text/html
Content-Length: 169
Connection: keep-alive
Location: http://www.127.0.0.1/some/path
```
