<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.18`](#nats-streaming018)
-	[`nats-streaming:0.18.0`](#nats-streaming0180)
-	[`nats-streaming:0.18.0-alpine`](#nats-streaming0180-alpine)
-	[`nats-streaming:0.18.0-alpine3.12`](#nats-streaming0180-alpine312)
-	[`nats-streaming:0.18.0-linux`](#nats-streaming0180-linux)
-	[`nats-streaming:0.18.0-nanoserver`](#nats-streaming0180-nanoserver)
-	[`nats-streaming:0.18.0-nanoserver-1809`](#nats-streaming0180-nanoserver-1809)
-	[`nats-streaming:0.18.0-scratch`](#nats-streaming0180-scratch)
-	[`nats-streaming:0.18.0-windowsservercore`](#nats-streaming0180-windowsservercore)
-	[`nats-streaming:0.18.0-windowsservercore-1809`](#nats-streaming0180-windowsservercore-1809)
-	[`nats-streaming:0.18.0-windowsservercore-ltsc2016`](#nats-streaming0180-windowsservercore-ltsc2016)
-	[`nats-streaming:0.18-alpine`](#nats-streaming018-alpine)
-	[`nats-streaming:0.18-alpine3.12`](#nats-streaming018-alpine312)
-	[`nats-streaming:0.18-linux`](#nats-streaming018-linux)
-	[`nats-streaming:0.18-nanoserver`](#nats-streaming018-nanoserver)
-	[`nats-streaming:0.18-nanoserver-1809`](#nats-streaming018-nanoserver-1809)
-	[`nats-streaming:0.18-scratch`](#nats-streaming018-scratch)
-	[`nats-streaming:0.18-windowsservercore`](#nats-streaming018-windowsservercore)
-	[`nats-streaming:0.18-windowsservercore-1809`](#nats-streaming018-windowsservercore-1809)
-	[`nats-streaming:0.18-windowsservercore-ltsc2016`](#nats-streaming018-windowsservercore-ltsc2016)
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

## `nats-streaming:0.18`

```console
$ docker pull nats-streaming@sha256:c53f528bf5d0cd4fd09874ad252cc1d5665c778ef6a0dbd10b3d393199e7ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0`

```console
$ docker pull nats-streaming@sha256:c53f528bf5d0cd4fd09874ad252cc1d5665c778ef6a0dbd10b3d393199e7ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18.0` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-alpine`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18.0-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-alpine3.12`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18.0-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-linux`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18.0-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-nanoserver`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18.0-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18.0-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-scratch`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18.0-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-windowsservercore`

```console
$ docker pull nats-streaming@sha256:47d55a5f852dacdef61afff77d97ddb939155e7c38be73278f44a1b1e3eef24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:0.18.0-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18.0-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:682087027e66bb745b188d0b1ca9a3cf0f0b0a2e6ae04d338d3ee24aba728347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18.0-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18.0-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:42262ddae4ea4f271a30da262eca5022b7cba71e8302c75a7a8f4ff3df6b4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:0.18.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-alpine`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-alpine3.12`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18-alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-linux`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-nanoserver`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-scratch`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.18-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-windowsservercore`

```console
$ docker pull nats-streaming@sha256:47d55a5f852dacdef61afff77d97ddb939155e7c38be73278f44a1b1e3eef24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:0.18-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.18-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:682087027e66bb745b188d0b1ca9a3cf0f0b0a2e6ae04d338d3ee24aba728347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:0.18-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.18-windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:42262ddae4ea4f271a30da262eca5022b7cba71e8302c75a7a8f4ff3df6b4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:0.18-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.12`

```console
$ docker pull nats-streaming@sha256:ef19a7373b6ab0b6b4a207cb550e85a7898d683aaae3d9e1361ba69d7d987541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.12` - linux; amd64

