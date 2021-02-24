## `consul:latest`

```console
$ docker pull consul@sha256:e9530d78c42bb2731948d2c7057d53f215e68a963b9455fb913fde99846f8c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:adbf5269451afbfdc6fc5119fe4edf01b530f443969cb3cff0a00109613db349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45605807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881134d490742be947022560fe1dc94f58a6d4de2cc356e00a9aac59392538f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:19:29 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:19:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:19:31 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:19:35 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:19:36 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:19:37 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:19:38 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:19:38 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:19:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea52006ac511368e3c6bcb4a73d30678c542c0c3fb8a37d65f827068653579f6`  
		Last Modified: Wed, 24 Feb 2021 21:20:31 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e14090bc9d8bfe39c13dfb297d4bcf1538266cec537752e4ad6efabd891756`  
		Last Modified: Wed, 24 Feb 2021 21:20:40 GMT  
		Size: 42.8 MB (42803082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cff81a0c3344b1ac69a78209a4d49549b47f75103613029c2b371ec7db7c9`  
		Last Modified: Wed, 24 Feb 2021 21:20:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aa5162537717ccc5634c8a34f89e58b1c4731856fee3c87fc09a800bd54898`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8e3c9e516b9424db7cd5c9c8f4f6f2ceae55ed0afaad8cecd7abedc5975740`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:e41722bc53a600ed9b6b6fcd1608e9bd20249bd40191c6af2cb508329cfdaa69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40859913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b835ce0d86f3c852ecba7dafa68b53c6517044e969e563985bc059dca7d869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:08:49 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:08:50 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:08:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:08:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:09:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:09:06 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:09:08 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:09:09 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:09:09 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:09:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:09:11 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:09:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:09:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:09:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb44b55f96ee001a4432da8272d7ffe73f0183ffb389a82f7667d28d0f07c26`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cd7d068879fd65d6274f175aec93067fe49c4889288e5612c3081bdc2bc11`  
		Last Modified: Wed, 24 Feb 2021 21:10:50 GMT  
		Size: 38.3 MB (38252105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188f40afa3bfa764ad72775287e9c6d1d545dee4297004580f7ed356b81f36bc`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7dd591ff83643e7b76fb5c0ec9663a8308008861886ab6746c8c01ffd9d8ab`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b12c42aa58449544394a012ea612b0f79a16e875e7e9c3ea8c2d0d4a2aea8f`  
		Last Modified: Wed, 24 Feb 2021 21:10:38 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:ba026ed01032d20a1a820a2a77acaa0afecaa03ca90077a6c7458c31ec2aca30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41083538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0119551dc9d961a19f7d069b7693f3a5e8d9d3b4839539adfa075d3928b9736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:29:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:29:41 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:29:42 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:29:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:29:45 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:29:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:29:54 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:29:56 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:29:57 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:29:59 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:30:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:30:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc2046d54b68e05b97d89063b0fb734fcb614068a9696992bb1ce4c69445f9`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7013c29a3b7b22d36bccdd822922143df6d8d08cc6fd53b047187dfa0c4cfd`  
		Last Modified: Wed, 24 Feb 2021 21:31:36 GMT  
		Size: 38.4 MB (38370368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223d45cdfdedeb253ed549dc365f3358bc97575e31c1394898f5a278c318528`  
		Last Modified: Wed, 24 Feb 2021 21:31:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f13575aa7031107847957acec156e196115cbd4a6d3ec50047762b62978b31`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0016fa33719e94e99da5b406c5aa9c07e5c5b3edbea62e5b5ac540ccceeb36d5`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:035c25bb69369d460af645c9b0c7054d1f7898b0c6846dc79c29153a76af41f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44931903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9278ff98c7391c7667b2aa6b4fa34542b6789fc023bcbfaf8c3e46a4aa60727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:55:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 20:55:02 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 20:55:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 20:55:09 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 20:55:10 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 20:55:11 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:55:12 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 20:55:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 20:55:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 20:55:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb2681bebeadff1ca0914e09619d419e7d4e39d6bec343d93e66fcede66d82e`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100266ffa9756a72fe161c8439fb8111b7db8c074946f18e76824e6cfd9a79e8`  
		Last Modified: Wed, 24 Feb 2021 20:56:10 GMT  
		Size: 42.1 MB (42133919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ff495a1d55d7f730f76ec25ae78705097b748f948b8297a401704f8a5c5d9`  
		Last Modified: Wed, 24 Feb 2021 20:56:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3087a92a4fe968273b0a7c2f115e35fb4a583a69c1263ee803510c407823241`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f513b227a70e0d8ddefaa0a1a53aeb0c26f4ef3e0644adeaf2156636c002b9`  
		Last Modified: Wed, 24 Feb 2021 20:56:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
