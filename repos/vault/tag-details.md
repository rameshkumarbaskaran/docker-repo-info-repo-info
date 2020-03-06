<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.3.3`](#vault133)
-	[`vault:1.4.0-beta1`](#vault140-beta1)
-	[`vault:latest`](#vaultlatest)

## `vault:1.3.3`

```console
$ docker pull vault@sha256:5b753351ad1d9fd67505590b6b09496b295e0ae2e2ef4362d9b4beeaff574018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.3.3` - linux; amd64

```console
$ docker pull vault@sha256:1b203c1d370e495d4379b3e755c2324410b6676b53c759aae22ca567af13db35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51661318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62afcace31e0772e99040ce20b031d771acecb0c6ca8e653444745a5fa4eaadd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 02:57:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 02:57:30 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 02:57:38 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 02:57:39 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 02:57:40 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 02:57:41 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 02:57:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 02:57:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914a97be7f78b18056a221c1d0023fbb661f9541b82ddccc9370196e778f8fe6`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b0f45b5b08ad853e3605785296cfeeda0aea4ac447db9aa84dfe229f2c4bed`  
		Last Modified: Fri, 06 Mar 2020 02:58:09 GMT  
		Size: 48.9 MB (48871118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87de0ca272088222aa4a962aff9e2f8208194873f9f9a91ddc75fe88d5e9a861`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bd5a355d95a63ef3fc609b4e2aa8d3a3353ae887c2e93c02aa501ca85eb8d3`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:1b9997d4c553acbe418a13a4b73c762d7b49015d8b4c5b0e86f0f048596875f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ffdc311923e5d54fa3a59a1df6abf786f5ccd342895029ddb150dc5ff605b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 00:55:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 00:55:33 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 00:55:45 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 00:55:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 00:55:49 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 00:55:51 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 00:55:52 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 00:55:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 00:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 00:55:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a567ddc30d56011de831c407b2129f5bcc2442b46cc8c15fbc1aacfabd3e0b9`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edef0bda03882a1e50ca392e314c92878306caf2c2f58bebf6704b063c12627b`  
		Last Modified: Fri, 06 Mar 2020 00:56:27 GMT  
		Size: 46.1 MB (46080203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbaaf71699968312efe22141bfd4dde74d64cc07f33fe3b282a61f501dbeff2`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b7574cc3a74ae3094aa9e06c60e43bae43d2fac658175c79d6d4f07cbff8f7`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:08da0299cf2660db43448fb5ee35c0756cbcdfa1fcf150864acefc5f76484d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ef60ed7fe0af081d599c6b9f80fa226c9b35b8022cc7984bc41edb7a138adf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 01:47:23 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 01:47:25 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 01:47:36 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 01:47:44 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 01:47:45 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 01:47:46 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 01:47:48 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 01:47:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 01:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 01:47:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ba3d7a0a1b09f2f2ba0550eeb29e8b8825c273d3a7bc682581606f0322023b`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f186b25fe941fee17f647a95d3e025d5f937707bcaf8a282ca23ed947725edc`  
		Last Modified: Fri, 06 Mar 2020 01:48:22 GMT  
		Size: 46.0 MB (45988656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68c51c0befa64223d4d09e12b0a5f7a733aead3357fab45e490326e048d036`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a752cc871ffdbf651cfa2e24fc6a82936583e1f4b2e1e8304d789361f9cc3047`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.3` - linux; 386

```console
$ docker pull vault@sha256:3cd22b722daff9917f9a08bde757562a2371dd05572cedf5aea35c59b951462d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22be18d5c2e0ddec9e1715f2c4bf24393cc5c43cce976152e11e57a961fed73c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 03:15:38 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 03:15:40 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 03:15:47 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 03:15:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 03:15:48 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 03:15:49 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 03:15:49 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 03:15:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 03:15:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 03:15:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2983c25fde9b3a5aac2130561da76af1294ddc9b74bf9009eb2938b24fc5f2d`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c475463be64b31e8be1fd9086c0b94fe2c0232287a87de9a6041c92605356ec`  
		Last Modified: Fri, 06 Mar 2020 03:16:12 GMT  
		Size: 47.3 MB (47326492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab3e6cabb9495f0b5417576d9a01675fffd8cc7af1cfca75d838b0ab15053e4`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e799b1d2c4f4b1f74ac84f65f440b52ed376f5887c1d692e1391fe7c6d77a56`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.4.0-beta1`

```console
$ docker pull vault@sha256:a54469a8c963d88f4dc86a8d66374cd4be294edc761fdeaf8a8df498960f8f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.4.0-beta1` - linux; amd64

```console
$ docker pull vault@sha256:f205e369306f6ec204c79f7ba69853eafaa1813e80302135c43184287de0cc3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52010840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647def44c08ce03b2365e39336050bec86a690236a0d4f540709489e23fb5420`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 21:26:28 GMT
ARG VAULT_VERSION=1.4.0-beta1
# Fri, 21 Feb 2020 21:26:29 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 21 Feb 2020 21:26:34 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 21 Feb 2020 21:26:35 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 21 Feb 2020 21:26:35 GMT
VOLUME [/vault/logs]
# Fri, 21 Feb 2020 21:26:36 GMT
VOLUME [/vault/file]
# Fri, 21 Feb 2020 21:26:36 GMT
EXPOSE 8200
# Fri, 21 Feb 2020 21:26:36 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 21:26:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 21:26:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272a4074827ee52e95a4e5079b43c16cc3391f6544f9fc3a8ad996e0bf2eb50d`  
		Last Modified: Fri, 21 Feb 2020 21:26:43 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44c454a98d38abd880a52c4ca26fd9a864c1b33b88a01a8f320e96016b81884`  
		Last Modified: Fri, 21 Feb 2020 21:26:51 GMT  
		Size: 49.2 MB (49220640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4af8f08e0e6dc3678e7ff64d15bb9e3dfdf6bbcd01b62948fe0d53089535e`  
		Last Modified: Fri, 21 Feb 2020 21:26:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad56ffcb217e17583660bb2eedf0159c9276cfad7dbac7b3eea493ebd461d44`  
		Last Modified: Fri, 21 Feb 2020 21:26:43 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.0-beta1` - linux; arm variant v6

```console
$ docker pull vault@sha256:18f6a12d2e98dd72116d6657708f04b6de0197bff85a1628bd7d55a70587199d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48658441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723d691a8a55622790829b97ca72ea469c4450a30b95a9f5ae132ef815e4150`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 21:49:58 GMT
ARG VAULT_VERSION=1.4.0-beta1
# Fri, 21 Feb 2020 21:50:03 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 21 Feb 2020 21:50:23 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 21 Feb 2020 21:50:28 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 21 Feb 2020 21:50:32 GMT
VOLUME [/vault/logs]
# Fri, 21 Feb 2020 21:50:34 GMT
VOLUME [/vault/file]
# Fri, 21 Feb 2020 21:50:36 GMT
EXPOSE 8200
# Fri, 21 Feb 2020 21:50:37 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 21:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 21:50:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4b3c5a0f821cd2e448c4335120bf374dec0ffc344e25cb3a1753dc820f515a`  
		Last Modified: Fri, 21 Feb 2020 21:50:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c933e1f4a0a7e1dde178db3224659ccce765e07ec28f3b0343620d65a97e12df`  
		Last Modified: Fri, 21 Feb 2020 21:51:11 GMT  
		Size: 46.1 MB (46083734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a758bd0497e4a9a3065cb5034fc0fcf25b9cc88e030ed643ec1086858e2e776`  
		Last Modified: Fri, 21 Feb 2020 21:50:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df2496b20fd685d3461085fe4614aa083ebee8c6271c8eb91177b57502f884b`  
		Last Modified: Fri, 21 Feb 2020 21:50:58 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.0-beta1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a4f140b27b07bea97db23755bf721d1e8852b8912006a815ff695a4e5ba5c396
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48939708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90ec7c616f8543a5149501364684c011f996645ad63fe8e544a6f9cc80309d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 21:52:55 GMT
ARG VAULT_VERSION=1.4.0-beta1
# Fri, 21 Feb 2020 21:53:01 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 21 Feb 2020 21:53:16 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 21 Feb 2020 21:53:19 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 21 Feb 2020 21:53:20 GMT
VOLUME [/vault/logs]
# Fri, 21 Feb 2020 21:53:21 GMT
VOLUME [/vault/file]
# Fri, 21 Feb 2020 21:53:22 GMT
EXPOSE 8200
# Fri, 21 Feb 2020 21:53:22 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 21:53:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37d82371099a6031464bb8a2bf89a814b0da7b4fa9a131d6c45fba91adcf2b4`  
		Last Modified: Fri, 21 Feb 2020 21:53:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c2945e999b033dd935d7673478dc23db1593e44070ec4ec1a410a9d619974c`  
		Last Modified: Fri, 21 Feb 2020 21:53:44 GMT  
		Size: 46.2 MB (46218673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55948ae29a81c6ac408c065af96b15708df1114031093f0e047576293c7d1397`  
		Last Modified: Fri, 21 Feb 2020 21:53:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cd49d4d08fd638433ee8dd2acacaef94630b58769bc8b131a1c9119f23b1d2`  
		Last Modified: Fri, 21 Feb 2020 21:53:33 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.0-beta1` - linux; 386

```console
$ docker pull vault@sha256:7b4d860b673ff4ba22ceff5e20fd702160b06bf2eb947f1f71918d4571fc768d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50165076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49068e7843b652e8aa3a43547ed10393a652a1c5d9f20f5913fa10785c6f5bd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 21 Feb 2020 21:40:42 GMT
ARG VAULT_VERSION=1.4.0-beta1
# Fri, 21 Feb 2020 21:40:43 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 21 Feb 2020 21:40:49 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 21 Feb 2020 21:40:50 GMT
# ARGS: VAULT_VERSION=1.4.0-beta1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 21 Feb 2020 21:40:50 GMT
VOLUME [/vault/logs]
# Fri, 21 Feb 2020 21:40:50 GMT
VOLUME [/vault/file]
# Fri, 21 Feb 2020 21:40:50 GMT
EXPOSE 8200
# Fri, 21 Feb 2020 21:40:51 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 21:40:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 21:40:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fe9d35f4094ce92e8ff3200455ad05b98eabd8a58190930016c0ca48c8c0df`  
		Last Modified: Fri, 21 Feb 2020 21:40:58 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23873910db1a74fadc7d51e254613e4fdc8b692fe468e56938f4f88e6fcf0ab`  
		Last Modified: Fri, 21 Feb 2020 21:41:06 GMT  
		Size: 47.4 MB (47375981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137e615ed509410ecf39f39850deb3adc26f3b85b958048951e0eaf337ed6ffd`  
		Last Modified: Fri, 21 Feb 2020 21:40:58 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa860f27f5af5474a9494573c478b199af71c0b491e275f0dafb9f7938d9fdc`  
		Last Modified: Fri, 21 Feb 2020 21:40:58 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:5b753351ad1d9fd67505590b6b09496b295e0ae2e2ef4362d9b4beeaff574018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:1b203c1d370e495d4379b3e755c2324410b6676b53c759aae22ca567af13db35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51661318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62afcace31e0772e99040ce20b031d771acecb0c6ca8e653444745a5fa4eaadd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 02:57:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 02:57:30 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 02:57:38 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 02:57:39 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 02:57:40 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 02:57:41 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 02:57:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 02:57:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914a97be7f78b18056a221c1d0023fbb661f9541b82ddccc9370196e778f8fe6`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b0f45b5b08ad853e3605785296cfeeda0aea4ac447db9aa84dfe229f2c4bed`  
		Last Modified: Fri, 06 Mar 2020 02:58:09 GMT  
		Size: 48.9 MB (48871118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87de0ca272088222aa4a962aff9e2f8208194873f9f9a91ddc75fe88d5e9a861`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bd5a355d95a63ef3fc609b4e2aa8d3a3353ae887c2e93c02aa501ca85eb8d3`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:1b9997d4c553acbe418a13a4b73c762d7b49015d8b4c5b0e86f0f048596875f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ffdc311923e5d54fa3a59a1df6abf786f5ccd342895029ddb150dc5ff605b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 00:55:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 00:55:33 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 00:55:45 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 00:55:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 00:55:49 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 00:55:51 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 00:55:52 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 00:55:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 00:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 00:55:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a567ddc30d56011de831c407b2129f5bcc2442b46cc8c15fbc1aacfabd3e0b9`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edef0bda03882a1e50ca392e314c92878306caf2c2f58bebf6704b063c12627b`  
		Last Modified: Fri, 06 Mar 2020 00:56:27 GMT  
		Size: 46.1 MB (46080203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbaaf71699968312efe22141bfd4dde74d64cc07f33fe3b282a61f501dbeff2`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b7574cc3a74ae3094aa9e06c60e43bae43d2fac658175c79d6d4f07cbff8f7`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:08da0299cf2660db43448fb5ee35c0756cbcdfa1fcf150864acefc5f76484d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ef60ed7fe0af081d599c6b9f80fa226c9b35b8022cc7984bc41edb7a138adf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 01:47:23 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 01:47:25 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 01:47:36 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 01:47:44 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 01:47:45 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 01:47:46 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 01:47:48 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 01:47:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 01:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 01:47:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ba3d7a0a1b09f2f2ba0550eeb29e8b8825c273d3a7bc682581606f0322023b`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f186b25fe941fee17f647a95d3e025d5f937707bcaf8a282ca23ed947725edc`  
		Last Modified: Fri, 06 Mar 2020 01:48:22 GMT  
		Size: 46.0 MB (45988656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68c51c0befa64223d4d09e12b0a5f7a733aead3357fab45e490326e048d036`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a752cc871ffdbf651cfa2e24fc6a82936583e1f4b2e1e8304d789361f9cc3047`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:3cd22b722daff9917f9a08bde757562a2371dd05572cedf5aea35c59b951462d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22be18d5c2e0ddec9e1715f2c4bf24393cc5c43cce976152e11e57a961fed73c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 03:15:38 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 03:15:40 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 03:15:47 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 03:15:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 03:15:48 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 03:15:49 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 03:15:49 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 03:15:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 03:15:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 03:15:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2983c25fde9b3a5aac2130561da76af1294ddc9b74bf9009eb2938b24fc5f2d`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c475463be64b31e8be1fd9086c0b94fe2c0232287a87de9a6041c92605356ec`  
		Last Modified: Fri, 06 Mar 2020 03:16:12 GMT  
		Size: 47.3 MB (47326492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab3e6cabb9495f0b5417576d9a01675fffd8cc7af1cfca75d838b0ab15053e4`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e799b1d2c4f4b1f74ac84f65f440b52ed376f5887c1d692e1391fe7c6d77a56`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
