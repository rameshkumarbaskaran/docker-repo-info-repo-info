<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.11`](#consul111)
-	[`consul:1.11.7`](#consul1117)
-	[`consul:1.12`](#consul112)
-	[`consul:1.12.3`](#consul1123)
-	[`consul:1.13`](#consul113)
-	[`consul:1.13.0`](#consul1130)
-	[`consul:latest`](#consullatest)

## `consul:1.11`

```console
$ docker pull consul@sha256:21eb0cc94877bbc35a2e32f3bd82f4324e3d5061562006f0bb1a9c9979eaae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:9164b6c513fec9a03abc6efe99d9355c589feacbc47225eb96bbfa6ae3a39ba9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44020540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56a326ea43b0885cd532da157a5af6dd6c52854797548efbe67d0d8319926c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:19:19 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:19:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:19:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:19:20 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:19:26 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:19:27 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:19:27 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:19:27 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:19:27 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:19:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:19:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:19:28 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:19:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115bd9fd340206331a072729749154d993456e00bb0f277a840ef38ceab8b26b`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2844531ef329af6bfb23606f53c4239f8360ccbc91f0063deef0c3bced84712`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 41.2 MB (41193650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547b9bad8c7936b047f559a82ec8076994fc86fd7a8f16d8bc0f50b87d2e1ee4`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff1ca68141b5e77239e341fc8bbc5bc521162ef2f7544d3606c91cfa23e5177`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406366761f2acadf0deb7925d86c70c2ad6623b4731c0ab6787212bd8f12ad0`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:ac0ec319cc6bbd8b02101ed8e9c03592725b0b19ceead62c07b7bdcae416e5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41766687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8540c7fa25f77babc802a7d7e0ad2329fb001fcfac86d2c3f85b6fcf175be32c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:36:39 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:36:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:36:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:36:40 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:36:47 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:36:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:36:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:36:48 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:36:48 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:36:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:36:49 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:36:49 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1255801a1565eeb6f25497b3edf1791cb212b991cdbec20db4e04d89c1090c`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8dfc047f6b899dae9644f99c336a543ddc8ecd519fe17f277df780a39181b`  
		Last Modified: Tue, 09 Aug 2022 18:37:57 GMT  
		Size: 39.1 MB (39132186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47177831ded205f1331b61c21b0ef153ab216660c8aeaa3b4f624b2bbab18e61`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3837219cb618d27dceae54ec46ecf58ee960dd16daf1ec8455f2b181c65e797e`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0002b2849cea686a738b50bdfc1c8c7d81e0823c3b152a408a65133612f055a`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7a2864da1ce20e1d60c117a6e5b928f6ffd764be28ade2d4be602de4ba8ac5a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41583718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e1347f9ac9963a60206dd01394c8ebec0318fa86e96b19ba25e3b3de456c4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:22:45 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:22:46 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:22:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:22:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:22:53 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:22:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:22:55 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:22:56 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:22:57 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:22:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:22:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:23:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:23:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:23:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c092e4c6c4453ff462a6c54b0f74cef2b56bc89633f30bc50fa9c3a389263bf`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e895db0e66285ba15cd555fecd24a1123194ee07e66037dc3b31bb24a0661bf1`  
		Last Modified: Tue, 09 Aug 2022 18:24:13 GMT  
		Size: 38.9 MB (38861960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99582fcdefab49a0e41ef5e47053890dfeb4f8bddfcc653a7c0cccba88b85c`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42670e0839e44cf5d433b07e8fb432c0267f4cd9f6232134ffbbba57c4abecbe`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f281f94ab1f2f2756bc4e4c03ca21acae42f7f3d90b0d6355eb88afc6307676e`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:7acb650b9c1fe85f643edfe653e24bd2d3143e18ce3e504ff13ed5ca7470de6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a71341888f47e71106b8c3f2327c8fa15cb6ae573f9ea0a3fbcfc28a72a241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:17:19 GMT
ARG CONSUL_VERSION=1.11.7
# Wed, 10 Aug 2022 00:17:20 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 10 Aug 2022 00:17:21 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 10 Aug 2022 00:17:22 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 10 Aug 2022 00:17:28 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 10 Aug 2022 00:17:29 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 10 Aug 2022 00:17:30 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Aug 2022 00:17:31 GMT
VOLUME [/consul/data]
# Wed, 10 Aug 2022 00:17:32 GMT
EXPOSE 8300
# Wed, 10 Aug 2022 00:17:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 10 Aug 2022 00:17:34 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 10 Aug 2022 00:17:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:17:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:17:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f522f02747bd2d3a2834675989ceec50f0bc52239836c2e561b41ebfbb7a8`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac21060086e619a824ba495e9f19883c23f2f55282da5cd2e4cbebf7168e03a`  
		Last Modified: Wed, 10 Aug 2022 00:19:01 GMT  
		Size: 40.0 MB (39999487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815468cea905621e0f276e2e23820038e3c28f9883a8a4bc3625a02853f460fc`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aa5292acd7fc7770e8bef76202c60c40bf534fe33a6d8bd341f6f83564b2f4`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708acb0b2d04ce7c877409b97063968378082c14f85a7406412145b88258fdfc`  
		Last Modified: Wed, 10 Aug 2022 00:18:53 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.7`

```console
$ docker pull consul@sha256:21eb0cc94877bbc35a2e32f3bd82f4324e3d5061562006f0bb1a9c9979eaae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.7` - linux; amd64

```console
$ docker pull consul@sha256:9164b6c513fec9a03abc6efe99d9355c589feacbc47225eb96bbfa6ae3a39ba9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44020540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56a326ea43b0885cd532da157a5af6dd6c52854797548efbe67d0d8319926c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:19:19 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:19:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:19:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:19:20 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:19:26 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:19:27 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:19:27 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:19:27 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:19:27 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:19:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:19:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:19:28 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:19:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115bd9fd340206331a072729749154d993456e00bb0f277a840ef38ceab8b26b`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2844531ef329af6bfb23606f53c4239f8360ccbc91f0063deef0c3bced84712`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 41.2 MB (41193650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547b9bad8c7936b047f559a82ec8076994fc86fd7a8f16d8bc0f50b87d2e1ee4`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff1ca68141b5e77239e341fc8bbc5bc521162ef2f7544d3606c91cfa23e5177`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406366761f2acadf0deb7925d86c70c2ad6623b4731c0ab6787212bd8f12ad0`  
		Last Modified: Tue, 09 Aug 2022 18:20:12 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:ac0ec319cc6bbd8b02101ed8e9c03592725b0b19ceead62c07b7bdcae416e5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41766687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8540c7fa25f77babc802a7d7e0ad2329fb001fcfac86d2c3f85b6fcf175be32c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:36:39 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:36:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:36:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:36:40 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:36:47 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:36:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:36:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:36:48 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:36:48 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:36:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:36:49 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:36:49 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1255801a1565eeb6f25497b3edf1791cb212b991cdbec20db4e04d89c1090c`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f8dfc047f6b899dae9644f99c336a543ddc8ecd519fe17f277df780a39181b`  
		Last Modified: Tue, 09 Aug 2022 18:37:57 GMT  
		Size: 39.1 MB (39132186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47177831ded205f1331b61c21b0ef153ab216660c8aeaa3b4f624b2bbab18e61`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3837219cb618d27dceae54ec46ecf58ee960dd16daf1ec8455f2b181c65e797e`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0002b2849cea686a738b50bdfc1c8c7d81e0823c3b152a408a65133612f055a`  
		Last Modified: Tue, 09 Aug 2022 18:37:50 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7a2864da1ce20e1d60c117a6e5b928f6ffd764be28ade2d4be602de4ba8ac5a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41583718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e1347f9ac9963a60206dd01394c8ebec0318fa86e96b19ba25e3b3de456c4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:22:45 GMT
ARG CONSUL_VERSION=1.11.7
# Tue, 09 Aug 2022 18:22:46 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:22:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:22:48 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:22:53 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:22:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:22:55 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:22:56 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:22:57 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:22:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:22:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:23:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:23:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:23:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c092e4c6c4453ff462a6c54b0f74cef2b56bc89633f30bc50fa9c3a389263bf`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e895db0e66285ba15cd555fecd24a1123194ee07e66037dc3b31bb24a0661bf1`  
		Last Modified: Tue, 09 Aug 2022 18:24:13 GMT  
		Size: 38.9 MB (38861960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99582fcdefab49a0e41ef5e47053890dfeb4f8bddfcc653a7c0cccba88b85c`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42670e0839e44cf5d433b07e8fb432c0267f4cd9f6232134ffbbba57c4abecbe`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f281f94ab1f2f2756bc4e4c03ca21acae42f7f3d90b0d6355eb88afc6307676e`  
		Last Modified: Tue, 09 Aug 2022 18:24:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; 386

```console
$ docker pull consul@sha256:7acb650b9c1fe85f643edfe653e24bd2d3143e18ce3e504ff13ed5ca7470de6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a71341888f47e71106b8c3f2327c8fa15cb6ae573f9ea0a3fbcfc28a72a241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:17:19 GMT
ARG CONSUL_VERSION=1.11.7
# Wed, 10 Aug 2022 00:17:20 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 10 Aug 2022 00:17:21 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 10 Aug 2022 00:17:22 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 10 Aug 2022 00:17:28 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 10 Aug 2022 00:17:29 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 10 Aug 2022 00:17:30 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Aug 2022 00:17:31 GMT
VOLUME [/consul/data]
# Wed, 10 Aug 2022 00:17:32 GMT
EXPOSE 8300
# Wed, 10 Aug 2022 00:17:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 10 Aug 2022 00:17:34 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 10 Aug 2022 00:17:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:17:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:17:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f522f02747bd2d3a2834675989ceec50f0bc52239836c2e561b41ebfbb7a8`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac21060086e619a824ba495e9f19883c23f2f55282da5cd2e4cbebf7168e03a`  
		Last Modified: Wed, 10 Aug 2022 00:19:01 GMT  
		Size: 40.0 MB (39999487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815468cea905621e0f276e2e23820038e3c28f9883a8a4bc3625a02853f460fc`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3aa5292acd7fc7770e8bef76202c60c40bf534fe33a6d8bd341f6f83564b2f4`  
		Last Modified: Wed, 10 Aug 2022 00:18:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708acb0b2d04ce7c877409b97063968378082c14f85a7406412145b88258fdfc`  
		Last Modified: Wed, 10 Aug 2022 00:18:53 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12`

```console
$ docker pull consul@sha256:1ddb1135324df19d7c506d119e8dac878cade0f8dce33705b08d24d22b139f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12` - linux; amd64

```console
$ docker pull consul@sha256:80ba62902f5a4dae5ad4810da3eac37cb948ae59a6ec0524465985f44957d9a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216943db9d18e2613fd812bd4b6447daeca27b5550fb687f576219cdc5a5080`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:19:08 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:19:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:19:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:19:08 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:19:15 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:19:15 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:19:16 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:19:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb9e335269b18d0845e0d82b72c7d3d2f0571c5954f6734337b8c4d60d95f65`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e4d825a41c32a2e07ecae383245ded626738fc5f86fdd2149b388c164b4c35`  
		Last Modified: Tue, 09 Aug 2022 18:19:59 GMT  
		Size: 46.8 MB (46759568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5c29d9b704cd1356870c2484a20f546037973d57c0a7c8d8c982ecd28cee51`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5dc3bdb3260a4989b28366b5e794b041d63af3ec202f55d0a64ea0c0041942`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c265a329c716dd93cfa6a6def5b846253e9fdb039345f81067aa0db68df70d33`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:419dcf2425d0c007f235c9ba8b8ed90664e1071fbf91ab0d9dd1e85c00ea7778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47446450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d266d267ab99fd27c5b971df6f0daada4bfcbe1b2da5a6967b47d1ea4c19a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:36:24 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:36:24 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:36:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:36:25 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:36:33 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:36:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:36:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58553ba144a53432002f40d76f6bf7d7f6065a39a2820c946d478ee8f22459da`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ac3584c0ad364b6fa5f95968e4e15dfb04ac04ba5d20a0d856096e2f3a88a6`  
		Last Modified: Tue, 09 Aug 2022 18:37:35 GMT  
		Size: 44.8 MB (44811940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af48f15de439742c66850976d741b1dce565149cf5c7046d16b7ee20b6428529`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e5a3ffd9e26027f007bd842b51a2d1c50b3b0f7072b3a044064cfdfa11770f`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df135dc978208126f1f661f5aca725fe6db9e250c17ab37115e588707725fb`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a4614e399c79b5af272bcca5c53213031f538c552be2571097c343c90b4ba51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47181871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111ec65d84070448431ac15e09c8e478d44eb319ec21026c1b3e7722ad95f13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:22:22 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:22:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:22:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:22:24 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:22:30 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:22:31 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:22:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:22:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:22:34 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:22:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:22:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:22:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:22:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fc95a3a7be56f234c7db964f3fe7cdb33ba9e329f2d8fbd64dc4bf15a528b6`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dcaf2f442c67fcfb785f52489b20007f58871b92d74c00505d7b0243eeefc`  
		Last Modified: Tue, 09 Aug 2022 18:23:53 GMT  
		Size: 44.5 MB (44460120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e111b8a7299438e3ea3ae161a26df7b6a57925337cdd824ac5c9d4052b94ff`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19722da856ca47f1ed77b12597e8c7c6927d43379b44b925d0654f764bef1e`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9af7c98a4dbd51d96eea352418ebb644faa889692060256f8b6bd6bd7a54ca`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; 386

```console
$ docker pull consul@sha256:b53768c319346cb0f199cfa875e2367365dcffe1f447bc4585a852969c0b3c6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48650963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a885d45be738663519a382206e7d4d25cb9c67a1fd9c99e35c3de8d7af09d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:16:53 GMT
ARG CONSUL_VERSION=1.12.3
# Wed, 10 Aug 2022 00:16:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 10 Aug 2022 00:16:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 10 Aug 2022 00:16:56 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 10 Aug 2022 00:17:02 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 10 Aug 2022 00:17:03 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 10 Aug 2022 00:17:04 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Aug 2022 00:17:05 GMT
VOLUME [/consul/data]
# Wed, 10 Aug 2022 00:17:06 GMT
EXPOSE 8300
# Wed, 10 Aug 2022 00:17:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 10 Aug 2022 00:17:08 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 10 Aug 2022 00:17:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:17:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39f34fabee1478b7c0843754eeab08ffcfff8f46f225947ccec5a1ce3c97427`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcea91349eca5ad61e8aedc1559a5ae7799ece5af76b54994e2d0aedba4b8f8`  
		Last Modified: Wed, 10 Aug 2022 00:18:38 GMT  
		Size: 45.8 MB (45819126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d7d681535a330fdf6323c163a9c8e4b8ad73ecb8ad94d166f0d73931b8bc99`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41452ce51b713a52b7189170938dca30cdec684cc538d1f3f30ed7d0c8d98e2`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f322737f395fead487e4fd88ada48065dcdeb6dd02eeec480b6f6c5fd612cc`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12.3`

```console
$ docker pull consul@sha256:1ddb1135324df19d7c506d119e8dac878cade0f8dce33705b08d24d22b139f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12.3` - linux; amd64

```console
$ docker pull consul@sha256:80ba62902f5a4dae5ad4810da3eac37cb948ae59a6ec0524465985f44957d9a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216943db9d18e2613fd812bd4b6447daeca27b5550fb687f576219cdc5a5080`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:19:08 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:19:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:19:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:19:08 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:19:15 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:19:15 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:19:16 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:19:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb9e335269b18d0845e0d82b72c7d3d2f0571c5954f6734337b8c4d60d95f65`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e4d825a41c32a2e07ecae383245ded626738fc5f86fdd2149b388c164b4c35`  
		Last Modified: Tue, 09 Aug 2022 18:19:59 GMT  
		Size: 46.8 MB (46759568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5c29d9b704cd1356870c2484a20f546037973d57c0a7c8d8c982ecd28cee51`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5dc3bdb3260a4989b28366b5e794b041d63af3ec202f55d0a64ea0c0041942`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c265a329c716dd93cfa6a6def5b846253e9fdb039345f81067aa0db68df70d33`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:419dcf2425d0c007f235c9ba8b8ed90664e1071fbf91ab0d9dd1e85c00ea7778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47446450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d266d267ab99fd27c5b971df6f0daada4bfcbe1b2da5a6967b47d1ea4c19a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:36:24 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:36:24 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:36:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:36:25 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:36:33 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:36:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:36:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58553ba144a53432002f40d76f6bf7d7f6065a39a2820c946d478ee8f22459da`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ac3584c0ad364b6fa5f95968e4e15dfb04ac04ba5d20a0d856096e2f3a88a6`  
		Last Modified: Tue, 09 Aug 2022 18:37:35 GMT  
		Size: 44.8 MB (44811940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af48f15de439742c66850976d741b1dce565149cf5c7046d16b7ee20b6428529`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e5a3ffd9e26027f007bd842b51a2d1c50b3b0f7072b3a044064cfdfa11770f`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df135dc978208126f1f661f5aca725fe6db9e250c17ab37115e588707725fb`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a4614e399c79b5af272bcca5c53213031f538c552be2571097c343c90b4ba51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47181871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111ec65d84070448431ac15e09c8e478d44eb319ec21026c1b3e7722ad95f13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:22:22 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:22:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:22:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:22:24 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:22:30 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:22:31 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:22:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:22:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:22:34 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:22:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:22:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:22:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:22:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fc95a3a7be56f234c7db964f3fe7cdb33ba9e329f2d8fbd64dc4bf15a528b6`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dcaf2f442c67fcfb785f52489b20007f58871b92d74c00505d7b0243eeefc`  
		Last Modified: Tue, 09 Aug 2022 18:23:53 GMT  
		Size: 44.5 MB (44460120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e111b8a7299438e3ea3ae161a26df7b6a57925337cdd824ac5c9d4052b94ff`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19722da856ca47f1ed77b12597e8c7c6927d43379b44b925d0654f764bef1e`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9af7c98a4dbd51d96eea352418ebb644faa889692060256f8b6bd6bd7a54ca`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; 386

```console
$ docker pull consul@sha256:b53768c319346cb0f199cfa875e2367365dcffe1f447bc4585a852969c0b3c6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48650963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a885d45be738663519a382206e7d4d25cb9c67a1fd9c99e35c3de8d7af09d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:16:53 GMT
ARG CONSUL_VERSION=1.12.3
# Wed, 10 Aug 2022 00:16:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 10 Aug 2022 00:16:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 10 Aug 2022 00:16:56 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 10 Aug 2022 00:17:02 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 10 Aug 2022 00:17:03 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 10 Aug 2022 00:17:04 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Aug 2022 00:17:05 GMT
VOLUME [/consul/data]
# Wed, 10 Aug 2022 00:17:06 GMT
EXPOSE 8300
# Wed, 10 Aug 2022 00:17:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 10 Aug 2022 00:17:08 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 10 Aug 2022 00:17:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:17:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39f34fabee1478b7c0843754eeab08ffcfff8f46f225947ccec5a1ce3c97427`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcea91349eca5ad61e8aedc1559a5ae7799ece5af76b54994e2d0aedba4b8f8`  
		Last Modified: Wed, 10 Aug 2022 00:18:38 GMT  
		Size: 45.8 MB (45819126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d7d681535a330fdf6323c163a9c8e4b8ad73ecb8ad94d166f0d73931b8bc99`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41452ce51b713a52b7189170938dca30cdec684cc538d1f3f30ed7d0c8d98e2`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f322737f395fead487e4fd88ada48065dcdeb6dd02eeec480b6f6c5fd612cc`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13`

**does not exist** (yet?)

## `consul:1.13.0`

**does not exist** (yet?)

## `consul:latest`

```console
$ docker pull consul@sha256:1ddb1135324df19d7c506d119e8dac878cade0f8dce33705b08d24d22b139f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:80ba62902f5a4dae5ad4810da3eac37cb948ae59a6ec0524465985f44957d9a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49586454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216943db9d18e2613fd812bd4b6447daeca27b5550fb687f576219cdc5a5080`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:19:08 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:19:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:19:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:19:08 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:19:14 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:19:15 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:19:15 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:19:15 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:19:16 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:19:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb9e335269b18d0845e0d82b72c7d3d2f0571c5954f6734337b8c4d60d95f65`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e4d825a41c32a2e07ecae383245ded626738fc5f86fdd2149b388c164b4c35`  
		Last Modified: Tue, 09 Aug 2022 18:19:59 GMT  
		Size: 46.8 MB (46759568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5c29d9b704cd1356870c2484a20f546037973d57c0a7c8d8c982ecd28cee51`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5dc3bdb3260a4989b28366b5e794b041d63af3ec202f55d0a64ea0c0041942`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c265a329c716dd93cfa6a6def5b846253e9fdb039345f81067aa0db68df70d33`  
		Last Modified: Tue, 09 Aug 2022 18:19:54 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:419dcf2425d0c007f235c9ba8b8ed90664e1071fbf91ab0d9dd1e85c00ea7778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47446450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d266d267ab99fd27c5b971df6f0daada4bfcbe1b2da5a6967b47d1ea4c19a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:36:24 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:36:24 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:36:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:36:25 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:36:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:36:33 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:36:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:36:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:36:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:36:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58553ba144a53432002f40d76f6bf7d7f6065a39a2820c946d478ee8f22459da`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ac3584c0ad364b6fa5f95968e4e15dfb04ac04ba5d20a0d856096e2f3a88a6`  
		Last Modified: Tue, 09 Aug 2022 18:37:35 GMT  
		Size: 44.8 MB (44811940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af48f15de439742c66850976d741b1dce565149cf5c7046d16b7ee20b6428529`  
		Last Modified: Tue, 09 Aug 2022 18:37:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e5a3ffd9e26027f007bd842b51a2d1c50b3b0f7072b3a044064cfdfa11770f`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df135dc978208126f1f661f5aca725fe6db9e250c17ab37115e588707725fb`  
		Last Modified: Tue, 09 Aug 2022 18:37:29 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a4614e399c79b5af272bcca5c53213031f538c552be2571097c343c90b4ba51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47181871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111ec65d84070448431ac15e09c8e478d44eb319ec21026c1b3e7722ad95f13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:22:22 GMT
ARG CONSUL_VERSION=1.12.3
# Tue, 09 Aug 2022 18:22:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 09 Aug 2022 18:22:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 09 Aug 2022 18:22:24 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 09 Aug 2022 18:22:30 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 09 Aug 2022 18:22:31 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 09 Aug 2022 18:22:32 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:22:33 GMT
VOLUME [/consul/data]
# Tue, 09 Aug 2022 18:22:34 GMT
EXPOSE 8300
# Tue, 09 Aug 2022 18:22:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 09 Aug 2022 18:22:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 09 Aug 2022 18:22:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 09 Aug 2022 18:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:22:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fc95a3a7be56f234c7db964f3fe7cdb33ba9e329f2d8fbd64dc4bf15a528b6`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dcaf2f442c67fcfb785f52489b20007f58871b92d74c00505d7b0243eeefc`  
		Last Modified: Tue, 09 Aug 2022 18:23:53 GMT  
		Size: 44.5 MB (44460120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e111b8a7299438e3ea3ae161a26df7b6a57925337cdd824ac5c9d4052b94ff`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19722da856ca47f1ed77b12597e8c7c6927d43379b44b925d0654f764bef1e`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9af7c98a4dbd51d96eea352418ebb644faa889692060256f8b6bd6bd7a54ca`  
		Last Modified: Tue, 09 Aug 2022 18:23:47 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:b53768c319346cb0f199cfa875e2367365dcffe1f447bc4585a852969c0b3c6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48650963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a885d45be738663519a382206e7d4d25cb9c67a1fd9c99e35c3de8d7af09d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:16:53 GMT
ARG CONSUL_VERSION=1.12.3
# Wed, 10 Aug 2022 00:16:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 10 Aug 2022 00:16:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 10 Aug 2022 00:16:56 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 10 Aug 2022 00:17:02 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 10 Aug 2022 00:17:03 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 10 Aug 2022 00:17:04 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Aug 2022 00:17:05 GMT
VOLUME [/consul/data]
# Wed, 10 Aug 2022 00:17:06 GMT
EXPOSE 8300
# Wed, 10 Aug 2022 00:17:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 10 Aug 2022 00:17:08 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 10 Aug 2022 00:17:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:17:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39f34fabee1478b7c0843754eeab08ffcfff8f46f225947ccec5a1ce3c97427`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcea91349eca5ad61e8aedc1559a5ae7799ece5af76b54994e2d0aedba4b8f8`  
		Last Modified: Wed, 10 Aug 2022 00:18:38 GMT  
		Size: 45.8 MB (45819126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d7d681535a330fdf6323c163a9c8e4b8ad73ecb8ad94d166f0d73931b8bc99`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41452ce51b713a52b7189170938dca30cdec684cc538d1f3f30ed7d0c8d98e2`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f322737f395fead487e4fd88ada48065dcdeb6dd02eeec480b6f6c5fd612cc`  
		Last Modified: Wed, 10 Aug 2022 00:18:29 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
