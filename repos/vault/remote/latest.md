## `vault:latest`

```console
$ docker pull vault@sha256:d6a888829685c42b664f86d18defea43c48ea01a84f0f2da317d32100c07caa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:f5d59e4661c476456436053c3fc095d44cfc3a1a567c946b480c9084519b31e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51638456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed4dfee4b28684a3ce4dc88e661fd7766c1f474f11de592584d4f9235e4c7e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 01:42:37 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 01:42:39 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 01:42:48 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 01:42:49 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 01:42:50 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 01:42:51 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 01:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 01:42:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28dde1fe3c3a096c6913f6ac86539b832c59b03752e505a79598bbb651cdd31`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5c8a53e93f6eb56cb61c0058c51b92748ad67df223fe5455d4793e108ad0d3`  
		Last Modified: Thu, 23 Jan 2020 01:43:28 GMT  
		Size: 48.8 MB (48848090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd37952b5471a8e7853bd82ccadb28eb577024017cc137ebcb88a0fd938cc13`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f49952ad5ba9abcb19b33d48ff892dca7268ed04c8f883cec3b453ad4a8684c`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:ace471023cfc4737f5a82c2680bce7ec2983e027ec2c27db7b764120fa2453b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48648959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800c5f6c32e01ada90c16c5b1fd319c3b3b5c7bbcc601fe5f7a9871295a1b20c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:55:25 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 20:55:29 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 20:55:40 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 20:55:44 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 20:55:44 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 20:55:46 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 20:55:47 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 20:55:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 20:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 20:55:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb635609e19b305a9a1d8ee4b0596d2da091b38cd70bbee0a686547ce41c97ca`  
		Last Modified: Thu, 23 Jan 2020 20:56:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eec7232ee57f98f7ba188234b448c8fab3791b8e92b29bfa00b72e49603523`  
		Last Modified: Thu, 23 Jan 2020 20:56:16 GMT  
		Size: 46.1 MB (46074256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f78ff3086e9bb54e05790bcf7d62a6b891dd911763c340890703b897ab7d42`  
		Last Modified: Thu, 23 Jan 2020 20:56:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1965bf3a3f6b1cd80ff3f7c0ff3c4e8881072ca3707d110ae32e0795f1142e0`  
		Last Modified: Thu, 23 Jan 2020 20:56:03 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:fb59ef841f6a2a6c17249c6c6022b7ae112a9304751e9b2993cb7de5709a0146
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48702901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefedb0590727014f2974db2e71335bd117779fedfd9e503e44993d023d2131e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:41:22 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 23:41:24 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 23:41:33 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 23:41:38 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 23:41:39 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 23:41:40 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 23:41:42 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 23:41:42 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 23:41:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 23:41:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1830a2af380c9ff4b25756d94d9ae345955aea8b28fbc1106cade60b8f27b41d`  
		Last Modified: Thu, 23 Jan 2020 23:41:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bdf02ed4c8e272e282b5359ad60ef433bd3c62a5e733d20d5cd5604df6f5c3`  
		Last Modified: Thu, 23 Jan 2020 23:42:13 GMT  
		Size: 46.0 MB (45981873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7607612f0494e36dba4135af80578f63abb54605226105b8135b46d859e9b83`  
		Last Modified: Thu, 23 Jan 2020 23:41:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75922dd29f1883db8eb8da1cd47e5f2cb12ac2dfaf414208df09b84f79da7b35`  
		Last Modified: Thu, 23 Jan 2020 23:41:55 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:a08805ef34293243ed0b42b2992cddada942af061928472b4179e43a8b0aa303
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50110969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a35287d792e022200aaba53c6a482be3e78713f916e6e9793a2d18c9ba33f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 16:46:04 GMT
ADD file:dd3b3676fd9c1e0983ade68242b9b9ac5c477f3e4bfc97c2e78fd5db93a441c9 in / 
# Mon, 21 Oct 2019 16:46:04 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 00:37:26 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 00:37:27 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 00:37:33 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 00:37:34 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 00:37:34 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 00:37:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 00:37:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 00:37:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f913bd05bf684aaa4bc173d73cfbb58abb45587962d74f0aa71df36b6b489def`  
		Last Modified: Mon, 21 Oct 2019 16:46:25 GMT  
		Size: 2.8 MB (2785939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff789d789e4d18dd368b4863e187d271f0dd7a14e13bef3dbbed045aa88a109`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031da651da359ea0381bae5680d7bca73dc7690e81fbb5cf1258ce0884c606d8`  
		Last Modified: Thu, 23 Jan 2020 00:37:54 GMT  
		Size: 47.3 MB (47321799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92ca2c9ac411ddcaa517ab7f9e4581b1485b098538a964c689e3eb04df783c0`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6ca638a990477e39c71747e693985f5a200fbe4ad4a9114f900e9794250ed1`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
