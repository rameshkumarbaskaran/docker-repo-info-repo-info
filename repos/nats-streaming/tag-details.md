<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.23`](#nats-streaming023)
-	[`nats-streaming:0.23-alpine`](#nats-streaming023-alpine)
-	[`nats-streaming:0.23-alpine3.14`](#nats-streaming023-alpine314)
-	[`nats-streaming:0.23-linux`](#nats-streaming023-linux)
-	[`nats-streaming:0.23-nanoserver`](#nats-streaming023-nanoserver)
-	[`nats-streaming:0.23-nanoserver-1809`](#nats-streaming023-nanoserver-1809)
-	[`nats-streaming:0.23-scratch`](#nats-streaming023-scratch)
-	[`nats-streaming:0.23-windowsservercore`](#nats-streaming023-windowsservercore)
-	[`nats-streaming:0.23-windowsservercore-1809`](#nats-streaming023-windowsservercore-1809)
-	[`nats-streaming:0.23-windowsservercore-ltsc2016`](#nats-streaming023-windowsservercore-ltsc2016)
-	[`nats-streaming:0.23.2`](#nats-streaming0232)
-	[`nats-streaming:0.23.2-alpine`](#nats-streaming0232-alpine)
-	[`nats-streaming:0.23.2-alpine3.14`](#nats-streaming0232-alpine314)
-	[`nats-streaming:0.23.2-linux`](#nats-streaming0232-linux)
-	[`nats-streaming:0.23.2-nanoserver`](#nats-streaming0232-nanoserver)
-	[`nats-streaming:0.23.2-nanoserver-1809`](#nats-streaming0232-nanoserver-1809)
-	[`nats-streaming:0.23.2-scratch`](#nats-streaming0232-scratch)
-	[`nats-streaming:0.23.2-windowsservercore`](#nats-streaming0232-windowsservercore)
-	[`nats-streaming:0.23.2-windowsservercore-1809`](#nats-streaming0232-windowsservercore-1809)
-	[`nats-streaming:0.23.2-windowsservercore-ltsc2016`](#nats-streaming0232-windowsservercore-ltsc2016)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.14`](#nats-streamingalpine314)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)
-	[`nats-streaming:windowsservercore-ltsc2016`](#nats-streamingwindowsservercore-ltsc2016)

## `nats-streaming:0.23`

```console
$ docker pull nats-streaming@sha256:b2d9a260b81f440b6fc59d81d53cc3cc65eca1fb72ccd410707d69654cc8f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-alpine`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-alpine3.14`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23-alpine3.14` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-linux`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-nanoserver`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23-nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-scratch`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-windowsservercore`

```console
$ docker pull nats-streaming@sha256:7a35498f180c36eed2453ef7771a48d709fd86b7f3abaf3d38f8cf57a73845e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2451; amd64
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:0.23-windowsservercore` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23-windowsservercore` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:2cc23cf34a30d07bbb4db6499522e0a48742fae86ad3997f52b88dbf88e2ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:8d7f645475c1ddf54332ac47ad4daa549c2a02a25e27f3062c39efed087fd0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:0.23-windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2`

```console
$ docker pull nats-streaming@sha256:b2d9a260b81f440b6fc59d81d53cc3cc65eca1fb72ccd410707d69654cc8f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23.2` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-alpine`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23.2-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-alpine3.14`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23.2-alpine3.14` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-linux`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23.2-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-nanoserver`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23.2-nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23.2-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-scratch`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.23.2-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-windowsservercore`

```console
$ docker pull nats-streaming@sha256:7a35498f180c36eed2453ef7771a48d709fd86b7f3abaf3d38f8cf57a73845e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2451; amd64
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:0.23.2-windowsservercore` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.23.2-windowsservercore` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:2cc23cf34a30d07bbb4db6499522e0a48742fae86ad3997f52b88dbf88e2ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:0.23.2-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.23.2-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:8d7f645475c1ddf54332ac47ad4daa549c2a02a25e27f3062c39efed087fd0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:0.23.2-windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.14`

```console
$ docker pull nats-streaming@sha256:1c78a54f4963d1eff5a6bd8759a20b2336a5e300fcf5f62611101679c61e7d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.14` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33d7a075703135ba18cf4918fccc35e6fbef1f74ac8bb18abb89a62fde7c4e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0d37898667fe6fa6289417167d7e7ce3799d21b08dc0ea4276850e2e8b54b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:20:53 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:20:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:20:56 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:20:56 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:20:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b719fc3addd4e8cc595271456fe9f9de32955502a0f0cadd27a40bfdce67cdf9`  
		Last Modified: Sat, 20 Nov 2021 02:21:41 GMT  
		Size: 7.6 MB (7581138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16eed54939fd32b16d2ffcc1ac1e816da3a11b3656bf2344d9d3180173bf5`  
		Last Modified: Sat, 20 Nov 2021 02:21:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.14` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:983f8ac2dbbaa85241dbc5508ee63b554e7ac9952787ddb8c11565fe8fa6f89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9694130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6428fa782d5b97614b699deec16e4b3715fe3df66e91d7c27b27104a5534c9f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 23:49:35 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Fri, 19 Nov 2021 23:49:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 19 Nov 2021 23:49:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 19 Nov 2021 23:49:41 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Nov 2021 23:49:42 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824cebd74c6dc7b249f375f4f8b9b003e37db5170f8a26342ed408ae5f39da31`  
		Last Modified: Fri, 19 Nov 2021 23:51:24 GMT  
		Size: 7.1 MB (7058316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba898a9271af9b0a02e91bab485a625e6bba3437f8ed1953bd6497c5a6fee966`  
		Last Modified: Fri, 19 Nov 2021 23:51:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.14` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:8d102ba94dd539c86ae564d1671562cd9687b6001ef28c0a3b9358a31b395259
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe704390d0d6f143b4d58b95fdb72ffd4050dc343669fad7792a25bbd8fc6ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 02:33:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 02:33:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 02:33:46 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 02:33:47 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:33:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 02:33:47 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b93296bc34cee4aad9d52835eae7e820697f4e8ce382165efb96a8901ea0c`  
		Last Modified: Sat, 20 Nov 2021 02:35:32 GMT  
		Size: 7.0 MB (7048204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c793edf6a99d693922586d1182b7f23998316f40d7f5f9e9c74fca0561094`  
		Last Modified: Sat, 20 Nov 2021 02:35:27 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c87eb1e5ff911b6ca53a44595f294a4e79baef015629cd41355e25a3bcbebffc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9669856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89205df0bff2640b3f02b3d8eddbce0582d123a8e34ae55fa68fb034b4e42bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 20 Nov 2021 04:20:45 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Sat, 20 Nov 2021 04:20:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='623cd04855e16ca52694964e01e3b50ded9747a45885bba1a705513da297f6fd' ;; 		armhf) natsArch='arm6'; sha256='fd40f251da335eb7b3cc63b08f8bc0a80d3a4df10fec4efdf6e60417248a5287' ;; 		armv7) natsArch='arm7'; sha256='83db867570654731de98f135f9f373d0758bd9c5a3ee304b65c8128e1d928023' ;; 		x86_64) natsArch='amd64'; sha256='d0c5ebc16901bdc4788d0382dab6f7ce69582e1bafea3ddba159b38ae87b6c81' ;; 		x86) natsArch='386'; sha256='8b9c5396a7747abc8415dc8ca915cf6cb2fd1b79b64ce7a4c3f5efb241cd389f' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 20 Nov 2021 04:20:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 20 Nov 2021 04:20:50 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:20:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Nov 2021 04:20:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a942eeaa58bb70c5a728104921dad38ccc6d39aca7c779aa1431c751506e6ab`  
		Last Modified: Sat, 20 Nov 2021 04:21:41 GMT  
		Size: 7.0 MB (6951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89828a2f02db651c46db6cbf2f637d36ecc30f847933336bb73135367cd013`  
		Last Modified: Sat, 20 Nov 2021 04:21:40 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:b2d9a260b81f440b6fc59d81d53cc3cc65eca1fb72ccd410707d69654cc8f8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:82605b4b655e4adb3b73823e0d51f5223dcc2b4a8b1c889b24c3e0654c991239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:3ca17dfe1d51f68e93f291806eee49a8f25907650f130db8aa2e05f0bafccfa4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110441726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dba39f0a0d9a36ff34a9a56c4572f23ee9e745feba7cf22143755af84a3505`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:15:41 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 21:23:32 GMT
RUN cmd /S /C #(nop) COPY file:bb30895f60b97f75adc45bbc64dd23d70df079c19ad26c4f8d07ce1c88e77c96 in C:\nats-streaming-server.exe 
# Tue, 11 Jan 2022 21:23:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7e0d8adfb71ce7eb5a4fc2b1c6af90cb9e67d616478257638845f142a0ca06d`  
		Last Modified: Tue, 11 Jan 2022 21:19:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441a264a7d8473af9caed52148ae0549a18201d06d4a75cb59a82472781cd037`  
		Last Modified: Tue, 11 Jan 2022 21:27:24 GMT  
		Size: 7.4 MB (7422482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506b90b16e9c62031d17aaddf2dde26e438a8bf5aa6f1be57c283e043cdc546e`  
		Last Modified: Tue, 11 Jan 2022 21:27:21 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7438eec0b8e62e4a1f7b069f7be76a682fbef565f6f7d78b5e51bc9ae47ff6c`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3f0db377b3fd8adf0559beb664f5f9bcd039777af88ee7b960b342b03b85b`  
		Last Modified: Tue, 11 Jan 2022 21:27:22 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:a80b4649e47eb1640ead441ff67bb621bffc4cecd39041fa6e9802fbdd9b3760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05a387b6bd267efd7806a67b7b4d431d054e69537a8dd00f0a874e71b48be7e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1cf392bf11cb1f2dac51f4d09fa86f69859583c3ac7d4812f6c1887d485073`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:21:16 GMT
COPY file:430b600f51b8ec2b8032b9ee2b54a3f23458b67e7fcd26e03d4a1c4fb292e8e3 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:21:16 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:21:16 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:21:17 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ea39d064fdb9df476b776a2728cf769791a02b09590387975647243e2266b1ca`  
		Last Modified: Sat, 20 Nov 2021 02:22:01 GMT  
		Size: 7.3 MB (7299150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:0c1a07390ec1c002d89b5bcd0d0048c95f33f859d53b607ffdc16678e3f79bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6774516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1392e1316cac3fc870ec9cd90c7973466ed1433895aee0166a624b060262b6b5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 19 Nov 2021 23:50:00 GMT
COPY file:d86d6a12a47b28bc562444b508d1508f4f436aa57b4f9785d2f72f13991058d9 in /nats-streaming-server 
# Fri, 19 Nov 2021 23:50:00 GMT
EXPOSE 4222 8222
# Fri, 19 Nov 2021 23:50:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 19 Nov 2021 23:50:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ada5d2acf52444276ec7168ad03307d61f3ac5bb2e33825f280ba40e265f0533`  
		Last Modified: Fri, 19 Nov 2021 23:51:55 GMT  
		Size: 6.8 MB (6774516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:62364f60027f7c3607653a956cf2578021f20431d07038537298bd2e053f622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e200b7f1afcc145455136db22812cb59ac4b91d3018f34d80f3df1980798dfa`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 04:21:01 GMT
COPY file:758facc101ea28c799c8630223bb78d0e4182d429b666642665350bc7a40a28d in /nats-streaming-server 
# Sat, 20 Nov 2021 04:21:01 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 04:21:02 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 04:21:03 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:372c129ce02fe71df79c38000ee3af5425ca18626def1095c58ab7c9cc6a31a8`  
		Last Modified: Sat, 20 Nov 2021 04:22:04 GMT  
		Size: 6.7 MB (6666709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:7a35498f180c36eed2453ef7771a48d709fd86b7f3abaf3d38f8cf57a73845e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2451; amd64
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:2cc23cf34a30d07bbb4db6499522e0a48742fae86ad3997f52b88dbf88e2ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:8d7f645475c1ddf54332ac47ad4daa549c2a02a25e27f3062c39efed087fd0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4886; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.4886; amd64

```console
$ docker pull nats-streaming@sha256:d55e31a14946b12f1d6c152dfb777ad1b2da038f0c957bde81c5cfb59cd1a97d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6290824289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111095c35ecacfdbe68e1ef364f73124e3888020c1fdffe9c88d2b78bd021fa8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:57:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:41 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:42 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:43 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:24:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:26:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:26:29 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:26:31 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:26:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25aec0a6b64c784bf7521344203ee5def4d38eedfdd68f4b452d3250b5b9ddcf`  
		Last Modified: Tue, 11 Jan 2022 21:19:46 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fffdd310a93f98578e45ffbf8e22c031b37efefcc042f21d2a63c2a77c4ee3`  
		Last Modified: Tue, 11 Jan 2022 21:19:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf3c8d8140ae38c2d505f95e5babf9f4505d67a6151d6fe3f9c751ef7d0dc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc2e3eee55193ca6704fc85c6992e8b9b8bd428d80239cd34ee31b8c72fdc5`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cc106ea2da4cb4db419ee1efe603754ac4e6645cde9bdf6ee8bde96b5e342a`  
		Last Modified: Tue, 11 Jan 2022 21:27:37 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b53c2023c3798cb5b4fb1bf2c6c906c1c9ec3f1a64fe6ca6832b146c5e926`  
		Last Modified: Tue, 11 Jan 2022 21:27:35 GMT  
		Size: 335.6 KB (335575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49df4cdedb96e996d903b4a909a6204919bef00f7a72eea5fc92c42249b541c`  
		Last Modified: Tue, 11 Jan 2022 21:27:48 GMT  
		Size: 12.3 MB (12274958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21ee223236021b829cf5aa5a4a19abe4854ed145378b8ca64aed39459a5611`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ccb79a6a3985e5a419e8c0f1256719adee45c6ab7d7a049e39e42ee798e91`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb13dd255898f881701597b01fa5e3b8873647e6098933da4de040996a6188d`  
		Last Modified: Tue, 11 Jan 2022 21:27:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
