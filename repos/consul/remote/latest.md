## `consul:latest`

```console
$ docker pull consul@sha256:78169b3d6a3b701902c597b37bf2ce9bd1d3ff4f4bb60f3fdb5ebe305555d4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:a24f8b7e304d00f0aebfb896d1660370501d42769e03d777e8fde57abe6a200a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43954472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94840f9c3d714de6095d3aa1ecd3c1eecf18b08949b2f4872eaf730dee42b1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Thu, 14 Apr 2022 21:19:28 GMT
ARG CONSUL_VERSION=1.11.5
# Thu, 14 Apr 2022 21:19:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Apr 2022 21:19:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Apr 2022 21:19:29 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Apr 2022 21:19:34 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Apr 2022 21:19:35 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Apr 2022 21:19:36 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Apr 2022 21:19:36 GMT
VOLUME [/consul/data]
# Thu, 14 Apr 2022 21:19:36 GMT
EXPOSE 8300
# Thu, 14 Apr 2022 21:19:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Apr 2022 21:19:36 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Apr 2022 21:19:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Apr 2022 21:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Apr 2022 21:19:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366e176f83f6feafec08fea5425e8ec846949df9c588dc803bede95b1cd76c15`  
		Last Modified: Thu, 14 Apr 2022 21:20:12 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3904ba849427da5c7775593539c1602dbd2b485737bd6b834b9292141c273b`  
		Last Modified: Thu, 14 Apr 2022 21:20:18 GMT  
		Size: 41.1 MB (41131797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dc1ee883bcf746b7818d21793756259a11b84efef9290267fc1909f324cf9c`  
		Last Modified: Thu, 14 Apr 2022 21:20:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6f99a54b8a09665a2d1207f397c7fc7cb88820a66ff4610b727ec40715542`  
		Last Modified: Thu, 14 Apr 2022 21:20:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d084a8149104cb332535bd837732450d3cc7cf33b6ad885ffb04cb37f71a5187`  
		Last Modified: Thu, 14 Apr 2022 21:20:12 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:f7cd3d8b1ce65ec05bf34c7c634164a7e109ffd24bf1afcc2fedfc7fe371dba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47360944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7d169deff3ee350ee3045c8014b90d0c4683236da625077b09752dba083d40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Thu, 21 Apr 2022 00:04:24 GMT
ARG CONSUL_VERSION=1.12.0
# Thu, 21 Apr 2022 00:04:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 21 Apr 2022 00:04:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 21 Apr 2022 00:04:31 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 21 Apr 2022 00:04:49 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 21 Apr 2022 00:04:55 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 21 Apr 2022 00:05:00 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 21 Apr 2022 00:05:00 GMT
VOLUME [/consul/data]
# Thu, 21 Apr 2022 00:05:01 GMT
EXPOSE 8300
# Thu, 21 Apr 2022 00:05:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 21 Apr 2022 00:05:03 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 21 Apr 2022 00:05:05 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 21 Apr 2022 00:05:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 00:05:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36aa94121a2db80c6e4b353603909ee487e9a1650e86b8e8d1573d52fa03c45`  
		Last Modified: Thu, 21 Apr 2022 00:06:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0cc44b42ed5e016eb276e18680f5c6e16fa7e9fa579b92bc01c966cb6782f3`  
		Last Modified: Thu, 21 Apr 2022 00:06:36 GMT  
		Size: 44.7 MB (44732427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04080b49a8e9747a531f857b11027f9e8044e363fe3150daa0bea9d99055d50`  
		Last Modified: Thu, 21 Apr 2022 00:06:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d011bfa36c14bab9d43017308ba5a57121f5925540d21a4c2f295f30c8a6138`  
		Last Modified: Thu, 21 Apr 2022 00:06:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc1dd017c3ebab8824689b1af78412a7842106ba1ee8832c181b0f30a967b73`  
		Last Modified: Thu, 21 Apr 2022 00:06:11 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6384c74ef13620dd0a1c4a7b2f0dc612068efb0e4fd3c1efc2e9e5c75a51ba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41544558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefa898eb6965c609dbea2c7bf9c1cedaada6d0ce2dcf967a62441331907e59d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Thu, 14 Apr 2022 21:39:30 GMT