```console
$ docker pull nats-streaming@sha256:f773acd3701babcf267f460eace482aaa2847fdb79d08850fca955fe69c12e8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9015139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6db6849462b8b7abf8b8226c566f28b86a57b5b89b7771e1987f837252cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:25:24 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:26:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:26:37 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:26:37 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:26:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd351f099985ea9a52973cdd0eaeff72c72744a8c9f82a1cbc8664bffc094fdb`  
		Last Modified: Wed, 29 Jul 2020 23:26:57 GMT  
		Size: 6.2 MB (6217176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd65001efde87dd38a54a1b153608623d270593a572dda8cfa5b0a144138251e`  
		Last Modified: Wed, 29 Jul 2020 23:26:55 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:e66e8c57c226879ac8535b680ee1391ef87ae2bcc5690ec7ecbf93a4066c82a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857496a37e19bdea5173718e9e76bb7a4a0d3c535b434feabab434f0ba9e90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 19:50:21 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:01:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:01:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:01:33 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:01:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:01:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c29efa0cf9678b606f95b786cc832aa806186815fb1ca94233b6704050bbc`  
		Last Modified: Wed, 29 Jul 2020 23:02:00 GMT  
		Size: 5.8 MB (5810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09492963cd9edfd3f0ced5fb4042e7d537ee7fde04c3880c4a91bc84f9b46a6f`  
		Last Modified: Wed, 29 Jul 2020 23:01:59 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:a20ba55bef224ae45cc82582ac9191883a54e523a0ccbbe04365a9d5f373e561
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed41b19417bfe6bc079828554b1e892e5b04728503f6b6742aaabf260080863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 25 Jun 2020 18:58:53 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 23:16:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:16:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 23:16:35 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:16:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a1e6d591214ac54fc11baa4e27cf3cc7d9f0b6a65f186a67a96ced744cc569`  
		Last Modified: Wed, 29 Jul 2020 23:17:02 GMT  
		Size: 5.8 MB (5806663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94627b007b78566192f9591c03d4e2245b2f4943dd979b9d14d389edc2b60f96`  
		Last Modified: Wed, 29 Jul 2020 23:17:00 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:2efd83c7baf426a5da8223e4bd05f9278545d8fe81270934a16416e73c68e5b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8459346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671f8011bed05657f23e61f2c1011683c94045a8c893ed9aab290b88aa383e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:29:11 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 29 Jul 2020 22:39:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='ff2a51618b79685264f980fe868f1c7af583c419b6406cc63d4811f3c98ca8fe' ;; 		armhf) natsArch='arm6'; sha256='629e17255f12fd80e051772a6dd18a7f65e692b4abef0786b421eb8b6ab85db4' ;; 		armv7) natsArch='arm7'; sha256='94e499af6a6391519315e8bcd5127c43c1d1a442ef945956286e77b4366c92c9' ;; 		x86_64) natsArch='amd64'; sha256='6252e9262efc81a41ade3f43b68e014d1e635d3e3bf9cbcd2b09c3a030a0d5e6' ;; 		x86) natsArch='386'; sha256='886ebd2e5eb99e30ff9e9d8907d7bd49dafacffce1dc921427e5754a4ec26f55' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:39:59 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Jul 2020 22:39:59 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:40:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b7179a5be80ec5254ffae42b351490af025c30cac276c5f48df27ba082d2c3`  
		Last Modified: Wed, 29 Jul 2020 22:40:30 GMT  
		Size: 5.8 MB (5750960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945e4e25ec28f56f7dd8226e5e8ce479b9fb61cb6456eda8662d9d35acbd583`  
		Last Modified: Wed, 29 Jul 2020 22:40:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:c53f528bf5d0cd4fd09874ad252cc1d5665c778ef6a0dbd10b3d393199e7ef8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:cdff6d98c8dff65fd60aba352c99c6ee39e282566cdb91d514d1e7be9fb1e99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:f2d2d80b35d2ae0297912bf68614d16034a5f9c5c347731b836b746d2bf85693
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106932571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff700b71ef9199e56207927a28c60cf58e106df01a17df68fad9abec2d7a4b`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:22 GMT
RUN cmd /S /C #(nop) COPY file:4a858ac4da943f868519572e3fb6817fd379875f2bff0bcb5f03c5bdddc496a8 in C:\nats-streaming-server.exe 
# Wed, 12 Aug 2020 18:30:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:25 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31864c628f03c67f9c29c8aaf7f1042fbc35616631cbf172e420ff988160a3f`  
		Last Modified: Wed, 12 Aug 2020 18:34:28 GMT  
		Size: 5.9 MB (5944149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd32edc6585f0485869486b6abc72c49434fbc3a95d3a2445ebcaa72704cdf1`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b1e2cc45dd1856a7dcae4e384bae77c7fad5b2153c6b983d9acbcb73f8798`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83b953e5df0291bf0058b7fe2292076c702e865da4a34658a5957f63a56b3e`  
		Last Modified: Wed, 12 Aug 2020 18:34:27 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:6ab20bdd5317c0c00aa163f02cbf5d430e4381f6f1ae77fba2063c797b5acbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:eff8b99b0e3d89b6161ceb975a8c1ca063ac9a8e868eed448736a866551357ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d28dc2950a94ff3d73d86750b57ba3c6dae964c671dbac699c2f17eecd5880`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:25:44 GMT
COPY file:6241d3a0b9f20d843fc13c1bd49fd4376e4daae879837447249456f65dfe9ead in /nats-streaming-server 
# Thu, 25 Jun 2020 19:25:44 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:25:44 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:25:44 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:908e6af6575b3ee0ca4b089b18f72d87607c39809caeee4bb662b347aa23b895`  
		Last Modified: Thu, 25 Jun 2020 19:26:07 GMT  
		Size: 5.9 MB (5936411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:95ded92d384b4d9631841677a2d34b175cba6cbb4b4fa127b7a754b9f57c849e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24577fc60833cbc345883a4b8ee0eed5044ed08c199307ea0b9f951f7d5b6d3c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:50:40 GMT
COPY file:7145d006cd221687dcd9139e9e58f09c1f07ee9ce00f3485d297197fdd5ba444 in /nats-streaming-server 
# Thu, 25 Jun 2020 19:50:41 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:50:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:50:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ef961e603a1ec489ef1932fb068478ad9e98f8417ff4fefb8d4678e8653a5771`  
		Last Modified: Thu, 25 Jun 2020 19:51:16 GMT  
		Size: 5.5 MB (5530521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:60e9dc71017275b017a750e7be04e9c16abd50c6b6bc589ddf399588e44a509c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b24c4ac594ac46c22186488b6b2138f48703c79ebce756ae461ac777a7b486`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 25 Jun 2020 19:02:38 GMT
COPY file:2b6e0add99a6d3c42ba8b65af53581560646dbdaf347b23e6dde1f4267fa57bc in /nats-streaming-server 
# Thu, 25 Jun 2020 19:02:38 GMT
EXPOSE 4222 8222
# Thu, 25 Jun 2020 19:02:39 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 25 Jun 2020 19:02:40 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7af54707b9f6fd805487c0afe7fd52962e5abd3d1ab43335ccfc7224a2018844`  
		Last Modified: Thu, 25 Jun 2020 19:03:22 GMT  
		Size: 5.5 MB (5523586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ed524c7b14a4b6e91428f8c765455f742c4351657468296a8b63bdefecd5ceb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5469641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424d5ea5176bb2af173ccb2222a5d39ff53c785fdad2bfc1045d5c66aee5185`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Jul 2020 22:40:10 GMT
COPY file:f3f47d8e20155d8cbd02ab8a9f26c3be2763cf0430c38ab1071fb6949f9e466c in /nats-streaming-server 
# Wed, 29 Jul 2020 22:40:11 GMT
EXPOSE 4222 8222
# Wed, 29 Jul 2020 22:40:11 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Jul 2020 22:40:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:58414d7c10a2a92ebdcb56bcf4a04f62f2f370c1e415c008fda228ab012a1a45`  
		Last Modified: Wed, 29 Jul 2020 22:40:42 GMT  
		Size: 5.5 MB (5469641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:47d55a5f852dacdef61afff77d97ddb939155e7c38be73278f44a1b1e3eef24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:682087027e66bb745b188d0b1ca9a3cf0f0b0a2e6ae04d338d3ee24aba728347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-ltsc2016`

```console
$ docker pull nats-streaming@sha256:42262ddae4ea4f271a30da262eca5022b7cba71e8302c75a7a8f4ff3df6b4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats-streaming:windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats-streaming@sha256:89e03a9aa43c0bdb588f21434ef27b8a7fbb22078dd92fd2e4d8904092f477cd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5759345739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ddb01ea7294dc74ae6adc0db5bec4bf64cdeabe17c5c7a20451f4641634cb1`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:30:30 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:30:31 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:30:31 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:31:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:33:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:33:31 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:33:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:33:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc178724568b0a2420fb8850ed0546a60d333fa1f23c34e94c71ab06b647ec5`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536da8d0a8e905c039f2308f1e3bdb97838b9cf6bc5c37430e118fbcaa8e7d9`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cba38fec9b073ade1a0c6dda91e36104b894652a380b76bbec19cf24e6a2695`  
		Last Modified: Wed, 12 Aug 2020 18:34:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072dda1f9db7b0b0327db1abb0a4ab10dc5830995b40ee063911f55b9af7a16`  
		Last Modified: Wed, 12 Aug 2020 18:34:43 GMT  
		Size: 5.4 MB (5389867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a180d1a5f8d118ec75fe9836ee20b46ab6c2ba5ea3f535245c46adadb1bf79f`  
		Last Modified: Wed, 12 Aug 2020 18:34:45 GMT  
		Size: 15.8 MB (15799524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923ee9d4a8b167e7d0240164f7cda58fdd12f6c179ef683ad4da6b9fea0dc99`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbacb00093bd8283cfce1fedfd5b7482263e99c0781041861bbe8ea1f3771a`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20adcf0b6de8eb3754b51205750c0c072878f2abcb5b39413238f4f026e8ca`  
		Last Modified: Wed, 12 Aug 2020 18:34:41 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
