## `vault:latest`

```console
$ docker pull vault@sha256:1a5e066e8c15d9c31d858a3974aaf3c4289c360a4a85c4685d791ec9a7e2518d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:71beaeca153c4cfb27fde00f778468ad5d8d3b6729aca29af5a6f530ac03b7ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52141093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeff8a0e63ad36dc9b200a6aa38aba61ba3a032d0c0523cb61f68490af4c00cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 03 Jul 2020 17:20:12 GMT
ARG VAULT_VERSION=1.4.3
# Fri, 03 Jul 2020 17:20:13 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Jul 2020 17:20:18 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Jul 2020 17:20:19 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Jul 2020 17:20:19 GMT
VOLUME [/vault/logs]
# Fri, 03 Jul 2020 17:20:19 GMT
VOLUME [/vault/file]
# Fri, 03 Jul 2020 17:20:20 GMT
EXPOSE 8200
# Fri, 03 Jul 2020 17:20:20 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Jul 2020 17:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Jul 2020 17:20:20 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33636826a943396873384b2ee6b43c080db2f1920e418b8d2ea33104b5a3efc`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38d5932db2a5e4c40690f53207ac6b13b3ac2b3f3ce6b9fdf98e823bc698d15`  
		Last Modified: Fri, 03 Jul 2020 17:20:48 GMT  
		Size: 49.3 MB (49342274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7982fbe652748b20a8efd499c18b93933b2af4ae182e8f1efd3e09b8ce70e3e`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5723939fa01f464fa05b331dd1943283486bfa213cb85185fa09271f80854704`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:a7197dee0d6ed411a66def9f0721bbea9c6853084f89a1fa9e59b9f9983205e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225360cf96e2abf2bd5bb1c5efaa0ed7fd4810df1f886e055e991fc206f64d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 03 Jul 2020 16:50:27 GMT
ARG VAULT_VERSION=1.4.3
# Fri, 03 Jul 2020 16:50:30 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Jul 2020 16:50:54 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Jul 2020 16:50:56 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Jul 2020 16:50:56 GMT
VOLUME [/vault/logs]
# Fri, 03 Jul 2020 16:50:57 GMT
VOLUME [/vault/file]
# Fri, 03 Jul 2020 16:50:57 GMT
EXPOSE 8200
# Fri, 03 Jul 2020 16:50:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Jul 2020 16:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Jul 2020 16:50:59 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55fbc041999fc2b59dd451c802e26b955c2c9f45fc376a033644e0fbec7d538`  
		Last Modified: Fri, 03 Jul 2020 16:51:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdab99a032b3f65109473b674a16f7ff401d24a23a5364debe26c4696205435`  
		Last Modified: Fri, 03 Jul 2020 16:51:50 GMT  
		Size: 46.2 MB (46244893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2b0cf842ee0b011b893eaadca627380e9af54d97c52a8efb9b6b14f82d64fa`  
		Last Modified: Fri, 03 Jul 2020 16:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81208e1208a8a16d2e685126cd2040ce76bbdce58676cd885812f35d4fb9ced`  
		Last Modified: Fri, 03 Jul 2020 16:51:37 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:51c2813c74997a005fe9c64715a934b93287ba6b2126220cbf8a7f475bde34be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49028493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c54deca72d1588ea06df9cfbc781d5a096e1f53052a0587adb3a92d3cdcb91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2020 01:59:50 GMT
ARG VAULT_VERSION=1.4.2
# Fri, 22 May 2020 01:59:51 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 22 May 2020 02:00:00 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 22 May 2020 02:00:02 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 22 May 2020 02:00:03 GMT
VOLUME [/vault/logs]
# Fri, 22 May 2020 02:00:04 GMT
VOLUME [/vault/file]
# Fri, 22 May 2020 02:00:04 GMT
EXPOSE 8200
# Fri, 22 May 2020 02:00:05 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 22 May 2020 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 02:00:07 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d873c96e3edf503e56bbb37aedd1fc4b333fb176afb3ac4da95b63ce8628578`  
		Last Modified: Fri, 22 May 2020 02:00:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f54e793c0dec968ac1cf41d623e1eb4f60b6b16089431d0bd62a796c956bbc`  
		Last Modified: Fri, 22 May 2020 02:00:56 GMT  
		Size: 46.3 MB (46306461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4012bdb6bbfd8327098390234a0e639058ee5ae6a356c39567d2997a7aa2c41`  
		Last Modified: Fri, 22 May 2020 02:00:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4a9146e4d83c63b86d1ec80096cdebd97d2c71b1aeeffe7b01bf2e57ebb2e6`  
		Last Modified: Fri, 22 May 2020 02:00:45 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:7a20b7ebc39ed5c5e4d288973706ff3825ec6dd47423fc95c6e9dc411e30f06e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50272518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07aafe2d52ee13c6e96e67bcf0d7cd8c0e40d7788f3afe9a7d6d6ec09c8279a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2020 01:39:15 GMT
ARG VAULT_VERSION=1.4.2
# Fri, 22 May 2020 01:39:16 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 22 May 2020 01:39:24 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 22 May 2020 01:39:25 GMT
# ARGS: VAULT_VERSION=1.4.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 22 May 2020 01:39:25 GMT
VOLUME [/vault/logs]
# Fri, 22 May 2020 01:39:25 GMT
VOLUME [/vault/file]
# Fri, 22 May 2020 01:39:25 GMT
EXPOSE 8200
# Fri, 22 May 2020 01:39:25 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 22 May 2020 01:39:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 May 2020 01:39:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf35f5b2313ed4f33dc793826798937f064d72a0b09786f2562f2e037989a42`  
		Last Modified: Fri, 22 May 2020 01:39:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27ad5098060efe25961a366003ed31e83611754fe7fb15d73c6bfef402a25b`  
		Last Modified: Fri, 22 May 2020 01:39:55 GMT  
		Size: 47.5 MB (47482152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f1baeadab2ee174406eafe8aa0e25d027505606f3770c0e8feddedc0e16c07`  
		Last Modified: Fri, 22 May 2020 01:39:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fc57e8b6fb80727bf7717db47f0820a3079dcc1bfb6ab0267e39fa02e7a59a`  
		Last Modified: Fri, 22 May 2020 01:39:46 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