ARG CONSUL_VERSION=1.11.5
# Thu, 14 Apr 2022 21:39:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Apr 2022 21:39:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Apr 2022 21:39:33 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Apr 2022 21:39:40 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Apr 2022 21:39:40 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Apr 2022 21:39:41 GMT
# ARGS: CONSUL_VERSION=1.11.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Apr 2022 21:39:42 GMT
VOLUME [/consul/data]
# Thu, 14 Apr 2022 21:39:43 GMT
EXPOSE 8300
# Thu, 14 Apr 2022 21:39:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Apr 2022 21:39:45 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Apr 2022 21:39:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Apr 2022 21:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Apr 2022 21:39:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8ba83fc8974ffe9ca2de6ccfe65988eb1a36e7023d174deab4891b44ee64c7`  
		Last Modified: Thu, 14 Apr 2022 21:40:55 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872ba7fca95b7eebc6bf1ad851d1438e7b455db74d07369d00715ac330a3d4c7`  
		Last Modified: Thu, 14 Apr 2022 21:41:09 GMT  
		Size: 38.8 MB (38820352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb3a46b024bb0414904dd2a30f39d396f568b1d3f1c152412a4747c2bad50f`  
		Last Modified: Thu, 14 Apr 2022 21:40:58 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9298fc2536c2f846eb65eaf4f86631d07b60a49a49d6e6a1fec58129f1e777f8`  
		Last Modified: Thu, 14 Apr 2022 21:40:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0995681561d4261543a5804d8a830837c81ccdcd05a582fed7c4d6fdd03fd762`  
		Last Modified: Thu, 14 Apr 2022 21:40:55 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:3faef884d4731795971556dc6a845088ca9955456496325f39b480e30b69554b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48548561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b61a8c9785d37c5a3ec12138e3c1d53f417e0d0f7a843f97a10a411fafb9cb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:38 GMT
ADD file:caa278dc5cc6257518d542227fef491a89b0b4a7fc4dcb87632c2b786b65752a in / 
# Mon, 04 Apr 2022 23:38:38 GMT
CMD ["/bin/sh"]
# Thu, 21 Apr 2022 02:08:09 GMT
ARG CONSUL_VERSION=1.12.0
# Thu, 21 Apr 2022 02:08:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 21 Apr 2022 02:08:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 21 Apr 2022 02:08:12 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 21 Apr 2022 02:08:20 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 21 Apr 2022 02:08:20 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 21 Apr 2022 02:08:21 GMT
# ARGS: CONSUL_VERSION=1.12.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 21 Apr 2022 02:08:22 GMT
VOLUME [/consul/data]
# Thu, 21 Apr 2022 02:08:23 GMT
EXPOSE 8300
# Thu, 21 Apr 2022 02:08:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 21 Apr 2022 02:08:25 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 21 Apr 2022 02:08:27 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 21 Apr 2022 02:08:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Apr 2022 02:08:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:54c95c2f58283907ca735a3fe8d3ac4a49a63dc20092eb6fddd7bad2429e3f67`  
		Last Modified: Mon, 04 Apr 2022 23:39:46 GMT  
		Size: 2.8 MB (2820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3c3a5b846afbcaeecb22d985a5d900806ba229bc87d910ffe1f07ebd4943d7`  
		Last Modified: Thu, 21 Apr 2022 02:09:01 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d520059bb9b811f92275db02d0a1941bd3bb21c81d7bc542204979f686c70bb0`  
		Last Modified: Thu, 21 Apr 2022 02:09:07 GMT  
		Size: 45.7 MB (45724718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6865f4c431db9e37e48149944b32fef7e11614794c5412b2712a707d482cec84`  
		Last Modified: Thu, 21 Apr 2022 02:09:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ce93115025a22775d6c5c26b04b66c4ce502d090e62967443d439e0cfb1181`  
		Last Modified: Thu, 21 Apr 2022 02:09:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9830e46d08be08c43eddd9fa87624663ba00f52292e8457a66c7bac0bb71597`  
		Last Modified: Thu, 21 Apr 2022 02:09:01 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
