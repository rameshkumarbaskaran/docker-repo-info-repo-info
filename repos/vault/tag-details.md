<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.10`](#vault11010)
-	[`vault:1.11.7`](#vault1117)
-	[`vault:1.12.3`](#vault1123)
-	[`vault:1.9.10`](#vault1910)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.10`

```console
$ docker pull vault@sha256:e4d56d51393e0a57ae9c87a65a6947def91dd5fe06ec53e5556f296824991f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `vault:1.10.10` - linux; amd64

```console
$ docker pull vault@sha256:f1bff704f93d96bb846a71e4b346f9981eb0b8c301c5a24624385c8e7d24e3ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85322908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08d3561ab54178aac9f278e2da605b3d677dc2c2ce646c01d47819e15b60ea9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 07 Feb 2023 21:20:39 GMT
ARG VAULT_VERSION=1.10.10
# Tue, 07 Feb 2023 21:20:40 GMT
# ARGS: VAULT_VERSION=1.10.10
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Feb 2023 21:20:48 GMT
# ARGS: VAULT_VERSION=1.10.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Feb 2023 21:20:49 GMT
# ARGS: VAULT_VERSION=1.10.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Feb 2023 21:20:49 GMT
VOLUME [/vault/logs]
# Tue, 07 Feb 2023 21:20:49 GMT
VOLUME [/vault/file]
# Tue, 07 Feb 2023 21:20:49 GMT
EXPOSE 8200
# Tue, 07 Feb 2023 21:20:49 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Feb 2023 21:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Feb 2023 21:20:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfaad4b04999667127c05060f1fd52d13dd2a5783c5d5ea5aae8dc326cad1e6`  
		Last Modified: Tue, 07 Feb 2023 21:21:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac125d75253eb0835fb6119dbb821c9090ac8494f832635f09afd47da312d1bb`  
		Last Modified: Tue, 07 Feb 2023 21:21:48 GMT  
		Size: 82.5 MB (82492145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adae2af542332e8ce09c076f2c2b18f5a4094a8b7db8cbd997c21496038f7224`  
		Last Modified: Tue, 07 Feb 2023 21:21:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e0e5745d01b0d92f969acb44604cdb6d4eb883cfc8186064a075ce299714bf`  
		Last Modified: Tue, 07 Feb 2023 21:21:39 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.11.7`

```console
$ docker pull vault@sha256:4f7a50d4724cade2d41ed7796c222a053471dc455a93fbef68d33b9d1b5966b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `vault:1.11.7` - linux; amd64

```console
$ docker pull vault@sha256:9f90ebd50c56c32a9d3cc36912e6eda247d352b052f93f71e96a78e9bc132ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81250055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c55444b67bc6d87d37a3913ea9d11a5cbc167ded4868e5fc270b4002fbbc1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 07 Feb 2023 21:20:25 GMT
ARG VAULT_VERSION=1.11.7
# Tue, 07 Feb 2023 21:20:26 GMT
# ARGS: VAULT_VERSION=1.11.7
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Feb 2023 21:20:34 GMT
# ARGS: VAULT_VERSION=1.11.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Feb 2023 21:20:35 GMT
# ARGS: VAULT_VERSION=1.11.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Feb 2023 21:20:35 GMT
VOLUME [/vault/logs]
# Tue, 07 Feb 2023 21:20:35 GMT
VOLUME [/vault/file]
# Tue, 07 Feb 2023 21:20:35 GMT
EXPOSE 8200
# Tue, 07 Feb 2023 21:20:35 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Feb 2023 21:20:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Feb 2023 21:20:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1a8c7b3fa6b96532ae63bbc0c4e7963b0042cefbb68402fde3548b519140c7`  
		Last Modified: Tue, 07 Feb 2023 21:21:23 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bb510a68e08984c0e8c84f6d886d3c29484eff6694c55755a42c57cb84de5d`  
		Last Modified: Tue, 07 Feb 2023 21:21:32 GMT  
		Size: 78.4 MB (78419295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a052a5324144f9855f50a7a3936c51dfc25c7d2f0f539df3de722a1ae91f1c1`  
		Last Modified: Tue, 07 Feb 2023 21:21:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4409f4ba54c10d5efb7bcc0bbce1fdbb733e14323373a6da61738e11402cb1`  
		Last Modified: Tue, 07 Feb 2023 21:21:23 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.3`

