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
$ docker pull nats@sha256:b039d2dfb3031fa6261a1b2596a3d52f0cb79f2f0eed5227b907f8442409eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

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

### `nats:2` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:b039d2dfb3031fa6261a1b2596a3d52f0cb79f2f0eed5227b907f8442409eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

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

### `nats:2.1` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9`

```console
$ docker pull nats@sha256:b039d2dfb3031fa6261a1b2596a3d52f0cb79f2f0eed5227b907f8442409eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

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

### `nats:2.1.9` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1.9-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-nanoserver-1809`

```console
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1.9-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:40dd502b9f02f4db012eaae1f62d31fd65250ae0f124f75b98ed2a0ff015e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats:2.1.9-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:b6b8fea1692f62d7fa95cbc1c26c327ebfb7fb462bcf244529c6673c4c2b9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1.9-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:1d71ba11a1ee5b14ee3fad76c51fd853c2e2045d8d0536c8cb6ce7f1b1e573ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats:2.1.9-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
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
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:40dd502b9f02f4db012eaae1f62d31fd65250ae0f124f75b98ed2a0ff015e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:b6b8fea1692f62d7fa95cbc1c26c327ebfb7fb462bcf244529c6673c4c2b9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:1d71ba11a1ee5b14ee3fad76c51fd853c2e2045d8d0536c8cb6ce7f1b1e573ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
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
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:40dd502b9f02f4db012eaae1f62d31fd65250ae0f124f75b98ed2a0ff015e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:b6b8fea1692f62d7fa95cbc1c26c327ebfb7fb462bcf244529c6673c4c2b9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:1d71ba11a1ee5b14ee3fad76c51fd853c2e2045d8d0536c8cb6ce7f1b1e573ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
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
$ docker pull nats@sha256:b039d2dfb3031fa6261a1b2596a3d52f0cb79f2f0eed5227b907f8442409eb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64

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

### `nats:latest` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:cb7929b7256bf8401f7fa667dbdb1af833f0422d90606ca4bf55b7bedfef67b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:3a1f2f32af49a82f0d43249dbbad7ed121fc6f626c8410537b6af6459800671b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a46c5c315ca02858761e34ef5a2cd1f0e42ab59c68b4cea38e1790a32fddd5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:03:29 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:30 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 11 Nov 2020 17:03:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fac4fef0003186669efa1b895f6bdd99aacb845c8fb8f9061c1a08c625ce8f4d`  
		Last Modified: Wed, 11 Nov 2020 17:08:04 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3447d6e84a963caa8a6e49ec0ec1a8b5371449d5f0826af40e34f445c21f39f2`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 4.0 MB (4042696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af953bd248b3dc06ff7ec9d2c52f3e0c48f584f49085fd21789ca9a8096843e`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5c9bba396ace7d1348a54ab9dd84abbb0a4ae07536d326a3798529a63013`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3310077998c938d435efdea215fcb075e376e93b58679e4d9f7d49005ed781b`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411fe1e8113d52497e7ffd78a00ef4e7e4c72d6de46713b1923f0dd5963d0c5`  
		Last Modified: Wed, 11 Nov 2020 17:08:01 GMT  
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
$ docker pull nats@sha256:40dd502b9f02f4db012eaae1f62d31fd65250ae0f124f75b98ed2a0ff015e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b6b8fea1692f62d7fa95cbc1c26c327ebfb7fb462bcf244529c6673c4c2b9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:1d71ba11a1ee5b14ee3fad76c51fd853c2e2045d8d0536c8cb6ce7f1b1e573ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull nats@sha256:f03afd1dcc484f1c80c557afc8d9ad63bf6d088a3c9f8ab02024589c5660d994
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5794741070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae8f96a11cd77a19f48b85cf82cb7bb20c6814f73902512321ec0c0e8c386ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 14:26:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:03:39 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:03:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:03:41 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:04:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:06:44 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:06:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:06:46 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:06:47 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:06:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9affba5fa493b09d48e6bd56c0d7b0eb03d1dbaa80493dd08cb18a3c9ddfbb67`  
		Last Modified: Wed, 11 Nov 2020 16:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d795e5fc593aa74d082785c3c5a0c7852d30cfdd8a38a78310041e80dbb85b`  
		Last Modified: Wed, 11 Nov 2020 17:08:28 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad5e8c441d5324871366395ae858a6b84c9bc78cdbbfb207a1bbf98b0ff897`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e61f3ceb9a75f95cfc182e19c400bd9fffc6fac72ed411c2da6d98c0358906`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279e124f0482ba70ab7ec374b3617678026809d8d926eebff3759122d1c64ea1`  
		Last Modified: Wed, 11 Nov 2020 17:08:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6131208320b311e8adc0c95654658d66b7b3bd41e733d25b1ee1f68e8000f`  
		Last Modified: Wed, 11 Nov 2020 17:08:27 GMT  
		Size: 10.1 MB (10064354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fdd9a12232d68b4e5d2e568f898cc07e274fa3acf8ec2a2e8447b6e989148`  
		Last Modified: Wed, 11 Nov 2020 17:08:25 GMT  
		Size: 14.1 MB (14107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7316cf30cb3d4df25cc1888d66e5944201951ba2e712a5270e7d328eb8ace9d`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91570b37edb29efdb09ea7065d3ffd9652dd628475bd4a9380c2130dfefb6f77`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92900d75de44922c22b67158d1e55940fe3d4d1ca816e66afbcbdaa9c26575e3`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8192741c290c24bdf6ded2d652da6f8ac13cb06915cece9fb99b67b3d44431b`  
		Last Modified: Wed, 11 Nov 2020 17:08:21 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
