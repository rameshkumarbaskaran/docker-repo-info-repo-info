<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.2`](#consul1102)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.15`](#consul1815)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.9`](#consul199)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:fba4745a0fa7573ddf4671538e7857d2d1342ec85b0854f6bd304c1257d66e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:2c69d8bee4e99c083f0930bc09cdd45b88365ae6b427221283502230ba1c1ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74a0a01afc431799adac9d7911b8e0d6961a3b9909380ec61af211e342f7a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:13:55 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 00:13:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:13:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:13:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:15 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:17 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:19 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:19 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:21 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:21 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f992def430ed8f2556f38262c7a72f4b73b90938c7b10d23ee8948153f50`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e185403d62712206d4d670a6dc1e9343046bcc9d308944262faeb165ab68a3`  
		Last Modified: Wed, 01 Sep 2021 00:15:47 GMT  
		Size: 40.4 MB (40402053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efdf2644d28f50e4d3a9beec818e4edd8d3af82a0b5154e335b0278e6da441`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a8413c32a8e922dbaba4d4e1028376cf9f171f84083e0bdf28e5921f37486`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b82ffb99af04063532bb252dc67c726dc483d2b709022906503c446ab3725`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:1d983545c4f84b1cd3c7ce4d838e166c65a925693844cfd5ed5c4746e204c881
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39244219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbff18b6c799e1a17924a92190f3411c4726b7afbeaa5ebc1351581730b23e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:23:36 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 01:23:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:23:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:23:38 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:23:53 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:23:55 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:23:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:23:57 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:23:57 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:23:59 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:24:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffb408206870dbfae898542f9fe08defc3d55425b9287f67b4e7bc9639b04d`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9f1d264c506179627ab82efe2c2f5b2a52cfb7e2e736e8f3b883acb84c30c`  
		Last Modified: Wed, 01 Sep 2021 01:26:14 GMT  
		Size: 36.6 MB (36617160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f321a2bdffc01f4f3cfc903b8d00c4711968c30929a7ba2208e54efc88b8974`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7731df45612e290f1b44073d40ca132679f33d61eb153abf17aecf4b0101f5`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313ef0d18b912146cb45f58d8570c5b193973da8ee33b986cf43d5df8f65e2df`  
		Last Modified: Wed, 01 Sep 2021 01:25:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:0081f4b20a6b484746ee30b2ede4f64241d94721c18b9c115ce61b88ca6588d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c65b74aabe05fbf0444ae754a6cf8bea788f8854c719189eecb6501793f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:33 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:19:33 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:19:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:40 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:41 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:41 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0bca027d4ed5928a09c462f06be2502d9e6dfd78d9ba3c527dc500cfcdfca`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b3128d8785d803695d60c92ef9482ab1ddc021eeb844a226ba40208ccb0a54`  
		Last Modified: Fri, 23 Jul 2021 04:20:40 GMT  
		Size: 36.9 MB (36869818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbf322ffab66a9b685be5eb28cf5499c409303c57282a74d1c3c7380cf2f5f7`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f3c6fd6c3e6a3b608722cdf776c98efb4d2ab2be357bf99716b7e6f5e8343`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418597e612cf3477bacd0c9730131f6a619802a05c2a5c37081550ec54fc2c60`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:17b520004b3a2623633c14b821adc7778348bb537ebfff5c60d2748d1459fbe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42597058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bedb65efe9b810ad73be975f82bd07358370d092f78608e1525f0f823239fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:23:44 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 03:23:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:23:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:23:46 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:01 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:03 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:04 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f7da53f439d00a34afad277f271e8d6601a55ad5425c7bab343206a090cbfd`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9bb807469664b1b7e9f2f39ec258ebeec3b98bd419fd12626039ac3d1373a`  
		Last Modified: Wed, 01 Sep 2021 03:25:31 GMT  
		Size: 39.8 MB (39772664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbcae0f50b0a16668a6242b7f4b2a37eb7bbba9ab5c681eef394b7744b2d5a1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6937a39eb1646e9da4597ac1ab4f329d69be5d448caee72177fd50a6b48823`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63276123b2c6bdf440e367d51a11433671f86ed4afec2bda8c94112e1697cb1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.2`

```console
$ docker pull consul@sha256:98fc190e2e7300211538bda275b07765fa6b68ffb9c43f1af78d868f8a1e5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.10.2` - linux; amd64

```console
$ docker pull consul@sha256:2c69d8bee4e99c083f0930bc09cdd45b88365ae6b427221283502230ba1c1ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74a0a01afc431799adac9d7911b8e0d6961a3b9909380ec61af211e342f7a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:13:55 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 00:13:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:13:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:13:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:15 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:17 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:19 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:19 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:21 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:21 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f992def430ed8f2556f38262c7a72f4b73b90938c7b10d23ee8948153f50`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e185403d62712206d4d670a6dc1e9343046bcc9d308944262faeb165ab68a3`  
		Last Modified: Wed, 01 Sep 2021 00:15:47 GMT  
		Size: 40.4 MB (40402053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efdf2644d28f50e4d3a9beec818e4edd8d3af82a0b5154e335b0278e6da441`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a8413c32a8e922dbaba4d4e1028376cf9f171f84083e0bdf28e5921f37486`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b82ffb99af04063532bb252dc67c726dc483d2b709022906503c446ab3725`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.2` - linux; arm variant v6

```console
$ docker pull consul@sha256:1d983545c4f84b1cd3c7ce4d838e166c65a925693844cfd5ed5c4746e204c881
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39244219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbff18b6c799e1a17924a92190f3411c4726b7afbeaa5ebc1351581730b23e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:23:36 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 01:23:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:23:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:23:38 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:23:53 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:23:55 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:23:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:23:57 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:23:57 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:23:59 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:24:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffb408206870dbfae898542f9fe08defc3d55425b9287f67b4e7bc9639b04d`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9f1d264c506179627ab82efe2c2f5b2a52cfb7e2e736e8f3b883acb84c30c`  
		Last Modified: Wed, 01 Sep 2021 01:26:14 GMT  
		Size: 36.6 MB (36617160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f321a2bdffc01f4f3cfc903b8d00c4711968c30929a7ba2208e54efc88b8974`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7731df45612e290f1b44073d40ca132679f33d61eb153abf17aecf4b0101f5`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313ef0d18b912146cb45f58d8570c5b193973da8ee33b986cf43d5df8f65e2df`  
		Last Modified: Wed, 01 Sep 2021 01:25:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.2` - linux; 386

```console
$ docker pull consul@sha256:17b520004b3a2623633c14b821adc7778348bb537ebfff5c60d2748d1459fbe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42597058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bedb65efe9b810ad73be975f82bd07358370d092f78608e1525f0f823239fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:23:44 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 03:23:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:23:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:23:46 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:01 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:03 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:04 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f7da53f439d00a34afad277f271e8d6601a55ad5425c7bab343206a090cbfd`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9bb807469664b1b7e9f2f39ec258ebeec3b98bd419fd12626039ac3d1373a`  
		Last Modified: Wed, 01 Sep 2021 03:25:31 GMT  
		Size: 39.8 MB (39772664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbcae0f50b0a16668a6242b7f4b2a37eb7bbba9ab5c681eef394b7744b2d5a1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6937a39eb1646e9da4597ac1ab4f329d69be5d448caee72177fd50a6b48823`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63276123b2c6bdf440e367d51a11433671f86ed4afec2bda8c94112e1697cb1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:8488fd252de4b256fc0bda23b0f6ac351de16110b0961c24df8316551f664970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:c0c9ec672dcf87c94bb555080b187d1e9254a60e2d9100904b0b15217f6298a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47432770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d457d6d43b12eb65504a59bfdcd71e930c56063b7eebba1dbe5dd8c946a3b7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:53 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 00:14:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:56 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:15:10 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:15:12 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:15:14 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:15:14 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:15:16 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:15:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0022ca2a5ccb519cc3605c37a29ef3a45038c36c196ec86055031a29fce2240a`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522424ab277ad162c8bfb55a2a14da0ac041b7785afef0528193f8b8a4dcdb7`  
		Last Modified: Wed, 01 Sep 2021 00:16:28 GMT  
		Size: 44.6 MB (44615396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6252447adce3c19393d4834b6a26429bcd0e9c7eb56284a2d0a910331c9710`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78b1ee93bf1b3b98bf06fecbbce5615b42405d83038ce1edeb26ef09c99b77`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31049982da237f431af58917845758512e4f3a00364a42f514a0761160498487`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:241b664e74d56eef760b2d272823c72658cdfa91ad48c6a17bc7310e79494445
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42632267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee290d13863b92cb4dbf97358f0068ec82960fd08f3c850a8ec817b45517b3bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:24:45 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 01:24:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:24:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:24:47 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:25:02 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:25:05 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:25:06 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:25:06 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:25:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:25:07 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:25:08 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:25:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4032e2b228f5ccc60ad07cf4ee3c170b47343148c637c28756f8cf146f89777`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b88d25a5bd50a0edc81f693360277e6aa2fc524c88b6fdf2a161e0463e6e92`  
		Last Modified: Wed, 01 Sep 2021 01:27:27 GMT  
		Size: 40.0 MB (40005213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38221551fcf9fd648f92570791f0770e3c877b1407311de72a16bcb0631df7cf`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fecfea8691076952fc775dcf1f84c509e45bb5f24ade12f75e396ef74c829b`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a218640f987b62022aae2ea74520f96544c9aaceb6ded72d19981308f18fa3`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:c37cd7c096c4a934d7095ba5dbe5b05d8841aebeeb47afd80b7cce3104b235b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cfde2c2c6d82ab2b74b9594be5f5f58d648747649a329cdcc46694d93f8144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:20:02 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:20:03 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:20:08 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:20:09 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:20:10 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:20:10 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:20:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:20:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cc36a972be65ab045851033f56e745ea4f4678929bce70330e8af9769a6de`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98890b27f5655b4e3c19e344c6b9a207eba9ed9001964fe7b3fdc0cbffe2675c`  
		Last Modified: Fri, 23 Jul 2021 04:21:19 GMT  
		Size: 40.5 MB (40515268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94ee3335668307662b7979c8f5823acbe7721dc8ee8ca6aaf811fdbf98aa9f5`  
		Last Modified: Fri, 23 Jul 2021 04:21:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ac26ba2e3632a67ccf90d5d45b54ffa2524c9e9cfb7f2c39d98cfc3af61f60`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5a760885ea0a6fbb9d790eca5c1b90b5def97ab9b489273e8bc37173f4170`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:27da86b0950ee599f7ccff2d783a04f75e3973daef248219989ab7751b28b5a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46978233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de21118e69353111803a381061dbdad716be322fe79601af106c7b359f5d93d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:24:35 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 03:24:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:24:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:24:36 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:43 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:44 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:45 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:45 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:46 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a210321841f927c4c3ed807c1557b050826c21980fb1ed5e60596a53985d5f7c`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7a79e76973114c4adcd314b9fef0913508d44d00dcd41ac51d6c22ca165f72`  
		Last Modified: Wed, 01 Sep 2021 03:26:28 GMT  
		Size: 44.2 MB (44153838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f044d34d1a827204be61dc3d802718dc2a8697cc5d7ea57c345de653df14825`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38c18a9e489836a7e15c4967fe3eea362c3359e04a64dabe73f9c4b62eb7969`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdf0b4c72abb1c51b87951bb6f7dd509d147a7a7346e2fa374b6d4de84c175b`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.15`

```console
$ docker pull consul@sha256:461527cb7f06455ac52a05754f463171e6ae1c8b208a36a7818caa784250dd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.8.15` - linux; amd64

```console
$ docker pull consul@sha256:c0c9ec672dcf87c94bb555080b187d1e9254a60e2d9100904b0b15217f6298a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47432770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d457d6d43b12eb65504a59bfdcd71e930c56063b7eebba1dbe5dd8c946a3b7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:53 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 00:14:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:56 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:15:10 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:15:12 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:15:14 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:15:14 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:15:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:15:16 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:15:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0022ca2a5ccb519cc3605c37a29ef3a45038c36c196ec86055031a29fce2240a`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522424ab277ad162c8bfb55a2a14da0ac041b7785afef0528193f8b8a4dcdb7`  
		Last Modified: Wed, 01 Sep 2021 00:16:28 GMT  
		Size: 44.6 MB (44615396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6252447adce3c19393d4834b6a26429bcd0e9c7eb56284a2d0a910331c9710`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78b1ee93bf1b3b98bf06fecbbce5615b42405d83038ce1edeb26ef09c99b77`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31049982da237f431af58917845758512e4f3a00364a42f514a0761160498487`  
		Last Modified: Wed, 01 Sep 2021 00:16:20 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.15` - linux; arm variant v6

```console
$ docker pull consul@sha256:241b664e74d56eef760b2d272823c72658cdfa91ad48c6a17bc7310e79494445
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42632267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee290d13863b92cb4dbf97358f0068ec82960fd08f3c850a8ec817b45517b3bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:24:45 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 01:24:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:24:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:24:47 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:25:02 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:25:05 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:25:06 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:25:06 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:25:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:25:07 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:25:08 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:25:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4032e2b228f5ccc60ad07cf4ee3c170b47343148c637c28756f8cf146f89777`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b88d25a5bd50a0edc81f693360277e6aa2fc524c88b6fdf2a161e0463e6e92`  
		Last Modified: Wed, 01 Sep 2021 01:27:27 GMT  
		Size: 40.0 MB (40005213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38221551fcf9fd648f92570791f0770e3c877b1407311de72a16bcb0631df7cf`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fecfea8691076952fc775dcf1f84c509e45bb5f24ade12f75e396ef74c829b`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a218640f987b62022aae2ea74520f96544c9aaceb6ded72d19981308f18fa3`  
		Last Modified: Wed, 01 Sep 2021 01:27:06 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.15` - linux; 386

```console
$ docker pull consul@sha256:27da86b0950ee599f7ccff2d783a04f75e3973daef248219989ab7751b28b5a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46978233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de21118e69353111803a381061dbdad716be322fe79601af106c7b359f5d93d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:24:35 GMT
ARG CONSUL_VERSION=1.8.15
# Wed, 01 Sep 2021 03:24:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.15 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:24:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:24:36 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:43 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:44 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:45 GMT
# ARGS: CONSUL_VERSION=1.8.15
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:45 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:46 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a210321841f927c4c3ed807c1557b050826c21980fb1ed5e60596a53985d5f7c`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7a79e76973114c4adcd314b9fef0913508d44d00dcd41ac51d6c22ca165f72`  
		Last Modified: Wed, 01 Sep 2021 03:26:28 GMT  
		Size: 44.2 MB (44153838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f044d34d1a827204be61dc3d802718dc2a8697cc5d7ea57c345de653df14825`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38c18a9e489836a7e15c4967fe3eea362c3359e04a64dabe73f9c4b62eb7969`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdf0b4c72abb1c51b87951bb6f7dd509d147a7a7346e2fa374b6d4de84c175b`  
		Last Modified: Wed, 01 Sep 2021 03:26:16 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:2794fcb8e6551d867bd4af5bd1f806df7e36fea4ad67f64862c6aeacdfad02fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:d08355ef1555bb782d486bc903bf75d397a32ed38f16d033b1e1cc28392b702e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45890066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f5d27f4606766adacd7db1f010bc5f056b9411c6285d981c2122cf143a6696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:27 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 00:14:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:30 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:42 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:43 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:45 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:45 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:46 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002deffc8d522ac27816e38f624fb99eb60e144f5ddae64c1db963f9f1f71c5`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585556722091a5853a673738ea0566385bddf805ae5d39b3ed5d875b1886bb8a`  
		Last Modified: Wed, 01 Sep 2021 00:16:10 GMT  
		Size: 43.1 MB (43072684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4118856830e8594ee52c9ce8f3c1a8130af6b714e1ea7d33eed9399a313ace`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76ee2bdeec48e7dbda3f1f9e1ccd0decaa72db4e54b2de9563763e3ec68be6d`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0d9dcde6a01972e13fc192727e0831d3b9ecd74412e8b9df5bc22baaf84a0`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:0c4233085f4b5c606bc137959ba0efafbe3d62d0d7f97c617ff953761b483dea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada64b389b255aa86e91ca04ad7d76cb932e6e15cb27f007043f615cf0e94835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:24:11 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 01:24:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:24:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:24:14 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:24:27 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:24:29 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:24:31 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:24:31 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:24:32 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:24:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:24:33 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:24:33 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:24:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:24:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5077d694d8b4f4026a8ccddc072bba9850729ab8c83942c7083de1e084293d`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e53b7f51828dd128841f1ce6911e1a708bb684ba6004a8aaf0d87725caf6a`  
		Last Modified: Wed, 01 Sep 2021 01:26:52 GMT  
		Size: 38.4 MB (38449829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595e3a03716ffd8c1ce7f7e386e06f55eb85b2684bd1da366751494861ae6e`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573fb312b7f1723a8073db0d55c0de12c6a35639cac51774a02b0424b2ef4f65`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c0fa773cd8c9b01159940ec6958165c652889dfc420ae517b7272dee17fdaa`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3ab243a22e89032c573560ba2682aa7fad92a0e86142c3ed5706c48f514af8ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41738920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef1d30cb383b4ec553439ee5154aaf85c52a2112827156b93300011252aee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:48 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:49 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:54 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:55 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:56 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:56 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b35a934ecade634b58bf55698d2b60aee4cec01f90f3a03e09672aea20b72fd`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35566cf101e3ccb53cedd918658c3a2ff588b51f2bf4f4cd7ed6815b5bafdd8b`  
		Last Modified: Fri, 23 Jul 2021 04:21:01 GMT  
		Size: 39.0 MB (39023605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73309e97ec1ff077f4f37791464cb53d50f136398aaf28ab215f221879af03`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb22b284bb2cb30fcdecafcb5ea07c8af1795d1c2cbe66f050b4d12ea37425e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf077c858b328a39a43c0f9ed3cbe6bdc4194fa3d62f54ddee67e4fbcbd5c1e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:c7e1e8a8f8c3577545659601eb3fac3fbd636eac6d806e7468b788ca4ad4d5ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45259357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf860480d3786b7087c913419f73135cd6eb8d14b37dbcc016326b322a1c0b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:24:11 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 03:24:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:24:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:24:12 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:25 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:26 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:27 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:27 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:27 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:28 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6260f461df58bea1babdc774881cd4b5b3308ed720603ecd823fcc3d6cc678`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f3162ac08a55267d33f525ae262d0a3e8359d1e0fa44f16fd97ab8af9515e`  
		Last Modified: Wed, 01 Sep 2021 03:26:01 GMT  
		Size: 42.4 MB (42434965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e93463c320af3d9f9927e9627f9e835f4122cea68271203d4b762ba2293cdc3`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310f0df835dd579e8e1dc333d93078e5cc68c5c5de5ed5b292d1cd5804f658e8`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8300a08a7f40722b7afc4b068c8006f182ae802dbe4d734dc7176fec52c811a1`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.9`

```console
$ docker pull consul@sha256:fa526f7c55c3ee02f07821542cfac32253f696dcb139b7a70465ab096e895031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386

### `consul:1.9.9` - linux; amd64

```console
$ docker pull consul@sha256:d08355ef1555bb782d486bc903bf75d397a32ed38f16d033b1e1cc28392b702e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45890066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f5d27f4606766adacd7db1f010bc5f056b9411c6285d981c2122cf143a6696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:14:27 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 00:14:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:14:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:14:30 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:42 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:43 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:45 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:45 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:46 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002deffc8d522ac27816e38f624fb99eb60e144f5ddae64c1db963f9f1f71c5`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585556722091a5853a673738ea0566385bddf805ae5d39b3ed5d875b1886bb8a`  
		Last Modified: Wed, 01 Sep 2021 00:16:10 GMT  
		Size: 43.1 MB (43072684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4118856830e8594ee52c9ce8f3c1a8130af6b714e1ea7d33eed9399a313ace`  
		Last Modified: Wed, 01 Sep 2021 00:16:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76ee2bdeec48e7dbda3f1f9e1ccd0decaa72db4e54b2de9563763e3ec68be6d`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b0d9dcde6a01972e13fc192727e0831d3b9ecd74412e8b9df5bc22baaf84a0`  
		Last Modified: Wed, 01 Sep 2021 00:16:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:0c4233085f4b5c606bc137959ba0efafbe3d62d0d7f97c617ff953761b483dea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41076889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada64b389b255aa86e91ca04ad7d76cb932e6e15cb27f007043f615cf0e94835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:24:11 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 01:24:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:24:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:24:14 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:24:27 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:24:29 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:24:31 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:24:31 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:24:32 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:24:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:24:33 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:24:33 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:24:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:24:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5077d694d8b4f4026a8ccddc072bba9850729ab8c83942c7083de1e084293d`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e53b7f51828dd128841f1ce6911e1a708bb684ba6004a8aaf0d87725caf6a`  
		Last Modified: Wed, 01 Sep 2021 01:26:52 GMT  
		Size: 38.4 MB (38449829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595e3a03716ffd8c1ce7f7e386e06f55eb85b2684bd1da366751494861ae6e`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573fb312b7f1723a8073db0d55c0de12c6a35639cac51774a02b0424b2ef4f65`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c0fa773cd8c9b01159940ec6958165c652889dfc420ae517b7272dee17fdaa`  
		Last Modified: Wed, 01 Sep 2021 01:26:31 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.9` - linux; 386

```console
$ docker pull consul@sha256:c7e1e8a8f8c3577545659601eb3fac3fbd636eac6d806e7468b788ca4ad4d5ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45259357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf860480d3786b7087c913419f73135cd6eb8d14b37dbcc016326b322a1c0b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:24:11 GMT
ARG CONSUL_VERSION=1.9.9
# Wed, 01 Sep 2021 03:24:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:24:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:24:12 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:25 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:26 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:27 GMT
# ARGS: CONSUL_VERSION=1.9.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:27 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:27 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:28 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6260f461df58bea1babdc774881cd4b5b3308ed720603ecd823fcc3d6cc678`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f3162ac08a55267d33f525ae262d0a3e8359d1e0fa44f16fd97ab8af9515e`  
		Last Modified: Wed, 01 Sep 2021 03:26:01 GMT  
		Size: 42.4 MB (42434965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e93463c320af3d9f9927e9627f9e835f4122cea68271203d4b762ba2293cdc3`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310f0df835dd579e8e1dc333d93078e5cc68c5c5de5ed5b292d1cd5804f658e8`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8300a08a7f40722b7afc4b068c8006f182ae802dbe4d734dc7176fec52c811a1`  
		Last Modified: Wed, 01 Sep 2021 03:25:49 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:fba4745a0fa7573ddf4671538e7857d2d1342ec85b0854f6bd304c1257d66e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:2c69d8bee4e99c083f0930bc09cdd45b88365ae6b427221283502230ba1c1ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43219430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74a0a01afc431799adac9d7911b8e0d6961a3b9909380ec61af211e342f7a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:13:55 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 00:13:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 00:13:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 00:13:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 00:14:15 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 00:14:17 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 00:14:19 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:14:19 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 00:14:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 00:14:21 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 00:14:21 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 00:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 00:14:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f992def430ed8f2556f38262c7a72f4b73b90938c7b10d23ee8948153f50`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e185403d62712206d4d670a6dc1e9343046bcc9d308944262faeb165ab68a3`  
		Last Modified: Wed, 01 Sep 2021 00:15:47 GMT  
		Size: 40.4 MB (40402053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52efdf2644d28f50e4d3a9beec818e4edd8d3af82a0b5154e335b0278e6da441`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a8413c32a8e922dbaba4d4e1028376cf9f171f84083e0bdf28e5921f37486`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b82ffb99af04063532bb252dc67c726dc483d2b709022906503c446ab3725`  
		Last Modified: Wed, 01 Sep 2021 00:15:39 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:1d983545c4f84b1cd3c7ce4d838e166c65a925693844cfd5ed5c4746e204c881
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39244219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbff18b6c799e1a17924a92190f3411c4726b7afbeaa5ebc1351581730b23e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:23:36 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 01:23:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 01:23:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 01:23:38 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 01:23:53 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 01:23:55 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 01:23:57 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 01:23:57 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 01:23:57 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 01:23:58 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 01:23:59 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 01:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 01:24:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffb408206870dbfae898542f9fe08defc3d55425b9287f67b4e7bc9639b04d`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9f1d264c506179627ab82efe2c2f5b2a52cfb7e2e736e8f3b883acb84c30c`  
		Last Modified: Wed, 01 Sep 2021 01:26:14 GMT  
		Size: 36.6 MB (36617160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f321a2bdffc01f4f3cfc903b8d00c4711968c30929a7ba2208e54efc88b8974`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7731df45612e290f1b44073d40ca132679f33d61eb153abf17aecf4b0101f5`  
		Last Modified: Wed, 01 Sep 2021 01:25:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313ef0d18b912146cb45f58d8570c5b193973da8ee33b986cf43d5df8f65e2df`  
		Last Modified: Wed, 01 Sep 2021 01:25:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:0081f4b20a6b484746ee30b2ede4f64241d94721c18b9c115ce61b88ca6588d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c65b74aabe05fbf0444ae754a6cf8bea788f8854c719189eecb6501793f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:33 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:19:33 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:19:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:40 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:41 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:41 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0bca027d4ed5928a09c462f06be2502d9e6dfd78d9ba3c527dc500cfcdfca`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b3128d8785d803695d60c92ef9482ab1ddc021eeb844a226ba40208ccb0a54`  
		Last Modified: Fri, 23 Jul 2021 04:20:40 GMT  
		Size: 36.9 MB (36869818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbf322ffab66a9b685be5eb28cf5499c409303c57282a74d1c3c7380cf2f5f7`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f3c6fd6c3e6a3b608722cdf776c98efb4d2ab2be357bf99716b7e6f5e8343`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418597e612cf3477bacd0c9730131f6a619802a05c2a5c37081550ec54fc2c60`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:17b520004b3a2623633c14b821adc7778348bb537ebfff5c60d2748d1459fbe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42597058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bedb65efe9b810ad73be975f82bd07358370d092f78608e1525f0f823239fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:23:44 GMT
ARG CONSUL_VERSION=1.10.2
# Wed, 01 Sep 2021 03:23:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 01 Sep 2021 03:23:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 01 Sep 2021 03:23:46 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 01 Sep 2021 03:24:01 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 01 Sep 2021 03:24:02 GMT
# ARGS: CONSUL_VERSION=1.10.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Sep 2021 03:24:03 GMT
VOLUME [/consul/data]
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8300
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 01 Sep 2021 03:24:03 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 01 Sep 2021 03:24:04 GMT
COPY file:f4999c9300ae549cb312108a9d1a23840829249bac4cd51e46d8466cfee3a6a1 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:24:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:24:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f7da53f439d00a34afad277f271e8d6601a55ad5425c7bab343206a090cbfd`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9bb807469664b1b7e9f2f39ec258ebeec3b98bd419fd12626039ac3d1373a`  
		Last Modified: Wed, 01 Sep 2021 03:25:31 GMT  
		Size: 39.8 MB (39772664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbcae0f50b0a16668a6242b7f4b2a37eb7bbba9ab5c681eef394b7744b2d5a1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6937a39eb1646e9da4597ac1ab4f329d69be5d448caee72177fd50a6b48823`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63276123b2c6bdf440e367d51a11433671f86ed4afec2bda8c94112e1697cb1`  
		Last Modified: Wed, 01 Sep 2021 03:25:20 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
