## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:a0e30641697ca722c68a26b104cb271c8f1d1bd9ec3431b06c1c31fe32d06709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab2f198889709d2a8c96373c713802ebf718c3d607a5d865339a07fde1351c9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95554039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669719fc32513aae9029a1f8d6de49809af5919a32f08db35e2af61583ef8e19`
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
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
# Fri, 21 Jan 2022 20:33:40 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 20:33:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 20:33:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 20:33:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 20:33:46 GMT
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
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd98d5908761c9c209aa32ce13b48a2d08571f9259b80a7836bc1f64d1a20d`  
		Last Modified: Fri, 21 Jan 2022 20:34:35 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e732110c5c1fe0503e484447374f44fe316487faddd706b7677bef3e7277e61`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db87b0b5a8a0bc668e24b62e413a751187f963dfe522339421ea6a935ee853`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ab341e7115cfdbece6bf8c6fd568a926610ee00aff041ca3022c00d8a10c8`  
		Last Modified: Fri, 21 Jan 2022 20:34:38 GMT  
		Size: 19.1 MB (19131944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b72a872f74ab4930415afca7a1e77c9db132369ea883da4d8698083f8052d3`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d907b9c8ef192ace2c0e03da806d502d75197c4757243a2847b93d6c18ddb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d79195eb6e0317cec176cf13daddf6e000c65a7c0fde8ff2cfde11466fe479`
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
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
# Fri, 21 Jan 2022 21:02:11 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 21:02:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 21:02:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 21:02:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 21:02:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 21:02:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 21:02:19 GMT
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
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da0b456f787fdd5045043a954f4535d6dc5fd25623135462e686af51fac330`  
		Last Modified: Fri, 21 Jan 2022 21:03:29 GMT  
		Size: 1.2 MB (1178052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aa8cb2a0b40b6a14458bda499fcfce021f46654814f2055fa7c5a464fbb5d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed441dcdb345cac707a1852c447bf8572017ab247e0ecd8cdac11dd173b718`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54ab9c013e77879ef7a63b0d40774c705e03213cb7627df975b1f544aab723`  
		Last Modified: Fri, 21 Jan 2022 21:03:32 GMT  
		Size: 21.1 MB (21105215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0202deee6aed51b38517aa88783c08700bb12b4f9c59308dbf266a972dc233d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