```console
$ docker pull vault@sha256:36286234ccbf14c4ec5a2dbdfffc76daeb21e9f751855086c610821c0b7f84ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `vault:1.12.3` - linux; amd64

```console
$ docker pull vault@sha256:f23aba53dc89568543cb239e473d40dee4014b7097e4df510fde7a4b3c5a9843
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85983475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129bb81edb9111fa2cd22036b8f7595cba5aa39c09790e007d1de33698f45216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 07 Feb 2023 21:20:11 GMT
ARG VAULT_VERSION=1.12.3
# Tue, 07 Feb 2023 21:20:12 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Feb 2023 21:20:20 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Feb 2023 21:20:21 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Feb 2023 21:20:21 GMT
VOLUME [/vault/logs]
# Tue, 07 Feb 2023 21:20:21 GMT
VOLUME [/vault/file]
# Tue, 07 Feb 2023 21:20:22 GMT
EXPOSE 8200
# Tue, 07 Feb 2023 21:20:22 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Feb 2023 21:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Feb 2023 21:20:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab302192407da647f7f5170b70371327df3d4a82103b17d9c8eabdf7d67f34d`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d7269c8c8840e21da4a1dd147dbf14b20563138c6fd1e40585096ceb41b49`  
		Last Modified: Tue, 07 Feb 2023 21:21:14 GMT  
		Size: 83.2 MB (83152715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f3bdc32c7e2d84c177114db9e5f9a7e05d5a3af56392c69262f24277028c8`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954125a41ef83a17c5a5a7a97d3b82f2ec901b829c2e30b99d08692ecb3e618f`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.10`

```console
$ docker pull vault@sha256:fe51eed602bf9f3291528e88c29f2cb371646ad1792cf1cd3ce860a802e166ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.9.10` - linux; amd64

```console
$ docker pull vault@sha256:6a56b6ca7b15272f2944cb6c84a460981bb24f4831b5eec6f386a7a5b6609fb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73205228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1319ffbfde70d487bd7ef0098f4dedece1fb605dd55af221d2a15405f5400642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 20:35:18 GMT
ARG VAULT_VERSION=1.9.10
# Fri, 07 Oct 2022 20:35:18 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 07 Oct 2022 20:35:26 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 07 Oct 2022 20:35:27 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 07 Oct 2022 20:35:27 GMT
VOLUME [/vault/logs]
# Fri, 07 Oct 2022 20:35:27 GMT
VOLUME [/vault/file]
# Fri, 07 Oct 2022 20:35:27 GMT
EXPOSE 8200
# Fri, 07 Oct 2022 20:35:27 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 Oct 2022 20:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 20:35:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129d697f1d97ba99daed110bda884d2a0785887b08be678dce80290044fe5e31`  
		Last Modified: Fri, 07 Oct 2022 20:36:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0a88106af746a4f335be2516f73e95c99fb26d4da850fb6551687503c56fb`  
		Last Modified: Fri, 07 Oct 2022 20:36:39 GMT  
		Size: 70.4 MB (70374464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daed4e617caf0936f1c7f4d8b8d99450ac92a378cb40bfcaa9b824545e4a53df`  
		Last Modified: Fri, 07 Oct 2022 20:36:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9864af2a51f0c3a5610c2543520008ed2bdfba6bec5b6f257fcd839d6ba6e85b`  
		Last Modified: Fri, 07 Oct 2022 20:36:31 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.10` - linux; arm variant v6

```console
$ docker pull vault@sha256:90a712fbedac6cd82a84b22f61c18903cda11e93af49d093d7070c46c26686cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66514809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d7993947d4b677c75a09761ba5be0442881f4e332faddd0797b0b66e5b1d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:43 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Thu, 10 Nov 2022 20:49:43 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:18:35 GMT
ARG VAULT_VERSION=1.9.10
# Fri, 11 Nov 2022 11:18:36 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 11 Nov 2022 11:18:44 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 11 Nov 2022 11:18:45 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 11 Nov 2022 11:18:45 GMT
VOLUME [/vault/logs]
# Fri, 11 Nov 2022 11:18:45 GMT
VOLUME [/vault/file]
# Fri, 11 Nov 2022 11:18:45 GMT
EXPOSE 8200
# Fri, 11 Nov 2022 11:18:45 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Nov 2022 11:18:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:18:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f9788d97bca9729754b282db12ac680c3ec3df5eb26350d1fca3270f7b06ac`  
		Last Modified: Fri, 11 Nov 2022 11:20:11 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c4c11f8106ab007e399ab983d5945f98ee4c8db26fb0c218ee169c6f80736b`  
		Last Modified: Fri, 11 Nov 2022 11:20:21 GMT  
		Size: 63.9 MB (63876101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefc9d51533ce9a9223591c4c6ab27e17023234f55598832356cababa8a330c`  
		Last Modified: Fri, 11 Nov 2022 11:20:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddc705b21c147a779054a9e9f17ddefc866b5d6ecb325d141e6f6a1dea0f560`  
		Last Modified: Fri, 11 Nov 2022 11:20:11 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.10` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7d93d291229181e4e78fedbe80841302dcc069d6c8849f3b046e45fd76f12cc1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68305784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef583c09b6683c21ffe68975817ece2d5428b516ae4d2b5b711eab59c28ccfbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:51 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Thu, 10 Nov 2022 20:39:51 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:27:16 GMT
ARG VAULT_VERSION=1.9.10
# Fri, 11 Nov 2022 05:27:17 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 11 Nov 2022 05:27:25 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 11 Nov 2022 05:27:26 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 11 Nov 2022 05:27:26 GMT
VOLUME [/vault/logs]
# Fri, 11 Nov 2022 05:27:26 GMT
VOLUME [/vault/file]
# Fri, 11 Nov 2022 05:27:26 GMT
EXPOSE 8200
# Fri, 11 Nov 2022 05:27:26 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Nov 2022 05:27:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:27:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a1afb6dafd0e1e530f629466ee49e34796efdc19dfd96c9984e2fc7efadf1`  
		Last Modified: Fri, 11 Nov 2022 05:28:23 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02018a2a0b1a97e98994b0b1e2e4d80cada167d58ee702317038f0ab6d2496d3`  
		Last Modified: Fri, 11 Nov 2022 05:28:30 GMT  
		Size: 65.6 MB (65580360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a73562d938b321d575fc6d2ac8fef5d264b02131f0202da9e9d8e45cdecb30c`  
		Last Modified: Fri, 11 Nov 2022 05:28:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db91b442ff15867738e6bd7fcff72d129e5d19bcf2f29a8edc889acbd884124`  
		Last Modified: Fri, 11 Nov 2022 05:28:23 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.9.10` - linux; 386

```console
$ docker pull vault@sha256:11ceae45e5122566c563931a5087f0f281a7122ff96c0fed26243c5ed3bc2897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69576445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041f436e9c64018fcd8cd88e3f621cf5dfe7b9f368ee6eaddf6fa38c08fd9ac7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:54 GMT
ADD file:fea8a3ba06779852956b0d3a2dd7514ab33217b1fd395231864c443797f077f6 in / 
# Tue, 09 Aug 2022 17:38:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 20:51:53 GMT
ARG VAULT_VERSION=1.9.10
# Fri, 07 Oct 2022 20:51:54 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 07 Oct 2022 20:52:02 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 07 Oct 2022 20:52:03 GMT
# ARGS: VAULT_VERSION=1.9.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 07 Oct 2022 20:52:04 GMT
VOLUME [/vault/logs]
# Fri, 07 Oct 2022 20:52:05 GMT
VOLUME [/vault/file]
# Fri, 07 Oct 2022 20:52:06 GMT
EXPOSE 8200
# Fri, 07 Oct 2022 20:52:08 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 Oct 2022 20:52:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 20:52:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2c44f983a875883421e7d5bc471f6437e0e377e6e7343b52c856caee71064d31`  
		Last Modified: Tue, 09 Aug 2022 17:40:01 GMT  
		Size: 2.8 MB (2832612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b6c8e40c34512957e16b1b20c5c3b3be109a5f3475dcb2d8389b64a93de2c`  
		Last Modified: Fri, 07 Oct 2022 20:53:17 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ddb4fda198f2c0901868cde900b0abc9142d1f2722989e7189e96ea278b2a`  
		Last Modified: Fri, 07 Oct 2022 20:53:24 GMT  
		Size: 66.7 MB (66740625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c02464e585952b48aa2e970a71e7a589c86384ab488debe8d7879141069c33f`  
		Last Modified: Fri, 07 Oct 2022 20:53:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5050d6a106f7372bbec28f9e113fb5d9ffbadcc73ea7bb0bc3e4a049d14a5b4c`  
		Last Modified: Fri, 07 Oct 2022 20:53:17 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:541472e3901217cfefb04060262675bb7a6c1ea7630d7a2e3996ba7e16061b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:f23aba53dc89568543cb239e473d40dee4014b7097e4df510fde7a4b3c5a9843
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85983475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129bb81edb9111fa2cd22036b8f7595cba5aa39c09790e007d1de33698f45216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 07 Feb 2023 21:20:11 GMT
ARG VAULT_VERSION=1.12.3
# Tue, 07 Feb 2023 21:20:12 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Feb 2023 21:20:20 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Feb 2023 21:20:21 GMT
# ARGS: VAULT_VERSION=1.12.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Feb 2023 21:20:21 GMT
VOLUME [/vault/logs]
# Tue, 07 Feb 2023 21:20:21 GMT
VOLUME [/vault/file]
# Tue, 07 Feb 2023 21:20:22 GMT
EXPOSE 8200
# Tue, 07 Feb 2023 21:20:22 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Feb 2023 21:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Feb 2023 21:20:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab302192407da647f7f5170b70371327df3d4a82103b17d9c8eabdf7d67f34d`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d7269c8c8840e21da4a1dd147dbf14b20563138c6fd1e40585096ceb41b49`  
		Last Modified: Tue, 07 Feb 2023 21:21:14 GMT  
		Size: 83.2 MB (83152715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f3bdc32c7e2d84c177114db9e5f9a7e05d5a3af56392c69262f24277028c8`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954125a41ef83a17c5a5a7a97d3b82f2ec901b829c2e30b99d08692ecb3e618f`  
		Last Modified: Tue, 07 Feb 2023 21:21:04 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:207fc0ee6952deb21f19c1aff2f5a5d92e8fd9ba83f8d0785a815bf6f0991abc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80633372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3016869d6bade3c40adfddd2f4d6c2a6b7d8f3433b42a3aab6f98e00b39d575e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:43 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Thu, 10 Nov 2022 20:49:43 GMT
CMD ["/bin/sh"]
# Mon, 05 Dec 2022 21:08:19 GMT
ARG VAULT_VERSION=1.12.2
# Mon, 05 Dec 2022 21:08:20 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 05 Dec 2022 21:08:31 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 05 Dec 2022 21:08:33 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 05 Dec 2022 21:08:33 GMT
VOLUME [/vault/logs]
# Mon, 05 Dec 2022 21:08:33 GMT
VOLUME [/vault/file]
# Mon, 05 Dec 2022 21:08:33 GMT
EXPOSE 8200
# Mon, 05 Dec 2022 21:08:33 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 05 Dec 2022 21:08:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:08:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620b5f4c8a213067f73e49d06997b7b802922bfe3a0c697afb293cbf16485e7`  
		Last Modified: Mon, 05 Dec 2022 21:09:34 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9561db60f9aaff2ff6ae623fcd2a72aa8b2a40ef41dc433c0414bd94b6486c4c`  
		Last Modified: Mon, 05 Dec 2022 21:09:46 GMT  
		Size: 78.0 MB (77994663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc169ea9a29328bfa0dd97643cfbfb74a5282a2b8919ddcc6a8eb348bda587d`  
		Last Modified: Mon, 05 Dec 2022 21:09:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d7b39cafcb0f6d142d36f65a46586a869568aa56be2e4f38cdb8705ef27d4a`  
		Last Modified: Mon, 05 Dec 2022 21:09:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:14525dc124826eb71d7ea389cf4a8718d8d7c8bf0625984ac02177a6ddaa7390
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80973885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf33d9d8966192bde4c4059f50795fd8b7454af8a4a512cb4d896c5b10652b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:51 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Thu, 10 Nov 2022 20:39:51 GMT
CMD ["/bin/sh"]
# Mon, 05 Dec 2022 21:34:03 GMT
ARG VAULT_VERSION=1.12.2
# Mon, 05 Dec 2022 21:34:03 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 05 Dec 2022 21:34:11 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 05 Dec 2022 21:34:13 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 05 Dec 2022 21:34:13 GMT
VOLUME [/vault/logs]
# Mon, 05 Dec 2022 21:34:13 GMT
VOLUME [/vault/file]
# Mon, 05 Dec 2022 21:34:13 GMT
EXPOSE 8200
# Mon, 05 Dec 2022 21:34:13 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 05 Dec 2022 21:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:34:13 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc8d880bf1dc8a671fa9d31313860ee0281a2bad1efbc10c05a4194f738309a`  
		Last Modified: Mon, 05 Dec 2022 21:34:53 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480111b36ad35f83edd72a7ebe790032c7945690007cfa44a963fd7dbbafbde8`  
		Last Modified: Mon, 05 Dec 2022 21:35:00 GMT  
		Size: 78.2 MB (78248461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ef4a565b99663c43c0180e715ee898be4762b2642518be79f1e412fc08ce4`  
		Last Modified: Mon, 05 Dec 2022 21:34:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa5cfbc7ed0db23990fcfa621b8c3e8b40165567ef638536e5ff814d97eb2ab`  
		Last Modified: Mon, 05 Dec 2022 21:34:53 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:c80b86214fce87748627593f4617cc8a53072d31d78e3b1a950664346ce0f6a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82391688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d469990fe1b96bfde2b3143822a4a5b9fdac48d9b3f435c46924bb70465dd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:54 GMT
ADD file:fea8a3ba06779852956b0d3a2dd7514ab33217b1fd395231864c443797f077f6 in / 
# Tue, 09 Aug 2022 17:38:54 GMT
CMD ["/bin/sh"]
# Mon, 05 Dec 2022 21:20:22 GMT
ARG VAULT_VERSION=1.12.2
# Mon, 05 Dec 2022 21:20:23 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 05 Dec 2022 21:20:34 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 05 Dec 2022 21:20:34 GMT
# ARGS: VAULT_VERSION=1.12.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 05 Dec 2022 21:20:35 GMT
VOLUME [/vault/logs]
# Mon, 05 Dec 2022 21:20:36 GMT
VOLUME [/vault/file]
# Mon, 05 Dec 2022 21:20:37 GMT
EXPOSE 8200
# Mon, 05 Dec 2022 21:20:39 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 05 Dec 2022 21:20:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:20:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2c44f983a875883421e7d5bc471f6437e0e377e6e7343b52c856caee71064d31`  
		Last Modified: Tue, 09 Aug 2022 17:40:01 GMT  
		Size: 2.8 MB (2832612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60188e223488b3b7af54fdbf828fa4aea3fb1b6d700666a3faa889acae098125`  
		Last Modified: Mon, 05 Dec 2022 21:21:50 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6108b505bd66a0dce2c8614c6a9380a952402c0247ceceb3cb5b11a50d02689`  
		Last Modified: Mon, 05 Dec 2022 21:21:58 GMT  
		Size: 79.6 MB (79555865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3474c7b02ac7ae48d793010aaf1b898c36c6f85c109afbb31e424919b1d08`  
		Last Modified: Mon, 05 Dec 2022 21:21:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df3ca5f05ead293bf171cedb94dc70d5c1af02813b181bf102384a6508e64c3`  
		Last Modified: Mon, 05 Dec 2022 21:21:50 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
