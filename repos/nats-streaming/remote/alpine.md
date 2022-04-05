## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:dc0e193ca9e830f3d545251b67a98ff9d8b705dc8a7c8691306a938a2ba39e73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10169964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30262df5de338662c0205776b9d726c3e76926a95702ec0cd0f3af9d51fd32a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:20:53 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Tue, 05 Apr 2022 07:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 05 Apr 2022 07:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 05 Apr 2022 07:20:56 GMT
EXPOSE 4222 8222
# Tue, 05 Apr 2022 07:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:20:56 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0697d3db732ba0795dafaed090d4c16e7b233441cac5bdf363c0fed728bc2b0d`  
		Last Modified: Tue, 05 Apr 2022 07:21:23 GMT  
		Size: 7.4 MB (7354984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1b831418498002d110731e4fe4c9c85234ec9c9339003b0631d84c6b91a5f5`  
		Last Modified: Tue, 05 Apr 2022 07:21:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ce38d16286eb4e4442a17ff66530a8a85c2ef434d798c01ea16ced2a1acee749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9492313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8513f2f948457ca06d7b7c9fca02a45bc9cd7a6ea65365405fc85ce5f63b3d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:39:07 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Tue, 05 Apr 2022 06:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 05 Apr 2022 06:39:12 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 05 Apr 2022 06:39:12 GMT
EXPOSE 4222 8222
# Tue, 05 Apr 2022 06:39:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 06:39:13 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cdd3e4b77199e123a46851438b751329d1ec9b44fd0ac88a174cd334040ab6`  
		Last Modified: Tue, 05 Apr 2022 06:40:53 GMT  
		Size: 6.9 MB (6869920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f304d8f94348c7bc570139050fa7ef0afe9bfc753d600ac8503ae1349dbce8b4`  
		Last Modified: Tue, 05 Apr 2022 06:40:48 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:56350c93b97431564e66fa2631c6ca8fbc559c812ddf7c53883b1b812626b2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9286907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7408e7aa5074eb00b524eaac63814b05bb76c11cd8cd2a56fc2e23d197ca04cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 15:58:40 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Tue, 05 Apr 2022 15:58:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 05 Apr 2022 15:58:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 05 Apr 2022 15:58:45 GMT
EXPOSE 4222 8222
# Tue, 05 Apr 2022 15:58:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 15:58:46 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1a238a48f5b09ad796a4820202d91b3465b96d3af0954566b3c48cea8da9ad`  
		Last Modified: Tue, 05 Apr 2022 16:00:49 GMT  
		Size: 6.9 MB (6862161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97fc813cc2b1799824f970d8383d9cb0e3db56e7d239103aa36a5a7e747e3cd`  
		Last Modified: Tue, 05 Apr 2022 16:00:45 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2bb6b3dfc031ca2d85c08f06724518b79a8172d220b9910a62b93e5bfc2c64fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9499968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737e9441ef4b0e3ac9d8b2eebf27f05fa328ac5b3b82a242adac734055fc3e41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:18:54 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Tue, 05 Apr 2022 14:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3d483a033dd054cf0446ca2c5a5d7c6b7ce58de3155008b2281c50922cbe6426' ;; 		armhf) natsArch='arm6'; sha256='f78977a51901034927264e8087acc05d65aecf77bf9f4e421168a0afd81587c2' ;; 		armv7) natsArch='arm7'; sha256='efb2a459cfef1c08b4041becdc16ae631c4bcd9ec767635051e67e609f4cacef' ;; 		x86_64) natsArch='amd64'; sha256='bf87f5e0ceb95e4fd12b7256cac9149de6f44b60a296547e7dc915c08f05859a' ;; 		x86) natsArch='386'; sha256='e5d0871f4c8c3bafa075e02604be0adc92cba1ebe8da0c7855bff3a4e5cb0ad1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 05 Apr 2022 14:18:58 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 05 Apr 2022 14:18:58 GMT
EXPOSE 4222 8222
# Tue, 05 Apr 2022 14:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:19:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2605a41f5286ccf3db519841cbe876f6d3c177db99d7b7f603487ae1d19bc4`  
		Last Modified: Tue, 05 Apr 2022 14:19:47 GMT  
		Size: 6.8 MB (6783069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02aac271c37ea72ff53709a15d36e2c35b1c15f4e53f68608efc9a0bb30fce02`  
		Last Modified: Tue, 05 Apr 2022 14:19:46 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
