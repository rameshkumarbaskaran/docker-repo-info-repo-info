<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.18`](#nats2-alpine318)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.18`](#nats210-alpine318)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.1`](#nats2101)
-	[`nats:2.10.1-alpine`](#nats2101-alpine)
-	[`nats:2.10.1-alpine3.18`](#nats2101-alpine318)
-	[`nats:2.10.1-linux`](#nats2101-linux)
-	[`nats:2.10.1-nanoserver`](#nats2101-nanoserver)
-	[`nats:2.10.1-nanoserver-1809`](#nats2101-nanoserver-1809)
-	[`nats:2.10.1-scratch`](#nats2101-scratch)
-	[`nats:2.10.1-windowsservercore`](#nats2101-windowsservercore)
-	[`nats:2.10.1-windowsservercore-1809`](#nats2101-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.22`](#nats2922)
-	[`nats:2.9.22-alpine`](#nats2922-alpine)
-	[`nats:2.9.22-alpine3.18`](#nats2922-alpine318)
-	[`nats:2.9.22-linux`](#nats2922-linux)
-	[`nats:2.9.22-nanoserver`](#nats2922-nanoserver)
-	[`nats:2.9.22-nanoserver-1809`](#nats2922-nanoserver-1809)
-	[`nats:2.9.22-scratch`](#nats2922-scratch)
-	[`nats:2.9.22-windowsservercore`](#nats2922-windowsservercore)
-	[`nats:2.9.22-windowsservercore-1809`](#nats2922-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.18`](#natsalpine318)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:897f64e44537e6e8eab8457196c789ea2764c28ca7e5b2f585c4ce67b0c4f9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4851; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:7be373ffcc0f0eef311699f3ee04c73cee78bdf9414b7fec2e31c7c0e8d69ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.18`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1`

```console
$ docker pull nats@sha256:7be373ffcc0f0eef311699f3ee04c73cee78bdf9414b7fec2e31c7c0e8d69ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10.1` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-alpine`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-alpine3.18`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.1-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-linux`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-nanoserver`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10.1-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-nanoserver-1809`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10.1-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-scratch`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-windowsservercore`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10.1-windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.10.1-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:e56e30eb3763a62b66ae1970fb8e950879a347724f75e79fbc7d58f194dc8ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea7a019f8f71ab49206a746200be09e7fab2b2319e21bdad84494942eea5129b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444ddccb29b2fad602512a5c072a5b423f530cd9ca1b62dc2fd2fafb844628e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:56 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:03:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:59 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ddae942421f08eba2d35ca5fb15207c059b05611526f2634f4f783b313195`  
		Last Modified: Thu, 28 Sep 2023 23:04:59 GMT  
		Size: 5.9 MB (5867784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ca948a616cb91c19cc7459b10b01c913677097d2bdc189c43d67a1a467011`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d044774dd68c36cd852a3a4486eb7da37c248e4ba4100bfa20c5ecfab4cba`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b13e03d487b41ad6e6201b9203fea9e88fad106d46dfd8514914f98a6bb98fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8749587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c342f1da19613cc424e3d59b510a8036b9a5239296ae2b7340e284376a6be9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:22 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:25 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630c915de7bdf058602fd319c5ad749f49f9eb9bacd5dd06e9ca18175eb84cad`  
		Last Modified: Thu, 28 Sep 2023 22:12:18 GMT  
		Size: 5.6 MB (5603293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc58f097ef6a2be1e278bae3263fedc9e6f5bf946000f3d48d677a165f4f402`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5692ecd59317b7715ef39bf4c3e08335f62de978373f2e7b0f242b553b54f`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6da5cc898bfdc25941dd437e96b9a961843df4116dcb0f3ed31412d37a98493
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee203567cc45c4a8288b4650f2afc365f43eb01c42fac9f92c3063cacd70c332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:49 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:17:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:51 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e6799cc112563f5bd57ccf66b5ae4e1acb9b0f9380f8ea5ff99bcdf394d87a`  
		Last Modified: Thu, 28 Sep 2023 23:18:48 GMT  
		Size: 5.6 MB (5592383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c2d8b97f2ee1947b9f1567d20195023a527212ead9b2fd1fc84c2c10f31282`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b817a337dea1e3c1d94395fec370c3af29bd89dbb0149d57dd4b93c72cb9de`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:974daab09263e17e09f36c429cdfa842c86e7f2a7f727e73ffa8d72a0c758228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8735321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010bd6c9016879b86bd554939bd0f2be66a0aeb82d807fe7288519980f99879d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:37 GMT
ENV NATS_SERVER=2.9.22
# Fri, 29 Sep 2023 02:05:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:39 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd4ee8336fd067d1c11dd90428c4b26bc79b3521db6ba65309bfd68fcfe6b3`  
		Last Modified: Fri, 29 Sep 2023 02:06:41 GMT  
		Size: 5.4 MB (5402492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7966cb0b0f8d4873987436d855fcb89402026d7357cf9799ebd7636393c7e55e`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6944ab51200e30863838a2feffd3da50d117f096e4dec219cedaa5b62dff1249`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:e56e30eb3763a62b66ae1970fb8e950879a347724f75e79fbc7d58f194dc8ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:ea7a019f8f71ab49206a746200be09e7fab2b2319e21bdad84494942eea5129b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444ddccb29b2fad602512a5c072a5b423f530cd9ca1b62dc2fd2fafb844628e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:56 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:03:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:59 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ddae942421f08eba2d35ca5fb15207c059b05611526f2634f4f783b313195`  
		Last Modified: Thu, 28 Sep 2023 23:04:59 GMT  
		Size: 5.9 MB (5867784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ca948a616cb91c19cc7459b10b01c913677097d2bdc189c43d67a1a467011`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d044774dd68c36cd852a3a4486eb7da37c248e4ba4100bfa20c5ecfab4cba`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b13e03d487b41ad6e6201b9203fea9e88fad106d46dfd8514914f98a6bb98fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8749587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c342f1da19613cc424e3d59b510a8036b9a5239296ae2b7340e284376a6be9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:22 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:25 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630c915de7bdf058602fd319c5ad749f49f9eb9bacd5dd06e9ca18175eb84cad`  
		Last Modified: Thu, 28 Sep 2023 22:12:18 GMT  
		Size: 5.6 MB (5603293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc58f097ef6a2be1e278bae3263fedc9e6f5bf946000f3d48d677a165f4f402`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5692ecd59317b7715ef39bf4c3e08335f62de978373f2e7b0f242b553b54f`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6da5cc898bfdc25941dd437e96b9a961843df4116dcb0f3ed31412d37a98493
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee203567cc45c4a8288b4650f2afc365f43eb01c42fac9f92c3063cacd70c332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:49 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:17:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:51 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e6799cc112563f5bd57ccf66b5ae4e1acb9b0f9380f8ea5ff99bcdf394d87a`  
		Last Modified: Thu, 28 Sep 2023 23:18:48 GMT  
		Size: 5.6 MB (5592383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c2d8b97f2ee1947b9f1567d20195023a527212ead9b2fd1fc84c2c10f31282`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b817a337dea1e3c1d94395fec370c3af29bd89dbb0149d57dd4b93c72cb9de`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:974daab09263e17e09f36c429cdfa842c86e7f2a7f727e73ffa8d72a0c758228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8735321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010bd6c9016879b86bd554939bd0f2be66a0aeb82d807fe7288519980f99879d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:37 GMT
ENV NATS_SERVER=2.9.22
# Fri, 29 Sep 2023 02:05:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:39 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd4ee8336fd067d1c11dd90428c4b26bc79b3521db6ba65309bfd68fcfe6b3`  
		Last Modified: Fri, 29 Sep 2023 02:06:41 GMT  
		Size: 5.4 MB (5402492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7966cb0b0f8d4873987436d855fcb89402026d7357cf9799ebd7636393c7e55e`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6944ab51200e30863838a2feffd3da50d117f096e4dec219cedaa5b62dff1249`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:a040fc4874378f2c73b2d333916a89e39936f9fb0bef541e4bdf241c9eea6343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:ef369c5330e436aca92b7521434dcad6019b82114a6095132bc5e4e582a93861
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109819053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053513aeb5883341d4904ae9f696d46f6f79373919c304dc1199f0cde262ef4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:393d7e944d1b6697a14f19f6cb9673d95da4e1a0fc9508b238325e94beebc857 in C:\nats-server.exe 
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:08:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf628408f2a1164bcd400567aa3cd56db3926c391837397914b8cd6c337369f`  
		Last Modified: Wed, 13 Sep 2023 05:08:47 GMT  
		Size: 5.3 MB (5320086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e6195a95c838cacd22627e342b84f22112007d2f4e70079c6de80beb6e7c45`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c249fb3d5e5f1f8e0ef37e85a0cfaed40a4bb8df20e92e8937d686c2ec18fed`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01b907719f9c8b285c36f7971a978e09c143bfa695bfcc5f46a9d56fd55458d`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af083ba70a28322391995a59e841ea4478fe0d88eabbb83b4cfcbf20fab0cc4`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:a040fc4874378f2c73b2d333916a89e39936f9fb0bef541e4bdf241c9eea6343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:ef369c5330e436aca92b7521434dcad6019b82114a6095132bc5e4e582a93861
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109819053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053513aeb5883341d4904ae9f696d46f6f79373919c304dc1199f0cde262ef4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:393d7e944d1b6697a14f19f6cb9673d95da4e1a0fc9508b238325e94beebc857 in C:\nats-server.exe 
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:08:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf628408f2a1164bcd400567aa3cd56db3926c391837397914b8cd6c337369f`  
		Last Modified: Wed, 13 Sep 2023 05:08:47 GMT  
		Size: 5.3 MB (5320086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e6195a95c838cacd22627e342b84f22112007d2f4e70079c6de80beb6e7c45`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c249fb3d5e5f1f8e0ef37e85a0cfaed40a4bb8df20e92e8937d686c2ec18fed`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01b907719f9c8b285c36f7971a978e09c143bfa695bfcc5f46a9d56fd55458d`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af083ba70a28322391995a59e841ea4478fe0d88eabbb83b4cfcbf20fab0cc4`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:0d1237c42b0bf510367a68f73790bafd41d3e4dba95502ecf7d630eb6dcf0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4bc9d7dc99d75f7813148b82653c884ac51975085d49de22b68ac981bf1b3c40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022365856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7856c543b220cf294996bece7566b5515805212fc38127b1450f60b3e3ba5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_SERVER=2.9.22
# Wed, 13 Sep 2023 05:05:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.22/nats-server-v2.9.22-windows-amd64.zip
# Wed, 13 Sep 2023 05:05:38 GMT
ENV NATS_SERVER_SHASUM=e91db73b02bd4dca3eb7a4bf32e29763450b08d593f73e87d0a6b70102dea0d4
# Wed, 13 Sep 2023 05:06:28 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Sep 2023 05:07:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Sep 2023 05:07:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:07:53 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:07:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:07:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e138a75d8a68c57acda5ac3d2a5ea38cfcd91aeeac6e996187886cdc4fe512b`  
		Last Modified: Wed, 13 Sep 2023 05:08:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba6b3e055f188fc0c938c464d3df287b87b4ebd990c6d3023e4043e9475882b`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d1091bb5b201027155aa6154441b33e21f06c80c98e5502f0ea97d3e6ac36`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf75715be616bda4fd455e8842d5c47e6361520831c79994aac63897f074a6`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 242.8 KB (242766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3267078f67f5f3fb7955bda584f1a858622791ed81e9c2e45ac79383c6c3795`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 5.8 MB (5779913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81aab1223d4ac5fade6bcbff4e433f5a038988f73089bb43aff8b974c715a2`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a790db19f2a0d625636fa4d186b3b076500c592809d8b95c7a725e0c46a094`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4edbf9880281abc4bccc4d818ad299ce3cd5ad235e1cb033fbc49b3096f3a7`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05fad63f054ab864e4484c552a76f82c3bf9e322da181d03f63a597755912`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:0d1237c42b0bf510367a68f73790bafd41d3e4dba95502ecf7d630eb6dcf0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4bc9d7dc99d75f7813148b82653c884ac51975085d49de22b68ac981bf1b3c40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022365856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7856c543b220cf294996bece7566b5515805212fc38127b1450f60b3e3ba5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_SERVER=2.9.22
# Wed, 13 Sep 2023 05:05:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.22/nats-server-v2.9.22-windows-amd64.zip
# Wed, 13 Sep 2023 05:05:38 GMT
ENV NATS_SERVER_SHASUM=e91db73b02bd4dca3eb7a4bf32e29763450b08d593f73e87d0a6b70102dea0d4
# Wed, 13 Sep 2023 05:06:28 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Sep 2023 05:07:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Sep 2023 05:07:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:07:53 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:07:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:07:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e138a75d8a68c57acda5ac3d2a5ea38cfcd91aeeac6e996187886cdc4fe512b`  
		Last Modified: Wed, 13 Sep 2023 05:08:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba6b3e055f188fc0c938c464d3df287b87b4ebd990c6d3023e4043e9475882b`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d1091bb5b201027155aa6154441b33e21f06c80c98e5502f0ea97d3e6ac36`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf75715be616bda4fd455e8842d5c47e6361520831c79994aac63897f074a6`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 242.8 KB (242766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3267078f67f5f3fb7955bda584f1a858622791ed81e9c2e45ac79383c6c3795`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 5.8 MB (5779913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81aab1223d4ac5fade6bcbff4e433f5a038988f73089bb43aff8b974c715a2`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a790db19f2a0d625636fa4d186b3b076500c592809d8b95c7a725e0c46a094`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4edbf9880281abc4bccc4d818ad299ce3cd5ad235e1cb033fbc49b3096f3a7`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05fad63f054ab864e4484c552a76f82c3bf9e322da181d03f63a597755912`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.22` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-alpine`

```console
$ docker pull nats@sha256:e56e30eb3763a62b66ae1970fb8e950879a347724f75e79fbc7d58f194dc8ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.22-alpine` - linux; amd64

```console
$ docker pull nats@sha256:ea7a019f8f71ab49206a746200be09e7fab2b2319e21bdad84494942eea5129b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444ddccb29b2fad602512a5c072a5b423f530cd9ca1b62dc2fd2fafb844628e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:56 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:03:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:59 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ddae942421f08eba2d35ca5fb15207c059b05611526f2634f4f783b313195`  
		Last Modified: Thu, 28 Sep 2023 23:04:59 GMT  
		Size: 5.9 MB (5867784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ca948a616cb91c19cc7459b10b01c913677097d2bdc189c43d67a1a467011`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d044774dd68c36cd852a3a4486eb7da37c248e4ba4100bfa20c5ecfab4cba`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b13e03d487b41ad6e6201b9203fea9e88fad106d46dfd8514914f98a6bb98fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8749587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c342f1da19613cc424e3d59b510a8036b9a5239296ae2b7340e284376a6be9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:22 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:25 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630c915de7bdf058602fd319c5ad749f49f9eb9bacd5dd06e9ca18175eb84cad`  
		Last Modified: Thu, 28 Sep 2023 22:12:18 GMT  
		Size: 5.6 MB (5603293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc58f097ef6a2be1e278bae3263fedc9e6f5bf946000f3d48d677a165f4f402`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5692ecd59317b7715ef39bf4c3e08335f62de978373f2e7b0f242b553b54f`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6da5cc898bfdc25941dd437e96b9a961843df4116dcb0f3ed31412d37a98493
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee203567cc45c4a8288b4650f2afc365f43eb01c42fac9f92c3063cacd70c332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:49 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:17:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:51 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e6799cc112563f5bd57ccf66b5ae4e1acb9b0f9380f8ea5ff99bcdf394d87a`  
		Last Modified: Thu, 28 Sep 2023 23:18:48 GMT  
		Size: 5.6 MB (5592383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c2d8b97f2ee1947b9f1567d20195023a527212ead9b2fd1fc84c2c10f31282`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b817a337dea1e3c1d94395fec370c3af29bd89dbb0149d57dd4b93c72cb9de`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:974daab09263e17e09f36c429cdfa842c86e7f2a7f727e73ffa8d72a0c758228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8735321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010bd6c9016879b86bd554939bd0f2be66a0aeb82d807fe7288519980f99879d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:37 GMT
ENV NATS_SERVER=2.9.22
# Fri, 29 Sep 2023 02:05:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:39 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd4ee8336fd067d1c11dd90428c4b26bc79b3521db6ba65309bfd68fcfe6b3`  
		Last Modified: Fri, 29 Sep 2023 02:06:41 GMT  
		Size: 5.4 MB (5402492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7966cb0b0f8d4873987436d855fcb89402026d7357cf9799ebd7636393c7e55e`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6944ab51200e30863838a2feffd3da50d117f096e4dec219cedaa5b62dff1249`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-alpine3.18`

```console
$ docker pull nats@sha256:e56e30eb3763a62b66ae1970fb8e950879a347724f75e79fbc7d58f194dc8ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.22-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:ea7a019f8f71ab49206a746200be09e7fab2b2319e21bdad84494942eea5129b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444ddccb29b2fad602512a5c072a5b423f530cd9ca1b62dc2fd2fafb844628e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:56 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:03:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:58 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:59 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ddae942421f08eba2d35ca5fb15207c059b05611526f2634f4f783b313195`  
		Last Modified: Thu, 28 Sep 2023 23:04:59 GMT  
		Size: 5.9 MB (5867784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ca948a616cb91c19cc7459b10b01c913677097d2bdc189c43d67a1a467011`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d044774dd68c36cd852a3a4486eb7da37c248e4ba4100bfa20c5ecfab4cba`  
		Last Modified: Thu, 28 Sep 2023 23:04:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b13e03d487b41ad6e6201b9203fea9e88fad106d46dfd8514914f98a6bb98fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8749587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c342f1da19613cc424e3d59b510a8036b9a5239296ae2b7340e284376a6be9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:22 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:25 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630c915de7bdf058602fd319c5ad749f49f9eb9bacd5dd06e9ca18175eb84cad`  
		Last Modified: Thu, 28 Sep 2023 22:12:18 GMT  
		Size: 5.6 MB (5603293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc58f097ef6a2be1e278bae3263fedc9e6f5bf946000f3d48d677a165f4f402`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5692ecd59317b7715ef39bf4c3e08335f62de978373f2e7b0f242b553b54f`  
		Last Modified: Thu, 28 Sep 2023 22:12:17 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6da5cc898bfdc25941dd437e96b9a961843df4116dcb0f3ed31412d37a98493
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee203567cc45c4a8288b4650f2afc365f43eb01c42fac9f92c3063cacd70c332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:49 GMT
ENV NATS_SERVER=2.9.22
# Thu, 28 Sep 2023 23:17:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:51 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e6799cc112563f5bd57ccf66b5ae4e1acb9b0f9380f8ea5ff99bcdf394d87a`  
		Last Modified: Thu, 28 Sep 2023 23:18:48 GMT  
		Size: 5.6 MB (5592383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c2d8b97f2ee1947b9f1567d20195023a527212ead9b2fd1fc84c2c10f31282`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b817a337dea1e3c1d94395fec370c3af29bd89dbb0149d57dd4b93c72cb9de`  
		Last Modified: Thu, 28 Sep 2023 23:18:47 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:974daab09263e17e09f36c429cdfa842c86e7f2a7f727e73ffa8d72a0c758228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8735321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010bd6c9016879b86bd554939bd0f2be66a0aeb82d807fe7288519980f99879d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:37 GMT
ENV NATS_SERVER=2.9.22
# Fri, 29 Sep 2023 02:05:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:39 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dd4ee8336fd067d1c11dd90428c4b26bc79b3521db6ba65309bfd68fcfe6b3`  
		Last Modified: Fri, 29 Sep 2023 02:06:41 GMT  
		Size: 5.4 MB (5402492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7966cb0b0f8d4873987436d855fcb89402026d7357cf9799ebd7636393c7e55e`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6944ab51200e30863838a2feffd3da50d117f096e4dec219cedaa5b62dff1249`  
		Last Modified: Fri, 29 Sep 2023 02:06:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-linux`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.22-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-nanoserver`

```console
$ docker pull nats@sha256:a040fc4874378f2c73b2d333916a89e39936f9fb0bef541e4bdf241c9eea6343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9.22-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:ef369c5330e436aca92b7521434dcad6019b82114a6095132bc5e4e582a93861
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109819053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053513aeb5883341d4904ae9f696d46f6f79373919c304dc1199f0cde262ef4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:393d7e944d1b6697a14f19f6cb9673d95da4e1a0fc9508b238325e94beebc857 in C:\nats-server.exe 
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:08:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf628408f2a1164bcd400567aa3cd56db3926c391837397914b8cd6c337369f`  
		Last Modified: Wed, 13 Sep 2023 05:08:47 GMT  
		Size: 5.3 MB (5320086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e6195a95c838cacd22627e342b84f22112007d2f4e70079c6de80beb6e7c45`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c249fb3d5e5f1f8e0ef37e85a0cfaed40a4bb8df20e92e8937d686c2ec18fed`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01b907719f9c8b285c36f7971a978e09c143bfa695bfcc5f46a9d56fd55458d`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af083ba70a28322391995a59e841ea4478fe0d88eabbb83b4cfcbf20fab0cc4`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-nanoserver-1809`

```console
$ docker pull nats@sha256:a040fc4874378f2c73b2d333916a89e39936f9fb0bef541e4bdf241c9eea6343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9.22-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:ef369c5330e436aca92b7521434dcad6019b82114a6095132bc5e4e582a93861
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109819053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053513aeb5883341d4904ae9f696d46f6f79373919c304dc1199f0cde262ef4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:393d7e944d1b6697a14f19f6cb9673d95da4e1a0fc9508b238325e94beebc857 in C:\nats-server.exe 
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:08:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf628408f2a1164bcd400567aa3cd56db3926c391837397914b8cd6c337369f`  
		Last Modified: Wed, 13 Sep 2023 05:08:47 GMT  
		Size: 5.3 MB (5320086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e6195a95c838cacd22627e342b84f22112007d2f4e70079c6de80beb6e7c45`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c249fb3d5e5f1f8e0ef37e85a0cfaed40a4bb8df20e92e8937d686c2ec18fed`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01b907719f9c8b285c36f7971a978e09c143bfa695bfcc5f46a9d56fd55458d`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af083ba70a28322391995a59e841ea4478fe0d88eabbb83b4cfcbf20fab0cc4`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-scratch`

```console
$ docker pull nats@sha256:488386bec6ea7b0822f48795e51ed1dd0b367e6e2fffe466d4f304e2fa628918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.22-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.22-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-windowsservercore`

```console
$ docker pull nats@sha256:0d1237c42b0bf510367a68f73790bafd41d3e4dba95502ecf7d630eb6dcf0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9.22-windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4bc9d7dc99d75f7813148b82653c884ac51975085d49de22b68ac981bf1b3c40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022365856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7856c543b220cf294996bece7566b5515805212fc38127b1450f60b3e3ba5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_SERVER=2.9.22
# Wed, 13 Sep 2023 05:05:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.22/nats-server-v2.9.22-windows-amd64.zip
# Wed, 13 Sep 2023 05:05:38 GMT
ENV NATS_SERVER_SHASUM=e91db73b02bd4dca3eb7a4bf32e29763450b08d593f73e87d0a6b70102dea0d4
# Wed, 13 Sep 2023 05:06:28 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Sep 2023 05:07:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Sep 2023 05:07:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:07:53 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:07:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:07:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e138a75d8a68c57acda5ac3d2a5ea38cfcd91aeeac6e996187886cdc4fe512b`  
		Last Modified: Wed, 13 Sep 2023 05:08:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba6b3e055f188fc0c938c464d3df287b87b4ebd990c6d3023e4043e9475882b`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d1091bb5b201027155aa6154441b33e21f06c80c98e5502f0ea97d3e6ac36`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf75715be616bda4fd455e8842d5c47e6361520831c79994aac63897f074a6`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 242.8 KB (242766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3267078f67f5f3fb7955bda584f1a858622791ed81e9c2e45ac79383c6c3795`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 5.8 MB (5779913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81aab1223d4ac5fade6bcbff4e433f5a038988f73089bb43aff8b974c715a2`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a790db19f2a0d625636fa4d186b3b076500c592809d8b95c7a725e0c46a094`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4edbf9880281abc4bccc4d818ad299ce3cd5ad235e1cb033fbc49b3096f3a7`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05fad63f054ab864e4484c552a76f82c3bf9e322da181d03f63a597755912`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.22-windowsservercore-1809`

```console
$ docker pull nats@sha256:0d1237c42b0bf510367a68f73790bafd41d3e4dba95502ecf7d630eb6dcf0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:2.9.22-windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4bc9d7dc99d75f7813148b82653c884ac51975085d49de22b68ac981bf1b3c40
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022365856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f7856c543b220cf294996bece7566b5515805212fc38127b1450f60b3e3ba5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_SERVER=2.9.22
# Wed, 13 Sep 2023 05:05:37 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.22/nats-server-v2.9.22-windows-amd64.zip
# Wed, 13 Sep 2023 05:05:38 GMT
ENV NATS_SERVER_SHASUM=e91db73b02bd4dca3eb7a4bf32e29763450b08d593f73e87d0a6b70102dea0d4
# Wed, 13 Sep 2023 05:06:28 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Sep 2023 05:07:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Sep 2023 05:07:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:07:53 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:07:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:07:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e138a75d8a68c57acda5ac3d2a5ea38cfcd91aeeac6e996187886cdc4fe512b`  
		Last Modified: Wed, 13 Sep 2023 05:08:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba6b3e055f188fc0c938c464d3df287b87b4ebd990c6d3023e4043e9475882b`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d1091bb5b201027155aa6154441b33e21f06c80c98e5502f0ea97d3e6ac36`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cf75715be616bda4fd455e8842d5c47e6361520831c79994aac63897f074a6`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 242.8 KB (242766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3267078f67f5f3fb7955bda584f1a858622791ed81e9c2e45ac79383c6c3795`  
		Last Modified: Wed, 13 Sep 2023 05:08:30 GMT  
		Size: 5.8 MB (5779913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81aab1223d4ac5fade6bcbff4e433f5a038988f73089bb43aff8b974c715a2`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a790db19f2a0d625636fa4d186b3b076500c592809d8b95c7a725e0c46a094`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4edbf9880281abc4bccc4d818ad299ce3cd5ad235e1cb033fbc49b3096f3a7`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c05fad63f054ab864e4484c552a76f82c3bf9e322da181d03f63a597755912`  
		Last Modified: Wed, 13 Sep 2023 05:08:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.18`

```console
$ docker pull nats@sha256:786d33ad98a8a73aa4f10d909dcb550de62f1552c1d33eb21c95758495d33a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:77d10af272e58ffd19001f0db49493589a4b0abba48a70b57a8029366d472254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9482518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39b0cb7c24aa23188baf203d418d2333d5d18953342751ee18b859dc679fcd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:03:50 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:03:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:03:53 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:03:53 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:03:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070583810f6cd68d8ea71179b6fdd705aa490f296a5cb5a66ecd97f5cc4c4330`  
		Last Modified: Thu, 28 Sep 2023 23:04:37 GMT  
		Size: 6.1 MB (6079551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be399c43b1b858806ac64baddb3196e62d8ea24152ed6a9489512be6cb5de85`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94775086e63d5b22fe439092d1f727e7f098513aab181522a5d2bfd9a85f736`  
		Last Modified: Thu, 28 Sep 2023 23:04:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:8675bafd39721847c4d00f207b9d3768732596d5fab8b3a476909115124542d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8947901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76cbecbcce8b069fc978f91aeb181148eee0820f3d4999ce161a6e0653cba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:11:17 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 22:11:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 22:11:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 22:11:21 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 22:11:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 22:11:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230e88f3bcce2dd085bcc8db5a5fa1b3b2902c366735c2e486ebe0d23eaf148`  
		Last Modified: Thu, 28 Sep 2023 22:11:57 GMT  
		Size: 5.8 MB (5801609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101e415dcaebc4f3d8a5a2735981ddd5d0ff1535d480afb574a4fc1658a9a7e4`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8e0798236e2d5f88e675761f8f7ca8d5a71335ac913a8fd96dc37cb9243d9`  
		Last Modified: Thu, 28 Sep 2023 22:11:55 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:b557c7a6554606de9058a753a0453c5f9d71fc1c149786656e3aba0c32336a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8694050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef603696f178c9c51ce9b8be6247a6cc42c3188316ffcfda6354e6b2f61e0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:17:43 GMT
ENV NATS_SERVER=2.10.1
# Thu, 28 Sep 2023 23:17:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 28 Sep 2023 23:17:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 28 Sep 2023 23:17:46 GMT
EXPOSE 4222 6222 8222
# Thu, 28 Sep 2023 23:17:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Sep 2023 23:17:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727be44ddc27d8b0d1ed688ce066b2cd9b41d31080217272fd6dc6f384b6056c`  
		Last Modified: Thu, 28 Sep 2023 23:18:26 GMT  
		Size: 5.8 MB (5793143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf6eba1077eb020231bb418974cfb72886f292d2273632609e9eacc438ac31`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede42bf5d94b22e3ef6a707e06032c8614ea0ce42dabf538b7c3cb37fd0b0f8e`  
		Last Modified: Thu, 28 Sep 2023 23:18:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:940b8267f14f366a3c4d80b12de99d7f8ad26fb1643e2fa934500cede1c900ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8ca6183ffc7017fd893acde6229d07fb2b96ae98303b2ab233fc8146f91c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:05:32 GMT
ENV NATS_SERVER=2.10.1
# Fri, 29 Sep 2023 02:05:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='13ab69dd6b35b4e253e97f469b61c4038fb6c1d0de89df6dfc93f75af1728ace' ;; 		armhf) natsArch='arm6'; sha256='ad6da4b3289293624e1e60dd0c719d3f2c9cc768774b9f25e580c236915a906b' ;; 		armv7) natsArch='arm7'; sha256='9a706550622ce44f06e6cc44621c01aa27aa9f5da4347d4295e65e986b5cb907' ;; 		x86_64) natsArch='amd64'; sha256='f058d6195931f28cd14d2ac1b9b6a7ce1d760c66c76ccea72aa6b936f4b8d75c' ;; 		x86) natsArch='386'; sha256='1c1e82380139758a69b5040631890914a9db5234517ef9d82b0173e37b8ca96a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 29 Sep 2023 02:05:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 29 Sep 2023 02:05:34 GMT
EXPOSE 4222 6222 8222
# Fri, 29 Sep 2023 02:05:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:05:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a93b754c4c7d951164f5ce0358c40f8ad2803f1f8a47302038e43126e92471e`  
		Last Modified: Fri, 29 Sep 2023 02:06:21 GMT  
		Size: 5.7 MB (5653009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529cf438b2192f3a29fcd2fa3b344bae10282212ed92896d2b38c8c1aa93bfe9`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add757d5e62b868a6063cc02f41f8acbc1baca1f76c468fe807a22e562d7707`  
		Last Modified: Fri, 29 Sep 2023 02:06:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:897f64e44537e6e8eab8457196c789ea2764c28ca7e5b2f585c4ce67b0c4f9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4851; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:2a08a0c1d913294be585667f17f76f028053f5bf47b9d317e5bc0e409011ed1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3517f7b93c37103553431effcb0b5a8262feb87c3649b04249d86012c34a9761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 20 Sep 2023 00:49:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:49:17 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:49:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:49:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1646134cd3aac5e501d3658b95fcfd870fb902c4c9591a801a5b370a5aa574`  
		Last Modified: Wed, 20 Sep 2023 00:50:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:64211266fe0d926796dae72e7484f5aebbdb77c7e7faa3fab3d01954fe03a82e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40010bd31b571ac24ead3a8630fa80ce8609b0352d5dab096c6b72940be90a6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 20 Sep 2023 00:39:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 20 Sep 2023 00:39:32 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:39:32 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Sep 2023 00:39:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969097b6afede4aab7deed51f12918311993aadbe7075d4965c14497831f4a12`  
		Last Modified: Wed, 20 Sep 2023 00:40:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:6670fad4a4d64481de5425c7a8ee8e602faef2f05646051096bfa59d9126cbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:3ae7b24041d5c7f8bb775c1fd47da96b2891f8c6821bfe25f6bcf95a0eaf6064
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf1d87f97e43bca95d8940d4aa3abf65c2c05adb6681005cb66f3f7d8001ffc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2b24d029bdf2310dcf6089c8f58986b6c70babf4fd4d433f329957862df58d77 in C:\nats-server.exe 
# Thu, 21 Sep 2023 00:18:29 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05405503d7afb6019521e5fa013d09e5c8636161e9408ba36c149f4853898e7`  
		Last Modified: Thu, 21 Sep 2023 00:19:36 GMT  
		Size: 5.6 MB (5569390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1f97d2316001518d35eb0b75ac1888c2fe2da51ce49c16012d2fef9ccf5e0c`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6a311706a8aadd91f05c001d3ffbd3a548f21286d0db22eed44fcd5999100f`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a3c2ef4f82e001ae8c4b096641708c8d404bd43dae8f46f843d21d8bb0fd69`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a063be69428345c92d570f896ffe0326401a9b501ba554a0c4ebf8dc1f5dd`  
		Last Modified: Thu, 21 Sep 2023 00:19:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:77c47cc0fe636b5d343f7c199f6e3b5d994639b39552b1e73aed192ffda485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:1875f12ff7878ddfe48c8de862438a1ad5ae7276f649b816881c2dea15ed26b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dbf1d04efd9a30a62425bd41207c511b14081999ce76172f281d0fe89bfd73`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:c6ff8909f7113222256ebebb968fe0190a269ad381596aefb35d156811fb1ac0 in /nats-server 
# Thu, 21 Sep 2023 09:48:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 09:48:48 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 09:48:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 09:48:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f4f97c87f3182f3eaa21bc8a4209e2a88915ccc12e763365b83e5854d4e7626`  
		Last Modified: Thu, 21 Sep 2023 09:49:36 GMT  
		Size: 5.5 MB (5456669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef02680465285626ba7e21b07e557d639af79221a9367ae68b2b3b7affc339`  
		Last Modified: Thu, 21 Sep 2023 09:49:35 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:cce3ff90a32531db64bb74852140a156326d487dafbf812da2168f78c0e85388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b8fef881498596233d1f7dda3dc1a4113c72bfe5e1088ded56d10a45d128f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:dbe6aeea160dba3a7bdcaf0c14808f7a7b31899bb87a50ed117996ead07014e6 in /nats-server 
# Thu, 21 Sep 2023 00:07:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 00:07:58 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:07:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 00:07:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6837114cbc023e4b8b17b6a951b2e91ab9668a1f3ffe65bec26f4ea44b812845`  
		Last Modified: Thu, 21 Sep 2023 00:08:53 GMT  
		Size: 5.2 MB (5177597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bde9589f631b3debf2ce00b1154c597464aeb530aac8a0016d7bee37f972958`  
		Last Modified: Thu, 21 Sep 2023 00:08:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:3f64956d0fd95665a5c832ed239c72c849f21337700393a702e41e6f2f1746d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf38230ebe561091e88c98d9e5cdc9d9cbfb7a714e3c47994bcc8e1742862bf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Sep 2023 00:39:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 10:40:11 GMT
COPY file:26e518de68a94421b4a77f614c7165ef51b1f4f8ef3ebbd5f1dd4ced7a078e87 in /nats-server 
# Thu, 21 Sep 2023 10:40:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 10:40:12 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 10:40:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 10:40:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02b06015072565fd114f11367725c50a0aa1a4949669f7a8308fbb2ebde2ea07`  
		Last Modified: Thu, 21 Sep 2023 10:40:57 GMT  
		Size: 5.2 MB (5170879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba28db888c799e852a8174a28420023cbf8b93c1cabfde2da64a920f59a3ec5`  
		Last Modified: Thu, 21 Sep 2023 10:40:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e6aea49e5eb407c078286700c1402c6eda155ae11cdd40f8604194f6f70d0dd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5029479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d109a8655a05cb22d5529db631b1a167bfae974cfc5d047c1ac261888ecd6e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:943544393eb61c235711dc43a87ec667d4491be8bcff70eee560d8276bd01b5b in /nats-server 
# Thu, 21 Sep 2023 05:05:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 21 Sep 2023 05:05:18 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 05:05:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 21 Sep 2023 05:05:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:85892a63e455fd1561bc50ef513a999a9a22152bbab4f029732ea77658da0b37`  
		Last Modified: Thu, 21 Sep 2023 05:06:05 GMT  
		Size: 5.0 MB (5028971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d6a1649b69be08c681087d8f2f84e750824c24acb44b6d1be0a9a706bb112`  
		Last Modified: Thu, 21 Sep 2023 05:06:04 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:caacdd68ac15825419bdd0d1ed333408d4c22b3a26035275e48d153c22268c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:6a50e306cf3f0c7dbd1e2df340d2696b1622ad3232c7d83cb0d1f72195089ca5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022614730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82b912330f09e1d0a6d64e3034e0da94f54645b45b8713a83652480b2bea1b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 03:56:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Sep 2023 05:05:36 GMT
ENV NATS_DOCKERIZED=1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER=2.10.1
# Thu, 21 Sep 2023 00:15:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.1/nats-server-v2.10.1-windows-amd64.zip
# Thu, 21 Sep 2023 00:15:16 GMT
ENV NATS_SERVER_SHASUM=88f2990dd6fea0bb2d8ba5cfde41ab5c96dd01bbaf4f9e9a3569815a0803cb1c
# Thu, 21 Sep 2023 00:16:19 GMT
RUN Set-PSDebug -Trace 2
# Thu, 21 Sep 2023 00:18:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 21 Sep 2023 00:18:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 21 Sep 2023 00:18:06 GMT
EXPOSE 4222 6222 8222
# Thu, 21 Sep 2023 00:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 21 Sep 2023 00:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b21bbf840142288ae2bce3465085b591133cf10f78f7dda43277db4838332d8`  
		Last Modified: Wed, 13 Sep 2023 04:36:45 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f616fe064e9d4e73bf2aec9a4fe9c58837ec84c2fc998a54ab7a77b52e109`  
		Last Modified: Wed, 13 Sep 2023 05:08:32 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f26828615c039d9da3e9f52c8b61ad3b2183a7ec3940bb1985bfc9a64be81`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a235c3fc87ed07702e70bb83fcbcb5ccaf81440d9ffd8d450d16bb7f273ce0`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759a393cccf186a4709cd9d0c4da137cade59a534bc53125be57217f7b21ef61`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cc61521de3ff29def7a6479a78dc7165d144b87f68e455eedb1ed30775aeaa`  
		Last Modified: Thu, 21 Sep 2023 00:19:20 GMT  
		Size: 242.8 KB (242789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d014e00481cb1e60003ba14c0a143d5126a763b4d413032ddad39559313825d`  
		Last Modified: Thu, 21 Sep 2023 00:19:19 GMT  
		Size: 6.0 MB (6028853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba83a190b4d5c219eab28b93cc94ab37e1a941e7270d4e60b5114f037589da`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ab4d57441cb1024559b87812361354ac635647bdb46a4ea450769c671d6f2`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd0e1cd2f7b50ded5cab327e6c888492fb4c4e022a0062cc719b9b6f9bcd8f4`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca70f3129ad44afad7b489a20cfd3a7bd2187694d47690907dab50fc4638c34`  
		Last Modified: Thu, 21 Sep 2023 00:19:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
