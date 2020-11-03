<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.19`](#nats-streaming019)
-	[`nats-streaming:0.19.0`](#nats-streaming0190)
-	[`nats-streaming:0.19.0-alpine`](#nats-streaming0190-alpine)
-	[`nats-streaming:0.19.0-alpine3.12`](#nats-streaming0190-alpine312)
-	[`nats-streaming:0.19.0-linux`](#nats-streaming0190-linux)
-	[`nats-streaming:0.19.0-nanoserver`](#nats-streaming0190-nanoserver)
-	[`nats-streaming:0.19.0-nanoserver-1809`](#nats-streaming0190-nanoserver-1809)
-	[`nats-streaming:0.19.0-scratch`](#nats-streaming0190-scratch)
-	[`nats-streaming:0.19.0-windowsservercore`](#nats-streaming0190-windowsservercore)
-	[`nats-streaming:0.19.0-windowsservercore-1809`](#nats-streaming0190-windowsservercore-1809)
-	[`nats-streaming:0.19.0-windowsservercore-ltsc2016`](#nats-streaming0190-windowsservercore-ltsc2016)
-	[`nats-streaming:0.19-alpine`](#nats-streaming019-alpine)
-	[`nats-streaming:0.19-alpine3.12`](#nats-streaming019-alpine312)
-	[`nats-streaming:0.19-linux`](#nats-streaming019-linux)
-	[`nats-streaming:0.19-nanoserver`](#nats-streaming019-nanoserver)
-	[`nats-streaming:0.19-nanoserver-1809`](#nats-streaming019-nanoserver-1809)
-	[`nats-streaming:0.19-scratch`](#nats-streaming019-scratch)
-	[`nats-streaming:0.19-windowsservercore`](#nats-streaming019-windowsservercore)
-	[`nats-streaming:0.19-windowsservercore-1809`](#nats-streaming019-windowsservercore-1809)
-	[`nats-streaming:0.19-windowsservercore-ltsc2016`](#nats-streaming019-windowsservercore-ltsc2016)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.12`](#nats-streamingalpine312)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)
-	[`nats-streaming:windowsservercore-ltsc2016`](#nats-streamingwindowsservercore-ltsc2016)

## `nats-streaming:0.19`

```console
$ docker pull nats-streaming@sha256:a533473ab8df95ad3a2317a3d3f177186b76014e8b7b2dd1a8d2fd9c968a01b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0`

```console
$ docker pull nats-streaming@sha256:a533473ab8df95ad3a2317a3d3f177186b76014e8b7b2dd1a8d2fd9c968a01b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19.0` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-nanoserver`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19.0-nanoserver` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19.0-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19.0-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore`

```console
$ docker pull nats-streaming@sha256:0ae3287ed23dc6163b1eae4339e2a00b685c19eeb1cfba03c672214ee3201fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:0.19.0-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19.0-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:9e2d55072dc77e8efb56cc87523742790e4ad3f409e8038434365ecaf37411f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19.0-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19.0-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:39c649ab47271e07c6ecf9cedfdc010d6bffba506c04f9a011d24c7cb704f797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:0.19.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-nanoserver`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19-nanoserver` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.19-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore`

```console
$ docker pull nats-streaming@sha256:0ae3287ed23dc6163b1eae4339e2a00b685c19eeb1cfba03c672214ee3201fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:0.19-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.19-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:9e2d55072dc77e8efb56cc87523742790e4ad3f409e8038434365ecaf37411f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:0.19-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.19-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:39c649ab47271e07c6ecf9cedfdc010d6bffba506c04f9a011d24c7cb704f797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:0.19-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.12`

```console
$ docker pull nats-streaming@sha256:5f15b51b2b447004408633f8f9458106fadad8f21393b1ed531071731e1ddb00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:a8fcf986c14ae3ad60206bd6ebde23999c28f9967f05b9c81a760054539a683d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b4ccbdde21c3fb61f4bd7fa3e83384f7e9d7f32f5bb86c88cd162a41403c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:33:01 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:33:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:33:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:33:04 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:33:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ef5561f154a9a5957cdf08a625861df698594add9ba490a54259e9a01cb1`  
		Last Modified: Tue, 03 Nov 2020 00:33:28 GMT  
		Size: 6.8 MB (6770312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef7e98823e252892036fb4b7e5ccf695c556028fa2f7dd6dc314f625ba9eb9`  
		Last Modified: Tue, 03 Nov 2020 00:33:27 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2a58d6644e94cc17212ec6a604029ebe9f855ceeee7fa66171bdc8aa6c7113ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8391afd58a04ec8cf1ab166357c9495c5aa4d32bc4bb4472e577874f42fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:56:13 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Mon, 02 Nov 2020 23:56:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:56:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 02 Nov 2020 23:56:18 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:56:19 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cba1ed5b5094a02c017d654b758674905ec0bb2535d3311fcdd61dce32b319`  
		Last Modified: Mon, 02 Nov 2020 23:56:50 GMT  
		Size: 6.3 MB (6329871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3992f15ff4c1a7660c4a81854ec33d3e4973405c7095ceb0bd8a7865fff21c9f`  
		Last Modified: Mon, 02 Nov 2020 23:56:47 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6a6c52fc272b91cff878ca25bddc432f19583a2e41e5e92288f0e64d0c649896
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8730479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4347330ee2d9b26f7fafaadc370627e71670505b340c9e4b54d791afcb3a6b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:05:05 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:05:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:05:09 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:05:10 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:05:11 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34033d6dabe9c0f77f765bf2fce39f1eef24c163cfa802ec78f0e2e1bea9da7c`  
		Last Modified: Tue, 03 Nov 2020 00:05:43 GMT  
		Size: 6.3 MB (6324384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a98c9d7b5d859df80140920031b236b38ff88a4ff09d3bf8cfc5b9776e436`  
		Last Modified: Tue, 03 Nov 2020 00:05:40 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36be57b574502addd00c81caaffedb9030eec583dbf4e3011a95aa7f998834aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8969159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b947ac7936fa0250ecf3f1aaa6e22a928bdb3cdd8f0dcbbc3b8912a0678290c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:43:12 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:43:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d582023b8f9fe33b98f0faa6396aae8d5366ecade7e56cde912e21e5b93ea670' ;; 		armhf) natsArch='arm6'; sha256='f4af03e6cbb19f3ad9ea57217607dcf4b68018e1879859c847e2680917fc7139' ;; 		armv7) natsArch='arm7'; sha256='ec8c5ca693344e8b24de9ac955c38de757af8c5760658fc29ed2fbd804803fad' ;; 		x86_64) natsArch='amd64'; sha256='fc15530faec66b61de5140c2b99927c5839caff1c4c17f8bffbf4432fab83017' ;; 		x86) natsArch='386'; sha256='655f0f7cebf727317974006ad4a13ddacd3520f15266e854c2b01681e499bf80' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:43:21 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 03 Nov 2020 00:43:23 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:43:27 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea83a41655c390ae2bea2fd6f2a83188ecb9c82e60ebde8040109e79a2eba5`  
		Last Modified: Tue, 03 Nov 2020 00:44:06 GMT  
		Size: 6.3 MB (6262183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eca3d16e3b7142a6392c550b0efad91076053f222028892a3ae01e63f58dec`  
		Last Modified: Tue, 03 Nov 2020 00:44:05 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:a533473ab8df95ad3a2317a3d3f177186b76014e8b7b2dd1a8d2fd9c968a01b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3cc0e52c1cb44fc5a90b9700182bfa9c89b1ac66467df20bdcab1ab04d6e0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:f2a55f70ee492ea8558418b26a10b4bab14502b221829bba37fc14f1ad1a52f6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107723872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaffa70349c9b3d0962938d3d354b287074d9f2a3ca53f3f880b0f2c4348372`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 16:26:27 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:17 GMT
RUN cmd /S /C #(nop) COPY file:cc6bae0f50b6e35b12e8233f240d95e093f7e44257bc87e06aed691866ec1477 in C:\nats-streaming-server.exe 
# Tue, 03 Nov 2020 00:28:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:28:20 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:93b9a3c3e46fc1677426e3be7ce449b91d540c5ae2147380034cc4e1dc7445c3`  
		Last Modified: Wed, 14 Oct 2020 16:31:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80c5ff22001aef46c227bbdf3bb49e81d719eaabb98e05f489316336046c353`  
		Last Modified: Tue, 03 Nov 2020 00:32:50 GMT  
		Size: 6.5 MB (6515148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bab211499304d94ab254d507f765f27913f9f1d2c2a7f144c8fb339b90255f`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b35db78e25d5e897749f516159111a429e7ff0a22bcdc8f2090bce6aa5d6c`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ffc7f1df369d7406946da80c5cea7b9338075a8e9975e92297d67b9d581f13`  
		Last Modified: Tue, 03 Nov 2020 00:32:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:8001e4db36785bd692d9ae1c9ed3857d972692b385e36c08994794a5254bb78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:053a4ca3955b9c5036e48bafb96c83003fe86c34c6928934e3fd1db0529a889c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6487259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a204b53252cabfc16952c1d2dc014dc6518d1a08d00bda1bc5008a139e37a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:33:13 GMT
COPY file:3ed83d1497b0535960e452435cb8b27e347f48da12693aa27ebaf9bff94d82de in /nats-streaming-server 
# Tue, 03 Nov 2020 00:33:13 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:33:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:33:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:57ac21f890a508f609eabea265197b18ce9dfe3e694034c7a06d37b536a707b2`  
		Last Modified: Tue, 03 Nov 2020 00:33:37 GMT  
		Size: 6.5 MB (6487259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:f334d10ef2a4663d8d7d920d96321cd97f050b82a5d55d588192f074f60dd814
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eecfd5ab4178a65e952a7cf1d248a556a6ae2c328ac8b68923146d64734db03`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Nov 2020 23:56:28 GMT
COPY file:d6896b1c93dcd497494c972f9274fcc634a4f4a8d63a0191bdb87f6336aec0d7 in /nats-streaming-server 
# Mon, 02 Nov 2020 23:56:28 GMT
EXPOSE 4222 8222
# Mon, 02 Nov 2020 23:56:29 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 02 Nov 2020 23:56:29 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7f165fb71ab77e8081dbfa13656cdf9e5e005002d6c3afa0aac40667a0f97af8`  
		Last Modified: Mon, 02 Nov 2020 23:57:04 GMT  
		Size: 6.0 MB (6049845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:5fd0943909d8aedafb888e099c9f64d234023ad780805ed7c939692ebfd8304d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37071e856ae40dc3c8c5e10b359d1640fd67a6110741c0957af2031032ed6ce`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:05:23 GMT
COPY file:d232132ddff1d85d3a2f5c80a91c80023cbc103d816387e06d604cf97238e52c in /nats-streaming-server 
# Tue, 03 Nov 2020 00:05:24 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:05:24 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:05:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:9c7227cc1040d04ca7763cfb53ab58bc32ae54921990516adf8e13374ac9ef29`  
		Last Modified: Tue, 03 Nov 2020 00:05:57 GMT  
		Size: 6.0 MB (6043163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:c058fd3e9a8ac44263bf53fa2f6f1e8e8cb3e95cd223f8353fdafc50fe57e417
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c915a80bd440362bd4a6743fee8134a3caf6271e3258e449fb106b19c050a3b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 03 Nov 2020 00:43:38 GMT
COPY file:55e70ee826cd5a662497337a2488e22833672bd031d85b4ee39556ab1e80df08 in /nats-streaming-server 
# Tue, 03 Nov 2020 00:43:40 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:43:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 03 Nov 2020 00:43:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3dc58a59de8a6ed19e9144b0189eb3b637a9e7fcd76ec6c6dc47561b2740a3a2`  
		Last Modified: Tue, 03 Nov 2020 00:44:19 GMT  
		Size: 6.0 MB (5978846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:0ae3287ed23dc6163b1eae4339e2a00b685c19eeb1cfba03c672214ee3201fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:9e2d55072dc77e8efb56cc87523742790e4ad3f409e8038434365ecaf37411f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull nats-streaming@sha256:2e9e0b6ef8ba0ff27016cb985da788724f7e08e55ae4f6104ac936b6cffc0385
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394654641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cb47e91084bb5e7e54d9d1785687e894a1d1eafda1b1213a37be4fa70f8a56`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:24:30 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:26:04 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:26:05 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:26:05 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:26:35 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:27:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:27:56 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:27:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:27:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad001e4fbf5cfc7ed201221adacaa53c349e1df3803ec7e47dadb618535d55ab`  
		Last Modified: Wed, 14 Oct 2020 16:30:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b48f3c9ac6d0046ff4274ab0943fca1ad28654b724bfc0cd25aeb43a89095`  
		Last Modified: Tue, 03 Nov 2020 00:32:13 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7268c90cbc525d65a379e893c16bcd12ac3ea7d673bf459ae490c39d64f75d99`  
		Last Modified: Tue, 03 Nov 2020 00:32:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71108b2c4a8822c3584510cdadc1b997218ab88ba4547f440a1d9b5b25163841`  
		Last Modified: Tue, 03 Nov 2020 00:32:12 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded576dc7d4e34fa8153f6be8ae076bf9981541b675155e88938f31a80a81f9b`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 4.8 MB (4842032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d69c4ef299a97dd1bde85dd99a73b1f69920f8d077b01c9087b678685d3e2b`  
		Last Modified: Tue, 03 Nov 2020 00:32:28 GMT  
		Size: 15.7 MB (15713408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0062707d7ddbda4409f2d0f426f27589f04a444bab1b3cdf8bdeb8810e457ac7`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8954f030c851b5b95251cdc60434c2ab35f38df5d1507834fb0385c2db606171`  
		Last Modified: Tue, 03 Nov 2020 00:32:10 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa475b9fe000d6c0e1b84fffec1f8414d7b447639559d25bdeb6f9962093586`  
		Last Modified: Tue, 03 Nov 2020 00:32:09 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:39c649ab47271e07c6ecf9cedfdc010d6bffba506c04f9a011d24c7cb704f797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull nats-streaming@sha256:35e5bb02ff024920be057ba4b7a73c745a8fd0cf0fa091cc22790f37a8e66ffa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5763185966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f223fc24f59ee866629216ffdb4bd80eaf3c69b92549029a313c03139261e9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 16:26:37 GMT
ENV NATS_DOCKERIZED=1
# Tue, 03 Nov 2020 00:28:26 GMT
ENV NATS_STREAMING_SERVER=0.19.0
# Tue, 03 Nov 2020 00:28:27 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.19.0/nats-streaming-server-v0.19.0-windows-amd64.zip
# Tue, 03 Nov 2020 00:28:27 GMT
ENV GIT_DOWNLOAD_SHA256=edafd6482bd71f3d6035d7f6871df1fd4c53acf0ac19e88b85e08a2c7ab1cec5
# Tue, 03 Nov 2020 00:29:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 03 Nov 2020 00:31:33 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 03 Nov 2020 00:31:35 GMT
EXPOSE 4222 8222
# Tue, 03 Nov 2020 00:31:36 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 03 Nov 2020 00:31:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8ce1a1e304feeddabd9e49e2e5fad5622924c75d97368a7fda9a6eacf3eb`  
		Last Modified: Wed, 14 Oct 2020 16:31:41 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fbe0a0fcd436f331cfee3f87631fae3164bf6dc3aa2dd45a85f147868b66c7`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0526b3e99f270f31feac4b3c5f94a05a95d91096d740fda29dc5a4ea0d99880`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcd7ab5cc73782b8c2e01a80df21dc947f80b65915387902d8c61613a461ed0`  
		Last Modified: Tue, 03 Nov 2020 00:33:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305ffa646d8595937e31823bb1ced30ef1e6906d9cca8c1d0a598a9eb675e4ab`  
		Last Modified: Tue, 03 Nov 2020 00:33:05 GMT  
		Size: 5.4 MB (5424929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ead19df7bb907bfbc9847a0f5d782f0b10e1474e1b935d9166417cdff850b8d`  
		Last Modified: Tue, 03 Nov 2020 00:33:23 GMT  
		Size: 16.4 MB (16400260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b8e54deb33e15e0558eef7a1093a58e542f498108112fb2f49a8b2d7e751c`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33627498853e7df374769b1ce8e933295e0414404d9dcb46f3de306c421a34d0`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172fe5886078c2ba7d56e5097b6719bc725804bc214011cc6dd0c3cea927995`  
		Last Modified: Tue, 03 Nov 2020 00:33:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
