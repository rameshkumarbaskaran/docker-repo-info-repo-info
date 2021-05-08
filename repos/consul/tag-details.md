<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10.0-beta`](#consul1100-beta)
-	[`consul:1.10.0-beta2`](#consul1100-beta2)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.14`](#consul1714)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.10`](#consul1810)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.5`](#consul195)
-	[`consul:latest`](#consullatest)

## `consul:1.10.0-beta`

```console
$ docker pull consul@sha256:8acde8ab5806b6023c2accd18a8e7c8d74002157b8a8d47047e5d331ad21e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.0-beta` - linux; amd64

```console
$ docker pull consul@sha256:438375112cdf26dd75bded2f6bdad24e3a5178305b6f71ad16ed610c56293161
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42800363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36182a0c170648292d86714f9bee760be9b14a24f12f6b6519127ef9e26123d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 20:19:36 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 20:19:36 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 20:19:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 20:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:19:47 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:19:49 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:19:51 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:19:51 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:19:51 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:19:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:19:52 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:19:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:19:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb90f7975ee035bbc9cc8b1f3590706013921dca2124fec06102ca390d41e83`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c649c981fb23b244e23a26cf926b6ba6c2dada43985579de06252eb4b820b2e9`  
		Last Modified: Fri, 07 May 2021 20:20:52 GMT  
		Size: 40.0 MB (39996500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed82556bc95b2cb82334281b9a7976cb8823ec68c654e72502eed1969a19f477`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cffa24ccd7c67fd8f228441ad87e4565edd07b51210b4659aedcbd3b801509`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3c69342f1b3339a59372c9dc37f6710ca08268e2a74093c61d5d28cbe8ea31`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; arm variant v6

```console
$ docker pull consul@sha256:04961cfd394b73be55b259d3cfb17603296e2de1dbedf3414bbe48321a13d5d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38808683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cb74ac47a5c6a0781a2b0233f83cf51ac80b70776d63ef34b796d243295347`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:49:33 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:49:33 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:49:36 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:49:47 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:49:54 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:49:57 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:49:58 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:49:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:50:00 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:50:01 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:50:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd9e0c771f94668e21ec8dd3f86637437c6c73aa245e6a37bd4effbc834144`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648830154ded162bc117ff5f14b972bbd9c65b83126b03974eedde671a14d15`  
		Last Modified: Fri, 07 May 2021 19:53:16 GMT  
		Size: 36.2 MB (36200137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940fab5f9e68e9b2ce1c72175ef2a0fe81a6e856fe241c6ad26aeb506cf0c0c1`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88be271ba9c212534f16cd1f64b139240557e7272d419799fc00ccb981118d1`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3289ab29e8edfd4f02192f1eed6620f956b359844b4678ba3b78c33d2ecb462c`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3ebc2fdeef159d01cd3ef91bcff1b9ddccf76ce9f04267f3692cb2fe7201d5dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38779956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b66dfd020fd66fb427ce4b7fa50cf7dc50c19d2bf9a8e87a2c253ff1128244c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:40:55 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:40:55 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:40:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:40:58 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:41:05 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:41:08 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:41:10 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:41:11 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:41:11 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:41:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:41:13 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:41:14 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:41:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6876dd81d4ce3df7e2d4ebcbde3c624dadaa9703701ff4ff57fc08ecc6ebed16`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2d13c86b8e2c193817273c6fa9743a1a4419b16e26f2a8e22a757320bc1157`  
		Last Modified: Fri, 07 May 2021 19:43:17 GMT  
		Size: 36.1 MB (36065968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03a32f6727d5b191c3d8ea9a7cad22f8fb040f6b3c547a5cf8ef9c5c4c3ff4`  
		Last Modified: Fri, 07 May 2021 19:43:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e743882506113dc5871bca4d0b54de0eaaff274047a425ee9a2cd3dab48d4a69`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276461d947c4047cdee5f4df593840f8b0d82129041eaf81390d81fc2b11500`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; 386

```console
$ docker pull consul@sha256:9273594603e532ba442c8e9c3248c63cd33271910cbe6f72660be1f420e6be10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42161064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264df230949cdd26b5a182b3ad900563184b660a50c6bac956208833e213384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:38:30 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:38:31 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:38:32 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:38:41 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:38:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb331bee2ca3e7c267a54d4cf6b0f05ee087d025b9fad3229cdb154476961bd`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61cb6421179180cd054b21c4109cfa6bcc4d0441bab43f9bba1db0b573a6b4`  
		Last Modified: Fri, 07 May 2021 19:39:58 GMT  
		Size: 39.4 MB (39361973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234db7ec0bab29592fca3a77fa0b4a9fb100368d27e0410bca10dbfe73672fc4`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1bcdff20cfee8b062b9196399270d0989e07e3525052cf7b98eb6003151a2`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f18752f9628d680b47431e639c740a6220e6318ba593e4c3606330e1c2871d`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.0-beta2`

```console
$ docker pull consul@sha256:8acde8ab5806b6023c2accd18a8e7c8d74002157b8a8d47047e5d331ad21e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.0-beta2` - linux; amd64

```console
$ docker pull consul@sha256:438375112cdf26dd75bded2f6bdad24e3a5178305b6f71ad16ed610c56293161
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42800363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36182a0c170648292d86714f9bee760be9b14a24f12f6b6519127ef9e26123d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 20:19:36 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 20:19:36 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 20:19:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 20:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:19:47 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:19:49 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:19:51 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:19:51 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:19:51 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:19:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:19:52 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:19:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:19:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb90f7975ee035bbc9cc8b1f3590706013921dca2124fec06102ca390d41e83`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c649c981fb23b244e23a26cf926b6ba6c2dada43985579de06252eb4b820b2e9`  
		Last Modified: Fri, 07 May 2021 20:20:52 GMT  
		Size: 40.0 MB (39996500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed82556bc95b2cb82334281b9a7976cb8823ec68c654e72502eed1969a19f477`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cffa24ccd7c67fd8f228441ad87e4565edd07b51210b4659aedcbd3b801509`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3c69342f1b3339a59372c9dc37f6710ca08268e2a74093c61d5d28cbe8ea31`  
		Last Modified: Fri, 07 May 2021 20:20:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta2` - linux; arm variant v6

```console
$ docker pull consul@sha256:04961cfd394b73be55b259d3cfb17603296e2de1dbedf3414bbe48321a13d5d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38808683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cb74ac47a5c6a0781a2b0233f83cf51ac80b70776d63ef34b796d243295347`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:49:33 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:49:33 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:49:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:49:36 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:49:47 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:49:54 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:49:57 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:49:58 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:49:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:50:00 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:50:01 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:50:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd9e0c771f94668e21ec8dd3f86637437c6c73aa245e6a37bd4effbc834144`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8648830154ded162bc117ff5f14b972bbd9c65b83126b03974eedde671a14d15`  
		Last Modified: Fri, 07 May 2021 19:53:16 GMT  
		Size: 36.2 MB (36200137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940fab5f9e68e9b2ce1c72175ef2a0fe81a6e856fe241c6ad26aeb506cf0c0c1`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88be271ba9c212534f16cd1f64b139240557e7272d419799fc00ccb981118d1`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3289ab29e8edfd4f02192f1eed6620f956b359844b4678ba3b78c33d2ecb462c`  
		Last Modified: Fri, 07 May 2021 19:53:06 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta2` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3ebc2fdeef159d01cd3ef91bcff1b9ddccf76ce9f04267f3692cb2fe7201d5dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38779956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b66dfd020fd66fb427ce4b7fa50cf7dc50c19d2bf9a8e87a2c253ff1128244c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:40:55 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:40:55 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:40:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:40:58 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:41:05 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:41:08 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:41:10 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:41:11 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:41:11 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:41:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:41:13 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:41:14 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:41:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6876dd81d4ce3df7e2d4ebcbde3c624dadaa9703701ff4ff57fc08ecc6ebed16`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2d13c86b8e2c193817273c6fa9743a1a4419b16e26f2a8e22a757320bc1157`  
		Last Modified: Fri, 07 May 2021 19:43:17 GMT  
		Size: 36.1 MB (36065968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df03a32f6727d5b191c3d8ea9a7cad22f8fb040f6b3c547a5cf8ef9c5c4c3ff4`  
		Last Modified: Fri, 07 May 2021 19:43:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e743882506113dc5871bca4d0b54de0eaaff274047a425ee9a2cd3dab48d4a69`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b276461d947c4047cdee5f4df593840f8b0d82129041eaf81390d81fc2b11500`  
		Last Modified: Fri, 07 May 2021 19:43:09 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta2` - linux; 386

```console
$ docker pull consul@sha256:9273594603e532ba442c8e9c3248c63cd33271910cbe6f72660be1f420e6be10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42161064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264df230949cdd26b5a182b3ad900563184b660a50c6bac956208833e213384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 07 May 2021 19:38:30 GMT
ARG CONSUL_VERSION=1.10.0-beta2
# Fri, 07 May 2021 19:38:31 GMT
LABEL org.opencontainers.image.version=1.10.0-beta2
# Fri, 07 May 2021 19:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 07 May 2021 19:38:32 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:38:41 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:38:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb331bee2ca3e7c267a54d4cf6b0f05ee087d025b9fad3229cdb154476961bd`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c61cb6421179180cd054b21c4109cfa6bcc4d0441bab43f9bba1db0b573a6b4`  
		Last Modified: Fri, 07 May 2021 19:39:58 GMT  
		Size: 39.4 MB (39361973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234db7ec0bab29592fca3a77fa0b4a9fb100368d27e0410bca10dbfe73672fc4`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1bcdff20cfee8b062b9196399270d0989e07e3525052cf7b98eb6003151a2`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f18752f9628d680b47431e639c740a6220e6318ba593e4c3606330e1c2871d`  
		Last Modified: Fri, 07 May 2021 19:39:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:d5bc1697a589648d5b8bdbf474961f227fd2595bba8540093d1b2b14fbd4de6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:39b85f0bf0d4bfbea54c408d8acbf9de1d8ebb40a700df01a5ffcf25819b3c26
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5cc4b8af79ec6f3f0ccced9e875518bd83b0054f5836f43965c3e79f78826e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:22 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:27 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:29 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:30 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:30 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3500336ca0dccc760254ac4274787d6035ad80339bac4345fd22ebc79a955bac`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63681fede5b4b7f696729a820ab2ad2c5e48760a332774a9e84c64b37c23d8fc`  
		Last Modified: Fri, 07 May 2021 20:21:47 GMT  
		Size: 40.8 MB (40827649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198aca0a6cd7a3a0fe81e2462199c5647ae6ba55badb513146893949a73c333`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb16e29a2099e26e72a04c6e26a3a084c27004458bc660d1ba32e55a61cbc858`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba0dc0e74e18c969fbd07578ef486f86bb211c4d37ba907eb4b6046046c8bcf`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:a9746f9b2d8c5b284b953183aa2667d2cf440558064c1d20c68284c74e115b4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39265662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340995f0284c3832b4f1028d794cc6f5aa3f51f194301ffcf17f05884d000835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:57:12 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:57:18 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:51:44 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:51:49 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:51:58 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:52:01 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:52:06 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:52:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:52:14 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:52:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:52:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5262634fe36fb0e798b90c10b4ef0d64415015c905ca56c9c660be3da5a93acf`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a73131d4aeadb10512c91e9a9a821bfcbef80d221e62fbf90afe8eb043d689`  
		Last Modified: Fri, 07 May 2021 19:54:16 GMT  
		Size: 36.7 MB (36657117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c663af429f7fda9ea899e7398aa4f003f419f29f963365d225524cbba838fff`  
		Last Modified: Fri, 07 May 2021 19:54:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04a4c85505e337faebd040cadda7e0611cecb362ad2d743a49bdb794df5c8e`  
		Last Modified: Fri, 07 May 2021 19:54:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef00affb5efda6eaf09ea93e55ee5a9d9e8da8a9644793bd2834be592e4a855f`  
		Last Modified: Fri, 07 May 2021 19:54:02 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b2c91ce05e046ac5fafde91b4761c05b4141fbad57ea8a94fbb4d9eeb778978c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39540155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c68504ace685875c5531c6703487e7cf1cf7c539f71100c70dcba8c26273f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:41:10 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:41:11 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:41:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:41:14 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:42:41 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:42:44 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:42:46 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:42:46 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:42:47 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:42:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:42:49 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:42:50 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:42:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b27a4ad2a0795e9f8ba72d575c043317cdfd82145646c20c317b7ad79d98d00`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617192fbd83faf55ec6f89e12108f0eaaf8092cbe8d26c5e1aad1a59803d43a`  
		Last Modified: Fri, 07 May 2021 19:44:05 GMT  
		Size: 36.8 MB (36826169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d069c8e1edb3f38c4cc9c7a0d54db50e6063f204dcd45362e68a5e8f00c18b3`  
		Last Modified: Fri, 07 May 2021 19:43:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e4c332f13dd7405cc9eb4377ed5c4b08284ee6c8a509da53163b470d7964`  
		Last Modified: Fri, 07 May 2021 19:43:56 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f965a1cc9605900ee8b9e7678c9c60f3d5bd4942a4a71d1bca18c9e30453fcf`  
		Last Modified: Fri, 07 May 2021 19:43:57 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:7b956c6c7002df613b9047a28ea2d9f48b2f31a0ac67dfc6210bd7686b0689ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42471287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74ab999f2de49db2fbe107bbac2cb1591a6991e3a7cf06a5dfe921853780608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:14 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:16 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:39:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:39:24 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:39:24 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:39:25 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:39:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:39:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:39:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d96f33ee206c0fa6e89a9f3e4b285df1c6822e288430f9c70ed09432729bd45`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23461d0229b5c1339761cacfbd26a338c41fc79c6f51de82b6bf8c7b764c9`  
		Last Modified: Fri, 07 May 2021 19:40:57 GMT  
		Size: 39.7 MB (39672201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef49ca8fc04c808e705b9c507e88b2238d55c1b78e631d6bd4cb42809ebb0eda`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85d0d31d42c7160ba7fb07a4b2c3ca0c4cdd1cf45e2891f8e476dcfc7f834e`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2eb3a58069876aa038b93b775e13649d7fffa4febc4c029b006529e4306e`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.14`

```console
$ docker pull consul@sha256:d5bc1697a589648d5b8bdbf474961f227fd2595bba8540093d1b2b14fbd4de6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.14` - linux; amd64

```console
$ docker pull consul@sha256:39b85f0bf0d4bfbea54c408d8acbf9de1d8ebb40a700df01a5ffcf25819b3c26
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5cc4b8af79ec6f3f0ccced9e875518bd83b0054f5836f43965c3e79f78826e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:22 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:27 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:29 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:30 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:30 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3500336ca0dccc760254ac4274787d6035ad80339bac4345fd22ebc79a955bac`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63681fede5b4b7f696729a820ab2ad2c5e48760a332774a9e84c64b37c23d8fc`  
		Last Modified: Fri, 07 May 2021 20:21:47 GMT  
		Size: 40.8 MB (40827649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198aca0a6cd7a3a0fe81e2462199c5647ae6ba55badb513146893949a73c333`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb16e29a2099e26e72a04c6e26a3a084c27004458bc660d1ba32e55a61cbc858`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba0dc0e74e18c969fbd07578ef486f86bb211c4d37ba907eb4b6046046c8bcf`  
		Last Modified: Fri, 07 May 2021 20:21:40 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:a9746f9b2d8c5b284b953183aa2667d2cf440558064c1d20c68284c74e115b4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39265662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340995f0284c3832b4f1028d794cc6f5aa3f51f194301ffcf17f05884d000835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:57:12 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:57:18 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:51:44 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:51:49 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:51:58 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:52:01 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:52:06 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:52:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:52:14 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:52:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:52:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5262634fe36fb0e798b90c10b4ef0d64415015c905ca56c9c660be3da5a93acf`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a73131d4aeadb10512c91e9a9a821bfcbef80d221e62fbf90afe8eb043d689`  
		Last Modified: Fri, 07 May 2021 19:54:16 GMT  
		Size: 36.7 MB (36657117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c663af429f7fda9ea899e7398aa4f003f419f29f963365d225524cbba838fff`  
		Last Modified: Fri, 07 May 2021 19:54:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b04a4c85505e337faebd040cadda7e0611cecb362ad2d743a49bdb794df5c8e`  
		Last Modified: Fri, 07 May 2021 19:54:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef00affb5efda6eaf09ea93e55ee5a9d9e8da8a9644793bd2834be592e4a855f`  
		Last Modified: Fri, 07 May 2021 19:54:02 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b2c91ce05e046ac5fafde91b4761c05b4141fbad57ea8a94fbb4d9eeb778978c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39540155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c68504ace685875c5531c6703487e7cf1cf7c539f71100c70dcba8c26273f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:41:10 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:41:11 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:41:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:41:14 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:42:41 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:42:44 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:42:46 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:42:46 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:42:47 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:42:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:42:49 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:42:50 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:42:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b27a4ad2a0795e9f8ba72d575c043317cdfd82145646c20c317b7ad79d98d00`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617192fbd83faf55ec6f89e12108f0eaaf8092cbe8d26c5e1aad1a59803d43a`  
		Last Modified: Fri, 07 May 2021 19:44:05 GMT  
		Size: 36.8 MB (36826169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d069c8e1edb3f38c4cc9c7a0d54db50e6063f204dcd45362e68a5e8f00c18b3`  
		Last Modified: Fri, 07 May 2021 19:43:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e4c332f13dd7405cc9eb4377ed5c4b08284ee6c8a509da53163b470d7964`  
		Last Modified: Fri, 07 May 2021 19:43:56 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f965a1cc9605900ee8b9e7678c9c60f3d5bd4942a4a71d1bca18c9e30453fcf`  
		Last Modified: Fri, 07 May 2021 19:43:57 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; 386

```console
$ docker pull consul@sha256:7b956c6c7002df613b9047a28ea2d9f48b2f31a0ac67dfc6210bd7686b0689ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42471287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74ab999f2de49db2fbe107bbac2cb1591a6991e3a7cf06a5dfe921853780608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:14 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:16 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:39:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:39:24 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:39:24 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:39:25 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:39:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:39:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:39:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:39:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d96f33ee206c0fa6e89a9f3e4b285df1c6822e288430f9c70ed09432729bd45`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23461d0229b5c1339761cacfbd26a338c41fc79c6f51de82b6bf8c7b764c9`  
		Last Modified: Fri, 07 May 2021 19:40:57 GMT  
		Size: 39.7 MB (39672201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef49ca8fc04c808e705b9c507e88b2238d55c1b78e631d6bd4cb42809ebb0eda`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85d0d31d42c7160ba7fb07a4b2c3ca0c4cdd1cf45e2891f8e476dcfc7f834e`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2eb3a58069876aa038b93b775e13649d7fffa4febc4c029b006529e4306e`  
		Last Modified: Fri, 07 May 2021 19:40:51 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:171e38d31c520698010084c3630977c44d79e30a8dd290d3ceffebd1995211a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:6fdf46efc19683e9fb0a1709695c0ee91ec76a583967741b8dc91e4d5dfb0ca3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47026042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a90cfdff762bf027488f15785e5a4716fdbe91f79c8c8c50639f0d28eeb6bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:08 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:16 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:18 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:18 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:18 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:19 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:19 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31fd7759efe4085bbe76d93789a91b3632bc1789749ef935f4cc4ebb4e28792`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032932a7b5e32ea020aba43dcb999d730ea228c6956ca5af99656f2aea2146e3`  
		Last Modified: Fri, 07 May 2021 20:21:29 GMT  
		Size: 44.2 MB (44222183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78ea22fcb2995db4bda540d8c17d75fafefe7fa228c73d08dc1cf03c0c8866`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47277a36bc521459f3004b20570d18601338f36dd523fd5aa1f97ec6da618f7`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770de61b17187c34303cc4e32f9b66cb31c55c0b8d99326d90f196e10cbf635d`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:36af2170fc936ffe8054b846a8e1cd1497b18c3071e45607e6ad192c9dba60c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42219338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0c10060e4114a82981c6eff0b763560ed84ceac269ae5f3c464b4b56a363c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:56:35 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:56:35 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:56:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:56:39 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:50:55 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:51:04 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:51:15 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:51:17 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:51:19 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:51:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:51:24 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:51:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:51:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675002a1a68b19d06e2736487641c5f05deb675397793969ee882f3305c3d141`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f84473f0d4629ad435dda176a2d3287169bac90954610463c5d404d5082c6a`  
		Last Modified: Fri, 07 May 2021 19:53:55 GMT  
		Size: 39.6 MB (39610789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b676651dbc15a96dc2be738696f001f7a35a6a5f91ef3fe32e03a94831a9d9d`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f196163c1c958a39bf1954ba0acc6a6bf2c414adde20051851b5a3018e5d3cd4`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2048333dd919f9e0df4420a24fde364c233519c6c31c64317fe5005c39e8a34`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:c23646d9b02a805a67cfb690bd56e9442307952c0a45e873f1c641823a8bd271
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275d3ce26d5576cb97f96ea6c7288aa88fdd09e68123f08b7f8d370b372ee31b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:43 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:47 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:42:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:42:20 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:42:22 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:42:22 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:42:23 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:42:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:42:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:42:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:42:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84076eb9bf0d9df8a9719fcbef511c596df8b3a98029728b9a641fc1b1bb35c`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86a51a0fbd6f0cdb2501b8af86b09c9fa7101b7ec0f6acc8990b4e873ea5900`  
		Last Modified: Fri, 07 May 2021 19:43:50 GMT  
		Size: 39.7 MB (39736201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cec0d7d4870ad79591b530086c53f147b774c88f9d2b77ee4f135772e9b0d3c`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb346b406350bf9a36b20ea4c5534ba60c4c38e6498441bdb82f24e28063f08`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a361af04af044e082ec097ea6da9ebe0fbc05a441498efb528e260264f4e356`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:a64334fa7468ff162337038396de8f18e299c66a60d302413a23427fc3e07e2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46576442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43eea70184b84f22162d23ce686373d2749d4971ac813b796662c5ab436e565`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:58 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:59 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:39:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:39:11 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:39:12 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:39:12 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:39:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:39:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:39:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f59dcd1edd92c70cabaf1b1d5a78dc21cdede8bd0d2c2650d0d0844ff1949da`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdcac94f5b0c5fbe89cabc22db6bcedbb83b77e408021e1f48c827bec6069fc`  
		Last Modified: Fri, 07 May 2021 19:40:39 GMT  
		Size: 43.8 MB (43777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4bfebd2f15fcedf5997f66ff5917d8860364077160c6b88ab6185da83df1a4`  
		Last Modified: Fri, 07 May 2021 19:40:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683301a7c91ba58435d9201fd611012461c13d87af9b9e573731ca2ecc43c62c`  
		Last Modified: Fri, 07 May 2021 19:40:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368aa732b1f78064d2fe7f560c8567de6a010b85e095140ca6e67954cbbf2e2`  
		Last Modified: Fri, 07 May 2021 19:40:32 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.10`

```console
$ docker pull consul@sha256:171e38d31c520698010084c3630977c44d79e30a8dd290d3ceffebd1995211a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.10` - linux; amd64

```console
$ docker pull consul@sha256:6fdf46efc19683e9fb0a1709695c0ee91ec76a583967741b8dc91e4d5dfb0ca3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47026042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a90cfdff762bf027488f15785e5a4716fdbe91f79c8c8c50639f0d28eeb6bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:08 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:16 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:18 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:18 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:18 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:19 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:19 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31fd7759efe4085bbe76d93789a91b3632bc1789749ef935f4cc4ebb4e28792`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032932a7b5e32ea020aba43dcb999d730ea228c6956ca5af99656f2aea2146e3`  
		Last Modified: Fri, 07 May 2021 20:21:29 GMT  
		Size: 44.2 MB (44222183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78ea22fcb2995db4bda540d8c17d75fafefe7fa228c73d08dc1cf03c0c8866`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47277a36bc521459f3004b20570d18601338f36dd523fd5aa1f97ec6da618f7`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770de61b17187c34303cc4e32f9b66cb31c55c0b8d99326d90f196e10cbf635d`  
		Last Modified: Fri, 07 May 2021 20:21:23 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:36af2170fc936ffe8054b846a8e1cd1497b18c3071e45607e6ad192c9dba60c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42219338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0c10060e4114a82981c6eff0b763560ed84ceac269ae5f3c464b4b56a363c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:56:35 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:56:35 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:56:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:56:39 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:50:55 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:51:04 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:51:15 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:51:17 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:51:19 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:51:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:51:24 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:51:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:51:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675002a1a68b19d06e2736487641c5f05deb675397793969ee882f3305c3d141`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f84473f0d4629ad435dda176a2d3287169bac90954610463c5d404d5082c6a`  
		Last Modified: Fri, 07 May 2021 19:53:55 GMT  
		Size: 39.6 MB (39610789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b676651dbc15a96dc2be738696f001f7a35a6a5f91ef3fe32e03a94831a9d9d`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f196163c1c958a39bf1954ba0acc6a6bf2c414adde20051851b5a3018e5d3cd4`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2048333dd919f9e0df4420a24fde364c233519c6c31c64317fe5005c39e8a34`  
		Last Modified: Fri, 07 May 2021 19:53:41 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:c23646d9b02a805a67cfb690bd56e9442307952c0a45e873f1c641823a8bd271
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42450185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275d3ce26d5576cb97f96ea6c7288aa88fdd09e68123f08b7f8d370b372ee31b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:43 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:47 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:42:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:42:20 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:42:22 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:42:22 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:42:23 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:42:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:42:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:42:25 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:42:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:42:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84076eb9bf0d9df8a9719fcbef511c596df8b3a98029728b9a641fc1b1bb35c`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86a51a0fbd6f0cdb2501b8af86b09c9fa7101b7ec0f6acc8990b4e873ea5900`  
		Last Modified: Fri, 07 May 2021 19:43:50 GMT  
		Size: 39.7 MB (39736201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cec0d7d4870ad79591b530086c53f147b774c88f9d2b77ee4f135772e9b0d3c`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb346b406350bf9a36b20ea4c5534ba60c4c38e6498441bdb82f24e28063f08`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a361af04af044e082ec097ea6da9ebe0fbc05a441498efb528e260264f4e356`  
		Last Modified: Fri, 07 May 2021 19:43:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; 386

```console
$ docker pull consul@sha256:a64334fa7468ff162337038396de8f18e299c66a60d302413a23427fc3e07e2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46576442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43eea70184b84f22162d23ce686373d2749d4971ac813b796662c5ab436e565`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:58 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:59 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:39:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:39:11 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:39:12 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:39:12 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:39:12 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:39:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:39:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:39:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f59dcd1edd92c70cabaf1b1d5a78dc21cdede8bd0d2c2650d0d0844ff1949da`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdcac94f5b0c5fbe89cabc22db6bcedbb83b77e408021e1f48c827bec6069fc`  
		Last Modified: Fri, 07 May 2021 19:40:39 GMT  
		Size: 43.8 MB (43777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4bfebd2f15fcedf5997f66ff5917d8860364077160c6b88ab6185da83df1a4`  
		Last Modified: Fri, 07 May 2021 19:40:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683301a7c91ba58435d9201fd611012461c13d87af9b9e573731ca2ecc43c62c`  
		Last Modified: Fri, 07 May 2021 19:40:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368aa732b1f78064d2fe7f560c8567de6a010b85e095140ca6e67954cbbf2e2`  
		Last Modified: Fri, 07 May 2021 19:40:32 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:c4a072f35aaf9f8d91d27b85a112457a572c52608f5aba3fe23759e6ed83bbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:092a641becbdb41fa0f1826735eaeebecca5a13a445b5efd4ddde8d977a42cc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e37a98f785e754896399ad511b2185e55c5b3eea954b58dfd11e32a08ece4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:04 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:05 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:07 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:08 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fcbcbcc3534ee83f0b25808f6573d5fd820496b5978d547d25c6672348d388`  
		Last Modified: Fri, 07 May 2021 20:21:09 GMT  
		Size: 43.4 MB (43392921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac12abe7a1d4c17500514d082d69b899725bf4791bf23a3298e949a705396519`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917bb6904142b9e755e4d9d4659efc4dff6b3d3fb924eb3cc89ec8601858ca65`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1aa76c5db67a8ff43a6c4ae95a19978ab1338e9daf129a000c903160f88b8b`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:1f64140fb9db33b350e1019e56489b122eb4167161dc9a1ab9ef46c7d2c230bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2146bac966dd772c2d932d31cbc6221369957a59084aa204acab38d474fb7bb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:50:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:50:29 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:50:31 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:50:32 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:50:33 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:50:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:50:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:50:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:50:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:50:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcddce7ce75931bceabbe3bdb273b7b02776c0d673c254ec6fb1aa0c48545158`  
		Last Modified: Fri, 07 May 2021 19:53:33 GMT  
		Size: 38.8 MB (38753144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41a6d5c48fe6d1da2f8cb22ae90f07a61beccee1825d1cc18b39c0d94889001`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17978f8b194371049a088a13cc022a74fea77fffca88fa45a89c4de9fbcdeb59`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae00f1101cb18324b0fd58088285423e0d2eeed7914391196f4aee0145bda14`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2af77af48392abeb99e56abe088a8b5b69ac8d6d10739bf31c49a40aef618630
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3254bc12ab453935808cd0eeae3a2b805c0f24e4fe52e51a348db73268bea02f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:41:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:41:45 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:41:47 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:41:48 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:41:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:41:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:41:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:41:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c0fcf66b167a68bc154a5067c6f2fb08d07c0ad57f138d528ac5c2531207`  
		Last Modified: Fri, 07 May 2021 19:43:32 GMT  
		Size: 38.9 MB (38926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd73357d8ec125a8897d9cab908ef40cce16b6f85d55adb97e9192441bb1fffe`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295f9b7d1d2d30104f6ba85fd5074cf561b0b4d772b465b14018f2b3061ad35`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130f3b1059e8c775955fa1f2991e0de8323451c74a1f6119f38dcc39dccee6a2`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:29db65ecf594897e86f6df1335337093dff08bdce18d9de413495c0e9fd49d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889cd77e4eeeda74555d1e24f2bc7448f5be755c407828719dfb5ab93d97ddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:38:56 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:38:57 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:38:58 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:38:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce95f5e7a87ca85a91ecc5a5ec9bbf163d22684bb544fd248ef760b3419fdcd`  
		Last Modified: Fri, 07 May 2021 19:40:16 GMT  
		Size: 42.8 MB (42750629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696b0c39fbf4a398d03b342f94b8dbf3618068c6a47e813226171589936ede9`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6acff100e571a7d633c0e4222cf98bc56191fd6b87f1f6d67026d55444da8b`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8de5224d105c760b27e4c25fe2a7b0ef2ee94dbc86cd06b46125d70bbf00`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.5`

```console
$ docker pull consul@sha256:c4a072f35aaf9f8d91d27b85a112457a572c52608f5aba3fe23759e6ed83bbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.5` - linux; amd64

```console
$ docker pull consul@sha256:092a641becbdb41fa0f1826735eaeebecca5a13a445b5efd4ddde8d977a42cc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e37a98f785e754896399ad511b2185e55c5b3eea954b58dfd11e32a08ece4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:04 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:05 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:07 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:08 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fcbcbcc3534ee83f0b25808f6573d5fd820496b5978d547d25c6672348d388`  
		Last Modified: Fri, 07 May 2021 20:21:09 GMT  
		Size: 43.4 MB (43392921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac12abe7a1d4c17500514d082d69b899725bf4791bf23a3298e949a705396519`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917bb6904142b9e755e4d9d4659efc4dff6b3d3fb924eb3cc89ec8601858ca65`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1aa76c5db67a8ff43a6c4ae95a19978ab1338e9daf129a000c903160f88b8b`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:1f64140fb9db33b350e1019e56489b122eb4167161dc9a1ab9ef46c7d2c230bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2146bac966dd772c2d932d31cbc6221369957a59084aa204acab38d474fb7bb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:50:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:50:29 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:50:31 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:50:32 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:50:33 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:50:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:50:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:50:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:50:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:50:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcddce7ce75931bceabbe3bdb273b7b02776c0d673c254ec6fb1aa0c48545158`  
		Last Modified: Fri, 07 May 2021 19:53:33 GMT  
		Size: 38.8 MB (38753144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41a6d5c48fe6d1da2f8cb22ae90f07a61beccee1825d1cc18b39c0d94889001`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17978f8b194371049a088a13cc022a74fea77fffca88fa45a89c4de9fbcdeb59`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae00f1101cb18324b0fd58088285423e0d2eeed7914391196f4aee0145bda14`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2af77af48392abeb99e56abe088a8b5b69ac8d6d10739bf31c49a40aef618630
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3254bc12ab453935808cd0eeae3a2b805c0f24e4fe52e51a348db73268bea02f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:41:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:41:45 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:41:47 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:41:48 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:41:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:41:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:41:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:41:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c0fcf66b167a68bc154a5067c6f2fb08d07c0ad57f138d528ac5c2531207`  
		Last Modified: Fri, 07 May 2021 19:43:32 GMT  
		Size: 38.9 MB (38926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd73357d8ec125a8897d9cab908ef40cce16b6f85d55adb97e9192441bb1fffe`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295f9b7d1d2d30104f6ba85fd5074cf561b0b4d772b465b14018f2b3061ad35`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130f3b1059e8c775955fa1f2991e0de8323451c74a1f6119f38dcc39dccee6a2`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; 386

```console
$ docker pull consul@sha256:29db65ecf594897e86f6df1335337093dff08bdce18d9de413495c0e9fd49d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889cd77e4eeeda74555d1e24f2bc7448f5be755c407828719dfb5ab93d97ddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:38:56 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:38:57 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:38:58 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:38:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce95f5e7a87ca85a91ecc5a5ec9bbf163d22684bb544fd248ef760b3419fdcd`  
		Last Modified: Fri, 07 May 2021 19:40:16 GMT  
		Size: 42.8 MB (42750629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696b0c39fbf4a398d03b342f94b8dbf3618068c6a47e813226171589936ede9`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6acff100e571a7d633c0e4222cf98bc56191fd6b87f1f6d67026d55444da8b`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8de5224d105c760b27e4c25fe2a7b0ef2ee94dbc86cd06b46125d70bbf00`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:c4a072f35aaf9f8d91d27b85a112457a572c52608f5aba3fe23759e6ed83bbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:092a641becbdb41fa0f1826735eaeebecca5a13a445b5efd4ddde8d977a42cc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e37a98f785e754896399ad511b2185e55c5b3eea954b58dfd11e32a08ece4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 20:20:04 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 20:20:05 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 20:20:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 20:20:07 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8300
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 20:20:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 20:20:08 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 20:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 20:20:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fcbcbcc3534ee83f0b25808f6573d5fd820496b5978d547d25c6672348d388`  
		Last Modified: Fri, 07 May 2021 20:21:09 GMT  
		Size: 43.4 MB (43392921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac12abe7a1d4c17500514d082d69b899725bf4791bf23a3298e949a705396519`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917bb6904142b9e755e4d9d4659efc4dff6b3d3fb924eb3cc89ec8601858ca65`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1aa76c5db67a8ff43a6c4ae95a19978ab1338e9daf129a000c903160f88b8b`  
		Last Modified: Fri, 07 May 2021 20:21:03 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:1f64140fb9db33b350e1019e56489b122eb4167161dc9a1ab9ef46c7d2c230bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2146bac966dd772c2d932d31cbc6221369957a59084aa204acab38d474fb7bb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:50:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:50:29 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:50:31 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:50:32 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:50:33 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:50:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:50:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:50:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:50:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:50:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcddce7ce75931bceabbe3bdb273b7b02776c0d673c254ec6fb1aa0c48545158`  
		Last Modified: Fri, 07 May 2021 19:53:33 GMT  
		Size: 38.8 MB (38753144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41a6d5c48fe6d1da2f8cb22ae90f07a61beccee1825d1cc18b39c0d94889001`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17978f8b194371049a088a13cc022a74fea77fffca88fa45a89c4de9fbcdeb59`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae00f1101cb18324b0fd58088285423e0d2eeed7914391196f4aee0145bda14`  
		Last Modified: Fri, 07 May 2021 19:53:23 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:2af77af48392abeb99e56abe088a8b5b69ac8d6d10739bf31c49a40aef618630
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3254bc12ab453935808cd0eeae3a2b805c0f24e4fe52e51a348db73268bea02f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:41:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:41:45 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:41:47 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:41:48 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:41:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:41:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:41:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:41:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:41:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c0fcf66b167a68bc154a5067c6f2fb08d07c0ad57f138d528ac5c2531207`  
		Last Modified: Fri, 07 May 2021 19:43:32 GMT  
		Size: 38.9 MB (38926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd73357d8ec125a8897d9cab908ef40cce16b6f85d55adb97e9192441bb1fffe`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295f9b7d1d2d30104f6ba85fd5074cf561b0b4d772b465b14018f2b3061ad35`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130f3b1059e8c775955fa1f2991e0de8323451c74a1f6119f38dcc39dccee6a2`  
		Last Modified: Fri, 07 May 2021 19:43:24 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:29db65ecf594897e86f6df1335337093dff08bdce18d9de413495c0e9fd49d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889cd77e4eeeda74555d1e24f2bc7448f5be755c407828719dfb5ab93d97ddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 07 May 2021 19:38:56 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 07 May 2021 19:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 07 May 2021 19:38:57 GMT
VOLUME [/consul/data]
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8300
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 07 May 2021 19:38:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 07 May 2021 19:38:58 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 07 May 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 May 2021 19:38:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce95f5e7a87ca85a91ecc5a5ec9bbf163d22684bb544fd248ef760b3419fdcd`  
		Last Modified: Fri, 07 May 2021 19:40:16 GMT  
		Size: 42.8 MB (42750629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696b0c39fbf4a398d03b342f94b8dbf3618068c6a47e813226171589936ede9`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6acff100e571a7d633c0e4222cf98bc56191fd6b87f1f6d67026d55444da8b`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af8de5224d105c760b27e4c25fe2a7b0ef2ee94dbc86cd06b46125d70bbf00`  
		Last Modified: Fri, 07 May 2021 19:40:10 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
