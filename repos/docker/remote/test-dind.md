## `docker:test-dind`

```console
$ docker pull docker@sha256:e7c2274945959b5ffbcb146ffb4fbeb769df27a8b0b6e5c04fe911f2d89a534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:98320e6e491d3c0b7be603066175eaa6e23f3b4dffe3f493e7ccab86b6948a4b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74573729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba63cfbc76778322c00026aa3dd95002fb50da4312955b8a544269b9f8c0a2db`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 23:20:49 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 23:20:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 23:20:50 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 23:20:50 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 23:20:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 23:20:56 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 23:20:56 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:20:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 23:20:57 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 23:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 23:20:58 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 23:21:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Dec 2019 23:21:05 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Dec 2019 23:21:05 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Dec 2019 23:21:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Dec 2019 23:21:06 GMT
COPY file:ecdfb2538258e3154663fab9321e96251276aff00fa2a01c2045656e10a627dd in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:21:07 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Dec 2019 23:21:07 GMT
EXPOSE 2375 2376
# Wed, 11 Dec 2019 23:21:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Dec 2019 23:21:07 GMT
CMD []
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ca718c007e090ea606c06ea2d0625898b7c360306699eb418b690c37a01d3e`  
		Last Modified: Wed, 11 Dec 2019 23:21:50 GMT  
		Size: 2.4 MB (2422634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cec70188224ea7ba22191c00accecaaf1b78e1f4fab18701e028cca51d3def4`  
		Last Modified: Wed, 11 Dec 2019 23:21:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c248f2b1183d8e2e483bf7ae591bba5e4a4acd64f28896ea24ccf2bba09b9df9`  
		Last Modified: Wed, 11 Dec 2019 23:22:01 GMT  
		Size: 63.8 MB (63803076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2503d20971037b9a2d5a7c7ffb0bc2ed815dd4aed7ff70ea8ca55d87b85c2ca`  
		Last Modified: Wed, 11 Dec 2019 23:21:49 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b0d619bd33ab28b4e8fe1717ca1f585c4b8fe378f75dba428d12e1a2363b0c`  
		Last Modified: Wed, 11 Dec 2019 23:21:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec7a6d53674b6e4eb41a4141aa72ac2894d0b720162d4def56525d374de64c5`  
		Last Modified: Wed, 11 Dec 2019 23:21:49 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a48ac35fa1a35012549ab3b78195b6d45ffab0a9fcc72c5341c7ea2f01ed5b5`  
		Last Modified: Wed, 11 Dec 2019 23:22:12 GMT  
		Size: 5.6 MB (5554448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377809b0e452b76b024c01a892aa670bfbd9dfc9e9f7de75109590269ab9afeb`  
		Last Modified: Wed, 11 Dec 2019 23:22:11 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84307aacff590d2c328103b231f259707f8c1ecbbe0affce9ab3040d44b5cc`  
		Last Modified: Wed, 11 Dec 2019 23:22:11 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86070856a0fc818943d9c9372bc5ebc270f3e067223110bd570b35fecbc250d`  
		Last Modified: Wed, 11 Dec 2019 23:22:11 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:877e47979983570e53f851aa8fb41b17e902ef6d6620662eb37d412ecfe62cce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67580864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf032d26bd6437dcb33784dfb7629082a2cb131aeb30415276d5a849895a533`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 22:49:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 22:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 22:49:39 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 22:49:40 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 22:49:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 22:49:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 22:49:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 22:49:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 22:49:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 22:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 22:49:55 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 22:50:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Dec 2019 22:50:16 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Dec 2019 22:50:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Dec 2019 22:50:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Dec 2019 22:50:32 GMT
COPY file:ecdfb2538258e3154663fab9321e96251276aff00fa2a01c2045656e10a627dd in /usr/local/bin/ 
# Wed, 11 Dec 2019 22:50:33 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Dec 2019 22:50:34 GMT
EXPOSE 2375 2376
# Wed, 11 Dec 2019 22:50:35 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Dec 2019 22:50:37 GMT
CMD []
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ff5944bdb7e9171cd9a0b4ff982e7f9f76bee3f40ac1a008ca4ef6a3fc27b`  
		Last Modified: Wed, 11 Dec 2019 22:51:15 GMT  
		Size: 2.3 MB (2336234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46de1899c6245f4aa2d837e9f7c82667f72436fcc7f851b6456f00a63952d93`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5467d422b56b61d8e91e846ad852dd7c79cdf05075198258733b2027d5f493c`  
		Last Modified: Wed, 11 Dec 2019 22:51:32 GMT  
		Size: 59.5 MB (59537105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57abdd7b742761c1733281558639e15c8c0451a6ec25fecee23119353c05b73`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8887fef07d0dab5b2fab086bf75186f5d24bc72b9c2e6ffce87a2391007c77cd`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ca6e031218cb5b93c4111cfec0b7f769837784da486b8aba989ca6b22acabb`  
		Last Modified: Wed, 11 Dec 2019 22:51:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a76b4f6e4121e7da80c4af4221d6d4c45f58180a2a612775425371f8cd1a05`  
		Last Modified: Wed, 11 Dec 2019 22:51:46 GMT  
		Size: 3.1 MB (3129714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f77cf40d4f1482950df90f7ab94549c4ccf3172e0f4070dee798f4b2747101`  
		Last Modified: Wed, 11 Dec 2019 22:51:44 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca9067df88c1168f38e515013336c2beb2823499303e55490cc4a09e404eb86`  
		Last Modified: Wed, 11 Dec 2019 22:51:44 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5dc55ddf941dd0b8d99b9b42f40856d8fd95b0e22b086d2c995cba76f06643`  
		Last Modified: Wed, 11 Dec 2019 22:51:45 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c47ad078efdff5fa4bf028276ba1607e6663be291623698923c30ec50b909f2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67086666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e7d9803d535503580af942a61ef24e2625a514b52818867b32d665f9919eaf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:01:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:01:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:01:51 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:01:51 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:02:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:02:02 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:02:03 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:02:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:02:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:02:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:02:07 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:02:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:02:18 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:02:19 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:02:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 26 Dec 2019 21:02:23 GMT
COPY file:ecdfb2538258e3154663fab9321e96251276aff00fa2a01c2045656e10a627dd in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:02:23 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Dec 2019 21:02:24 GMT
EXPOSE 2375 2376
# Thu, 26 Dec 2019 21:02:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Dec 2019 21:02:26 GMT
CMD []
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50cee0efcbfb35406895e68c92bc2bbfb3447d96a7abb40d288629b4b60dbb7`  
		Last Modified: Thu, 26 Dec 2019 21:02:53 GMT  
		Size: 2.3 MB (2254389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616c380c09fcd10304ae95afaf65a56079f310bcd7660b163370efdf0b33a965`  
		Last Modified: Thu, 26 Dec 2019 21:02:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8eb6de7546b474ea400c5f6d22a866ae4d7f2f6464cf86db2adb1213fb57e`  
		Last Modified: Thu, 26 Dec 2019 21:03:10 GMT  
		Size: 59.5 MB (59532264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb49dcdc6cb96b28a162723f7d13520268128fb0dee031e3205e7bb0bb5a26`  
		Last Modified: Thu, 26 Dec 2019 21:02:51 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4531e095724b34fddfb3866f12630bc9e4c059191411ee8d896b8cc994e91`  
		Last Modified: Thu, 26 Dec 2019 21:02:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcae309c142f252026c7392e3ed4340e1de544c8175e791bc420106117a57fc6`  
		Last Modified: Thu, 26 Dec 2019 21:02:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1958f1bd036df3edf8860a0cdbf99ef8a1d34c053f4812b9d32f99acaf33c6bc`  
		Last Modified: Thu, 26 Dec 2019 21:03:27 GMT  
		Size: 2.9 MB (2876858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0091e1ec4c073c221cb6c4f2085c7e859299056cc8df8cba557acb067a84600`  
		Last Modified: Thu, 26 Dec 2019 21:03:27 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685a123dd0c5cb45703dc6a8b0cb7a72b005a6c4fb805828ba00dfbe4152cf89`  
		Last Modified: Thu, 26 Dec 2019 21:03:27 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa2d4c9fd05aa0d967ca626250d341a07529bac37d124f08b69e5ad916d2c3e`  
		Last Modified: Thu, 26 Dec 2019 21:03:27 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8003ebd5f122dc9d2c6cbd9039e69d0d13b602e904fda320641dbc7c5f87661f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67759986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08132b3cbd5d257416b6f79cc8a12f20d85cb41a4d40f097454b5e7fbbea6c1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2019 23:39:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 11 Dec 2019 23:39:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 11 Dec 2019 23:39:42 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Dec 2019 23:39:43 GMT
ENV DOCKER_VERSION=19.03.5
# Wed, 11 Dec 2019 23:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Dec 2019 23:39:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Dec 2019 23:39:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:39:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Dec 2019 23:39:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Dec 2019 23:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2019 23:39:55 GMT
CMD ["sh"]
# Wed, 11 Dec 2019 23:40:07 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Dec 2019 23:40:11 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Dec 2019 23:40:12 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Dec 2019 23:40:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Dec 2019 23:40:17 GMT
COPY file:ecdfb2538258e3154663fab9321e96251276aff00fa2a01c2045656e10a627dd in /usr/local/bin/ 
# Wed, 11 Dec 2019 23:40:22 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Dec 2019 23:40:23 GMT
EXPOSE 2375 2376
# Wed, 11 Dec 2019 23:40:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Dec 2019 23:40:33 GMT
CMD []
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4930edba01571f06733f51438ff75fd189643faaa974ecd081fe02c862f30`  
		Last Modified: Wed, 11 Dec 2019 23:41:12 GMT  
		Size: 2.5 MB (2451440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168cec15ea7d22d62052eca3277505f95f654ea420b93214e439c7bed4e67b95`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b561127bf77d73eae5e1ef05a721ee95b4049642c37de2926df6801485b285e`  
		Last Modified: Wed, 11 Dec 2019 23:41:28 GMT  
		Size: 57.0 MB (57006217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14fc1df435300bb4cc734e1c5ec8835e63a6c4974878ae1df55a0138fbe393`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141662ea1213cce657fd7271df8105b45251ae241897b99143f1c4ecae5c4bd1`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b753173eaf4bfc3b344c536cebf062ddc0d56aa0ab88d30fc4e80cb23e96325`  
		Last Modified: Wed, 11 Dec 2019 23:41:09 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b1c5f65ee755dd97182c2641d94eb393fc0496adf7f1b4bf78bf5b50944e1c`  
		Last Modified: Wed, 11 Dec 2019 23:41:44 GMT  
		Size: 5.6 MB (5578054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b8444b828db4cd92dfcaa796e6a15d1fc3377b030024a8b87c1087429c0762`  
		Last Modified: Wed, 11 Dec 2019 23:41:41 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dd84dc8fd332bb6571553ec1bf4c65377a8924e867bf51c7f6ddfc4daa3efa`  
		Last Modified: Wed, 11 Dec 2019 23:41:41 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ee095995d2a1c5fe6eaf5e8ceaf7ae5a4ef428406c8e3f4b42a12b06af1db2`  
		Last Modified: Wed, 11 Dec 2019 23:41:41 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
