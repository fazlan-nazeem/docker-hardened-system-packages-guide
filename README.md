# docker-hardened-system-packages-guide

## Alpine

```
docker run -it <org_name>/dhi-alpine-base:3.22-alpine3.22-dev
```
within the container shell, execute the following commands

```
# adds the signing public key
cd /etc/apk/keys && wget -O https://dhi.io/keyring/dhi-apk@docker-0F81AD7700D99184.rsa.pub

# point the default config to point to docker hardened system packages repo 
echo https://dhi.io/apk/alpine/v3.23/main > etc/apk/repositories

apk update

#install the libpng package
apk add libpng
```
