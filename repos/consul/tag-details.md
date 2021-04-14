<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.7`](#consul17)
-	[`consul:1.7.13`](#consul1713)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.9`](#consul189)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.4`](#consul194)
-	[`consul:latest`](#consullatest)

## `consul:1.7`

```console
$ docker pull consul@sha256:6b649940ed789dff0d391f05d142ec14b6b0db3e156d0ea7c1a647e564c30567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:99ce7f93fa338b174b41e4232ab629ce04a36d4a89eba5d8a253d867f45d4f08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43132781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea0d70916c0f52a063e51028a42816593e4f3e61c54115efe6ffa51900d3d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:58:27 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 01 Apr 2021 13:58:27 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 01 Apr 2021 13:58:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:58:28 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:58:33 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:58:34 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:58:35 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:58:36 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d76bfb1d9f848c669287051235329a8f47f5263bbf6e01baf0e6a9d750b13a`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dff4edafd1eaccf1815c24781c204035dca6796707a5b16ab4867f69408b65f`  
		Last Modified: Thu, 01 Apr 2021 13:59:44 GMT  
		Size: 40.3 MB (40329779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e31edf64debe816fbd0b0a0c559284d9d7d558fe17fd050dc6494791351e1c`  
		Last Modified: Thu, 01 Apr 2021 13:59:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae22bedb3935281cb594a2eaf0f0d232c9a2360bb309dbe35165b8a4db93de6`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41c1db4f3ee381cd5f185723ec27c880de5a81f45e6df153f9ecc10312dd47`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:56d4778b8542176ab9f9787f283c11a51db09ae620e335210acfe30b5264df86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff0c663b94bafa65171effcad2ce02299d760c2abf094c491344bfb2780cbc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:19:48 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:54 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:20:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:20:12 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:20:13 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:20:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:20:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:20:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529e7baba67302a45e39b19648a7a5087420bd12e6c5e7edd264de9bf0c5246`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe80981258c00e5deeae7d6a7bd7c31df363947dfc611fc8f63f58c0da83539c`  
		Last Modified: Wed, 31 Mar 2021 18:21:29 GMT  
		Size: 36.2 MB (36221735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a12e832dc4bf86a46031d49fdf7baec415ef626977c66eb162dd10bc0991259`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575599c9a8e8beba97f517f4a60988ab6436cbc40263726f09e72b20799ce06`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65db31c460e548d6b2581483491186419b784f36355111139539d912f60190dc`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1afafb751bd0a85b255a51b60db53d646ac6bf61395d7f408212a9d4031981b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39071149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02eb9fc189c0ec658af38a9baf46dc258de16998316cf5ebedf505539e849ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:24:03 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 14 Apr 2021 19:24:04 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 14 Apr 2021 19:24:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:24:08 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:24:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:24:18 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:24:20 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:24:21 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:24:22 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:24:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:24:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:24:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:24:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:24:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f734f535e02dbd4e906c37c98f41711a2e686b87be5c4e5b4cd0209425de3`  
		Last Modified: Wed, 14 Apr 2021 19:25:26 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7e39bb1820fdec3015b10ee854d61c1d26efac1a4d168f2ae8b240ee42c31`  
		Last Modified: Wed, 14 Apr 2021 19:25:33 GMT  
		Size: 36.4 MB (36357165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b4f3df551660cfb737ba89506d0cce8d9b2903afb4ee7e04b97d37e477e04`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f94cfd07f9c44ebe79b4b829856c413af484bc30a473f8b94d4fd5a5c4fc58`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf32e2d0ec7733fe6fc7cf834e221ec44257147f5c7631a0a54c80ef996f713`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:e36f2b17709f22341fb80d892f852fb2a653c1c3c05eb09b4ec4a0443f017727
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41967695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad2c4ba0498e14730d0e35f973293145c985da63b8a5289dee1adb533ec8d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:56:07 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 14 Apr 2021 18:56:07 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 14 Apr 2021 18:56:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:56:08 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:56:13 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:56:14 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:56:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:56:15 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:56:15 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:56:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:56:16 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:56:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:56:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:56:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e51d0cf9f34fc8ef57ae4d7f8312d898899a7d394e62f68c75668c7c392af5d`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a6cfb7bf36bcf37242b07431d6db85c7c63f17226062c385c77e9aebfeb560`  
		Last Modified: Wed, 14 Apr 2021 18:57:47 GMT  
		Size: 39.2 MB (39168609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007d5a25290063f49c42946d7bd8a9269aff393731dd02c47b246baa64f1f86e`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bf9d5f8cc42a78be8dc2b92dd3c8b70e13f968a11a13a4e8971d74f16410cd`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b421f9d51d4bba68eec8dd875989856dac5f1b65093cc8b72f8c54cd55d3901e`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.13`

```console
$ docker pull consul@sha256:6b649940ed789dff0d391f05d142ec14b6b0db3e156d0ea7c1a647e564c30567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.13` - linux; amd64

```console
$ docker pull consul@sha256:99ce7f93fa338b174b41e4232ab629ce04a36d4a89eba5d8a253d867f45d4f08
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43132781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea0d70916c0f52a063e51028a42816593e4f3e61c54115efe6ffa51900d3d7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:58:27 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 01 Apr 2021 13:58:27 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 01 Apr 2021 13:58:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:58:28 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:58:33 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:58:34 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:58:35 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:58:36 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:58:36 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d76bfb1d9f848c669287051235329a8f47f5263bbf6e01baf0e6a9d750b13a`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dff4edafd1eaccf1815c24781c204035dca6796707a5b16ab4867f69408b65f`  
		Last Modified: Thu, 01 Apr 2021 13:59:44 GMT  
		Size: 40.3 MB (40329779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e31edf64debe816fbd0b0a0c559284d9d7d558fe17fd050dc6494791351e1c`  
		Last Modified: Thu, 01 Apr 2021 13:59:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae22bedb3935281cb594a2eaf0f0d232c9a2360bb309dbe35165b8a4db93de6`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41c1db4f3ee381cd5f185723ec27c880de5a81f45e6df153f9ecc10312dd47`  
		Last Modified: Thu, 01 Apr 2021 13:59:37 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:56d4778b8542176ab9f9787f283c11a51db09ae620e335210acfe30b5264df86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff0c663b94bafa65171effcad2ce02299d760c2abf094c491344bfb2780cbc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:19:48 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:54 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:20:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:20:12 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:20:13 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:20:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:20:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:20:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529e7baba67302a45e39b19648a7a5087420bd12e6c5e7edd264de9bf0c5246`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe80981258c00e5deeae7d6a7bd7c31df363947dfc611fc8f63f58c0da83539c`  
		Last Modified: Wed, 31 Mar 2021 18:21:29 GMT  
		Size: 36.2 MB (36221735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a12e832dc4bf86a46031d49fdf7baec415ef626977c66eb162dd10bc0991259`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575599c9a8e8beba97f517f4a60988ab6436cbc40263726f09e72b20799ce06`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65db31c460e548d6b2581483491186419b784f36355111139539d912f60190dc`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1afafb751bd0a85b255a51b60db53d646ac6bf61395d7f408212a9d4031981b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39071149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02eb9fc189c0ec658af38a9baf46dc258de16998316cf5ebedf505539e849ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:24:03 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 14 Apr 2021 19:24:04 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 14 Apr 2021 19:24:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:24:08 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:24:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:24:18 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:24:20 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:24:21 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:24:22 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:24:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:24:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:24:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:24:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:24:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f734f535e02dbd4e906c37c98f41711a2e686b87be5c4e5b4cd0209425de3`  
		Last Modified: Wed, 14 Apr 2021 19:25:26 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7e39bb1820fdec3015b10ee854d61c1d26efac1a4d168f2ae8b240ee42c31`  
		Last Modified: Wed, 14 Apr 2021 19:25:33 GMT  
		Size: 36.4 MB (36357165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0b4f3df551660cfb737ba89506d0cce8d9b2903afb4ee7e04b97d37e477e04`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f94cfd07f9c44ebe79b4b829856c413af484bc30a473f8b94d4fd5a5c4fc58`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf32e2d0ec7733fe6fc7cf834e221ec44257147f5c7631a0a54c80ef996f713`  
		Last Modified: Wed, 14 Apr 2021 19:25:25 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; 386

```console
$ docker pull consul@sha256:e36f2b17709f22341fb80d892f852fb2a653c1c3c05eb09b4ec4a0443f017727
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41967695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad2c4ba0498e14730d0e35f973293145c985da63b8a5289dee1adb533ec8d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:56:07 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 14 Apr 2021 18:56:07 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 14 Apr 2021 18:56:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:56:08 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:56:13 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:56:14 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:56:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:56:15 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:56:15 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:56:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:56:16 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:56:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:56:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:56:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e51d0cf9f34fc8ef57ae4d7f8312d898899a7d394e62f68c75668c7c392af5d`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a6cfb7bf36bcf37242b07431d6db85c7c63f17226062c385c77e9aebfeb560`  
		Last Modified: Wed, 14 Apr 2021 18:57:47 GMT  
		Size: 39.2 MB (39168609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007d5a25290063f49c42946d7bd8a9269aff393731dd02c47b246baa64f1f86e`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bf9d5f8cc42a78be8dc2b92dd3c8b70e13f968a11a13a4e8971d74f16410cd`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b421f9d51d4bba68eec8dd875989856dac5f1b65093cc8b72f8c54cd55d3901e`  
		Last Modified: Wed, 14 Apr 2021 18:57:41 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:4893825218a12a74464b03b16db95b5f1fb9f76beffd8f233d8bdfed07fe70da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:1c85a1abf85528c0b96c75c783db902f5c5d9f0204af066a241661765d5afef5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46519178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb5800a09fb0ad08ed9b9f34ac56a367aed36dc31b09fb0e862e443888a1dec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:58:14 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 01 Apr 2021 13:58:14 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 01 Apr 2021 13:58:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:58:15 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:58:20 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:58:22 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:58:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:58:23 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9b771409f4f3f2f129221ce337f2081dd152cce17c174a9fac5c12459293f1`  
		Last Modified: Thu, 01 Apr 2021 13:59:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf511b0af74102bdd5dc799e059f0babaaa036a3e2aa77ec680dca6b0bcb181`  
		Last Modified: Thu, 01 Apr 2021 13:59:27 GMT  
		Size: 43.7 MB (43716176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26be0088f3fb542426f3b16b714a6e2c6bb96c3cb271c8a3be4357659b2708ca`  
		Last Modified: Thu, 01 Apr 2021 13:59:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404a0ea273d8d2a6357df52a8febc721807149a5dfdf98a3ba72a7a8e4c1d77f`  
		Last Modified: Thu, 01 Apr 2021 13:59:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e18aef70ec04c786d67ed4f9edc24be85880db30dcd107c010de51044f86a96`  
		Last Modified: Thu, 01 Apr 2021 13:59:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:3ce0aaf87899af79726707ca5f6cce3aa05c0e09e60f744238f6c10ff02b379e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41786936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df4b2e9e8f5beee9f678fb146d62f8f893031e03ca8d415e89ff6eba77f3e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:18:52 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 31 Mar 2021 18:18:55 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 31 Mar 2021 18:18:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:19:12 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:19:16 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:19:19 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:19:21 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:19:22 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:19:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:19:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:19:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:19:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6361f4b4701b9c8dd7e21881c0145615ccb6a248aa8747974b044ce2c13c79bd`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf5025eb71243b618ec0eb15217a060db83fe892c2df7c8dd7d7141a7b985d3`  
		Last Modified: Wed, 31 Mar 2021 18:21:10 GMT  
		Size: 39.2 MB (39178987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0009e1bfe638c28c30aad9b1b37a68410e1b5781cc64f528cd63f10e765c92`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bcca113639fa0e6481b1d4bc011c7302a4cca8a97f2dabe9f8445ae6dec5a1`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4819c38721e3cda06e2ad730593405bc4f0fd135ef6f6c9f75cf720ffa2896d`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:efa6e7ca940f6a14444b4f84ed7ed23db7cda69629c641a0c0962295b920ce85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41982267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d398fd2f340fc1b4b2dc2ba57d5c86e6b32367860efb35cab1023fd376027`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:23:26 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 14 Apr 2021 19:23:28 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 14 Apr 2021 19:23:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:23:31 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:23:38 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:23:41 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:23:44 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:23:45 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:23:46 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:23:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:23:48 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:23:49 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b5571393035c4757df133370d5c2d1c7b9a5c0b6a1c991e2644048a71814b8`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c763675dd4ef92e3623c1b49e892cf59de5e3f3d14a3c6a675fbfa98481ac`  
		Last Modified: Wed, 14 Apr 2021 19:25:17 GMT  
		Size: 39.3 MB (39268281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcaec3c757f98193db9c9837ddcf261f3bab3eddd4ccb6dc42ed48ee79e688c`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf224d390c88605c93f6484c31f95889a6ff4e4ab16e07d708f02c58efd3442a`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4501b62f777fbc16d208c09cb46bda23b3e53e0a58aa442a55605985dbaa056b`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:5dce80a9c00ce04e6bc012d8f02f948f3b1b3ca069668d0403228fc9e8cd2268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46072303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bba23041c7d8beaa473e2b676c66eb2d8a60b83fb61ec6cce850b6b1d33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:55:53 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 14 Apr 2021 18:55:53 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 14 Apr 2021 18:55:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:55:54 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:55:59 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:56:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:56:01 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:56:01 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:56:01 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:56:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:56:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:56:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:56:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8db9ae0b7b83ba7b1defb913bc9dbed81c21def51442f927dd0e716b89f6f5`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3da24a16fbc35b0e5b01d6803bd687e835baedd549845c2b3c6db5065b23b3a`  
		Last Modified: Wed, 14 Apr 2021 18:57:29 GMT  
		Size: 43.3 MB (43273215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57cf0eb793920b9309d2f2d5887c0f9956e4f4ac3544e91ea1a0db4a358df60`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa6e9893eb45f30ce4ae14c4d89e283a022f5a46bd1cfab3498da4c718d7d93`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a179f593ded316386fbf4301a8eb438e4495471af99b86246711ff5af6109021`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.9`

```console
$ docker pull consul@sha256:4893825218a12a74464b03b16db95b5f1fb9f76beffd8f233d8bdfed07fe70da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.9` - linux; amd64

```console
$ docker pull consul@sha256:1c85a1abf85528c0b96c75c783db902f5c5d9f0204af066a241661765d5afef5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46519178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb5800a09fb0ad08ed9b9f34ac56a367aed36dc31b09fb0e862e443888a1dec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:58:14 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 01 Apr 2021 13:58:14 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 01 Apr 2021 13:58:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:58:15 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:58:20 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:58:22 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:58:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:58:23 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:58:23 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9b771409f4f3f2f129221ce337f2081dd152cce17c174a9fac5c12459293f1`  
		Last Modified: Thu, 01 Apr 2021 13:59:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf511b0af74102bdd5dc799e059f0babaaa036a3e2aa77ec680dca6b0bcb181`  
		Last Modified: Thu, 01 Apr 2021 13:59:27 GMT  
		Size: 43.7 MB (43716176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26be0088f3fb542426f3b16b714a6e2c6bb96c3cb271c8a3be4357659b2708ca`  
		Last Modified: Thu, 01 Apr 2021 13:59:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404a0ea273d8d2a6357df52a8febc721807149a5dfdf98a3ba72a7a8e4c1d77f`  
		Last Modified: Thu, 01 Apr 2021 13:59:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e18aef70ec04c786d67ed4f9edc24be85880db30dcd107c010de51044f86a96`  
		Last Modified: Thu, 01 Apr 2021 13:59:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:3ce0aaf87899af79726707ca5f6cce3aa05c0e09e60f744238f6c10ff02b379e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41786936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df4b2e9e8f5beee9f678fb146d62f8f893031e03ca8d415e89ff6eba77f3e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:18:52 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 31 Mar 2021 18:18:55 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 31 Mar 2021 18:18:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:19:12 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:19:16 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:19:19 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:19:21 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:19:22 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:19:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:19:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:19:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:19:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6361f4b4701b9c8dd7e21881c0145615ccb6a248aa8747974b044ce2c13c79bd`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf5025eb71243b618ec0eb15217a060db83fe892c2df7c8dd7d7141a7b985d3`  
		Last Modified: Wed, 31 Mar 2021 18:21:10 GMT  
		Size: 39.2 MB (39178987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0009e1bfe638c28c30aad9b1b37a68410e1b5781cc64f528cd63f10e765c92`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bcca113639fa0e6481b1d4bc011c7302a4cca8a97f2dabe9f8445ae6dec5a1`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4819c38721e3cda06e2ad730593405bc4f0fd135ef6f6c9f75cf720ffa2896d`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:efa6e7ca940f6a14444b4f84ed7ed23db7cda69629c641a0c0962295b920ce85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41982267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d398fd2f340fc1b4b2dc2ba57d5c86e6b32367860efb35cab1023fd376027`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:23:26 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 14 Apr 2021 19:23:28 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 14 Apr 2021 19:23:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:23:31 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:23:38 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:23:41 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:23:44 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:23:45 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:23:46 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:23:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:23:48 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:23:49 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b5571393035c4757df133370d5c2d1c7b9a5c0b6a1c991e2644048a71814b8`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c763675dd4ef92e3623c1b49e892cf59de5e3f3d14a3c6a675fbfa98481ac`  
		Last Modified: Wed, 14 Apr 2021 19:25:17 GMT  
		Size: 39.3 MB (39268281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcaec3c757f98193db9c9837ddcf261f3bab3eddd4ccb6dc42ed48ee79e688c`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf224d390c88605c93f6484c31f95889a6ff4e4ab16e07d708f02c58efd3442a`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4501b62f777fbc16d208c09cb46bda23b3e53e0a58aa442a55605985dbaa056b`  
		Last Modified: Wed, 14 Apr 2021 19:25:09 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; 386

```console
$ docker pull consul@sha256:5dce80a9c00ce04e6bc012d8f02f948f3b1b3ca069668d0403228fc9e8cd2268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46072303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bba23041c7d8beaa473e2b676c66eb2d8a60b83fb61ec6cce850b6b1d33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:55:53 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 14 Apr 2021 18:55:53 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 14 Apr 2021 18:55:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:55:54 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:55:59 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:56:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:56:01 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:56:01 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:56:01 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:56:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:56:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:56:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:56:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8db9ae0b7b83ba7b1defb913bc9dbed81c21def51442f927dd0e716b89f6f5`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3da24a16fbc35b0e5b01d6803bd687e835baedd549845c2b3c6db5065b23b3a`  
		Last Modified: Wed, 14 Apr 2021 18:57:29 GMT  
		Size: 43.3 MB (43273215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57cf0eb793920b9309d2f2d5887c0f9956e4f4ac3544e91ea1a0db4a358df60`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa6e9893eb45f30ce4ae14c4d89e283a022f5a46bd1cfab3498da4c718d7d93`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a179f593ded316386fbf4301a8eb438e4495471af99b86246711ff5af6109021`  
		Last Modified: Wed, 14 Apr 2021 18:57:22 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:1152755f95f428285a951fc37a3442f557a16cd0069e52d82291a7e81a93e2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:c28c1495e8b6ab3dc8b80585b9eb269c3a8ce70d534fc141936ca5e62a425c8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb701064c41aef58ca3504b14eed918eaba77f3d21967694a08329d64272e321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:55:33 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 13:55:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:55:35 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:57:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:57:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:57:59 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:57:59 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258501eb950bc3320ca3f00551a08bc5c4ff077f4a74028afb9226581d3c5c75`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786844d2dd3a2bdedd54c5517778e834b06533b35cf74ff910a1fdccfd2f27ea`  
		Last Modified: Thu, 01 Apr 2021 13:59:03 GMT  
		Size: 42.8 MB (42827918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb33e490aaf4758702ef5641b86b2ff5c8ce2d2bb002b4a07c61c9e6630710e`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2060c3060ba858186857225b4e10fe20cf36750d7539b2745bc75711efe93c`  
		Last Modified: Thu, 01 Apr 2021 13:58:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b0c7e5b1257c37ec8c067350b190446fa79363350c5b36f52b92cc8856a38`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:794c24fbbd979bf5af6af9630d7d9325aa6f01f668f4bca857204c5994c54b3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41126204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a825e2fced0b53948b4f9e7bfc5d1609481cc108c2d60c1c6fd96b2643c9736a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:22:51 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 19:22:52 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 19:22:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:22:56 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:23:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:23:06 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:23:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:23:10 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:23:13 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:23:14 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b96788e82b6af129f934f44e3be6e11bd50c5aa4aa7f153d5c23ccb0dc12cf`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face225286cec8239bf7c33e3977ca020cbc18e6b8cd3865c520feb00357f466`  
		Last Modified: Wed, 14 Apr 2021 19:24:57 GMT  
		Size: 38.4 MB (38412219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb33ef170a52b1969e77c98378e9677623a19a6c6c17b581a3b345a3f9d387`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3befdfcaca0963f39f847c37604e9867e38aaca2fa8bbfde33c3515e22ec18`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b246d545ee670f4fd4a8233c1a1fb4233cba1d92c226cf5fad4566571d125075`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:f7b2894fa2b2cce628874cb34c141e154a36af139a2ce7cf8ea879057ec1f36a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44978347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e6b7fa39b52e886a1bcecc2e7cca9076c09427848558ee7631e8b5a9a924e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:55:36 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:55:37 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:55:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:55:45 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:55:46 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:55:46 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:55:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:55:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3831ff37459cebceaf36d2175d922fea9abe8aa2d956f29596fcce2b12cc90d`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf5d944668f1ce4efe25c8da04427ff173e57ba09ae72f16313fe5fd01d77b`  
		Last Modified: Wed, 14 Apr 2021 18:56:48 GMT  
		Size: 42.2 MB (42179261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f75e489a23c08e7c8d80a390517626ae20d9bc1900e38f640c3ceb3c452289`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9108803843267de412c0c6aa141a1d17bc55047f1b59d3602ce336005d6a81`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f9b370fadecaa06e11cd41a1054987b24cf57a0b49c6b4d3f1c4a64928e40`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.4`

```console
$ docker pull consul@sha256:1152755f95f428285a951fc37a3442f557a16cd0069e52d82291a7e81a93e2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.4` - linux; amd64

```console
$ docker pull consul@sha256:c28c1495e8b6ab3dc8b80585b9eb269c3a8ce70d534fc141936ca5e62a425c8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb701064c41aef58ca3504b14eed918eaba77f3d21967694a08329d64272e321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:55:33 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 13:55:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:55:35 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:57:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:57:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:57:59 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:57:59 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258501eb950bc3320ca3f00551a08bc5c4ff077f4a74028afb9226581d3c5c75`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786844d2dd3a2bdedd54c5517778e834b06533b35cf74ff910a1fdccfd2f27ea`  
		Last Modified: Thu, 01 Apr 2021 13:59:03 GMT  
		Size: 42.8 MB (42827918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb33e490aaf4758702ef5641b86b2ff5c8ce2d2bb002b4a07c61c9e6630710e`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2060c3060ba858186857225b4e10fe20cf36750d7539b2745bc75711efe93c`  
		Last Modified: Thu, 01 Apr 2021 13:58:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b0c7e5b1257c37ec8c067350b190446fa79363350c5b36f52b92cc8856a38`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:794c24fbbd979bf5af6af9630d7d9325aa6f01f668f4bca857204c5994c54b3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41126204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a825e2fced0b53948b4f9e7bfc5d1609481cc108c2d60c1c6fd96b2643c9736a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:22:51 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 19:22:52 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 19:22:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:22:56 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:23:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:23:06 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:23:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:23:10 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:23:13 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:23:14 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b96788e82b6af129f934f44e3be6e11bd50c5aa4aa7f153d5c23ccb0dc12cf`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face225286cec8239bf7c33e3977ca020cbc18e6b8cd3865c520feb00357f466`  
		Last Modified: Wed, 14 Apr 2021 19:24:57 GMT  
		Size: 38.4 MB (38412219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb33ef170a52b1969e77c98378e9677623a19a6c6c17b581a3b345a3f9d387`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3befdfcaca0963f39f847c37604e9867e38aaca2fa8bbfde33c3515e22ec18`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b246d545ee670f4fd4a8233c1a1fb4233cba1d92c226cf5fad4566571d125075`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; 386

```console
$ docker pull consul@sha256:f7b2894fa2b2cce628874cb34c141e154a36af139a2ce7cf8ea879057ec1f36a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44978347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e6b7fa39b52e886a1bcecc2e7cca9076c09427848558ee7631e8b5a9a924e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:55:36 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:55:37 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:55:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:55:45 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:55:46 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:55:46 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:55:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:55:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3831ff37459cebceaf36d2175d922fea9abe8aa2d956f29596fcce2b12cc90d`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf5d944668f1ce4efe25c8da04427ff173e57ba09ae72f16313fe5fd01d77b`  
		Last Modified: Wed, 14 Apr 2021 18:56:48 GMT  
		Size: 42.2 MB (42179261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f75e489a23c08e7c8d80a390517626ae20d9bc1900e38f640c3ceb3c452289`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9108803843267de412c0c6aa141a1d17bc55047f1b59d3602ce336005d6a81`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f9b370fadecaa06e11cd41a1054987b24cf57a0b49c6b4d3f1c4a64928e40`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:1152755f95f428285a951fc37a3442f557a16cd0069e52d82291a7e81a93e2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:c28c1495e8b6ab3dc8b80585b9eb269c3a8ce70d534fc141936ca5e62a425c8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb701064c41aef58ca3504b14eed918eaba77f3d21967694a08329d64272e321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 13:55:33 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 13:55:33 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 13:55:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 13:55:35 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 13:57:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 13:57:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 13:57:59 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 13:57:59 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 13:57:59 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 13:58:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 13:58:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 13:58:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258501eb950bc3320ca3f00551a08bc5c4ff077f4a74028afb9226581d3c5c75`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786844d2dd3a2bdedd54c5517778e834b06533b35cf74ff910a1fdccfd2f27ea`  
		Last Modified: Thu, 01 Apr 2021 13:59:03 GMT  
		Size: 42.8 MB (42827918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb33e490aaf4758702ef5641b86b2ff5c8ce2d2bb002b4a07c61c9e6630710e`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2060c3060ba858186857225b4e10fe20cf36750d7539b2745bc75711efe93c`  
		Last Modified: Thu, 01 Apr 2021 13:58:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b0c7e5b1257c37ec8c067350b190446fa79363350c5b36f52b92cc8856a38`  
		Last Modified: Thu, 01 Apr 2021 13:58:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:794c24fbbd979bf5af6af9630d7d9325aa6f01f668f4bca857204c5994c54b3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41126204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a825e2fced0b53948b4f9e7bfc5d1609481cc108c2d60c1c6fd96b2643c9736a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 19:22:51 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 19:22:52 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 19:22:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 19:22:56 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 19:23:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 19:23:06 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 19:23:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:23:10 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 19:23:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 19:23:13 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 19:23:14 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b96788e82b6af129f934f44e3be6e11bd50c5aa4aa7f153d5c23ccb0dc12cf`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face225286cec8239bf7c33e3977ca020cbc18e6b8cd3865c520feb00357f466`  
		Last Modified: Wed, 14 Apr 2021 19:24:57 GMT  
		Size: 38.4 MB (38412219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fb33ef170a52b1969e77c98378e9677623a19a6c6c17b581a3b345a3f9d387`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3befdfcaca0963f39f847c37604e9867e38aaca2fa8bbfde33c3515e22ec18`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b246d545ee670f4fd4a8233c1a1fb4233cba1d92c226cf5fad4566571d125075`  
		Last Modified: Wed, 14 Apr 2021 19:24:48 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:f7b2894fa2b2cce628874cb34c141e154a36af139a2ce7cf8ea879057ec1f36a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44978347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e6b7fa39b52e886a1bcecc2e7cca9076c09427848558ee7631e8b5a9a924e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 14 Apr 2021 18:55:36 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 14 Apr 2021 18:55:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Apr 2021 18:55:37 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Apr 2021 18:55:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Apr 2021 18:55:45 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Apr 2021 18:55:46 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 18:55:46 GMT
VOLUME [/consul/data]
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8300
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Apr 2021 18:55:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Apr 2021 18:55:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 18:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 18:55:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3831ff37459cebceaf36d2175d922fea9abe8aa2d956f29596fcce2b12cc90d`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf5d944668f1ce4efe25c8da04427ff173e57ba09ae72f16313fe5fd01d77b`  
		Last Modified: Wed, 14 Apr 2021 18:56:48 GMT  
		Size: 42.2 MB (42179261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f75e489a23c08e7c8d80a390517626ae20d9bc1900e38f640c3ceb3c452289`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9108803843267de412c0c6aa141a1d17bc55047f1b59d3602ce336005d6a81`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f9b370fadecaa06e11cd41a1054987b24cf57a0b49c6b4d3f1c4a64928e40`  
		Last Modified: Wed, 14 Apr 2021 18:56:42 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
