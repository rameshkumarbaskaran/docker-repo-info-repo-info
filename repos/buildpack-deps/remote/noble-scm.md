## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:710d0edbef7b839e05b9dfebd96e206012f64fe41f0ac20247d8fc9293d2a99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8757a4d7341250eae9e1564ff372a4a49e3759cffeea1c862fb415a435a19c33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89475216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a289c1539f37686baccc02946c595f47b935d28d16b7563996888f8bca6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6e962016133a2e69bf8bb72544b211445633f148627c656908805f0ca1e2a14`  
		Last Modified: Tue, 02 Jan 2024 21:20:35 GMT  
		Size: 30.4 MB (30350118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eab6a772f8ed88e9b2ee72076bfd4fb0e94a8febad8182dcac2722aae4058e9`  
		Last Modified: Thu, 04 Jan 2024 20:38:23 GMT  
		Size: 13.7 MB (13719056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83015b407bd25e9a38ff1e9a1ca59ef575f0077db6367f8f8cd79d31b4a5927`  
		Last Modified: Thu, 04 Jan 2024 20:38:41 GMT  
		Size: 45.4 MB (45406042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6c06a74a47db524ae79ec5645d5364d06186a22b7fa2191cfe19e13876dc5873
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90000476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5a05f1061aea384ddffa8ec4cd2626c6bcbb4460e55d3d382a578248d677ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:18:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b1fdfccfb097e3ea8369bc634c0a794c7f5dfa00a944deeff4a97c9496acd7f`  
		Last Modified: Thu, 04 Jan 2024 20:24:32 GMT  
		Size: 25.8 MB (25769091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7239c158ae97251c79c79b045912b146acfff69748a2146ac66091ac11d3a817`  
		Last Modified: Thu, 04 Jan 2024 20:24:29 GMT  
		Size: 14.6 MB (14621580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c081032e5a1ca0b2ee6ccbe8744305fff5852c50bfa4b299f822b5171ea558b`  
		Last Modified: Thu, 04 Jan 2024 20:24:52 GMT  
		Size: 49.6 MB (49609805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b9512e3dab5cd4f8fc21534628fb5fa50af94c07f522a09813289af9594ec1a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88395720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f785e8bf0de5fbcbbd9fa3f78ee16734d508c6889bad2aa26db885188982353`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 21:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 21:03:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:894886ead4cb9562f49271af0159d0a1ca3cd047fe095546a95b2547503278bc`  
		Last Modified: Thu, 04 Jan 2024 21:08:18 GMT  
		Size: 27.4 MB (27440272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad4c764df2e8f81f9fa5b16b3c9e87d20f8f97148504bbf60a3eb3b51fc5d07`  
		Last Modified: Thu, 04 Jan 2024 21:08:16 GMT  
		Size: 15.5 MB (15513863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d862754097df8334260a7b8dea49368f16c5774027e67a5d49d6bfb113e346`  
		Last Modified: Thu, 04 Jan 2024 21:08:32 GMT  
		Size: 45.4 MB (45441585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4dc0d23af7170e6cc5d5796ab42204acd3d1b2fcd636d8c0f192593c9f5381a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101460725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a3258e9ec283ace102ecb08f077f530f015e2cd2a55a058575cb7ec8492d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:30:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:31:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7ae3c70a47814103cc56d7659dc773a9caf5ce8df4d8324b88d9b5043e063d4`  
		Last Modified: Thu, 04 Jan 2024 20:38:35 GMT  
		Size: 32.4 MB (32405112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a6c7c9e8ceb49b67e3dbdacee3d70552db6ae83ceaea6d637dab7c45794b13`  
		Last Modified: Thu, 04 Jan 2024 20:38:28 GMT  
		Size: 18.5 MB (18547889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac382586005ae922fe6b9228080ee73150c2591819f6db9347fc6a9316dd0b86`  
		Last Modified: Thu, 04 Jan 2024 20:38:54 GMT  
		Size: 50.5 MB (50507724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:167f8d3384613fce84df28ed853cf2f17b96b109b341e9be8881b7f69253d77d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91644083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226ec3c7773350f8e9196d9c51a13d17be2fb1f1795c312912446e4946023f9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jan 2024 20:46:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0eb0ee1ee32a505c711b23ae33e7ecc888899622d95c7e982ef82dbb529c5d8`  
		Last Modified: Thu, 04 Jan 2024 20:50:14 GMT  
		Size: 28.2 MB (28174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02199b1c3761965bf141c9010678515a9c50e39cc89d2a830d1dd5d17aa25bc2`  
		Last Modified: Thu, 04 Jan 2024 20:50:13 GMT  
		Size: 16.6 MB (16609480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35074eaa320e26e298de6603d259e32c732e9b59403ef9ded95fc308e880cdb`  
		Last Modified: Thu, 04 Jan 2024 20:50:27 GMT  
		Size: 46.9 MB (46860079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
