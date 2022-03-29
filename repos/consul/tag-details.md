<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.9`](#consul1109)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.4`](#consul1114)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.16`](#consul1916)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:c7f99d746f3ccadd70956586e35a674bc8f278e2272e325e9e1f8980371c4b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:6f931adf007237b709150c5e9bc4fb289ec782cb407db61890c4a52959da042e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43746018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8aaaa737702c10fa9096169d2aed7a479baff8fb491e23b1e83146ab790623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:29 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 06:03:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:30 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:35 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:36 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:37 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:37 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b620ae326ec16663d72602f5d0277a6dd91406dadb2247659d60aa354629bc`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371d92c7361281165878cfa686318408788f453346d278d2c48a33573645a15f`  
		Last Modified: Tue, 29 Mar 2022 06:04:23 GMT  
		Size: 40.9 MB (40923427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ec7ae220a40d009ceb5a935486118cb69bf669bff723b9adb003ee7b8d205a`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3d93c84a84b61182fd7c89e9220f030da268afd6dc4a1a27df4652c0693cc8`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db353a0c102a2adfe621722f3fc23af2cf930f115463461c96e5a8176b32149`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:4dc0e00a3a503e10fe5cbf09305d56c477ca1104bc0a31237fc77334f0548a25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41803431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a65564f5fad6c974269ff3146f438f0ef8010e5824f29ba182efba41a14bf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:33:13 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 07:33:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:33:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:33:16 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:33:28 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:33:30 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:33:32 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:33:32 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:33:33 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:33:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:33:34 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:33:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:33:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72c06af49d2d18824053061f28d92db9a1fcbd556180d33bb42c81667b1b904`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c1bf62cb56d79043332ed10ed766e9d498edd7a3cadd5fe30d79320ec3df8`  
		Last Modified: Tue, 29 Mar 2022 07:35:49 GMT  
		Size: 39.2 MB (39174919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3389d2276cabf5a0d4f4ff8c0cfc57e57d77a82f5c405a46b50e961b97e4998`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7e0f5d196da6bc508243597c709fed5dba6c477ea0769c634fe6f16e9b53cb`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daad5c75e22a5e992760e1318472b3e8c02f95b612e2dc714671b98dc99b5d65`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:fac994b83f3f140e0b2bc95985a95e6cb49c20b5386b400bd733e28992bc298f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41774180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30cc62a7582362c1cb9f472ecbc544b923ae60e0673e961c9ccf0f5737d6b7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:34:44 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 10:34:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:34:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:34:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:34:54 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:34:55 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:34:56 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:34:57 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:34:58 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:34:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:35:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:35:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:35:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:35:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88a0824faf18130a43f518dbc8a572d2cee4f1743ec3edfa077fd8e998a3a37`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055e57b181ef422c17a5e90eb0365bb34321dc279cb191ddc65c8e8034f66cf5`  
		Last Modified: Tue, 29 Mar 2022 10:36:16 GMT  
		Size: 39.1 MB (39050021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35abeed6d5f9ce07c39dbb4a1ca65e313a886188399293ff71d967f8bab4837`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f8b6caa5ef5165a349e1d453360fc69f279218892db2f3b9050327461ca491`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9e112e6c5ec7a53bbfb97f004ba3bb64b72850b505b9cd74af701a71d2ebf6`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:9580b2b82b8dff4ef3dfd1fc7c31a82e61437791adae465eb97abec2ce4f64ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43109871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a77e4b27d88d920a6cf9f34ff255bfd68f4f04c19db335761bbdc5f6d2abc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:16:09 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 04:16:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:16:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:16:12 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:16:18 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:16:18 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:16:19 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:16:20 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:16:21 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:16:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:16:23 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9981c445fb878fa644dd510d28f11bd264ef14ca7123c6355089a7b8c9ac3`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9173da9900b5d0949f93e9a78793a56f1df0406af5fd501d2b3e738f2f37b3a`  
		Last Modified: Tue, 29 Mar 2022 04:17:39 GMT  
		Size: 40.3 MB (40286174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c0a4cbd730a36a137b67b6757787056dfae83faa1f1a29c6618840080b5940`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c91e0dd408155cab4d5cacf35f664ec202b6c6656c0a85d8c7e23aaf9e666a`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85716bf3675d101cd4c95bd6d74511f4679fd0630b4c9d9a7eb92ba89198d391`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.9`

```console
$ docker pull consul@sha256:c7f99d746f3ccadd70956586e35a674bc8f278e2272e325e9e1f8980371c4b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.9` - linux; amd64

```console
$ docker pull consul@sha256:6f931adf007237b709150c5e9bc4fb289ec782cb407db61890c4a52959da042e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43746018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8aaaa737702c10fa9096169d2aed7a479baff8fb491e23b1e83146ab790623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:29 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 06:03:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:30 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:35 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:36 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:37 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:37 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:37 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b620ae326ec16663d72602f5d0277a6dd91406dadb2247659d60aa354629bc`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371d92c7361281165878cfa686318408788f453346d278d2c48a33573645a15f`  
		Last Modified: Tue, 29 Mar 2022 06:04:23 GMT  
		Size: 40.9 MB (40923427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ec7ae220a40d009ceb5a935486118cb69bf669bff723b9adb003ee7b8d205a`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3d93c84a84b61182fd7c89e9220f030da268afd6dc4a1a27df4652c0693cc8`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db353a0c102a2adfe621722f3fc23af2cf930f115463461c96e5a8176b32149`  
		Last Modified: Tue, 29 Mar 2022 06:04:18 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:4dc0e00a3a503e10fe5cbf09305d56c477ca1104bc0a31237fc77334f0548a25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41803431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a65564f5fad6c974269ff3146f438f0ef8010e5824f29ba182efba41a14bf0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:33:13 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 07:33:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:33:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:33:16 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:33:28 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:33:30 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:33:32 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:33:32 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:33:33 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:33:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:33:34 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:33:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:33:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72c06af49d2d18824053061f28d92db9a1fcbd556180d33bb42c81667b1b904`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c1bf62cb56d79043332ed10ed766e9d498edd7a3cadd5fe30d79320ec3df8`  
		Last Modified: Tue, 29 Mar 2022 07:35:49 GMT  
		Size: 39.2 MB (39174919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3389d2276cabf5a0d4f4ff8c0cfc57e57d77a82f5c405a46b50e961b97e4998`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7e0f5d196da6bc508243597c709fed5dba6c477ea0769c634fe6f16e9b53cb`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daad5c75e22a5e992760e1318472b3e8c02f95b612e2dc714671b98dc99b5d65`  
		Last Modified: Tue, 29 Mar 2022 07:35:29 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:fac994b83f3f140e0b2bc95985a95e6cb49c20b5386b400bd733e28992bc298f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41774180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30cc62a7582362c1cb9f472ecbc544b923ae60e0673e961c9ccf0f5737d6b7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:34:44 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 10:34:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:34:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:34:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:34:54 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:34:55 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:34:56 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:34:57 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:34:58 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:34:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:35:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:35:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:35:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:35:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88a0824faf18130a43f518dbc8a572d2cee4f1743ec3edfa077fd8e998a3a37`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055e57b181ef422c17a5e90eb0365bb34321dc279cb191ddc65c8e8034f66cf5`  
		Last Modified: Tue, 29 Mar 2022 10:36:16 GMT  
		Size: 39.1 MB (39050021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35abeed6d5f9ce07c39dbb4a1ca65e313a886188399293ff71d967f8bab4837`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f8b6caa5ef5165a349e1d453360fc69f279218892db2f3b9050327461ca491`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9e112e6c5ec7a53bbfb97f004ba3bb64b72850b505b9cd74af701a71d2ebf6`  
		Last Modified: Tue, 29 Mar 2022 10:36:11 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; 386

```console
$ docker pull consul@sha256:9580b2b82b8dff4ef3dfd1fc7c31a82e61437791adae465eb97abec2ce4f64ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43109871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a77e4b27d88d920a6cf9f34ff255bfd68f4f04c19db335761bbdc5f6d2abc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:16:09 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 29 Mar 2022 04:16:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:16:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:16:12 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:16:18 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:16:18 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:16:19 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:16:20 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:16:21 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:16:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:16:23 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9981c445fb878fa644dd510d28f11bd264ef14ca7123c6355089a7b8c9ac3`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9173da9900b5d0949f93e9a78793a56f1df0406af5fd501d2b3e738f2f37b3a`  
		Last Modified: Tue, 29 Mar 2022 04:17:39 GMT  
		Size: 40.3 MB (40286174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c0a4cbd730a36a137b67b6757787056dfae83faa1f1a29c6618840080b5940`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c91e0dd408155cab4d5cacf35f664ec202b6c6656c0a85d8c7e23aaf9e666a`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85716bf3675d101cd4c95bd6d74511f4679fd0630b4c9d9a7eb92ba89198d391`  
		Last Modified: Tue, 29 Mar 2022 04:17:34 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:8a6c72bffbbc071635d3aae6b1a9781ce228183b18c86c9c6baae5b9e929118e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:5c638c0ceaaee10de5ce5bc6c12f9fc6e573654a74b4e46bc3c503770e945509
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd576c5f6970fdbfe3516834beae052fb1ec2843661a9586f1a9a2d958a766`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:18 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 06:03:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:19 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:24 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:26 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:26 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cd86ddf7d416a94b4a886647c21c03a1391ea840677ba38d6a7fe86e38bb81`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f957e9afb7a8579402f028966cfd109fbc17d08e18f3a698481fb5c4a069c7`  
		Last Modified: Tue, 29 Mar 2022 06:04:05 GMT  
		Size: 41.1 MB (41121471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb8f5f08d6297bc8fa44d778250df3a159fe3554b8673a9036d16781ba512e0`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a87013b95bb5ed340413ca055c1e362987adecc8912204c3d00c4bdd632591`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d174ae4eb977244b11874e8830088fc8900cd26377aff48b1fcb188a5be20c`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:1888ef354a12ac56ddb2b96276c9e83eb633fdd916f52269f7144f1585bc0cf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41703939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97660c8bc3b3f9b0672769a9dc29c524199ccd13f94a04a7581e23a9baf67fe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:32:39 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 07:32:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:32:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:32:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:32:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:32:56 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:32:58 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:32:58 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:33:00 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:33:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfc635fd4572e0b70d19743f459e9d969acc08352742323089eba57d8f38e86`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d091c6e914999d5b31228dcafdc4d91e48f3b2bc401c8fdcec1b6fa739f4a6e`  
		Last Modified: Tue, 29 Mar 2022 07:35:14 GMT  
		Size: 39.1 MB (39075430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b554cf8d29231e5d8b40ad185f6c62049d25d3aac1bdc5641a1a1db1845b6f99`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa142476d37f45100f6069bde9cd7be3f84353fc72d26791c8465e9a3afab0a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148913beff486f9ad60fbde76bf5290ab1c93f5d09ed189df21bc61eb486d4a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:66b2fa65222251fe2e043a3f99ffc463392432a9e2963cb8c088ad79dd2303b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41548739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f96c12d39fbaab84a8819ac3dced48eef204eff39ada2a24bd8471e0566438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:34:17 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 10:34:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:34:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:34:20 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:34:28 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:34:30 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:34:31 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:34:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:34:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:34:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:34:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:34:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d421b63501abd7eb5acfea66de064cce3d12f19b7d827e341af38468541824`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda5a94750831ddfd91231bceafd6ce1f58fd37b5e8e13734f60b500c3794474`  
		Last Modified: Tue, 29 Mar 2022 10:35:56 GMT  
		Size: 38.8 MB (38824582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf164bd3d26bc6d1e8b48cd190c4838ed43d3d68bf1e0c158bdfda521bcff790`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4cab6e8dee57b92aae2cecae23333870064100a8d37d323181fc06ce2cc113`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986dc022b5fdff77aa3482f623f56a75e264b47252f0a6917db1495cb918f59`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:7609c7af79d816640380ea00bf3b51729f6b0ea2ce8f3d366f9ced1eec46ee81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42762465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e177daf1713020f8185275a5cb7ff3099fca059b497c43b522b1b27705fc5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:15:43 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 04:15:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:15:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:15:46 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:15:53 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:15:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:15:55 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:15:56 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:15:57 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:15:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:15:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6563152e47763d9972ac28a087bc8ae8869f1b12824e5e10d949b90f50940`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d132466b4692fe52eb1e51fe72f2d8aa6ed1824741b21caf4e59a6c5cc899b8`  
		Last Modified: Tue, 29 Mar 2022 04:17:20 GMT  
		Size: 39.9 MB (39938763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6f6eb96f21ad2bf510d01e9b0a9f98d7c3d30ecaf3a6ea96d5bb6c08f50b77`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d510af9be8debeae9069e66ef33a087a81a0ff04bccb2c3a6d935ebb8580c`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ba92db007797b9a757bd5a525cbc5039b229d5e419e7c3422e5618f4426a`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.4`

```console
$ docker pull consul@sha256:8a6c72bffbbc071635d3aae6b1a9781ce228183b18c86c9c6baae5b9e929118e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.4` - linux; amd64

```console
$ docker pull consul@sha256:5c638c0ceaaee10de5ce5bc6c12f9fc6e573654a74b4e46bc3c503770e945509
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd576c5f6970fdbfe3516834beae052fb1ec2843661a9586f1a9a2d958a766`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:18 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 06:03:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:19 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:24 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:26 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:26 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cd86ddf7d416a94b4a886647c21c03a1391ea840677ba38d6a7fe86e38bb81`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f957e9afb7a8579402f028966cfd109fbc17d08e18f3a698481fb5c4a069c7`  
		Last Modified: Tue, 29 Mar 2022 06:04:05 GMT  
		Size: 41.1 MB (41121471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb8f5f08d6297bc8fa44d778250df3a159fe3554b8673a9036d16781ba512e0`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a87013b95bb5ed340413ca055c1e362987adecc8912204c3d00c4bdd632591`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d174ae4eb977244b11874e8830088fc8900cd26377aff48b1fcb188a5be20c`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:1888ef354a12ac56ddb2b96276c9e83eb633fdd916f52269f7144f1585bc0cf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41703939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97660c8bc3b3f9b0672769a9dc29c524199ccd13f94a04a7581e23a9baf67fe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:32:39 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 07:32:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:32:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:32:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:32:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:32:56 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:32:58 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:32:58 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:33:00 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:33:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfc635fd4572e0b70d19743f459e9d969acc08352742323089eba57d8f38e86`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d091c6e914999d5b31228dcafdc4d91e48f3b2bc401c8fdcec1b6fa739f4a6e`  
		Last Modified: Tue, 29 Mar 2022 07:35:14 GMT  
		Size: 39.1 MB (39075430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b554cf8d29231e5d8b40ad185f6c62049d25d3aac1bdc5641a1a1db1845b6f99`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa142476d37f45100f6069bde9cd7be3f84353fc72d26791c8465e9a3afab0a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148913beff486f9ad60fbde76bf5290ab1c93f5d09ed189df21bc61eb486d4a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:66b2fa65222251fe2e043a3f99ffc463392432a9e2963cb8c088ad79dd2303b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41548739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f96c12d39fbaab84a8819ac3dced48eef204eff39ada2a24bd8471e0566438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:34:17 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 10:34:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:34:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:34:20 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:34:28 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:34:30 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:34:31 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:34:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:34:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:34:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:34:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:34:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d421b63501abd7eb5acfea66de064cce3d12f19b7d827e341af38468541824`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda5a94750831ddfd91231bceafd6ce1f58fd37b5e8e13734f60b500c3794474`  
		Last Modified: Tue, 29 Mar 2022 10:35:56 GMT  
		Size: 38.8 MB (38824582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf164bd3d26bc6d1e8b48cd190c4838ed43d3d68bf1e0c158bdfda521bcff790`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4cab6e8dee57b92aae2cecae23333870064100a8d37d323181fc06ce2cc113`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986dc022b5fdff77aa3482f623f56a75e264b47252f0a6917db1495cb918f59`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; 386

```console
$ docker pull consul@sha256:7609c7af79d816640380ea00bf3b51729f6b0ea2ce8f3d366f9ced1eec46ee81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42762465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e177daf1713020f8185275a5cb7ff3099fca059b497c43b522b1b27705fc5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:15:43 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 04:15:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:15:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:15:46 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:15:53 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:15:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:15:55 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:15:56 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:15:57 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:15:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:15:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6563152e47763d9972ac28a087bc8ae8869f1b12824e5e10d949b90f50940`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d132466b4692fe52eb1e51fe72f2d8aa6ed1824741b21caf4e59a6c5cc899b8`  
		Last Modified: Tue, 29 Mar 2022 04:17:20 GMT  
		Size: 39.9 MB (39938763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6f6eb96f21ad2bf510d01e9b0a9f98d7c3d30ecaf3a6ea96d5bb6c08f50b77`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d510af9be8debeae9069e66ef33a087a81a0ff04bccb2c3a6d935ebb8580c`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ba92db007797b9a757bd5a525cbc5039b229d5e419e7c3422e5618f4426a`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:f3398876019ff10ed45710ed7021fbda3b8a299f8fd24f07b4d31fbc26614a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:1cd200f40e014641621eb970c5813fe36ad4772dc10223ce9187380cc788f08b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40153774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d569aa7e4ddb795f026b0b9d927110fde7600e76d79c06f14a2115ea0c03dd27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:41 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 06:03:41 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:41 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:46 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:47 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:48 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:48 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b130a277b3c71b0c6f20f2fb8612215ef72444dddbf3fe12f0b218caed0f67`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38e7b8d140a14310125ff7f91dc64cb19cd3a0a5a817cce506e5695d84dbd27`  
		Last Modified: Tue, 29 Mar 2022 06:04:38 GMT  
		Size: 37.3 MB (37331182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0447c1a5bb5a74be1c06c517005ec07770f5b73c7d65c3ba265d7bca561dcef7`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd851f9ae4bd13336311e681d92ae1ee4f16923e3ee452666b21f6c6fbd86d0`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574aa87164bb614c33eba24a552adf30f335396154bb677b12d6ee7dea78432d`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:3a19df42f304d3159308cf0e1bd50549253329fd58106d1dd118162eb088bbe0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38202335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788d8ce3c1098f883bc19fc081e64563082b6d3cc198ba0d0a9db6179ceea0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:33:47 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 07:33:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:33:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:33:50 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:34:01 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:34:03 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:34:05 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:34:06 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:34:06 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:34:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:34:07 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:34:08 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:34:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:34:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78374832d4f35022f215e00ba71b8d8a6715f2604e50be6676aaeb584febd5`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25b9d879af1e5cad9f6328a81f46bdca1772ec1780368873d7a10ed48d65659`  
		Last Modified: Tue, 29 Mar 2022 07:36:18 GMT  
		Size: 35.6 MB (35573828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653751aa02c7ec9a66af269e30576c9fd48ed32bbeb6a0fd2a721af3964c9ef2`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3c9783148cddc0f3c36b394a4110f84bcb378069ad08b353b299b1463a2f0`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e1cdc235c39a3bb10542ac09f7e36106333e537be7cae66b5fd9b19fcf1c0e`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f3e40c0b739b9daaf0343c624cd6cf742104faa726549c056d6112a6368b93cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38170103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9d8100cb643e96e94a36a7b728b878de30b56de3edc1c199c745b8d636dc44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:35:10 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 10:35:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:35:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:35:13 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:35:20 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:35:20 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:35:21 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:35:22 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:35:23 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:35:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:35:25 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:35:27 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:35:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15e5e87f79a95792f7734354d34f77a74388032e6506fd750d941b914391a7d`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304416e9d5f69ec82fc993f216eb92552914ad68e0e69f359db42b8a9179afe2`  
		Last Modified: Tue, 29 Mar 2022 10:36:32 GMT  
		Size: 35.4 MB (35445947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc25a722a0c2836f58b95939275a32b70745a0312a3fd4b65cd1110d1c26a05`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac178aa8bfd3745261cfda581772495497ba88d5d7b884bb763aa2b682083630`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a2f51b84250dd16d071ae5b5c4529e339c13a1b990a006c33ecabf46c8439`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:5b9b2f1e98144577f72e4cb317650a75afa360304947b78c728913d986a69533
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39506999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f68d47bc38594a93f69d8f07d790950d9bc0cdb016c892eb36878e1d797a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:16:32 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 04:16:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:16:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:16:35 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:16:40 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:16:41 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:16:42 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:16:43 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:16:44 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:16:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:16:46 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3035dab6c52d3583c2bc3d4c0f7d01d63155c37fc4b510268c910559287cff5`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97085476e88aceae3c890b817ac343a3cf43d52d79361176be00ab9ee524d76`  
		Last Modified: Tue, 29 Mar 2022 04:17:55 GMT  
		Size: 36.7 MB (36683303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9284c2e3362e2463b74dbfbcfd98549722d8e53e8db2072936b56c230a35444`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a06a61eb7fb76f87969e8c54a3b67aae9c38cbfe5edad83f784a05ce47b9790`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3885f98cff34417a4ea7d6b074b391332cc5320797aac2ccf7f9d9ad6a9808d`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.16`

```console
$ docker pull consul@sha256:f3398876019ff10ed45710ed7021fbda3b8a299f8fd24f07b4d31fbc26614a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.16` - linux; amd64

```console
$ docker pull consul@sha256:1cd200f40e014641621eb970c5813fe36ad4772dc10223ce9187380cc788f08b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40153774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d569aa7e4ddb795f026b0b9d927110fde7600e76d79c06f14a2115ea0c03dd27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:41 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 06:03:41 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:41 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:46 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:47 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:48 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:48 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b130a277b3c71b0c6f20f2fb8612215ef72444dddbf3fe12f0b218caed0f67`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38e7b8d140a14310125ff7f91dc64cb19cd3a0a5a817cce506e5695d84dbd27`  
		Last Modified: Tue, 29 Mar 2022 06:04:38 GMT  
		Size: 37.3 MB (37331182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0447c1a5bb5a74be1c06c517005ec07770f5b73c7d65c3ba265d7bca561dcef7`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd851f9ae4bd13336311e681d92ae1ee4f16923e3ee452666b21f6c6fbd86d0`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574aa87164bb614c33eba24a552adf30f335396154bb677b12d6ee7dea78432d`  
		Last Modified: Tue, 29 Mar 2022 06:04:33 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; arm variant v6

```console
$ docker pull consul@sha256:3a19df42f304d3159308cf0e1bd50549253329fd58106d1dd118162eb088bbe0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38202335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788d8ce3c1098f883bc19fc081e64563082b6d3cc198ba0d0a9db6179ceea0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:33:47 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 07:33:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:33:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:33:50 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:34:01 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:34:03 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:34:05 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:34:06 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:34:06 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:34:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:34:07 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:34:08 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:34:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:34:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78374832d4f35022f215e00ba71b8d8a6715f2604e50be6676aaeb584febd5`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25b9d879af1e5cad9f6328a81f46bdca1772ec1780368873d7a10ed48d65659`  
		Last Modified: Tue, 29 Mar 2022 07:36:18 GMT  
		Size: 35.6 MB (35573828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653751aa02c7ec9a66af269e30576c9fd48ed32bbeb6a0fd2a721af3964c9ef2`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3c9783148cddc0f3c36b394a4110f84bcb378069ad08b353b299b1463a2f0`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e1cdc235c39a3bb10542ac09f7e36106333e537be7cae66b5fd9b19fcf1c0e`  
		Last Modified: Tue, 29 Mar 2022 07:36:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f3e40c0b739b9daaf0343c624cd6cf742104faa726549c056d6112a6368b93cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38170103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9d8100cb643e96e94a36a7b728b878de30b56de3edc1c199c745b8d636dc44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:35:10 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 10:35:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:35:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:35:13 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:35:20 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:35:20 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:35:21 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:35:22 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:35:23 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:35:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:35:25 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:35:27 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:35:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:35:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15e5e87f79a95792f7734354d34f77a74388032e6506fd750d941b914391a7d`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304416e9d5f69ec82fc993f216eb92552914ad68e0e69f359db42b8a9179afe2`  
		Last Modified: Tue, 29 Mar 2022 10:36:32 GMT  
		Size: 35.4 MB (35445947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc25a722a0c2836f58b95939275a32b70745a0312a3fd4b65cd1110d1c26a05`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac178aa8bfd3745261cfda581772495497ba88d5d7b884bb763aa2b682083630`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a2f51b84250dd16d071ae5b5c4529e339c13a1b990a006c33ecabf46c8439`  
		Last Modified: Tue, 29 Mar 2022 10:36:27 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; 386

```console
$ docker pull consul@sha256:5b9b2f1e98144577f72e4cb317650a75afa360304947b78c728913d986a69533
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39506999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f68d47bc38594a93f69d8f07d790950d9bc0cdb016c892eb36878e1d797a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:16:32 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 29 Mar 2022 04:16:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:16:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:16:35 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:16:40 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:16:41 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:16:42 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:16:43 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:16:44 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:16:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:16:46 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3035dab6c52d3583c2bc3d4c0f7d01d63155c37fc4b510268c910559287cff5`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97085476e88aceae3c890b817ac343a3cf43d52d79361176be00ab9ee524d76`  
		Last Modified: Tue, 29 Mar 2022 04:17:55 GMT  
		Size: 36.7 MB (36683303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9284c2e3362e2463b74dbfbcfd98549722d8e53e8db2072936b56c230a35444`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a06a61eb7fb76f87969e8c54a3b67aae9c38cbfe5edad83f784a05ce47b9790`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3885f98cff34417a4ea7d6b074b391332cc5320797aac2ccf7f9d9ad6a9808d`  
		Last Modified: Tue, 29 Mar 2022 04:17:50 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:8a6c72bffbbc071635d3aae6b1a9781ce228183b18c86c9c6baae5b9e929118e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:5c638c0ceaaee10de5ce5bc6c12f9fc6e573654a74b4e46bc3c503770e945509
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cd576c5f6970fdbfe3516834beae052fb1ec2843661a9586f1a9a2d958a766`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:03:18 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 06:03:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 06:03:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 06:03:19 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 06:03:24 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 06:03:25 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 06:03:26 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 06:03:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 06:03:26 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 06:03:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 06:03:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cd86ddf7d416a94b4a886647c21c03a1391ea840677ba38d6a7fe86e38bb81`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f957e9afb7a8579402f028966cfd109fbc17d08e18f3a698481fb5c4a069c7`  
		Last Modified: Tue, 29 Mar 2022 06:04:05 GMT  
		Size: 41.1 MB (41121471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb8f5f08d6297bc8fa44d778250df3a159fe3554b8673a9036d16781ba512e0`  
		Last Modified: Tue, 29 Mar 2022 06:04:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a87013b95bb5ed340413ca055c1e362987adecc8912204c3d00c4bdd632591`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d174ae4eb977244b11874e8830088fc8900cd26377aff48b1fcb188a5be20c`  
		Last Modified: Tue, 29 Mar 2022 06:03:59 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:1888ef354a12ac56ddb2b96276c9e83eb633fdd916f52269f7144f1585bc0cf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41703939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97660c8bc3b3f9b0672769a9dc29c524199ccd13f94a04a7581e23a9baf67fe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:32:39 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 07:32:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 07:32:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 07:32:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 07:32:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 07:32:56 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 07:32:58 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:32:58 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 07:32:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 07:33:00 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 07:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 07:33:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfc635fd4572e0b70d19743f459e9d969acc08352742323089eba57d8f38e86`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d091c6e914999d5b31228dcafdc4d91e48f3b2bc401c8fdcec1b6fa739f4a6e`  
		Last Modified: Tue, 29 Mar 2022 07:35:14 GMT  
		Size: 39.1 MB (39075430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b554cf8d29231e5d8b40ad185f6c62049d25d3aac1bdc5641a1a1db1845b6f99`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa142476d37f45100f6069bde9cd7be3f84353fc72d26791c8465e9a3afab0a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148913beff486f9ad60fbde76bf5290ab1c93f5d09ed189df21bc61eb486d4a`  
		Last Modified: Tue, 29 Mar 2022 07:34:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:66b2fa65222251fe2e043a3f99ffc463392432a9e2963cb8c088ad79dd2303b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41548739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f96c12d39fbaab84a8819ac3dced48eef204eff39ada2a24bd8471e0566438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:34:17 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 10:34:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 10:34:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 10:34:20 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 10:34:28 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 10:34:29 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:34:30 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 10:34:31 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 10:34:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 10:34:33 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 10:34:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 10:34:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:34:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d421b63501abd7eb5acfea66de064cce3d12f19b7d827e341af38468541824`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda5a94750831ddfd91231bceafd6ce1f58fd37b5e8e13734f60b500c3794474`  
		Last Modified: Tue, 29 Mar 2022 10:35:56 GMT  
		Size: 38.8 MB (38824582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf164bd3d26bc6d1e8b48cd190c4838ed43d3d68bf1e0c158bdfda521bcff790`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4cab6e8dee57b92aae2cecae23333870064100a8d37d323181fc06ce2cc113`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986dc022b5fdff77aa3482f623f56a75e264b47252f0a6917db1495cb918f59`  
		Last Modified: Tue, 29 Mar 2022 10:35:51 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:7609c7af79d816640380ea00bf3b51729f6b0ea2ce8f3d366f9ced1eec46ee81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42762465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e177daf1713020f8185275a5cb7ff3099fca059b497c43b522b1b27705fc5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:45 GMT
ADD file:f1abe5c2930209c2d735059c8e767e630c0818cc18a4fd10b0b90e6efbc675e2 in / 
# Tue, 29 Mar 2022 00:38:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 04:15:43 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 29 Mar 2022 04:15:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 29 Mar 2022 04:15:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 29 Mar 2022 04:15:46 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 29 Mar 2022 04:15:53 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 29 Mar 2022 04:15:54 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 29 Mar 2022 04:15:55 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 04:15:56 GMT
VOLUME [/consul/data]
# Tue, 29 Mar 2022 04:15:57 GMT
EXPOSE 8300
# Tue, 29 Mar 2022 04:15:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 29 Mar 2022 04:15:59 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 29 Mar 2022 04:16:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 29 Mar 2022 04:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 04:16:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dadad3128a09e6d507e89afe042cb1d48da14a72b28ca79dec7c6acf971bd9e6`  
		Last Modified: Tue, 29 Mar 2022 00:40:03 GMT  
		Size: 2.8 MB (2820388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6563152e47763d9972ac28a087bc8ae8869f1b12824e5e10d949b90f50940`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d132466b4692fe52eb1e51fe72f2d8aa6ed1824741b21caf4e59a6c5cc899b8`  
		Last Modified: Tue, 29 Mar 2022 04:17:20 GMT  
		Size: 39.9 MB (39938763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6f6eb96f21ad2bf510d01e9b0a9f98d7c3d30ecaf3a6ea96d5bb6c08f50b77`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d510af9be8debeae9069e66ef33a087a81a0ff04bccb2c3a6d935ebb8580c`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0618ba92db007797b9a757bd5a525cbc5039b229d5e419e7c3422e5618f4426a`  
		Last Modified: Tue, 29 Mar 2022 04:17:12 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
