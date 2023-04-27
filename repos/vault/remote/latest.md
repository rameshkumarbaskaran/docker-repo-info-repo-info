## `vault:latest`

```console
$ docker pull vault@sha256:eb910358ab988d1f132fbe67869f3a5e63e210f9a4d97dfbb4929a4922ede421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:472e3f23f87d3b342e192040032a5b180c71b5a79ef74fc3597ab9d6f7af19b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa9c3f0708d01b46c50683d6f12dee2f1573e2dfc8e290142bfb1392c0245a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:22:16 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:22:16 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:22:23 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:22:24 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:22:24 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:22:24 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:22:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:22:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5c87a2b3cf5178bb2b01489a0896610aa75b4d74d827a75ebe1c1f6220ffe0`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e09e6dc12b97e85b5509f1ab3022ab16868d9dd0f9595f65c26d12446c870c0`  
		Last Modified: Thu, 27 Apr 2023 19:23:09 GMT  
		Size: 50.1 MB (50112033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b003dccbe77bf2dccff4024e42e4b8504aedfe3efc81e8500005e073e38ad2a`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640451d14d72c74b1eed8c79a3009ef61474533c2480cf15d0c69ba939cd4a15`  
		Last Modified: Thu, 27 Apr 2023 19:23:02 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:ad2d30d1ab890817b09020d72cbbcfff38d9443c073750a1aca2799c1a45a30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50025624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ce76f70c01101780912889feb12748f64f62462d9607568222f178cf62ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:49:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:49:27 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:49:42 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:49:43 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:49:43 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:49:43 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:49:44 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:49:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81cd9319c9e96c0d74a2f37945c7a6ebeefd3afb563225cdd4d6de82637f3a2`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811e6ae161b1d746eb72519482618ebd06b08b801cdd606be98b548486f34cd8`  
		Last Modified: Thu, 27 Apr 2023 19:50:30 GMT  
		Size: 47.4 MB (47384095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6b43dd5e88bb79a43ca4940445db5214aac5b59ce19eb374de7109c971ceb3`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47987bdff503410a6c7392fb3bd3486e1156e51ea5cff36c8f352719b85bc107`  
		Last Modified: Thu, 27 Apr 2023 19:50:21 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:533b8cc77262ea254a098628dfd9d1d8ca970e2ef07ba79646a5cb4eeb725c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48802428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc57a2ad9f154824f52b24424fe2b96518e33cb84be6653b31eb8adea6a55b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:47:02 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:47:03 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:47:09 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:47:10 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:47:10 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:47:10 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:47:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:47:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:47:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97f0b119a2f5a8e0f00d0890aa69ff142c47ebf09eb894f03d7d05af92db40`  
		Last Modified: Thu, 27 Apr 2023 19:47:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce5a2b6799700f279a3dde8c9ff0b95286944146bdd8d725c33f87fa99c4a2c`  
		Last Modified: Thu, 27 Apr 2023 19:47:51 GMT  
		Size: 46.1 MB (46074010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf4649dcb8a3476d927316442beb05516fd44ae8b41408f54ea01445a997348`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d68cd01d93e81ea286bab38202928cfb045d0db9c3d8954badff60115ab7c`  
		Last Modified: Thu, 27 Apr 2023 19:47:46 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:d8658d8297c41e1735d881821308824a611aed85a9d3ceaab26b4f9c728d5f2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49636809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f47ad2fd5c9054f60a886e2b7391c258b5fb9b87a05a5f4aca998dc628a2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 27 Apr 2023 19:38:27 GMT
ARG VAULT_VERSION=1.13.2
# Thu, 27 Apr 2023 19:38:28 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 27 Apr 2023 19:38:40 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 27 Apr 2023 19:38:41 GMT
# ARGS: VAULT_VERSION=1.13.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/logs]
# Thu, 27 Apr 2023 19:38:41 GMT
VOLUME [/vault/file]
# Thu, 27 Apr 2023 19:38:41 GMT
EXPOSE 8200
# Thu, 27 Apr 2023 19:38:41 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 27 Apr 2023 19:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Apr 2023 19:38:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ea130633cae1a572c761a4728f37e1df1b2b29b956269149063e5f55dd2f30`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d4d0677d342258cb20902dbecea128eab19360a127859be376bba6b44e635`  
		Last Modified: Thu, 27 Apr 2023 19:39:30 GMT  
		Size: 46.8 MB (46798337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c032fbbf147af3fde561aafac6afc459f9fd1af1c178512ee2b6fdebaaeefd7`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f209a2868f1846c7024afab6803c993a1bd711888b19d72dd68b44dc622b418`  
		Last Modified: Thu, 27 Apr 2023 19:39:21 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
