## `docker:dind-rootless`

```console
$ docker pull docker@sha256:8e107e375a0e2f043627b58ff216828221ab55c6a70de3c3cf55171cef4a674e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6a92617cb4df46747dc2fd832bae2ddda144ab9c1116ea2753df44cb211a55ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96448562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d466e72290286bcdfbc871e8561fae40d9eef80790216bb18f18b5313b6e088b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Mar 2022 00:19:37 GMT
ENV DOCKER_VERSION=20.10.13
# Fri, 11 Mar 2022 00:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Mar 2022 00:19:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Mar 2022 00:19:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:19:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Mar 2022 00:19:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Mar 2022 00:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Mar 2022 00:19:42 GMT
CMD ["sh"]
# Fri, 11 Mar 2022 00:19:47 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Mar 2022 00:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Mar 2022 00:19:48 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 11 Mar 2022 00:19:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Mar 2022 00:19:48 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:19:48 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Mar 2022 00:19:49 GMT
EXPOSE 2375 2376
# Fri, 11 Mar 2022 00:19:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Mar 2022 00:19:49 GMT
CMD []
# Fri, 11 Mar 2022 00:19:52 GMT
RUN apk add --no-cache iproute2
# Fri, 11 Mar 2022 00:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 11 Mar 2022 00:19:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 11 Mar 2022 00:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 11 Mar 2022 00:19:57 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 11 Mar 2022 00:19:57 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 11 Mar 2022 00:19:57 GMT
USER rootless
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd0a7b1dec526be119d73f0018052afa23e65ea79e09049a54a5954f2a374`  
		Last Modified: Fri, 11 Mar 2022 00:20:32 GMT  
		Size: 64.6 MB (64612571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317ecb07c86c68358ba3d763bea251b7baf1befde793d08f074abf2743a388dc`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52850491ed6a707afb12e76035b1a36f408c071e00d1de77b26ec2cb178c9a8a`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2b84e11d9e63efd7d7cad8459ac6f5326f44d93991a59380b186824079bdf`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd217e3dc5c63b9a21276d1a8b9b2c0a19dd9aeecf5c242902d63e8dd7c251f`  
		Last Modified: Fri, 11 Mar 2022 00:20:50 GMT  
		Size: 6.7 MB (6734617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f85497bc6212a4fbd95757776ba9f0cfc449ba5ec26f58dc4b48718582d256`  
		Last Modified: Fri, 11 Mar 2022 00:20:49 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63824672dbc4b8bf906bba2cabad90a9964a4de17f7df52debc99611d2782d66`  
		Last Modified: Fri, 11 Mar 2022 00:20:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330cf4336db2c7c1846de44144ed6eb30ac0942792712aeca3f5b38acbd16933`  
		Last Modified: Fri, 11 Mar 2022 00:20:49 GMT  
		Size: 2.7 KB (2747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9243af40d6dedb8bec94753185a0e50302ceca90029164040a3c567cfe6649ed`  
		Last Modified: Fri, 11 Mar 2022 00:21:10 GMT  
		Size: 1.2 MB (1162145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad945e48854711031ed9581488dcd35e6a7281c7cef4273cc6c4fd49fb768ebd`  
		Last Modified: Fri, 11 Mar 2022 00:21:08 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dbac2c48de1cb6054512bc0b3967aa776ed177ce538b1901e10390d2e83250`  
		Last Modified: Fri, 11 Mar 2022 00:21:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2445b41c3397a2f9da27c43cc92a64a2e373b418307bc1a0322072b6f87096`  
		Last Modified: Fri, 11 Mar 2022 00:21:12 GMT  
		Size: 19.1 MB (19131808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec68c91cc2997a8e6a4a961bc06b2a2af234d24e8f116a0ba3a2e0305beaf7`  
		Last Modified: Fri, 11 Mar 2022 00:21:08 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:14752310fd91fd0526dc6695a28eb84ff5801cf2933100d0192e0f1c820c3f2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92143303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8f4cb2d0d6f07648c28e0e32fb7535b1721f91c1eeaf013067af93d831d7f4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Mar 2022 00:39:35 GMT
ENV DOCKER_VERSION=20.10.13
# Fri, 11 Mar 2022 00:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Mar 2022 00:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Mar 2022 00:39:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:39:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Mar 2022 00:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Mar 2022 00:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Mar 2022 00:39:45 GMT
CMD ["sh"]
# Fri, 11 Mar 2022 00:39:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 11 Mar 2022 00:39:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 11 Mar 2022 00:39:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 11 Mar 2022 00:39:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 11 Mar 2022 00:39:59 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:39:59 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Mar 2022 00:40:00 GMT
EXPOSE 2375 2376
# Fri, 11 Mar 2022 00:40:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Mar 2022 00:40:02 GMT
CMD []
# Fri, 11 Mar 2022 00:40:10 GMT
RUN apk add --no-cache iproute2
# Fri, 11 Mar 2022 00:40:11 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 11 Mar 2022 00:40:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 11 Mar 2022 00:40:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 11 Mar 2022 00:40:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 11 Mar 2022 00:40:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 11 Mar 2022 00:40:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6561b7705fefb0b49b335b56a2b49274f9ff6b55220626bd898f2c2d0be00eb4`  
		Last Modified: Fri, 11 Mar 2022 00:41:15 GMT  
		Size: 58.6 MB (58565241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d2cb917414c2052fac63a7dedd59be928c94d5cc572b24406d235f6990010`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250af0478077d2d3407f9444430c3a215d0d39ff3a77f230331773e1c3f44daf`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a445181e9f39b44e6f761cd46ca2a0d56de49eb3c85bd2b43086ca8141bbb9fd`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9894f129b15fd2337ba1fdb4b77a9cf6e3e5c773220ee73406378a8293b5ba3a`  
		Last Modified: Fri, 11 Mar 2022 00:41:37 GMT  
		Size: 6.6 MB (6615365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e626240271e48d4d433148acfaa6af366653f3c34573687464e044e2beb22`  
		Last Modified: Fri, 11 Mar 2022 00:41:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004fde07379e6e576523d144fbf9d7fd6c795d671c38215c689952035cb2f092`  
		Last Modified: Fri, 11 Mar 2022 00:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2bc896368bafb46deb464bcf39c5483fc4dcca552df31c8110d4821e25eae4`  
		Last Modified: Fri, 11 Mar 2022 00:41:36 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2f4edff8765ef5513615882eecbad64a30e2715a9a752a3e8df508c3eb8187`  
		Last Modified: Fri, 11 Mar 2022 00:42:00 GMT  
		Size: 1.2 MB (1178063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90e25edd6329b4c8ad2802a4eb82ffa938400eee901b2ff92ef5245867c3879`  
		Last Modified: Fri, 11 Mar 2022 00:42:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b679094d7c7e29b60bfac146a90eb990f1d8669361e9b498320a87a57905889`  
		Last Modified: Fri, 11 Mar 2022 00:42:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e133d24234a67e712499637a56ad406769172dd157d608a19c5b1ac10e469933`  
		Last Modified: Fri, 11 Mar 2022 00:42:03 GMT  
		Size: 21.1 MB (21111206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea97cb1c4ef21d084778e5a00edc9337177c12dff60964b322dd8f2ad0f8a24`  
		Last Modified: Fri, 11 Mar 2022 00:42:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
