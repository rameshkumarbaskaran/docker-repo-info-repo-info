<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.24`](#nats-streaming024)
-	[`nats-streaming:0.24-alpine`](#nats-streaming024-alpine)
-	[`nats-streaming:0.24-alpine3.15`](#nats-streaming024-alpine315)
-	[`nats-streaming:0.24-linux`](#nats-streaming024-linux)
-	[`nats-streaming:0.24-nanoserver`](#nats-streaming024-nanoserver)
-	[`nats-streaming:0.24-nanoserver-1809`](#nats-streaming024-nanoserver-1809)
-	[`nats-streaming:0.24-scratch`](#nats-streaming024-scratch)
-	[`nats-streaming:0.24-windowsservercore`](#nats-streaming024-windowsservercore)
-	[`nats-streaming:0.24-windowsservercore-1809`](#nats-streaming024-windowsservercore-1809)
-	[`nats-streaming:0.24.3`](#nats-streaming0243)
-	[`nats-streaming:0.24.3-alpine`](#nats-streaming0243-alpine)
-	[`nats-streaming:0.24.3-alpine3.15`](#nats-streaming0243-alpine315)
-	[`nats-streaming:0.24.3-linux`](#nats-streaming0243-linux)
-	[`nats-streaming:0.24.3-nanoserver`](#nats-streaming0243-nanoserver)
-	[`nats-streaming:0.24.3-nanoserver-1809`](#nats-streaming0243-nanoserver-1809)
-	[`nats-streaming:0.24.3-scratch`](#nats-streaming0243-scratch)
-	[`nats-streaming:0.24.3-windowsservercore`](#nats-streaming0243-windowsservercore)
-	[`nats-streaming:0.24.3-windowsservercore-1809`](#nats-streaming0243-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.15`](#nats-streamingalpine315)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.24`

```console
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine` - linux; amd64

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

### `nats-streaming:0.24-alpine` - linux; arm variant v6

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

### `nats-streaming:0.24-alpine` - linux; arm variant v7

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

### `nats-streaming:0.24-alpine` - linux; arm64 variant v8

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

## `nats-streaming:0.24-alpine3.15`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine3.15` - linux; amd64

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

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v6

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

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v7

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

### `nats-streaming:0.24-alpine3.15` - linux; arm64 variant v8

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

## `nats-streaming:0.24-linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3`

```console
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-alpine`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-alpine` - linux; amd64

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

### `nats-streaming:0.24.3-alpine` - linux; arm variant v6

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

### `nats-streaming:0.24.3-alpine` - linux; arm variant v7

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

### `nats-streaming:0.24.3-alpine` - linux; arm64 variant v8

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

## `nats-streaming:0.24.3-alpine3.15`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-alpine3.15` - linux; amd64

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

### `nats-streaming:0.24.3-alpine3.15` - linux; arm variant v6

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

### `nats-streaming:0.24.3-alpine3.15` - linux; arm variant v7

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

### `nats-streaming:0.24.3-alpine3.15` - linux; arm64 variant v8

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

## `nats-streaming:0.24.3-linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.3-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.3-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:0.24.3-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `nats-streaming:alpine3.15`

```console
$ docker pull nats-streaming@sha256:a28aa20d2054cd70a7abe3e0224dbc6d46eba90e9b43b2f83c5f5ae5b72fbf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.15` - linux; amd64

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

### `nats-streaming:alpine3.15` - linux; arm variant v6

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

### `nats-streaming:alpine3.15` - linux; arm variant v7

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

### `nats-streaming:alpine3.15` - linux; arm64 variant v8

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

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:9f8cedbf2e74e6679e9ab44848904ad048f1f9202d1dd72e203002605ba4a331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:427167cf68f6cc7da882af2fe3a4b7c8089d370a60bdfb20d1c2f432095618d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:bf5f4238170d36fdc3b99a4ab8acea5c5755564d3d97131d48d0730dee33bbdc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110249474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68219116c19a9ac4e2603cd23ba4233e15f3ab67ba4a4e9169a2c000801679cc`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:21:44 GMT
RUN cmd /S /C #(nop) COPY file:2bdfa73d50ba6f64f600945ecab061708a66086f5dd80ec5e00ad93c8bf3b8b6 in C:\nats-streaming-server.exe 
# Wed, 09 Mar 2022 23:21:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:47 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3128e56b52a1dd66549cb7830a9bc9f9352ab11829fe936a4bd03858ac830160`  
		Last Modified: Wed, 09 Mar 2022 23:22:35 GMT  
		Size: 7.2 MB (7190251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c581f41ddfe2959d4092845a36fa343eaddd42a160cd818cbca5c31671bff`  
		Last Modified: Wed, 09 Mar 2022 23:22:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba79d16ae428589a386d36328db720a9ac0eb1abd0014da9992cb03cf4df1e`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c567d244b9f979dfa1c24fe471a72b7dc849619f91830d175ca5454f357a2eb`  
		Last Modified: Wed, 09 Mar 2022 23:22:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:4f097bcee579937a2b55f7702298c9d0ccf44bc8fc2820b81ef02b1a9b146e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eea355922fa3e329228180c171fe18939205a5828944f3c0ec23c0816eef7982
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db0f18c883ff929dfaae3de15de5562de5be34b4a941aa05c6d52112b8e4c84`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:21:18 GMT
COPY file:6fcfe62a6cc0951979b80258fb3d207e13828d9234e227e1398cab40548702d7 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:21:18 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:21:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:64b920df5d588d78c6c317a08480a016eb7b6433705c1a3811a22e4e422e61d0`  
		Last Modified: Wed, 09 Mar 2022 23:22:00 GMT  
		Size: 7.1 MB (7081263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:36364386127a72bc130f59fb33c4119222fc6c671e33aea460f694025b82cd46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6597197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a965dc95f8a3e6631c5ca714f0aafd2acc1508a1f6d3298300876536949f11b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:49:55 GMT
COPY file:d62d923585419f7f9d263c0018d56cc159b1092bf7bae749223f339a514a81d9 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:49:56 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:49:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:0b00cb53513f9c5bd72363c73ee281128c2cedd1d7653aa7278a2a6536c86a14`  
		Last Modified: Wed, 09 Mar 2022 23:51:50 GMT  
		Size: 6.6 MB (6597197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:c786255507edae1bf8167b3adbe962fa9c4ba18fd683462921df662c86e5f36f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6589565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb16b4f9d4a38de66adad0c74fd19049b37e96277e0cd459805b74bdf9474ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:29:51 GMT
COPY file:a5f2524f76b038dc99564d67f8cf6396171fe569b86b60aa9892eca88643b977 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:29:52 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:29:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:29:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:271fefa5e75537e471ab2e96d1b28b6614b2103db059b37f0e60bcc9b8ab40d8`  
		Last Modified: Wed, 09 Mar 2022 23:31:44 GMT  
		Size: 6.6 MB (6589565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bb6e16886863d8c84bc6427c4a45c43bca8f97adcddd602756dddc70fa826a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd1fc4d49faf17ca5b2a9d116b2758a93de1af0ea5b526e23128bd6bbd00b5f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 09 Mar 2022 23:41:07 GMT
COPY file:f47e5ea058ace7f6cdb8bca186dec2b15d364fff4ff67303ae8d2cfe38435050 in /nats-streaming-server 
# Wed, 09 Mar 2022 23:41:07 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:41:08 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 09 Mar 2022 23:41:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9e32cf3eae8c97676148171d71a3cc25149de87eecd89a137222b3b382cdf8f2`  
		Last Modified: Wed, 09 Mar 2022 23:42:13 GMT  
		Size: 6.5 MB (6510632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:112510afc4add9efb62621bbcbd4c03a62c4efa7bebfa2854d896a3b81b4822b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats-streaming@sha256:38aa3744b326ea3530932f9ae38c5884a7cc4f4e5e71b77f330b5634d79fa79a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723329559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5125257a9aa0beaab36a017e9f82750b3aac24f4719374d6cc8e339fc187cdd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER=0.24.3
# Wed, 09 Mar 2022 23:18:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.3/nats-streaming-server-v0.24.3-windows-amd64.zip
# Wed, 09 Mar 2022 23:18:48 GMT
ENV NATS_STREAMING_SERVER_SHASUM=7473bfa7efd734ca6984907bc9586260031cca926883b468b4752557ecefaff0
# Wed, 09 Mar 2022 23:19:49 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 23:21:27 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 23:21:28 GMT
EXPOSE 4222 8222
# Wed, 09 Mar 2022 23:21:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Mar 2022 23:21:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1aac6ec834525c931dc81bbbb6d32996b82fd755a3bd625af11f40b8fc66bb`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d303e56675a80a6fa4eef8ef31d6f93742709f41058dcf6e36b8ba6d71a466f8`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8122e4b6aba607bd3d7b17a847d8ab75da7d7cb7a2bbb035e4a31cfc1b7ce6`  
		Last Modified: Wed, 09 Mar 2022 23:22:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393372fa0a20ba2589a43d177f33a0360245be974d231efaa7ab980bc342b574`  
		Last Modified: Wed, 09 Mar 2022 23:22:13 GMT  
		Size: 349.0 KB (348988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cf158dc37e43f4d84e520f088e32b2851abbf4a70af92161ab5e0d7e3ecbd`  
		Last Modified: Wed, 09 Mar 2022 23:22:20 GMT  
		Size: 7.5 MB (7516588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fff4072b17e75a66709617708b8b9263dabe4a12c4e0a594fb52e058977fa83`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de86f56dd22fbee61ed7161f763ba9de61d7cbf9623b85a879723ea5670f6e20`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04add3ff0ef25a1f32aab83f90a95cffab3d4b55afd3eb376a861b36094a0b0`  
		Last Modified: Wed, 09 Mar 2022 23:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
