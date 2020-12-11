<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.6`](#consul16)
-	[`consul:1.6.10`](#consul1610)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.10`](#consul1710)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.6`](#consul186)
-	[`consul:1.8.7-beta1`](#consul187-beta1)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.0`](#consul190)
-	[`consul:latest`](#consullatest)

## `consul:1.6`

```console
$ docker pull consul@sha256:9a9510d58a643135f17d97d5ae172a13197ebc95ba577edfe672fbc2adfb39c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6` - linux; amd64

```console
$ docker pull consul@sha256:dd84a400239d14d8f1778a2a2a8cacb129382c1527afb6be972eaff722d3ca5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44791257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54a78fa9cfb1418f1991fdf3c70b3d43538183d39fb205fad04a48c8dbb2fe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:56:33 GMT
ENV CONSUL_VERSION=1.6.10
# Fri, 11 Dec 2020 02:56:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:56:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:45 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:45 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637e1a6d2f2eb8b86a1165b06157992ac04f4f487e63929224ba58831d2f1389`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81380126608683d3f3e322217e25bf30a385a0d65377739de011d33578bb05c5`  
		Last Modified: Fri, 11 Dec 2020 02:58:18 GMT  
		Size: 42.0 MB (41991077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6e3a4d48893837760d565dec5302d5439662035f273c6747f288936b81544`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301a486e7cfbb4be1077de6adb467923208f0ee9ac3118e19b0cead9103d2a3`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b0368ea3a8ac9d3a3bca026da11b96f9ec8ce28a1cbd81aaa14606b42f4681`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:3d16e27dbd80e122713a7abb4c4ce7976d1ee5faeddc99316825321a71474372
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40611108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ccd5a279004be4fa388a1bcdf8b8365539a30fd602a40808c19e6ef82ed596`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:52:01 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:52:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:52:03 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:52:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:52:15 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:52:16 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:52:17 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:52:18 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:52:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:52:19 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:52:19 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:52:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e8387711c42f9833a0f6a8486c3a9ef2a636f01c2f4e6d2500f65ef497447`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba1a8d686c527655780d0b9d1f43030f3c83c6124ece9a4f2a2a9eab8efc254`  
		Last Modified: Sat, 21 Nov 2020 01:53:24 GMT  
		Size: 38.0 MB (38005904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a39f5f1ad9553f69b60b8e6838c3641a964a21ff4782bea731d9bb45cfe93c`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45d38492c8e656be41694bbeca2a3bcd60fbe80646b79e8fed479bbb5a7739`  
		Last Modified: Sat, 21 Nov 2020 01:53:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d52ddce60c01097cae445608b13b8ec019745ebc22b412c61bcae9da6381137`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:92061681bb594e70c9f91cf874d27c062445462566a97a64fe345565677006c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41048179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cddec463dccfcedd8418401c1f042740d2d1778895c0af7f70447f16991bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:41:09 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:41:17 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:41:20 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:41:21 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:41:22 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:41:23 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:41:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:41:25 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:41:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:41:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:41:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40208d4b1481cbea89e5048238270fe3b31233bdeebbd2976eabba81c4d20f8`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59480e92a014ac01fde03bf2469707d9e8499240b02983a89c8844252c516a`  
		Last Modified: Sat, 21 Nov 2020 01:42:25 GMT  
		Size: 38.3 MB (38338330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492f92778006e76a49f48043533c669db7000681b547857219d882fbb70cdf2a`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427fa4101529169daa91c0e54cf89eec60cff8b9a0641d6f27326908bfad83b`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ee59295b508b3ed6f278fa14f5aa99fa7c8e485e2148618abb969b88072a`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; 386

```console
$ docker pull consul@sha256:4e0f5cacbf900e90e3aab47c6dd8f07d057a792e7f45aae0236f27d2fbb33ab4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43952807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044965116ab4acbbd2bf8bfc28c6b639f9481aad24c9de88722e24bbd3b75b35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:39:11 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:39:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:39:12 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:39:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:39:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:39:20 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:39:20 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:39:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:39:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073955cd82a1400897e9e8c0f871d7b3382f2bd068abd5e4523ff14758e2e908`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c3020e8d98304dd9177e08ba742685d53a076f9807fd4ef84a1f3109abaf2e`  
		Last Modified: Sat, 21 Nov 2020 01:40:14 GMT  
		Size: 41.2 MB (41158168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e881d4d393cffbf1679126019e5c1dabe5ed7875a78005f7b2570cce62c46ae`  
		Last Modified: Sat, 21 Nov 2020 01:40:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b2209f9062b82406066a16ac9005018f448a0c1bc06f426c031f864b05ebd`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b2426aa309c8071a39df0069984a071114bb3777032933745d60603f0a5fea`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.6.10`

```console
$ docker pull consul@sha256:9a9510d58a643135f17d97d5ae172a13197ebc95ba577edfe672fbc2adfb39c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6.10` - linux; amd64

```console
$ docker pull consul@sha256:dd84a400239d14d8f1778a2a2a8cacb129382c1527afb6be972eaff722d3ca5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44791257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54a78fa9cfb1418f1991fdf3c70b3d43538183d39fb205fad04a48c8dbb2fe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:56:33 GMT
ENV CONSUL_VERSION=1.6.10
# Fri, 11 Dec 2020 02:56:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:56:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:45 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:45 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637e1a6d2f2eb8b86a1165b06157992ac04f4f487e63929224ba58831d2f1389`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81380126608683d3f3e322217e25bf30a385a0d65377739de011d33578bb05c5`  
		Last Modified: Fri, 11 Dec 2020 02:58:18 GMT  
		Size: 42.0 MB (41991077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6e3a4d48893837760d565dec5302d5439662035f273c6747f288936b81544`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301a486e7cfbb4be1077de6adb467923208f0ee9ac3118e19b0cead9103d2a3`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b0368ea3a8ac9d3a3bca026da11b96f9ec8ce28a1cbd81aaa14606b42f4681`  
		Last Modified: Fri, 11 Dec 2020 02:58:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:3d16e27dbd80e122713a7abb4c4ce7976d1ee5faeddc99316825321a71474372
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40611108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ccd5a279004be4fa388a1bcdf8b8365539a30fd602a40808c19e6ef82ed596`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:52:01 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:52:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:52:03 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:52:13 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:52:15 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:52:16 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:52:17 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:52:18 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:52:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:52:19 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:52:19 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:52:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e8387711c42f9833a0f6a8486c3a9ef2a636f01c2f4e6d2500f65ef497447`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba1a8d686c527655780d0b9d1f43030f3c83c6124ece9a4f2a2a9eab8efc254`  
		Last Modified: Sat, 21 Nov 2020 01:53:24 GMT  
		Size: 38.0 MB (38005904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a39f5f1ad9553f69b60b8e6838c3641a964a21ff4782bea731d9bb45cfe93c`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45d38492c8e656be41694bbeca2a3bcd60fbe80646b79e8fed479bbb5a7739`  
		Last Modified: Sat, 21 Nov 2020 01:53:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d52ddce60c01097cae445608b13b8ec019745ebc22b412c61bcae9da6381137`  
		Last Modified: Sat, 21 Nov 2020 01:53:14 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:92061681bb594e70c9f91cf874d27c062445462566a97a64fe345565677006c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41048179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845cddec463dccfcedd8418401c1f042740d2d1778895c0af7f70447f16991bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:41:09 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:41:17 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:41:20 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:41:21 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:41:22 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:41:23 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:41:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:41:25 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:41:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:41:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:41:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40208d4b1481cbea89e5048238270fe3b31233bdeebbd2976eabba81c4d20f8`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59480e92a014ac01fde03bf2469707d9e8499240b02983a89c8844252c516a`  
		Last Modified: Sat, 21 Nov 2020 01:42:25 GMT  
		Size: 38.3 MB (38338330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492f92778006e76a49f48043533c669db7000681b547857219d882fbb70cdf2a`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427fa4101529169daa91c0e54cf89eec60cff8b9a0641d6f27326908bfad83b`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e5ee59295b508b3ed6f278fa14f5aa99fa7c8e485e2148618abb969b88072a`  
		Last Modified: Sat, 21 Nov 2020 01:42:16 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.10` - linux; 386

```console
$ docker pull consul@sha256:4e0f5cacbf900e90e3aab47c6dd8f07d057a792e7f45aae0236f27d2fbb33ab4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43952807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044965116ab4acbbd2bf8bfc28c6b639f9481aad24c9de88722e24bbd3b75b35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:39:11 GMT
ENV CONSUL_VERSION=1.6.10
# Sat, 21 Nov 2020 01:39:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:39:12 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:39:19 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     apk -X https://dl-cdn.alpinelinux.org/alpine/v3.8/main add tzdata=2020a-r0 &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:39:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:39:20 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:39:20 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:39:21 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:39:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:39:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073955cd82a1400897e9e8c0f871d7b3382f2bd068abd5e4523ff14758e2e908`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c3020e8d98304dd9177e08ba742685d53a076f9807fd4ef84a1f3109abaf2e`  
		Last Modified: Sat, 21 Nov 2020 01:40:14 GMT  
		Size: 41.2 MB (41158168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e881d4d393cffbf1679126019e5c1dabe5ed7875a78005f7b2570cce62c46ae`  
		Last Modified: Sat, 21 Nov 2020 01:40:04 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b2209f9062b82406066a16ac9005018f448a0c1bc06f426c031f864b05ebd`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b2426aa309c8071a39df0069984a071114bb3777032933745d60603f0a5fea`  
		Last Modified: Sat, 21 Nov 2020 01:40:05 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:40d5f0bb70e95769faa92dcca3515417af9b9948ecf4d31d19cc459438e2a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:bc16b5304bdcc40a3cea9f6c106363434717586467744d1ce78b2e63a1e5dc6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bd34dbc3c3f1f7f4b43cd12ed01b4015baa93ac1392d2b07a12689c6254721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:56:13 GMT
ENV CONSUL_VERSION=1.7.10
# Fri, 11 Dec 2020 02:56:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:56:15 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:22 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:24 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:25 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:25 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574c36a12202c0f0e34f4b8bf84ddde9f9a0924c19895a461058527f3a0a2cdd`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0855f7e506d7ddff6882d7974e8eb68c3505d7c723ad5698323743bd64fcd902`  
		Last Modified: Fri, 11 Dec 2020 02:58:04 GMT  
		Size: 40.3 MB (40293661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1238aa95aaba6e5cdc6775497bf004a2e4228df6c8da4e7b2bfa7ef9c4f794`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b6c78cc972e1067d1fd8489942639d41f191f3905fc0ce3a2e7130aac3d1be`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02172411f977cfe47523404a06fd5b7b3d3cda3780e621ca6740a4431d8e236`  
		Last Modified: Fri, 11 Dec 2020 02:57:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:9898e52e14bff1b3253c7c2e55f5d96c0b811996d660b95c9bbbe17c3924e5b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39188612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd65b663c29d650428766e072216c95f4bd8175f4d84dac1b503cc28b136f26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:51:34 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:51:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:51:37 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:51:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:51:47 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:51:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:51:50 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:51:50 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:51:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:51:52 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:51:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:51:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1a095f2c01406b324aecee6ea15b9382a7f9d3911742cc95943b482697b9cd`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c1d8fd42c534d53d881613da0bb84d8c43286324887e006b1b7546ac962b65`  
		Last Modified: Sat, 21 Nov 2020 01:53:06 GMT  
		Size: 36.6 MB (36583407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9a2173853dd15d974475841118cbd7e2b13753d79b5c5b2594bfbef4214a5f`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c92bac46c11832762dc2ff097f7722ebd2214322f1f27e7145ac1b5368c2a2`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99776bd6406ac1737981c6af30b75ae07dc17d3d0ba2486fb5d2400f6fedebe7`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:18e46ed1d4d6cbecfca7efbb99a6004d251e53ad1fd3b09ef568c78092aaa232
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39412443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b7ea4c4a47d0867cdbb6f9f6345ba9d98569bc13744b5a414d38f17419cff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:40:35 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:40:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:40:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:40:47 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:40:50 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:40:52 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:40:52 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:40:53 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:40:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:40:54 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:40:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:40:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:40:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ca11a9c4f0e01c15269e1a922b3e85cace4c6a4e8012fe46d991c3b631543b`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0deadfb700fc32b539eb184f000ab8428f2e3949738e1395648a45ab6b322a2`  
		Last Modified: Sat, 21 Nov 2020 01:42:08 GMT  
		Size: 36.7 MB (36702593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be84067000b0818bb382343e10626a5a994433c7709d998bfd0fd4f72899e175`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515b9e6d5bca0056bbc4fa69d34ec0bf6e33aa2b86357cc377bda959870c449`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c666cac88ee672bc0f44329987bf2a1bc19238d7c54b4e2bd428726f9bff8cd0`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:9060331ac68bc5b49ca118d89b3de037f26d930318384931d8ddae9fdac3689a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42273476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5388bbbe3074d5368f55e8be06633a0207adc15d8b1ed956b25f4932e74d47d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:38:55 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:38:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:38:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:39:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:39:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:39:05 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:39:05 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:39:05 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:39:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:39:06 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:39:06 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:39:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:39:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad9d9e88674a9ee11182151110497f18d229130a39fa8c6afa877d3f68d7211`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c3807ca6a52a3d92cceb7f8c1c3ecd3a0e3bebfcf603fc0e1f18ab493350b3`  
		Last Modified: Sat, 21 Nov 2020 01:40:00 GMT  
		Size: 39.5 MB (39478832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f655fb0d3f657436baef11ac6955a8e4d91c3f95bc563042c8e3ee4a83dca2f`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8581f6b37196be59e34bc65d25f14344d505b62347fd78de5598bffac35f0c0`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b6f208b77ae07b8b434483ec34c407e10c1b89b132f816cae1a8d498c9fb92`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.10`

```console
$ docker pull consul@sha256:40d5f0bb70e95769faa92dcca3515417af9b9948ecf4d31d19cc459438e2a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.10` - linux; amd64

```console
$ docker pull consul@sha256:bc16b5304bdcc40a3cea9f6c106363434717586467744d1ce78b2e63a1e5dc6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bd34dbc3c3f1f7f4b43cd12ed01b4015baa93ac1392d2b07a12689c6254721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:56:13 GMT
ENV CONSUL_VERSION=1.7.10
# Fri, 11 Dec 2020 02:56:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:56:15 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:22 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:24 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:25 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:25 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574c36a12202c0f0e34f4b8bf84ddde9f9a0924c19895a461058527f3a0a2cdd`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0855f7e506d7ddff6882d7974e8eb68c3505d7c723ad5698323743bd64fcd902`  
		Last Modified: Fri, 11 Dec 2020 02:58:04 GMT  
		Size: 40.3 MB (40293661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1238aa95aaba6e5cdc6775497bf004a2e4228df6c8da4e7b2bfa7ef9c4f794`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b6c78cc972e1067d1fd8489942639d41f191f3905fc0ce3a2e7130aac3d1be`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02172411f977cfe47523404a06fd5b7b3d3cda3780e621ca6740a4431d8e236`  
		Last Modified: Fri, 11 Dec 2020 02:57:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:9898e52e14bff1b3253c7c2e55f5d96c0b811996d660b95c9bbbe17c3924e5b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39188612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd65b663c29d650428766e072216c95f4bd8175f4d84dac1b503cc28b136f26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:51:34 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:51:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:51:37 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:51:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:51:47 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:51:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:51:50 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:51:50 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:51:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:51:52 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:51:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:51:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1a095f2c01406b324aecee6ea15b9382a7f9d3911742cc95943b482697b9cd`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c1d8fd42c534d53d881613da0bb84d8c43286324887e006b1b7546ac962b65`  
		Last Modified: Sat, 21 Nov 2020 01:53:06 GMT  
		Size: 36.6 MB (36583407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9a2173853dd15d974475841118cbd7e2b13753d79b5c5b2594bfbef4214a5f`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c92bac46c11832762dc2ff097f7722ebd2214322f1f27e7145ac1b5368c2a2`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99776bd6406ac1737981c6af30b75ae07dc17d3d0ba2486fb5d2400f6fedebe7`  
		Last Modified: Sat, 21 Nov 2020 01:52:56 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:18e46ed1d4d6cbecfca7efbb99a6004d251e53ad1fd3b09ef568c78092aaa232
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39412443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b7ea4c4a47d0867cdbb6f9f6345ba9d98569bc13744b5a414d38f17419cff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:40:35 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:40:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:40:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:40:47 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:40:50 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:40:52 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:40:52 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:40:53 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:40:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:40:54 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:40:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:40:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:40:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ca11a9c4f0e01c15269e1a922b3e85cace4c6a4e8012fe46d991c3b631543b`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0deadfb700fc32b539eb184f000ab8428f2e3949738e1395648a45ab6b322a2`  
		Last Modified: Sat, 21 Nov 2020 01:42:08 GMT  
		Size: 36.7 MB (36702593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be84067000b0818bb382343e10626a5a994433c7709d998bfd0fd4f72899e175`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515b9e6d5bca0056bbc4fa69d34ec0bf6e33aa2b86357cc377bda959870c449`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c666cac88ee672bc0f44329987bf2a1bc19238d7c54b4e2bd428726f9bff8cd0`  
		Last Modified: Sat, 21 Nov 2020 01:41:59 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.10` - linux; 386

```console
$ docker pull consul@sha256:9060331ac68bc5b49ca118d89b3de037f26d930318384931d8ddae9fdac3689a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42273476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5388bbbe3074d5368f55e8be06633a0207adc15d8b1ed956b25f4932e74d47d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:38:55 GMT
ENV CONSUL_VERSION=1.7.10
# Sat, 21 Nov 2020 01:38:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:38:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:39:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:39:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:39:05 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:39:05 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:39:05 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:39:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:39:06 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:39:06 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:39:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:39:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad9d9e88674a9ee11182151110497f18d229130a39fa8c6afa877d3f68d7211`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c3807ca6a52a3d92cceb7f8c1c3ecd3a0e3bebfcf603fc0e1f18ab493350b3`  
		Last Modified: Sat, 21 Nov 2020 01:40:00 GMT  
		Size: 39.5 MB (39478832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f655fb0d3f657436baef11ac6955a8e4d91c3f95bc563042c8e3ee4a83dca2f`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8581f6b37196be59e34bc65d25f14344d505b62347fd78de5598bffac35f0c0`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b6f208b77ae07b8b434483ec34c407e10c1b89b132f816cae1a8d498c9fb92`  
		Last Modified: Sat, 21 Nov 2020 01:39:49 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:23bd83aece84cdd9e2d9f3ab63303f94bcea004f3c6add4f8d881dd2db50a51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:3efabf42b246dae092b236df440d95b25cc79f08941128653fbb490d8068f779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46461787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36094c09e82962f378f08056864385d0ac1a28ef278b9050423de34b6bd2d07d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:54 GMT
ENV CONSUL_VERSION=1.8.6
# Fri, 11 Dec 2020 02:55:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:06 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:06 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe56e704066b43589bb857c9465831a2c34bbbef933b423569c4afe1f8511e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:37 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854da3823fa235c4710a7558b08efd96290dd80cf0c0252c3100b83f264dfc5`  
		Last Modified: Fri, 11 Dec 2020 02:57:47 GMT  
		Size: 43.7 MB (43661611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b68bd84e508f434ab57fdd39663b88c3e9541e86b01051eb13f41e02049edaa`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8494b9fb8d1cc1a0ce36ca17d71f50be0eeb0a299ac3fa836fc54beb2a75e4d`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cce9eef4f2ebc00b962a237fa3e9451a52b28d2d744e48f2ee9d751b4c8d2f0`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:30ce10937e1d673c8242958397d168a6d9a71ee2e3488b2fbca16af75338c706
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee4d822f21c5fb9c35b91eaeeea482f8cbf9ed84ca90b5e35989edff35fbb10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:51:02 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:51:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:51:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:51:17 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:51:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:51:22 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:51:22 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:51:23 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:51:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:51:24 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:51:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:51:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384109437fd92f8b9265dc381f1089c20ca2603e336a675d7bd58e3191eafd16`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae8e56ff7b1d183cb864e12d05ddb1e77df7af34e361a4185315c3c85922a5`  
		Last Modified: Sat, 21 Nov 2020 01:52:47 GMT  
		Size: 39.5 MB (39500891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef12435db2335bf36731672017bb9572a1265b3a52ed5827922df4c311962933`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509c3fd0fd13c7db56f4ad43051efc5b427090edd08ce26c6e2d1213dae3a1bd`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a1bdd705ca3038315b24920dfca3ced76e40c66bea8a70a8b84c6e11777f7f`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:060e41ee571dc8c701f386868dd7b7fc2dc3105e62f83966815608a43bbf9e3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42279876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53eface40401e9c8fcfb315dd1b0a5d964592eac19ad1c0bef0d2919f1cb6a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:40:04 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:40:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:40:07 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:40:14 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:40:16 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:40:19 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:40:19 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:40:20 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:40:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:40:22 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:40:22 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:40:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f31e847d124c01a2f9c8776d3fc597739c8f02f7d18e1f16b476a0cb491e4`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e829303c21b36a12039c446b8aef07c347401504e6d94c8c8af00f4111eff`  
		Last Modified: Sat, 21 Nov 2020 01:41:50 GMT  
		Size: 39.6 MB (39570023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceaca592f0142a3cca6fa64bd59e9fe13a8aa84e3c73be6d6316ee81eae2b58`  
		Last Modified: Sat, 21 Nov 2020 01:41:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703f0c7f3af2a729d9c92c7a9cffdc2b0cb3a7399ed0b51febcdc28ae6c5c828`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7965b226005be1e899999da5778b410df38621c8ca1d1cffa1033539d9f9ba4`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:84ae85b48c8d01fce5cc0e9a6e90e9f8afcf43489c397a86af1094e1edcbb979
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46352079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138cc84a33f3f503a4f09b51b0c3e2ed7fe7f7d6fb2a0a76dc1aed4a30c4c2e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:38:31 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:38:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:38:33 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:38:41 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:38:42 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:38:44 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:38:44 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:38:44 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:38:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:38:45 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:38:45 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:38:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f7ea6bb49fcd83fa1e2532a46fa73673811b4f190eabbeac27b70126e99483`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f5b10ad85a8ca78f92681700a4adf4286665337db08649aade4832e289c1b1`  
		Last Modified: Sat, 21 Nov 2020 01:39:42 GMT  
		Size: 43.6 MB (43557436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc233fbc0a691dfc0d0d6632924d73a80241aace4095d2562084aada2f889003`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b2f813151022af8a8d729fd038d6d97deeb7edf8cda7cd53b6d584074f09d`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fb85334aeb38ba47abe71d6bafa659b496f04bb6b2195305ef4dcafbe7929e`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.6`

```console
$ docker pull consul@sha256:23bd83aece84cdd9e2d9f3ab63303f94bcea004f3c6add4f8d881dd2db50a51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.6` - linux; amd64

```console
$ docker pull consul@sha256:3efabf42b246dae092b236df440d95b25cc79f08941128653fbb490d8068f779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46461787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36094c09e82962f378f08056864385d0ac1a28ef278b9050423de34b6bd2d07d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:54 GMT
ENV CONSUL_VERSION=1.8.6
# Fri, 11 Dec 2020 02:55:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:06 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:06 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe56e704066b43589bb857c9465831a2c34bbbef933b423569c4afe1f8511e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:37 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854da3823fa235c4710a7558b08efd96290dd80cf0c0252c3100b83f264dfc5`  
		Last Modified: Fri, 11 Dec 2020 02:57:47 GMT  
		Size: 43.7 MB (43661611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b68bd84e508f434ab57fdd39663b88c3e9541e86b01051eb13f41e02049edaa`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8494b9fb8d1cc1a0ce36ca17d71f50be0eeb0a299ac3fa836fc54beb2a75e4d`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cce9eef4f2ebc00b962a237fa3e9451a52b28d2d744e48f2ee9d751b4c8d2f0`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:30ce10937e1d673c8242958397d168a6d9a71ee2e3488b2fbca16af75338c706
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42106096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee4d822f21c5fb9c35b91eaeeea482f8cbf9ed84ca90b5e35989edff35fbb10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:51:02 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:51:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:51:05 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:51:17 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:51:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:51:22 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:51:22 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:51:23 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:51:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:51:24 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:51:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:51:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384109437fd92f8b9265dc381f1089c20ca2603e336a675d7bd58e3191eafd16`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae8e56ff7b1d183cb864e12d05ddb1e77df7af34e361a4185315c3c85922a5`  
		Last Modified: Sat, 21 Nov 2020 01:52:47 GMT  
		Size: 39.5 MB (39500891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef12435db2335bf36731672017bb9572a1265b3a52ed5827922df4c311962933`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509c3fd0fd13c7db56f4ad43051efc5b427090edd08ce26c6e2d1213dae3a1bd`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a1bdd705ca3038315b24920dfca3ced76e40c66bea8a70a8b84c6e11777f7f`  
		Last Modified: Sat, 21 Nov 2020 01:52:36 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:060e41ee571dc8c701f386868dd7b7fc2dc3105e62f83966815608a43bbf9e3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42279876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53eface40401e9c8fcfb315dd1b0a5d964592eac19ad1c0bef0d2919f1cb6a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:40:04 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:40:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:40:07 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:40:14 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:40:16 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:40:19 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:40:19 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:40:20 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:40:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:40:22 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:40:22 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:40:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f31e847d124c01a2f9c8776d3fc597739c8f02f7d18e1f16b476a0cb491e4`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e829303c21b36a12039c446b8aef07c347401504e6d94c8c8af00f4111eff`  
		Last Modified: Sat, 21 Nov 2020 01:41:50 GMT  
		Size: 39.6 MB (39570023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceaca592f0142a3cca6fa64bd59e9fe13a8aa84e3c73be6d6316ee81eae2b58`  
		Last Modified: Sat, 21 Nov 2020 01:41:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703f0c7f3af2a729d9c92c7a9cffdc2b0cb3a7399ed0b51febcdc28ae6c5c828`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7965b226005be1e899999da5778b410df38621c8ca1d1cffa1033539d9f9ba4`  
		Last Modified: Sat, 21 Nov 2020 01:41:41 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.6` - linux; 386

```console
$ docker pull consul@sha256:84ae85b48c8d01fce5cc0e9a6e90e9f8afcf43489c397a86af1094e1edcbb979
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46352079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138cc84a33f3f503a4f09b51b0c3e2ed7fe7f7d6fb2a0a76dc1aed4a30c4c2e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 21 Nov 2020 01:38:31 GMT
ENV CONSUL_VERSION=1.8.6
# Sat, 21 Nov 2020 01:38:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 21 Nov 2020 01:38:33 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 21 Nov 2020 01:38:41 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 21 Nov 2020 01:38:42 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 21 Nov 2020 01:38:44 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 21 Nov 2020 01:38:44 GMT
VOLUME [/consul/data]
# Sat, 21 Nov 2020 01:38:44 GMT
EXPOSE 8300
# Sat, 21 Nov 2020 01:38:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 21 Nov 2020 01:38:45 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 21 Nov 2020 01:38:45 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 21 Nov 2020 01:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Nov 2020 01:38:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f7ea6bb49fcd83fa1e2532a46fa73673811b4f190eabbeac27b70126e99483`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f5b10ad85a8ca78f92681700a4adf4286665337db08649aade4832e289c1b1`  
		Last Modified: Sat, 21 Nov 2020 01:39:42 GMT  
		Size: 43.6 MB (43557436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc233fbc0a691dfc0d0d6632924d73a80241aace4095d2562084aada2f889003`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b2f813151022af8a8d729fd038d6d97deeb7edf8cda7cd53b6d584074f09d`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fb85334aeb38ba47abe71d6bafa659b496f04bb6b2195305ef4dcafbe7929e`  
		Last Modified: Sat, 21 Nov 2020 01:39:33 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.7-beta1`

```console
$ docker pull consul@sha256:526037d98007e2b98bdba56a87249d8bf08773f855f50626acee2e8b28f5696b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.7-beta1` - linux; amd64

```console
$ docker pull consul@sha256:452254bbabf95081f81104cbff556ad545f1d3cc92035975b04f7fb2e38d2dcc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46491832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f951f2e924c9281ed7a899fade78dabdf91f67af08b5927059f2a6a1dbb9a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:34 GMT
ENV CONSUL_VERSION=1.8.7-beta1
# Fri, 11 Dec 2020 02:55:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:36 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:43 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:44 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:45 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:46 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:46 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a66b9ce7b221ab146c84eb25a277e06a0826b99714e7eeb6ca8c40b6b66a787`  
		Last Modified: Fri, 11 Dec 2020 02:57:24 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cea40e081f3be1faad62cc0af4827326a61331123e121af23383402571e7e9`  
		Last Modified: Fri, 11 Dec 2020 02:57:33 GMT  
		Size: 43.7 MB (43691656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9334338c9897f03737e2af9b77f01c9cf2ac2a502bdd374bdd680bb5b1bcac6`  
		Last Modified: Fri, 11 Dec 2020 02:57:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd80cf0e6584242464edce17d4d1bd4ec3440846670e94ae28b71d548e775026`  
		Last Modified: Fri, 11 Dec 2020 02:57:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69d15a5375864740337be4930e5922f7bf471c0705072381e4664bab65be81`  
		Last Modified: Fri, 11 Dec 2020 02:57:24 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.7-beta1` - linux; arm variant v6

```console
$ docker pull consul@sha256:53acab5be27216440950ea9ed5eb1fdce24cbbeb5aac28d413d27bdc79614556
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42130774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68652134df5e03238beaec69340628583150ba485b9b43c8a71bcdc836a13e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 03 Dec 2020 22:49:38 GMT
ENV CONSUL_VERSION=1.8.7-beta1
# Thu, 03 Dec 2020 22:49:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 03 Dec 2020 22:49:45 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 03 Dec 2020 22:50:01 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 03 Dec 2020 22:50:09 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 03 Dec 2020 22:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 22:50:15 GMT
VOLUME [/consul/data]
# Thu, 03 Dec 2020 22:50:18 GMT
EXPOSE 8300
# Thu, 03 Dec 2020 22:50:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 03 Dec 2020 22:50:22 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 03 Dec 2020 22:50:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Dec 2020 22:50:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 22:50:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ad73776acb8117f96b85eec6ba7d79a67852d6e038fd3b2fc414c8d96b986`  
		Last Modified: Thu, 03 Dec 2020 22:51:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7996ebad063ca07f856926bf56b3be667ebd7adfc519189e6a9f67d752893815`  
		Last Modified: Thu, 03 Dec 2020 22:51:15 GMT  
		Size: 39.5 MB (39525562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf5aef8fb29e0b2c6b0485be1e03002fee1be37d8ba566c833f3a963690c6f`  
		Last Modified: Thu, 03 Dec 2020 22:51:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7058ecc910e3318853fb2d17748a889e7be558f041963c7052f2568837dfbff7`  
		Last Modified: Thu, 03 Dec 2020 22:51:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e90e978faf17eb373710e8ccc9801cd78ed8a7cca20d0a67f3221599643e1f`  
		Last Modified: Thu, 03 Dec 2020 22:51:05 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.7-beta1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:34039eb6bc56bfa3207f6f823fcb0ca27cc89ee7d93d1e22e8570c64aa16c748
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42312288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2fc0385621aabf98e534f56f22791e0fb118d0a980a86deaa5b41de45946c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 03 Dec 2020 22:42:04 GMT
ENV CONSUL_VERSION=1.8.7-beta1
# Thu, 03 Dec 2020 22:42:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 03 Dec 2020 22:42:08 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 03 Dec 2020 22:42:16 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 03 Dec 2020 22:42:19 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 03 Dec 2020 22:42:21 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 22:42:22 GMT
VOLUME [/consul/data]
# Thu, 03 Dec 2020 22:42:23 GMT
EXPOSE 8300
# Thu, 03 Dec 2020 22:42:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 03 Dec 2020 22:42:25 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 03 Dec 2020 22:42:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Dec 2020 22:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 22:42:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9831733a3f741354196c5866b9bcd0885ddd8df06d362cbff3c14ce7db0e4f`  
		Last Modified: Thu, 03 Dec 2020 22:42:57 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe5349a66faef15ed47d4020edbfcba721cce1ec6795fe8903646d5599247a`  
		Last Modified: Thu, 03 Dec 2020 22:43:07 GMT  
		Size: 39.6 MB (39602434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d9d55c1688d28eafda3b62d04da7d3c680b48e16d1a3318141aaef8c46a155`  
		Last Modified: Thu, 03 Dec 2020 22:42:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b797e88d8c0b6ef2c1b36021ac6fe6d157b830133897ea62f20403de6912b`  
		Last Modified: Thu, 03 Dec 2020 22:42:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f3830a7f7bba57a94849267694747addbf210895a057afdf3dc2fb2b79e3cd`  
		Last Modified: Thu, 03 Dec 2020 22:42:57 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.7-beta1` - linux; 386

```console
$ docker pull consul@sha256:430eb1c9a4629c9df39cc4e11b03cdd4621435054416b7ffc97d246479cc730f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46375562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dee82c387312983169c74fcb38bc412cb73a5f6ec48e58a5644568a9570c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 03 Dec 2020 22:40:05 GMT
ENV CONSUL_VERSION=1.8.7-beta1
# Thu, 03 Dec 2020 22:40:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 03 Dec 2020 22:40:06 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 03 Dec 2020 22:40:12 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 03 Dec 2020 22:40:13 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 03 Dec 2020 22:40:14 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 22:40:14 GMT
VOLUME [/consul/data]
# Thu, 03 Dec 2020 22:40:14 GMT
EXPOSE 8300
# Thu, 03 Dec 2020 22:40:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 03 Dec 2020 22:40:14 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 03 Dec 2020 22:40:15 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 03 Dec 2020 22:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 22:40:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da464d16ffb961dc677b6a098d9b882abdf5e13fc48e2eb7328b0613fffcdb`  
		Last Modified: Thu, 03 Dec 2020 22:40:40 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542fe049b69d9d812b17c8f5fabf2a54e9d238ba8082e93f9a25d96a7c675cde`  
		Last Modified: Thu, 03 Dec 2020 22:40:48 GMT  
		Size: 43.6 MB (43580920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7918d136acf07af5f2dd94795f491dba2e90c52c6a23c05a1082bab54fd25863`  
		Last Modified: Thu, 03 Dec 2020 22:40:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8bf6b229e96c0f834f0fd4135d5e3755f79dad031a8150f7e79f7fe76b6963`  
		Last Modified: Thu, 03 Dec 2020 22:40:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d6b49718a62a616e193eb296177e636a6fd9d0c6aca0972283fc440478632a`  
		Last Modified: Thu, 03 Dec 2020 22:40:40 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:3fe008a8686bf95664e6f18cc18be0f4e9a235dc3edfed6f04f61c0eb0054be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:3aeb5ab2d0fa9189ed99692f8cce218d1c5eb591255ac38c389b680aad3bd5bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8429e82f47dd20c7833966453d571fc43ece763fa5cadec460390351f99d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:15 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 02:55:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:24 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:28 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc5b4d599656ad90b0d9809894af2414f9ffadb68145140f4038ecac2eb174`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ae847c23d3422b795a3bdf170616176238924d44bb8b99503f34b86222246`  
		Last Modified: Fri, 11 Dec 2020 02:57:17 GMT  
		Size: 42.7 MB (42720248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f01f506e7a1412784c106cd451bf530c4e2fa89b82da5494eb7fcee179ee04`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54d30ff31eeef79e6a8ecf14d92c4324b82f4be1176b8a22b89172bdbb1e535`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0811e7d6f99e0f9f0104dbcbb3682d6b9da402b2d9993c9ba173c6c014904e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:45629f4f5ed311f73724880098846df68977ea44bfb74197cfb6b40666e1e87a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41177693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a659f752b75b6bf5c28cdf21067ce3e1e53f2fc457a6181331e89cfe7748928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:49:37 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:49:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:49:45 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:50:04 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:50:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:50:15 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:50:17 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:50:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:50:19 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:50:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:50:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:50:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541d1797ef1170490288147b99ee5d41a948a7f4e79f641fafc5f6fed3d80b38`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412943d31f925789bbd6d15ce0453a3b619149b5ab000b93ddf626356ca6e8b5`  
		Last Modified: Wed, 25 Nov 2020 00:51:18 GMT  
		Size: 38.6 MB (38572484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03138968c5fe96a538b0bf6df3091212fd588bcf78dbeb51b3c4dc8d044cfb66`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691e110ed2b0a550bf4acbc2e4d169923f3fec45f1fd7020ec1ec81d1fd4fd36`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af8e92dfceb088c9546e2566415d438f1874b57b0ed365044b1a67d27bae92`  
		Last Modified: Wed, 25 Nov 2020 00:51:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1012b86c1b4f0c40be0449c239cdd6f1adfbf34ce7a6ccf5903245f890ff677d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41394856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6a768f504e8509835bc02fa5a484eba01a4389908306659d0829492078a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:39:32 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:39:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:39:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:39:43 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:39:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:39:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:39:50 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:39:50 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:39:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:39:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:39:53 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:39:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4785ac6d608aceb5c11acbff79d38f8310fe7ea952dbc1fe0f16ee4157bb7fb`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda07bb163802553eb787a581765163466d5b9d9fcdf8079b1f9a15d30a000ed`  
		Last Modified: Wed, 25 Nov 2020 00:40:35 GMT  
		Size: 38.7 MB (38685008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbadd110c842ac687b4e011516cbb85cb5351ed410ffc7d9ce8e29d6a81b980a`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fc41f7bedc3f964514a77a849e654c872f9a7ff56dedee9354f0931c41552`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b79696f40f83b31ed9b8fa30c52dc07c56f018ae83b8e705fae062b94b651`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:3ad6148e3cdb242420b209f4d1fe73da7c23f2c78598dbb3df16f6538d5a013a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45231403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addffb46e74179410991b94d4784f09f5e804e3345dea67754c93b743b861fbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:38:31 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:38:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:38:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:38:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:38:39 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:38:40 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:38:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:38:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b670227cf5b0369dec1890afd49daa761d5219f770e6e1717eeb94aa0d30d795`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886f4ead96bdf58722ac9a1bb62e065252db84d364caac2f2f162484607b9679`  
		Last Modified: Wed, 25 Nov 2020 00:39:12 GMT  
		Size: 42.4 MB (42436764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9099eaffdcf30a6fc42310fad858f1210dc9a72b912f3867f84114f14283e4b1`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60de6fed51016b0bc661d53792674a602f12405b5ee4fa32ff4760a2c97fd0a`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1722523c085b312cc345217410e18206bcf15369b2bb5c423315508580a7e0`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.0`

```console
$ docker pull consul@sha256:3fe008a8686bf95664e6f18cc18be0f4e9a235dc3edfed6f04f61c0eb0054be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.0` - linux; amd64

```console
$ docker pull consul@sha256:3aeb5ab2d0fa9189ed99692f8cce218d1c5eb591255ac38c389b680aad3bd5bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8429e82f47dd20c7833966453d571fc43ece763fa5cadec460390351f99d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:15 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 02:55:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:24 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:28 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc5b4d599656ad90b0d9809894af2414f9ffadb68145140f4038ecac2eb174`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ae847c23d3422b795a3bdf170616176238924d44bb8b99503f34b86222246`  
		Last Modified: Fri, 11 Dec 2020 02:57:17 GMT  
		Size: 42.7 MB (42720248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f01f506e7a1412784c106cd451bf530c4e2fa89b82da5494eb7fcee179ee04`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54d30ff31eeef79e6a8ecf14d92c4324b82f4be1176b8a22b89172bdbb1e535`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0811e7d6f99e0f9f0104dbcbb3682d6b9da402b2d9993c9ba173c6c014904e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0` - linux; arm variant v6

```console
$ docker pull consul@sha256:45629f4f5ed311f73724880098846df68977ea44bfb74197cfb6b40666e1e87a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41177693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a659f752b75b6bf5c28cdf21067ce3e1e53f2fc457a6181331e89cfe7748928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:49:37 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:49:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:49:45 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:50:04 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:50:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:50:15 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:50:17 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:50:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:50:19 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:50:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:50:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:50:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541d1797ef1170490288147b99ee5d41a948a7f4e79f641fafc5f6fed3d80b38`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412943d31f925789bbd6d15ce0453a3b619149b5ab000b93ddf626356ca6e8b5`  
		Last Modified: Wed, 25 Nov 2020 00:51:18 GMT  
		Size: 38.6 MB (38572484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03138968c5fe96a538b0bf6df3091212fd588bcf78dbeb51b3c4dc8d044cfb66`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691e110ed2b0a550bf4acbc2e4d169923f3fec45f1fd7020ec1ec81d1fd4fd36`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af8e92dfceb088c9546e2566415d438f1874b57b0ed365044b1a67d27bae92`  
		Last Modified: Wed, 25 Nov 2020 00:51:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1012b86c1b4f0c40be0449c239cdd6f1adfbf34ce7a6ccf5903245f890ff677d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41394856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6a768f504e8509835bc02fa5a484eba01a4389908306659d0829492078a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:39:32 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:39:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:39:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:39:43 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:39:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:39:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:39:50 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:39:50 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:39:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:39:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:39:53 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:39:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4785ac6d608aceb5c11acbff79d38f8310fe7ea952dbc1fe0f16ee4157bb7fb`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda07bb163802553eb787a581765163466d5b9d9fcdf8079b1f9a15d30a000ed`  
		Last Modified: Wed, 25 Nov 2020 00:40:35 GMT  
		Size: 38.7 MB (38685008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbadd110c842ac687b4e011516cbb85cb5351ed410ffc7d9ce8e29d6a81b980a`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fc41f7bedc3f964514a77a849e654c872f9a7ff56dedee9354f0931c41552`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b79696f40f83b31ed9b8fa30c52dc07c56f018ae83b8e705fae062b94b651`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0` - linux; 386

```console
$ docker pull consul@sha256:3ad6148e3cdb242420b209f4d1fe73da7c23f2c78598dbb3df16f6538d5a013a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45231403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addffb46e74179410991b94d4784f09f5e804e3345dea67754c93b743b861fbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:38:31 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:38:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:38:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:38:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:38:39 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:38:40 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:38:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:38:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b670227cf5b0369dec1890afd49daa761d5219f770e6e1717eeb94aa0d30d795`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886f4ead96bdf58722ac9a1bb62e065252db84d364caac2f2f162484607b9679`  
		Last Modified: Wed, 25 Nov 2020 00:39:12 GMT  
		Size: 42.4 MB (42436764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9099eaffdcf30a6fc42310fad858f1210dc9a72b912f3867f84114f14283e4b1`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60de6fed51016b0bc661d53792674a602f12405b5ee4fa32ff4760a2c97fd0a`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1722523c085b312cc345217410e18206bcf15369b2bb5c423315508580a7e0`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:3fe008a8686bf95664e6f18cc18be0f4e9a235dc3edfed6f04f61c0eb0054be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:3aeb5ab2d0fa9189ed99692f8cce218d1c5eb591255ac38c389b680aad3bd5bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8429e82f47dd20c7833966453d571fc43ece763fa5cadec460390351f99d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:15 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 02:55:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:24 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:28 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc5b4d599656ad90b0d9809894af2414f9ffadb68145140f4038ecac2eb174`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ae847c23d3422b795a3bdf170616176238924d44bb8b99503f34b86222246`  
		Last Modified: Fri, 11 Dec 2020 02:57:17 GMT  
		Size: 42.7 MB (42720248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f01f506e7a1412784c106cd451bf530c4e2fa89b82da5494eb7fcee179ee04`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54d30ff31eeef79e6a8ecf14d92c4324b82f4be1176b8a22b89172bdbb1e535`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0811e7d6f99e0f9f0104dbcbb3682d6b9da402b2d9993c9ba173c6c014904e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:45629f4f5ed311f73724880098846df68977ea44bfb74197cfb6b40666e1e87a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41177693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a659f752b75b6bf5c28cdf21067ce3e1e53f2fc457a6181331e89cfe7748928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:49:37 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:49:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:49:45 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:50:04 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:50:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:50:13 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:50:15 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:50:17 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:50:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:50:19 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:50:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:50:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:50:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541d1797ef1170490288147b99ee5d41a948a7f4e79f641fafc5f6fed3d80b38`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412943d31f925789bbd6d15ce0453a3b619149b5ab000b93ddf626356ca6e8b5`  
		Last Modified: Wed, 25 Nov 2020 00:51:18 GMT  
		Size: 38.6 MB (38572484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03138968c5fe96a538b0bf6df3091212fd588bcf78dbeb51b3c4dc8d044cfb66`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691e110ed2b0a550bf4acbc2e4d169923f3fec45f1fd7020ec1ec81d1fd4fd36`  
		Last Modified: Wed, 25 Nov 2020 00:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af8e92dfceb088c9546e2566415d438f1874b57b0ed365044b1a67d27bae92`  
		Last Modified: Wed, 25 Nov 2020 00:51:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1012b86c1b4f0c40be0449c239cdd6f1adfbf34ce7a6ccf5903245f890ff677d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41394856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6a768f504e8509835bc02fa5a484eba01a4389908306659d0829492078a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:39:32 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:39:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:39:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:39:43 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:39:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:39:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:39:50 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:39:50 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:39:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:39:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:39:53 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:39:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4785ac6d608aceb5c11acbff79d38f8310fe7ea952dbc1fe0f16ee4157bb7fb`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda07bb163802553eb787a581765163466d5b9d9fcdf8079b1f9a15d30a000ed`  
		Last Modified: Wed, 25 Nov 2020 00:40:35 GMT  
		Size: 38.7 MB (38685008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbadd110c842ac687b4e011516cbb85cb5351ed410ffc7d9ce8e29d6a81b980a`  
		Last Modified: Wed, 25 Nov 2020 00:40:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044fc41f7bedc3f964514a77a849e654c872f9a7ff56dedee9354f0931c41552`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b79696f40f83b31ed9b8fa30c52dc07c56f018ae83b8e705fae062b94b651`  
		Last Modified: Wed, 25 Nov 2020 00:40:26 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:3ad6148e3cdb242420b209f4d1fe73da7c23f2c78598dbb3df16f6538d5a013a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45231403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addffb46e74179410991b94d4784f09f5e804e3345dea67754c93b743b861fbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 25 Nov 2020 00:38:31 GMT
ENV CONSUL_VERSION=1.9.0
# Wed, 25 Nov 2020 00:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 25 Nov 2020 00:38:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 25 Nov 2020 00:38:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 25 Nov 2020 00:38:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 25 Nov 2020 00:38:39 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 25 Nov 2020 00:38:40 GMT
VOLUME [/consul/data]
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8300
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 25 Nov 2020 00:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 25 Nov 2020 00:38:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 25 Nov 2020 00:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Nov 2020 00:38:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b670227cf5b0369dec1890afd49daa761d5219f770e6e1717eeb94aa0d30d795`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886f4ead96bdf58722ac9a1bb62e065252db84d364caac2f2f162484607b9679`  
		Last Modified: Wed, 25 Nov 2020 00:39:12 GMT  
		Size: 42.4 MB (42436764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9099eaffdcf30a6fc42310fad858f1210dc9a72b912f3867f84114f14283e4b1`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60de6fed51016b0bc661d53792674a602f12405b5ee4fa32ff4760a2c97fd0a`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1722523c085b312cc345217410e18206bcf15369b2bb5c423315508580a7e0`  
		Last Modified: Wed, 25 Nov 2020 00:39:03 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
