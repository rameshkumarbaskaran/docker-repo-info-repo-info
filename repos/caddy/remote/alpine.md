## `caddy:alpine`

```console
$ docker pull caddy@sha256:c1adaee50c275c671ec04466d34beb647b3dc19399e1282e6d272eaef25c77d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:09f31d1398820362f71bd863c8435a37aaedda9d02fe76c71ccc1c6bc62e46cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13319309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ffdd09752fbe7b156120e1250d5383a3670292ae5e9a0e317883f52e732cde`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 07 Sep 2021 19:17:07 GMT
ENV CADDY_VERSION=v2.4.5
# Tue, 07 Sep 2021 19:17:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='1a19a8d94c6c16d8e671c4dad1e835e7d0d586a36e15f5300b374e5d31cf10eafdf07bc2c24d5589cdfaff1dd276e4627917802e858e14dc2351797d7dec7586' ;; 		armhf)   binArch='armv6'; checksum='5b68e8b9491507591bfa42880a771f5c687e9e081ccc249a2356b0a1cafc108214e6915d86a5342e6eb99c329942cd027bfd8960d38dae11c91a47a43926b1a8' ;; 		armv7)   binArch='armv7'; checksum='e39210f8e3634ebc85a3a32bda4bcb2263d508744f8ba3b2e9e56012cda17cabe16f2318f991e3d1d8306da49fcc2fa3bfef98f3412bbcf734376ea3bcbdf2ea' ;; 		aarch64) binArch='arm64'; checksum='da23940ff938c953d288555366e09632b31fd248e337da1990cebf0471957d14196f38396fd055d4b409f9960e2d8fb94b26ab435662a871b5ea300b9e77ad25' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='cf8d73a238628cfacea7d309f64248a6e25c76dd76a669a646845b4ca729fd677e30a2a29c75936d810b9f55df89fa17f9b6bc42c5d69e8e02b12ef4e334ad91' ;; 		s390x)   binArch='s390x'; checksum='21631de0d9c93346a9ab8658990c87bacda9c401ddb4b850a59f0c9f9665e0b93b02c0516df55eb03829f0eb5fb546683ba2d5e7b8f6174a7dfb3d13db9d81cd' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.5/caddy_2.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 07 Sep 2021 19:17:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 07 Sep 2021 19:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 07 Sep 2021 19:17:56 GMT
ENV XDG_DATA_HOME=/data
# Tue, 07 Sep 2021 19:18:01 GMT
VOLUME [/config]
# Tue, 07 Sep 2021 19:18:05 GMT
VOLUME [/data]
# Tue, 07 Sep 2021 19:18:12 GMT
LABEL org.opencontainers.image.version=v2.4.5
# Tue, 07 Sep 2021 19:18:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 07 Sep 2021 19:18:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 07 Sep 2021 19:18:25 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 07 Sep 2021 19:18:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 07 Sep 2021 19:18:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 07 Sep 2021 19:18:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 07 Sep 2021 19:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 07 Sep 2021 19:18:55 GMT
EXPOSE 80
# Tue, 07 Sep 2021 19:19:04 GMT
EXPOSE 443
# Tue, 07 Sep 2021 19:19:12 GMT
EXPOSE 2019
# Tue, 07 Sep 2021 19:19:21 GMT
WORKDIR /srv
# Tue, 07 Sep 2021 19:19:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475efcd27e409cc064d659d255fbfb70896b95c3c36149b9a5b8d1abe86e656b`  
		Last Modified: Tue, 07 Sep 2021 19:21:14 GMT  
		Size: 10.2 MB (10197877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a9218ca8c9a1a05649cc5d0eb91f1b2985152d796a63f525c75f5380288bf8`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
