1. Environment variables

```
services:
  my-app: 
    …
    environment:
      VIRTUAL_HOST: your-website.tld 
      VIRTUAL_PORT: 3000
      LETSENCRYPT_HOST: your-website.tld
      LETSENCRYPT_EMAIL: your-email@domain.tld
```

2. Ports

```
services:
  my-app: 
    …
    expose:
      - 3000
```

3. Network

```
networks:
  default:
    external:
      name: nginx-proxy
```

4. Boot up

```
docker network create nginx-proxy
```