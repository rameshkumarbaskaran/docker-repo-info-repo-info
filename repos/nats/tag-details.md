<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.9`](#nats219)
-	[`nats:2.1.9-alpine`](#nats219-alpine)
-	[`nats:2.1.9-alpine3.12`](#nats219-alpine312)
-	[`nats:2.1.9-linux`](#nats219-linux)
-	[`nats:2.1.9-nanoserver`](#nats219-nanoserver)
-	[`nats:2.1.9-nanoserver-1809`](#nats219-nanoserver-1809)
-	[`nats:2.1.9-scratch`](#nats219-scratch)
-	[`nats:2.1.9-windowsservercore`](#nats219-windowsservercore)
-	[`nats:2.1.9-windowsservercore-1809`](#nats219-windowsservercore-1809)
-	[`nats:2.1.9-windowsservercore-ltsc2016`](#nats219-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.12`](#nats21-alpine312)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.12`](#nats2-alpine312)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.12`](#natsalpine312)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:53ae1d95ea740054da65664fd73ed9d8ab4e2bbe087cc70b84d0c6396baa26e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:53ae1d95ea740054da65664fd73ed9d8ab4e2bbe087cc70b84d0c6396baa26e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9`

```console
$ docker pull nats@sha256:53ae1d95ea740054da65664fd73ed9d8ab4e2bbe087cc70b84d0c6396baa26e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1.9` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-alpine`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-alpine3.12`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-nanoserver`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1.9-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-nanoserver-1809`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1.9-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore`

```console
$ docker pull nats@sha256:7147a7db5b990f60d71d46f1acffdedb3743fdcdcac43f33a0c03ca1bc1e148a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats:2.1.9-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:651bab66a30a39cd2d8f448d5f7f0f3f36fd37e4930143bdc8ef9c4a73b1db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1.9-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:facdd3c6075ebb638a42ebcd90b030274bebf6b423fc7c4bea7ef95fc9f9f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats:2.1.9-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.12`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:7147a7db5b990f60d71d46f1acffdedb3743fdcdcac43f33a0c03ca1bc1e148a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:651bab66a30a39cd2d8f448d5f7f0f3f36fd37e4930143bdc8ef9c4a73b1db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:facdd3c6075ebb638a42ebcd90b030274bebf6b423fc7c4bea7ef95fc9f9f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.12`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:7147a7db5b990f60d71d46f1acffdedb3743fdcdcac43f33a0c03ca1bc1e148a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:651bab66a30a39cd2d8f448d5f7f0f3f36fd37e4930143bdc8ef9c4a73b1db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:facdd3c6075ebb638a42ebcd90b030274bebf6b423fc7c4bea7ef95fc9f9f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.12`

```console
$ docker pull nats@sha256:1a31d19bc5fb81288c2dc5bcdef6c1bfe89692ebacb19e54e9131d63407c7a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:9e48df44aebb727f47d0dcba60b78c28a0ef104e36ff33080ecc8aace4f7b268
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19529e739baf0662c8730673c66c4b5fd30e95cf209a9aa4c92aeee96f944d22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Mon, 02 Nov 2020 23:53:12 GMT
ENV NATS_SERVER=2.1.9
# Mon, 02 Nov 2020 23:53:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Mon, 02 Nov 2020 23:53:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Mon, 02 Nov 2020 23:53:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 02 Nov 2020 23:53:17 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Nov 2020 23:53:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3160b7583dbd74fb51d0252fa0081efe742be228ffce0f8a8376b5fd40406c0d`  
		Last Modified: Mon, 02 Nov 2020 23:53:59 GMT  
		Size: 4.1 MB (4099220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaddabf5d9ffe7bfcbfdf91dcc457fa4df2b23ac4092c8fdaaafcaac17c1cf7`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0f36eeef476b5d018b5a4d45c3faa40dfd23693bdbd60011f9c55f808d9c70`  
		Last Modified: Mon, 02 Nov 2020 23:53:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:57a1feff0b8a1d875b723f8610882b4a440c5743b412ec85ef067d1ccba969c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d468e0ee5d5f12746ec4d791b447385a9ba784869e5d72cd799b98569b839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:03:16 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:03:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:03:20 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:03:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:03:21 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:03:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfce6983e3f7c06d074642c9b764d3233981dca2919b8d28e1239ffdde794d9`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 4.1 MB (4094632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7049631684363461d086d36dd5cab857aa52e898ffcddb6da26ccd8eaf27b4`  
		Last Modified: Tue, 03 Nov 2020 00:04:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfa4e9bce9726a8a6a7e2a357bc9012a2c3f6078047c5e30d7ff9f2d56358e4`  
		Last Modified: Tue, 03 Nov 2020 00:04:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a8c72687d1f87ca5cb5029208d51b114351c7f455e57c7f22ee4a8116f6a145e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff83f910483bc8d7394412b3e53cc592fd3eb49a5bb5ae022735dd4428d57e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:21:20 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:21:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:21:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:21:26 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:21:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ff07faf3e4cbb5e1bec5aecbccbe35999dd3d1eb388be39bc1472e5308951`  
		Last Modified: Tue, 03 Nov 2020 00:21:58 GMT  
		Size: 4.1 MB (4078804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80725eeaee5b58ba0c9acc97579d2e1bf9418cd21ce711b6e150c5dd6f97207`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99207a0471cdb39e044e8cb88c8e9cddfe20227a677d0c962ef4c1455c1daca2`  
		Last Modified: Tue, 03 Nov 2020 00:21:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:53ae1d95ea740054da65664fd73ed9d8ab4e2bbe087cc70b84d0c6396baa26e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:nanoserver` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:0a39aeaadbb842c439549bffa0f940293adb91a235958507450a06d693fe0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:f089f6b6168e445f291093a759c80876fd953745c5a4efbb0bbbe27232280d5c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105312508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1964d13564fc70a1239f4fcd93e8717355a577b7760832a75bc9f58f29a615`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 17:38:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 09 Dec 2020 17:38:03 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:38:04 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:38:05 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8a3891744a5ba41f01e625a0a70d755ffe93de4d4f124ad6d069420d5c7956d4`  
		Last Modified: Wed, 09 Dec 2020 17:42:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd77e3347ee1efde74138c42f5ed07c716af3d52bb7499dfb003d25c6d5b5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 4.0 MB (4042685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b77e5cb9bc99aa916c2db3ebad1347563d720ebc123aa4796db91c2ac9d6e`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 1.5 KB (1491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea2999feb8b98ef7e21f68ce28de1133bf96ef5369627ac7bb147f10f56e2f`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c602d1c53857aa5840085986f47df6377ec7c41a235c7491f0b5758880365c3b`  
		Last Modified: Wed, 09 Dec 2020 17:42:30 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2f9dd7a5851e5cda4e832d7eb4789774018521831f4d699736f495a205ce5`  
		Last Modified: Wed, 09 Dec 2020 17:42:29 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:7147a7db5b990f60d71d46f1acffdedb3743fdcdcac43f33a0c03ca1bc1e148a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:651bab66a30a39cd2d8f448d5f7f0f3f36fd37e4930143bdc8ef9c4a73b1db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull nats@sha256:45be90b14254e72787810aad606ccd4d37b296d1969e815017fa1cf7540cb26a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408976712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e98282f2d93288883d04152d4182e9faf78d3d41b1cef34f258f27aa602d513`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:36:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:36:05 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:36:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:36:36 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:37:50 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:37:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:37:52 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:37:53 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:37:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9257be76bd37cad15d45905ec5910266409794a9dbd8a0428174f8b2f352a`  
		Last Modified: Wed, 09 Dec 2020 17:42:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce12d099c4f8deaeb8b91eecc396f9b0db017e29087d9b101a7b24c8e53f2db`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbf54e6b3a7d9cf4345b6cbbf9bb383129ce792795dccf79a53db79869fc968`  
		Last Modified: Wed, 09 Dec 2020 17:41:58 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278cf3ca07ba69ac82df664d7396cd49a61c1cc509f82f5f2a991ad12e660a9b`  
		Last Modified: Wed, 09 Dec 2020 17:41:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11b4ea4e91b3c9ad1f6ad9bd4c51a0961e8a10eafe40691439fff4e66616e6`  
		Last Modified: Wed, 09 Dec 2020 17:42:02 GMT  
		Size: 4.8 MB (4843263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2755f47bf0200184985eec72df9064186ed7a6ea2bfa1da09e3e7187dbdb5b`  
		Last Modified: Wed, 09 Dec 2020 17:42:08 GMT  
		Size: 13.2 MB (13248209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aec46694c6b5483c50d068186be07a5e00247bfe4678d9804a2386f9608386`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21af927ab73dbbc8dbf9a9d9c46cf1cd1b8f67af5de09608cf59941ac8a65bed`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48e8a4bdf82163a3715d172cad9fab44e5416d28730c3e48a9164e1d5352f6`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24890fc54bc0b6cd916c3d35fb39241cec6ee1bb968a47bd96b0869dece707dc`  
		Last Modified: Wed, 09 Dec 2020 17:41:54 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:facdd3c6075ebb638a42ebcd90b030274bebf6b423fc7c4bea7ef95fc9f9f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull nats@sha256:ba8cbaf5e36dfdcd37b9e918fd2cc886c8cc3fafc8808dae497bacc183d745e3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5788476333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e172644f80835a4f78fc0018bf8f88b6142d081b2d166e940a7dddcc97cfb2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Dec 2020 17:38:10 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Dec 2020 17:38:11 GMT
ENV NATS_SERVER=2.1.9
# Wed, 09 Dec 2020 17:38:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 09 Dec 2020 17:38:12 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 09 Dec 2020 17:39:27 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Dec 2020 17:41:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Dec 2020 17:41:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 09 Dec 2020 17:41:09 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Dec 2020 17:41:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Dec 2020 17:41:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d972336c8bcee0026c76e8f199cef405112a70aeef9917f07d2859f15162c1`  
		Last Modified: Wed, 09 Dec 2020 17:42:56 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ee25b9ee0dbb74c7344f2268eca0fe12cbab50686e5599161f0a1ac9551b9`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52522e634e61b08c619c31493c71f64b012d88c2c0f9d62de9ef030d900c8509`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3993f45e3a5a5bde078cab89bde915db85dd81728f5a352bcf5e5b55dfb108`  
		Last Modified: Wed, 09 Dec 2020 17:42:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472002c8f80706a70d4b77715607371840371b671fd2613d37d0b1e2451f940e`  
		Last Modified: Wed, 09 Dec 2020 17:42:55 GMT  
		Size: 5.5 MB (5527273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a1d06af3304903d1a68825b06f391bc852c9192e2c7a6d3b1220494345b65`  
		Last Modified: Wed, 09 Dec 2020 17:42:54 GMT  
		Size: 14.1 MB (14094240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac20c369ae9c45216a01a294ec2fc2380695619a3c260fdb32b5507279e3c5`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cef71a2e187c833a30a7835117238614fea4ba6c8075231c20583411961f9`  
		Last Modified: Wed, 09 Dec 2020 17:42:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86998d0fd113ce31ff0af7d95b6a7bb90462095535903edea2ed8e58120d4ef6`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ea1f19a2b6b2f5920dff6a1c5da61c674ec5decab9570c67e5f0cd0fa76f5`  
		Last Modified: Wed, 09 Dec 2020 17:42:51 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
