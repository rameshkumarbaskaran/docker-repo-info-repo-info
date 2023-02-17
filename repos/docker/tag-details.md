<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-cli`](#docker20-cli)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20-windowsservercore-ltsc2022`](#docker20-windowsservercore-ltsc2022)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-cli`](#docker2010-cli)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10-windowsservercore-ltsc2022`](#docker2010-windowsservercore-ltsc2022)
-	[`docker:20.10.23`](#docker201023)
-	[`docker:20.10.23-alpine3.17`](#docker201023-alpine317)
-	[`docker:20.10.23-cli`](#docker201023-cli)
-	[`docker:20.10.23-cli-alpine3.17`](#docker201023-cli-alpine317)
-	[`docker:20.10.23-dind`](#docker201023-dind)
-	[`docker:20.10.23-dind-alpine3.17`](#docker201023-dind-alpine317)
-	[`docker:20.10.23-dind-rootless`](#docker201023-dind-rootless)
-	[`docker:20.10.23-git`](#docker201023-git)
-	[`docker:20.10.23-windowsservercore`](#docker201023-windowsservercore)
-	[`docker:20.10.23-windowsservercore-1809`](#docker201023-windowsservercore-1809)
-	[`docker:20.10.23-windowsservercore-ltsc2022`](#docker201023-windowsservercore-ltsc2022)
-	[`docker:23`](#docker23)
-	[`docker:23-cli`](#docker23-cli)
-	[`docker:23-dind`](#docker23-dind)
-	[`docker:23-dind-rootless`](#docker23-dind-rootless)
-	[`docker:23-git`](#docker23-git)
-	[`docker:23-windowsservercore`](#docker23-windowsservercore)
-	[`docker:23-windowsservercore-1809`](#docker23-windowsservercore-1809)
-	[`docker:23-windowsservercore-ltsc2022`](#docker23-windowsservercore-ltsc2022)
-	[`docker:23.0`](#docker230)
-	[`docker:23.0-cli`](#docker230-cli)
-	[`docker:23.0-dind`](#docker230-dind)
-	[`docker:23.0-dind-rootless`](#docker230-dind-rootless)
-	[`docker:23.0-git`](#docker230-git)
-	[`docker:23.0-windowsservercore`](#docker230-windowsservercore)
-	[`docker:23.0-windowsservercore-1809`](#docker230-windowsservercore-1809)
-	[`docker:23.0-windowsservercore-ltsc2022`](#docker230-windowsservercore-ltsc2022)
-	[`docker:23.0.1`](#docker2301)
-	[`docker:23.0.1-alpine3.17`](#docker2301-alpine317)
-	[`docker:23.0.1-cli`](#docker2301-cli)
-	[`docker:23.0.1-cli-alpine3.17`](#docker2301-cli-alpine317)
-	[`docker:23.0.1-dind`](#docker2301-dind)
-	[`docker:23.0.1-dind-alpine3.17`](#docker2301-dind-alpine317)
-	[`docker:23.0.1-dind-rootless`](#docker2301-dind-rootless)
-	[`docker:23.0.1-git`](#docker2301-git)
-	[`docker:23.0.1-windowsservercore`](#docker2301-windowsservercore)
-	[`docker:23.0.1-windowsservercore-1809`](#docker2301-windowsservercore-1809)
-	[`docker:23.0.1-windowsservercore-ltsc2022`](#docker2301-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-cli`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-cli` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:a52c2b40979a7e24e17998e10b3886903f6de600e38097b782404467599612e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:0b2133093d15f9d48e1dce13b3b2bdce319fb4c3f672a3f510e9643cb0308dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110627599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52b157278521b647847b1f573d67b6b1858535f04414cd8b5f492fc31ec677`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a96daa706f089e063622bfcfc5826c1d9828df4c14f2c1ccf42a804638820c07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101975259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042a788dc83212962b89655267cdcba0866afcb821b4f0c8ccf9c1fea726b23`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:4bb75f99ab5775ef2e758445018779adff14f444002c372c4c88ebdac6884e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ec3a3ed08227980d4ce3aeffabed14030037f00f7c079982b959d0f081dabba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131914511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74704cbdb083c8036e15ee3b2723767632e9354d7b28173e5f67498037404b40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
# Fri, 17 Feb 2023 19:26:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819af3a19eb2fb8344ce5b04fa757fb9fb63812e40af441d06dc6ac69eac599c`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 1.4 MB (1375655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f238c7ade23b8178f135a1bf39b920063dcbb59a2dbd0a5026fda04ec0905`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b6cd94b662230d0cc1b1526e981dcf554042288936616ba0d28704aaf85a4`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0564c9b685495c4ee540edd499e066c7585736ab104cee7722448912575c6c0b`  
		Last Modified: Fri, 17 Feb 2023 19:29:42 GMT  
		Size: 19.9 MB (19909539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398903f47c4f6dad9cb5ebeae6746d1afb7c2627a997d396ee0e6359dab2a42`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ec7002337a9491c5caae0f7c82793248eaba8c7a0c8bbb11a1200d567cb87ff7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125260397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca5c224bcfaf868e57609c2642c901d1e56c9b6cdf10dba6b80b1c24bfcdca1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
# Fri, 10 Feb 2023 22:04:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:04:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:04:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:04:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:04:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a767b46c33cc833e0bcf245534c191c68cf32ebf765eef74c47663ed796e289f`  
		Last Modified: Fri, 10 Feb 2023 22:07:02 GMT  
		Size: 1.4 MB (1401566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b515ff6208b3505bba2f69d8d4821442513386c34d65d9b138a1ae750652c252`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa510103ead3d27710b020f7f8bf3bb28adb714e55db50822c60c748c1f0ec75`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4cf9d898670b5486da5807068b7230549fcb6942700e7240388cf32995a846`  
		Last Modified: Fri, 10 Feb 2023 22:07:04 GMT  
		Size: 21.9 MB (21881853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a06f669dca8222af3f880e10330de1497816d41b18bf3e114f27e1bc9a0656`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:7fa036b71a8096fce5d1706b785209ebc408b525a8abd991ff02230dd8cf93dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:1cef88c2c0419d6b8ea726faa1860728d69018835270a29108645e8be9e75ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54912287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838f01493e2988f321b25d3243dc3180730ad6afa16abd323faa3a1306a8f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:50 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea72f980c593793d970639b307d4efeb5da9468ac364edb38e25928764bf6907`  
		Last Modified: Fri, 17 Feb 2023 19:29:54 GMT  
		Size: 4.1 MB (4144480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:458445d96bce320422801b33f6a1c3e2dd9cf3d85d44cccf7224020dafb39488
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50484416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c5a8e84e05fefe68fa4d279e5dddb43da2651bd3d22820dc725b2da10b0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:04:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55ceea83c47df10a018c83e8bd987ff9ee6eea8533cb7d43e959d5656c0f1a`  
		Last Modified: Fri, 10 Feb 2023 22:07:16 GMT  
		Size: 4.2 MB (4185891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:61f4966bd752e18b674e693cafad07303be06ec33ab8f88007315fc2d320afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:2a8687e6f6e4513ee9d48f8623c510e20b05b621179f88c74b2d64c3f0959508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d55a941b389ec4009308d0733fc7bb856bfe460af5d5d8bb182c34bd33b7be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-cli`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-cli` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:a52c2b40979a7e24e17998e10b3886903f6de600e38097b782404467599612e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:0b2133093d15f9d48e1dce13b3b2bdce319fb4c3f672a3f510e9643cb0308dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110627599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52b157278521b647847b1f573d67b6b1858535f04414cd8b5f492fc31ec677`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a96daa706f089e063622bfcfc5826c1d9828df4c14f2c1ccf42a804638820c07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101975259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042a788dc83212962b89655267cdcba0866afcb821b4f0c8ccf9c1fea726b23`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:4bb75f99ab5775ef2e758445018779adff14f444002c372c4c88ebdac6884e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ec3a3ed08227980d4ce3aeffabed14030037f00f7c079982b959d0f081dabba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131914511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74704cbdb083c8036e15ee3b2723767632e9354d7b28173e5f67498037404b40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
# Fri, 17 Feb 2023 19:26:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819af3a19eb2fb8344ce5b04fa757fb9fb63812e40af441d06dc6ac69eac599c`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 1.4 MB (1375655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f238c7ade23b8178f135a1bf39b920063dcbb59a2dbd0a5026fda04ec0905`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b6cd94b662230d0cc1b1526e981dcf554042288936616ba0d28704aaf85a4`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0564c9b685495c4ee540edd499e066c7585736ab104cee7722448912575c6c0b`  
		Last Modified: Fri, 17 Feb 2023 19:29:42 GMT  
		Size: 19.9 MB (19909539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398903f47c4f6dad9cb5ebeae6746d1afb7c2627a997d396ee0e6359dab2a42`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ec7002337a9491c5caae0f7c82793248eaba8c7a0c8bbb11a1200d567cb87ff7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125260397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca5c224bcfaf868e57609c2642c901d1e56c9b6cdf10dba6b80b1c24bfcdca1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
# Fri, 10 Feb 2023 22:04:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:04:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:04:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:04:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:04:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a767b46c33cc833e0bcf245534c191c68cf32ebf765eef74c47663ed796e289f`  
		Last Modified: Fri, 10 Feb 2023 22:07:02 GMT  
		Size: 1.4 MB (1401566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b515ff6208b3505bba2f69d8d4821442513386c34d65d9b138a1ae750652c252`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa510103ead3d27710b020f7f8bf3bb28adb714e55db50822c60c748c1f0ec75`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4cf9d898670b5486da5807068b7230549fcb6942700e7240388cf32995a846`  
		Last Modified: Fri, 10 Feb 2023 22:07:04 GMT  
		Size: 21.9 MB (21881853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a06f669dca8222af3f880e10330de1497816d41b18bf3e114f27e1bc9a0656`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:7fa036b71a8096fce5d1706b785209ebc408b525a8abd991ff02230dd8cf93dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:1cef88c2c0419d6b8ea726faa1860728d69018835270a29108645e8be9e75ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54912287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838f01493e2988f321b25d3243dc3180730ad6afa16abd323faa3a1306a8f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:50 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea72f980c593793d970639b307d4efeb5da9468ac364edb38e25928764bf6907`  
		Last Modified: Fri, 17 Feb 2023 19:29:54 GMT  
		Size: 4.1 MB (4144480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:458445d96bce320422801b33f6a1c3e2dd9cf3d85d44cccf7224020dafb39488
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50484416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c5a8e84e05fefe68fa4d279e5dddb43da2651bd3d22820dc725b2da10b0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:04:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55ceea83c47df10a018c83e8bd987ff9ee6eea8533cb7d43e959d5656c0f1a`  
		Last Modified: Fri, 10 Feb 2023 22:07:16 GMT  
		Size: 4.2 MB (4185891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:61f4966bd752e18b674e693cafad07303be06ec33ab8f88007315fc2d320afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:2a8687e6f6e4513ee9d48f8623c510e20b05b621179f88c74b2d64c3f0959508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d55a941b389ec4009308d0733fc7bb856bfe460af5d5d8bb182c34bd33b7be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-alpine3.17`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-cli`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-cli` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-cli-alpine3.17`

```console
$ docker pull docker@sha256:dfdd3f89f93fa6ca92aec5efad4d53f49ff1a8d2de51c90fae1dee2e32f91cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-cli-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:9e4496ad7edb0dfdcb67a49a39c2377d159e08790020960044d48bae6d94ab48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50767807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6712ab53721778ecf796f682ce8b2349fcaa8ddff7996c3a1f202fadf562d47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-cli-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b83b1e6fb7166be7520c918b109be782874bbb18be91216071b5a36004a49d5c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46298525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47084ddf64cdf77f86d90b95acd6c55b53f9167110e995cd18aa201cef1acb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-dind`

```console
$ docker pull docker@sha256:a52c2b40979a7e24e17998e10b3886903f6de600e38097b782404467599612e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-dind` - linux; amd64

```console
$ docker pull docker@sha256:0b2133093d15f9d48e1dce13b3b2bdce319fb4c3f672a3f510e9643cb0308dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110627599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52b157278521b647847b1f573d67b6b1858535f04414cd8b5f492fc31ec677`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a96daa706f089e063622bfcfc5826c1d9828df4c14f2c1ccf42a804638820c07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101975259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042a788dc83212962b89655267cdcba0866afcb821b4f0c8ccf9c1fea726b23`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-dind-alpine3.17`

```console
$ docker pull docker@sha256:a52c2b40979a7e24e17998e10b3886903f6de600e38097b782404467599612e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-dind-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:0b2133093d15f9d48e1dce13b3b2bdce319fb4c3f672a3f510e9643cb0308dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110627599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52b157278521b647847b1f573d67b6b1858535f04414cd8b5f492fc31ec677`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-dind-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a96daa706f089e063622bfcfc5826c1d9828df4c14f2c1ccf42a804638820c07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101975259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0042a788dc83212962b89655267cdcba0866afcb821b4f0c8ccf9c1fea726b23`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-dind-rootless`

```console
$ docker pull docker@sha256:4bb75f99ab5775ef2e758445018779adff14f444002c372c4c88ebdac6884e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ec3a3ed08227980d4ce3aeffabed14030037f00f7c079982b959d0f081dabba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131914511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74704cbdb083c8036e15ee3b2723767632e9354d7b28173e5f67498037404b40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
# Fri, 17 Feb 2023 19:26:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819af3a19eb2fb8344ce5b04fa757fb9fb63812e40af441d06dc6ac69eac599c`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 1.4 MB (1375655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f238c7ade23b8178f135a1bf39b920063dcbb59a2dbd0a5026fda04ec0905`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b6cd94b662230d0cc1b1526e981dcf554042288936616ba0d28704aaf85a4`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0564c9b685495c4ee540edd499e066c7585736ab104cee7722448912575c6c0b`  
		Last Modified: Fri, 17 Feb 2023 19:29:42 GMT  
		Size: 19.9 MB (19909539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398903f47c4f6dad9cb5ebeae6746d1afb7c2627a997d396ee0e6359dab2a42`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ec7002337a9491c5caae0f7c82793248eaba8c7a0c8bbb11a1200d567cb87ff7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125260397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca5c224bcfaf868e57609c2642c901d1e56c9b6cdf10dba6b80b1c24bfcdca1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:55 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:56 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:56 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:56 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:56 GMT
CMD []
# Fri, 10 Feb 2023 22:04:01 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:04:01 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:04:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:04:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:04:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:04:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab41a8c294982338edcae560e4d73498fb43ba88e0df5dfda54237ced0a8afb`  
		Last Modified: Fri, 10 Feb 2023 22:06:43 GMT  
		Size: 7.0 MB (6991119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14aaed14c2dda88e8eabf763345c48fb5d853ef1f31cacbb1db298f1ae61de`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abadd0ea582cfca5f94bdddd097f0ffe559fa44e78b3fbad3b78c07502c12c83`  
		Last Modified: Fri, 10 Feb 2023 22:06:47 GMT  
		Size: 48.7 MB (48680437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528a867ba5accdfa9dcbf66fba8002ab7cd594379e953a9de25ca420f2b637`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96953ecb31c85ee06be4c7daad60cb2f6ad060ec900bd67dcbf219e182299af`  
		Last Modified: Fri, 10 Feb 2023 22:06:41 GMT  
		Size: 2.8 KB (2816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a767b46c33cc833e0bcf245534c191c68cf32ebf765eef74c47663ed796e289f`  
		Last Modified: Fri, 10 Feb 2023 22:07:02 GMT  
		Size: 1.4 MB (1401566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b515ff6208b3505bba2f69d8d4821442513386c34d65d9b138a1ae750652c252`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa510103ead3d27710b020f7f8bf3bb28adb714e55db50822c60c748c1f0ec75`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4cf9d898670b5486da5807068b7230549fcb6942700e7240388cf32995a846`  
		Last Modified: Fri, 10 Feb 2023 22:07:04 GMT  
		Size: 21.9 MB (21881853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a06f669dca8222af3f880e10330de1497816d41b18bf3e114f27e1bc9a0656`  
		Last Modified: Fri, 10 Feb 2023 22:07:01 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-git`

```console
$ docker pull docker@sha256:7fa036b71a8096fce5d1706b785209ebc408b525a8abd991ff02230dd8cf93dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.23-git` - linux; amd64

```console
$ docker pull docker@sha256:1cef88c2c0419d6b8ea726faa1860728d69018835270a29108645e8be9e75ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54912287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838f01493e2988f321b25d3243dc3180730ad6afa16abd323faa3a1306a8f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:50 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea72f980c593793d970639b307d4efeb5da9468ac364edb38e25928764bf6907`  
		Last Modified: Fri, 17 Feb 2023 19:29:54 GMT  
		Size: 4.1 MB (4144480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:458445d96bce320422801b33f6a1c3e2dd9cf3d85d44cccf7224020dafb39488
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50484416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c5a8e84e05fefe68fa4d279e5dddb43da2651bd3d22820dc725b2da10b0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:40 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:45 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:04:07 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dcf7fa45e4a97f72fe054ffe127d08a375e02b3f9ffac373af0f9c91d3f7b`  
		Last Modified: Fri, 10 Feb 2023 22:06:18 GMT  
		Size: 14.4 MB (14436884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3135edd6882a727a25f8a9281ab4a9c2515b3a27b9b18088228d38b57ae9e601`  
		Last Modified: Fri, 10 Feb 2023 22:06:17 GMT  
		Size: 13.8 MB (13819066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa598a398b5f970fcc5c64314883b925827fa97d19fbd40214755009f0c511`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199244f0e47ba599c9cd04c1654c7cd26c520f6d5cea9a375cac422de3a0dc7`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b36371db29f6c279718abf59a19a582913f960e5e11dce53dc6a4c0fc885b2`  
		Last Modified: Fri, 10 Feb 2023 22:06:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55ceea83c47df10a018c83e8bd987ff9ee6eea8533cb7d43e959d5656c0f1a`  
		Last Modified: Fri, 10 Feb 2023 22:07:16 GMT  
		Size: 4.2 MB (4185891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-windowsservercore`

```console
$ docker pull docker@sha256:61f4966bd752e18b674e693cafad07303be06ec33ab8f88007315fc2d320afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:20.10.23-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.23-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-windowsservercore-1809`

```console
$ docker pull docker@sha256:2a8687e6f6e4513ee9d48f8623c510e20b05b621179f88c74b2d64c3f0959508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:20.10.23-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:129a9c270cd9ad4a683c46d4ca6bb902a0a15550b1699f1af58c8a88ec562380
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019216859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2dd9f3ee76f0e8b511e3c27fc245e0d385baa9934e4398824da5e2a65b6a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:38:43 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:38:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:40:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0b4bbc1480a317988f088f1dde1ea8db127278dc02abee34914efec310919`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34394b061f1fb129f4945bdd6b34b289924c9362c4566c3b5dcba92523e9c334`  
		Last Modified: Thu, 16 Feb 2023 02:41:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f9c27a974e711d0fe130afe51966a55008d5db57e075d7cb1f6cd044c3caf6`  
		Last Modified: Thu, 16 Feb 2023 02:41:51 GMT  
		Size: 55.7 MB (55742637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d55a941b389ec4009308d0733fc7bb856bfe460af5d5d8bb182c34bd33b7be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:20.10.23-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:4655a0b8d4f3330fa0c50eb2b64e94dc84c0e9d2c43be3e23628a5baf9e0c146
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736088778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574248f638bfdc64b21b8fb1134c4bd6a4582327162776ffed1c9510cb99b9b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:37:56 GMT
ENV DOCKER_VERSION=20.10.23
# Thu, 16 Feb 2023 02:37:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.23.zip
# Thu, 16 Feb 2023 02:38:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37000251b28c80b932b3966a757f238990dd0606d478d8de8cccb1d802ec715`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9bb19df9823688a18314d31ef7b8dace8b26e828c29f902f388073292c7ee`  
		Last Modified: Thu, 16 Feb 2023 02:41:21 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e72881b95eb9b53a07b0a42327076108754c7e0c89547c51a0c821550082`  
		Last Modified: Thu, 16 Feb 2023 02:41:31 GMT  
		Size: 56.0 MB (55968992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-cli`

```console
$ docker pull docker@sha256:ba7715200ca50204c6a05eb888d97734aaf9e3e02432cbd3ceb2f3953b00ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-cli` - linux; amd64

```console
$ docker pull docker@sha256:650368b0dc8a063fb3270e4cef9218e06fea7a069bcbe31b90623c2664a18376
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53004959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56f59ab776c03c289ca288ce2bf621ada0be521accf1ccc4bc08ba7b884968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31a164c1dcbf7649915745cd3bfc580325d7feda7b8e480a500f1257bc42cb15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48851272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4083138fdbf3532478533f42d00d1fe2ae133286ecf00152b2baba9d57c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-dind-rootless`

```console
$ docker pull docker@sha256:56388e4b4951e829a41b07fe364e0e186d33726205918a208e6b717121e247d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:21331136487e821a589993a0b606c16ed10de9638ad5a72eb8adbe9cd8d80b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133067430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574e467c5a50409b5c0b3ef5bf9e18107a13ef5354255569d4c5ed4aead3aa70`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
# Fri, 17 Feb 2023 19:26:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66e753b1062321b657051257578ef83061828cc1f581f66395ca773f94bb87`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.4 MB (1375664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeba1442d0c5d69ff3f8d3a040b8c4377df139f2885c290ed6e9e970784f6ec`  
		Last Modified: Fri, 17 Feb 2023 19:28:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0af8d3f5bf4a1d20cf79f65972a3854d77acf15d3a9a96e8308d3d65d0ba35`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999a5dd5cc8951f4e9d3e24579b71bf9a1c00ccfab4644ff4bf4c63766abb11`  
		Last Modified: Fri, 17 Feb 2023 19:28:25 GMT  
		Size: 20.3 MB (20325933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b8134a0e6971c937ad9b65188a9d31b0d30842999630170da4a3c815fc2205`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6edc4afdc775e58abb65035db44a1ebe78a8e326294118fbf66dad96996c2c4c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126406028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d206a66e25d882b70783832ee2a4c587266bb04f46a1f68d714d92b6ff4de173`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
# Fri, 10 Feb 2023 22:03:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:03:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:03:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:03:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:03:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:03:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7b5dd45ca6bedf8857c5b90d0473140b250c200bdc4ea2afae1f517ad6cd5`  
		Last Modified: Fri, 10 Feb 2023 22:05:45 GMT  
		Size: 1.4 MB (1401580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee41d2ea8850509ff17faaf9cedbf68be4a3cde91a1040617cfdbc7a4d2259`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662e137aa58da9af20bfe7afd03bfa3c6c579f232a82a0e64ad18d2b6b85ce1f`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e50c6d35c6de35ee4dfce417fe533e2bcdb62cbba9d57da43fd0e96699254d`  
		Last Modified: Fri, 10 Feb 2023 22:05:48 GMT  
		Size: 22.2 MB (22232244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d5f32b05612e847606aecce43133db7d22da1b8b27bcc13b696428996758b`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-git`

```console
$ docker pull docker@sha256:ca4a8842aeb242b88302c2bdfe819ad016316d804dab8e3de7a8070fb264bea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-git` - linux; amd64

```console
$ docker pull docker@sha256:1f3bdb597458d6a86256b34a0053952c3091adad0f2b0a273b4fda97dabd70ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e18e7e6ae8e182e961b297f85ae2814235dafe557cc94d0d3b1843a40cded0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae4507ff882dba876294ee5d8e013faf283e3c3eaced29c96455e2b39fd319`  
		Last Modified: Fri, 17 Feb 2023 19:28:40 GMT  
		Size: 4.1 MB (4144482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b7702e5bd417e89d06bfbeb8c6c49be0f1e8394bc5c938532242d5ede12baab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53037160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c620ee79c98e27ec77e0353f42c0b33ae9806e657756891ff1347f55fbcd97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3856995d1d810dc5db3ed2e906e3a7441eb58d2dc4b57cd0c35e9d7806bfd1`  
		Last Modified: Fri, 10 Feb 2023 22:06:03 GMT  
		Size: 4.2 MB (4185888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore`

```console
$ docker pull docker@sha256:6f834f3715ec6b13edce4e396ab6efc5fd776d928401644ef9ced439d5eae364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:23-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-1809`

```console
$ docker pull docker@sha256:bd18955fd7e4876bd05f686f9d45c67cc80dac0addce95d3177682bdf55c72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:23-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:69b86145f5a384fe0215f4ec0bd5e56c2c206fea0adbfbf65be51136b1ddf849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:23-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-cli`

```console
$ docker pull docker@sha256:ba7715200ca50204c6a05eb888d97734aaf9e3e02432cbd3ceb2f3953b00ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:650368b0dc8a063fb3270e4cef9218e06fea7a069bcbe31b90623c2664a18376
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53004959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56f59ab776c03c289ca288ce2bf621ada0be521accf1ccc4bc08ba7b884968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31a164c1dcbf7649915745cd3bfc580325d7feda7b8e480a500f1257bc42cb15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48851272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4083138fdbf3532478533f42d00d1fe2ae133286ecf00152b2baba9d57c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-dind-rootless`

```console
$ docker pull docker@sha256:56388e4b4951e829a41b07fe364e0e186d33726205918a208e6b717121e247d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:21331136487e821a589993a0b606c16ed10de9638ad5a72eb8adbe9cd8d80b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133067430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574e467c5a50409b5c0b3ef5bf9e18107a13ef5354255569d4c5ed4aead3aa70`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
# Fri, 17 Feb 2023 19:26:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66e753b1062321b657051257578ef83061828cc1f581f66395ca773f94bb87`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.4 MB (1375664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeba1442d0c5d69ff3f8d3a040b8c4377df139f2885c290ed6e9e970784f6ec`  
		Last Modified: Fri, 17 Feb 2023 19:28:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0af8d3f5bf4a1d20cf79f65972a3854d77acf15d3a9a96e8308d3d65d0ba35`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999a5dd5cc8951f4e9d3e24579b71bf9a1c00ccfab4644ff4bf4c63766abb11`  
		Last Modified: Fri, 17 Feb 2023 19:28:25 GMT  
		Size: 20.3 MB (20325933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b8134a0e6971c937ad9b65188a9d31b0d30842999630170da4a3c815fc2205`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6edc4afdc775e58abb65035db44a1ebe78a8e326294118fbf66dad96996c2c4c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126406028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d206a66e25d882b70783832ee2a4c587266bb04f46a1f68d714d92b6ff4de173`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
# Fri, 10 Feb 2023 22:03:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:03:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:03:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:03:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:03:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:03:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7b5dd45ca6bedf8857c5b90d0473140b250c200bdc4ea2afae1f517ad6cd5`  
		Last Modified: Fri, 10 Feb 2023 22:05:45 GMT  
		Size: 1.4 MB (1401580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee41d2ea8850509ff17faaf9cedbf68be4a3cde91a1040617cfdbc7a4d2259`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662e137aa58da9af20bfe7afd03bfa3c6c579f232a82a0e64ad18d2b6b85ce1f`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e50c6d35c6de35ee4dfce417fe533e2bcdb62cbba9d57da43fd0e96699254d`  
		Last Modified: Fri, 10 Feb 2023 22:05:48 GMT  
		Size: 22.2 MB (22232244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d5f32b05612e847606aecce43133db7d22da1b8b27bcc13b696428996758b`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-git`

```console
$ docker pull docker@sha256:ca4a8842aeb242b88302c2bdfe819ad016316d804dab8e3de7a8070fb264bea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0-git` - linux; amd64

```console
$ docker pull docker@sha256:1f3bdb597458d6a86256b34a0053952c3091adad0f2b0a273b4fda97dabd70ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e18e7e6ae8e182e961b297f85ae2814235dafe557cc94d0d3b1843a40cded0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae4507ff882dba876294ee5d8e013faf283e3c3eaced29c96455e2b39fd319`  
		Last Modified: Fri, 17 Feb 2023 19:28:40 GMT  
		Size: 4.1 MB (4144482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b7702e5bd417e89d06bfbeb8c6c49be0f1e8394bc5c938532242d5ede12baab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53037160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c620ee79c98e27ec77e0353f42c0b33ae9806e657756891ff1347f55fbcd97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3856995d1d810dc5db3ed2e906e3a7441eb58d2dc4b57cd0c35e9d7806bfd1`  
		Last Modified: Fri, 10 Feb 2023 22:06:03 GMT  
		Size: 4.2 MB (4185888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore`

```console
$ docker pull docker@sha256:6f834f3715ec6b13edce4e396ab6efc5fd776d928401644ef9ced439d5eae364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:23.0-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:bd18955fd7e4876bd05f686f9d45c67cc80dac0addce95d3177682bdf55c72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:23.0-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:69b86145f5a384fe0215f4ec0bd5e56c2c206fea0adbfbf65be51136b1ddf849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:23.0-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-alpine3.17`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-cli`

```console
$ docker pull docker@sha256:ba7715200ca50204c6a05eb888d97734aaf9e3e02432cbd3ceb2f3953b00ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:650368b0dc8a063fb3270e4cef9218e06fea7a069bcbe31b90623c2664a18376
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53004959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56f59ab776c03c289ca288ce2bf621ada0be521accf1ccc4bc08ba7b884968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31a164c1dcbf7649915745cd3bfc580325d7feda7b8e480a500f1257bc42cb15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48851272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4083138fdbf3532478533f42d00d1fe2ae133286ecf00152b2baba9d57c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-cli-alpine3.17`

```console
$ docker pull docker@sha256:ba7715200ca50204c6a05eb888d97734aaf9e3e02432cbd3ceb2f3953b00ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-cli-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:650368b0dc8a063fb3270e4cef9218e06fea7a069bcbe31b90623c2664a18376
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53004959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56f59ab776c03c289ca288ce2bf621ada0be521accf1ccc4bc08ba7b884968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-cli-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31a164c1dcbf7649915745cd3bfc580325d7feda7b8e480a500f1257bc42cb15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48851272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4083138fdbf3532478533f42d00d1fe2ae133286ecf00152b2baba9d57c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-dind`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-dind-alpine3.17`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-dind-alpine3.17` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-dind-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-dind-rootless`

```console
$ docker pull docker@sha256:56388e4b4951e829a41b07fe364e0e186d33726205918a208e6b717121e247d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:21331136487e821a589993a0b606c16ed10de9638ad5a72eb8adbe9cd8d80b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133067430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574e467c5a50409b5c0b3ef5bf9e18107a13ef5354255569d4c5ed4aead3aa70`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
# Fri, 17 Feb 2023 19:26:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66e753b1062321b657051257578ef83061828cc1f581f66395ca773f94bb87`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.4 MB (1375664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeba1442d0c5d69ff3f8d3a040b8c4377df139f2885c290ed6e9e970784f6ec`  
		Last Modified: Fri, 17 Feb 2023 19:28:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0af8d3f5bf4a1d20cf79f65972a3854d77acf15d3a9a96e8308d3d65d0ba35`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999a5dd5cc8951f4e9d3e24579b71bf9a1c00ccfab4644ff4bf4c63766abb11`  
		Last Modified: Fri, 17 Feb 2023 19:28:25 GMT  
		Size: 20.3 MB (20325933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b8134a0e6971c937ad9b65188a9d31b0d30842999630170da4a3c815fc2205`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6edc4afdc775e58abb65035db44a1ebe78a8e326294118fbf66dad96996c2c4c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126406028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d206a66e25d882b70783832ee2a4c587266bb04f46a1f68d714d92b6ff4de173`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
# Fri, 10 Feb 2023 22:03:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:03:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:03:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:03:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:03:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:03:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7b5dd45ca6bedf8857c5b90d0473140b250c200bdc4ea2afae1f517ad6cd5`  
		Last Modified: Fri, 10 Feb 2023 22:05:45 GMT  
		Size: 1.4 MB (1401580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee41d2ea8850509ff17faaf9cedbf68be4a3cde91a1040617cfdbc7a4d2259`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662e137aa58da9af20bfe7afd03bfa3c6c579f232a82a0e64ad18d2b6b85ce1f`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e50c6d35c6de35ee4dfce417fe533e2bcdb62cbba9d57da43fd0e96699254d`  
		Last Modified: Fri, 10 Feb 2023 22:05:48 GMT  
		Size: 22.2 MB (22232244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d5f32b05612e847606aecce43133db7d22da1b8b27bcc13b696428996758b`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-git`

```console
$ docker pull docker@sha256:ca4a8842aeb242b88302c2bdfe819ad016316d804dab8e3de7a8070fb264bea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23.0.1-git` - linux; amd64

```console
$ docker pull docker@sha256:1f3bdb597458d6a86256b34a0053952c3091adad0f2b0a273b4fda97dabd70ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e18e7e6ae8e182e961b297f85ae2814235dafe557cc94d0d3b1843a40cded0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae4507ff882dba876294ee5d8e013faf283e3c3eaced29c96455e2b39fd319`  
		Last Modified: Fri, 17 Feb 2023 19:28:40 GMT  
		Size: 4.1 MB (4144482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b7702e5bd417e89d06bfbeb8c6c49be0f1e8394bc5c938532242d5ede12baab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53037160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c620ee79c98e27ec77e0353f42c0b33ae9806e657756891ff1347f55fbcd97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3856995d1d810dc5db3ed2e906e3a7441eb58d2dc4b57cd0c35e9d7806bfd1`  
		Last Modified: Fri, 10 Feb 2023 22:06:03 GMT  
		Size: 4.2 MB (4185888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-windowsservercore`

```console
$ docker pull docker@sha256:6f834f3715ec6b13edce4e396ab6efc5fd776d928401644ef9ced439d5eae364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:23.0.1-windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23.0.1-windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:bd18955fd7e4876bd05f686f9d45c67cc80dac0addce95d3177682bdf55c72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:23.0.1-windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:23.0.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:69b86145f5a384fe0215f4ec0bd5e56c2c206fea0adbfbf65be51136b1ddf849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:23.0.1-windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:ba7715200ca50204c6a05eb888d97734aaf9e3e02432cbd3ceb2f3953b00ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:650368b0dc8a063fb3270e4cef9218e06fea7a069bcbe31b90623c2664a18376
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53004959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56f59ab776c03c289ca288ce2bf621ada0be521accf1ccc4bc08ba7b884968`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31a164c1dcbf7649915745cd3bfc580325d7feda7b8e480a500f1257bc42cb15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48851272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4083138fdbf3532478533f42d00d1fe2ae133286ecf00152b2baba9d57c77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:56388e4b4951e829a41b07fe364e0e186d33726205918a208e6b717121e247d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:21331136487e821a589993a0b606c16ed10de9638ad5a72eb8adbe9cd8d80b34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133067430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574e467c5a50409b5c0b3ef5bf9e18107a13ef5354255569d4c5ed4aead3aa70`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
# Fri, 17 Feb 2023 19:26:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66e753b1062321b657051257578ef83061828cc1f581f66395ca773f94bb87`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.4 MB (1375664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeba1442d0c5d69ff3f8d3a040b8c4377df139f2885c290ed6e9e970784f6ec`  
		Last Modified: Fri, 17 Feb 2023 19:28:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0af8d3f5bf4a1d20cf79f65972a3854d77acf15d3a9a96e8308d3d65d0ba35`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999a5dd5cc8951f4e9d3e24579b71bf9a1c00ccfab4644ff4bf4c63766abb11`  
		Last Modified: Fri, 17 Feb 2023 19:28:25 GMT  
		Size: 20.3 MB (20325933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b8134a0e6971c937ad9b65188a9d31b0d30842999630170da4a3c815fc2205`  
		Last Modified: Fri, 17 Feb 2023 19:28:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6edc4afdc775e58abb65035db44a1ebe78a8e326294118fbf66dad96996c2c4c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126406028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d206a66e25d882b70783832ee2a4c587266bb04f46a1f68d714d92b6ff4de173`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
# Fri, 10 Feb 2023 22:03:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 10 Feb 2023 22:03:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 10 Feb 2023 22:03:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 10 Feb 2023 22:03:31 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 10 Feb 2023 22:03:31 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 10 Feb 2023 22:03:31 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7b5dd45ca6bedf8857c5b90d0473140b250c200bdc4ea2afae1f517ad6cd5`  
		Last Modified: Fri, 10 Feb 2023 22:05:45 GMT  
		Size: 1.4 MB (1401580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee41d2ea8850509ff17faaf9cedbf68be4a3cde91a1040617cfdbc7a4d2259`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662e137aa58da9af20bfe7afd03bfa3c6c579f232a82a0e64ad18d2b6b85ce1f`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e50c6d35c6de35ee4dfce417fe533e2bcdb62cbba9d57da43fd0e96699254d`  
		Last Modified: Fri, 10 Feb 2023 22:05:48 GMT  
		Size: 22.2 MB (22232244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d5f32b05612e847606aecce43133db7d22da1b8b27bcc13b696428996758b`  
		Last Modified: Fri, 10 Feb 2023 22:05:44 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:ca4a8842aeb242b88302c2bdfe819ad016316d804dab8e3de7a8070fb264bea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:1f3bdb597458d6a86256b34a0053952c3091adad0f2b0a273b4fda97dabd70ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e18e7e6ae8e182e961b297f85ae2814235dafe557cc94d0d3b1843a40cded0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae4507ff882dba876294ee5d8e013faf283e3c3eaced29c96455e2b39fd319`  
		Last Modified: Fri, 17 Feb 2023 19:28:40 GMT  
		Size: 4.1 MB (4144482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b7702e5bd417e89d06bfbeb8c6c49be0f1e8394bc5c938532242d5ede12baab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53037160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c620ee79c98e27ec77e0353f42c0b33ae9806e657756891ff1347f55fbcd97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:35 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3856995d1d810dc5db3ed2e906e3a7441eb58d2dc4b57cd0c35e9d7806bfd1`  
		Last Modified: Fri, 10 Feb 2023 22:06:03 GMT  
		Size: 4.2 MB (4185888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:3667e5ce0987a11dafcf7eceaccae8e462ec04925f9d7a4111c94ce517a994d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:ed6220b0de0f309f0844cf8cf1a6b861e981fb7f5c28bec6acc97abc910bd0a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111364117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd27a71ea4555b89fda3a6fd0118200e247b9f05cd07d3c16c58e67bee7c290d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:16 GMT
ENV DOCKER_VERSION=23.0.1
# Sat, 11 Feb 2023 04:50:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:25:48 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:25:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:25:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:25:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:25:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:25:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:25:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:25:54 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:25:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:05 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:05 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:06 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:06 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:06 GMT
CMD []
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3fda0e4f2a8480f6cb5d35df4883f73567fa3dd3902a8f5423c6c6ebc8a973`  
		Last Modified: Sat, 11 Feb 2023 04:52:14 GMT  
		Size: 16.2 MB (16220350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c70a1254cd87decca9ed97306f9b92ef371436d9670ea2a9ce32f4e682217`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d355096f56e1f024a28c87f75f8ccf419e437857285a8c3e0a160f10071a2f4`  
		Last Modified: Fri, 17 Feb 2023 19:27:30 GMT  
		Size: 15.3 MB (15343451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8bd29c066ab92d0c06530de84e038ad2f392d069d755f931fabeae7f1ed2c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12a7ad2f196eda7496dadde6f61894f7d81672a2cad69034d36a1878f2142c`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df61e21546809fd69cf4887ef6cfdd512400350adc10b5dba02165fcfe7648df`  
		Last Modified: Fri, 17 Feb 2023 19:27:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd742750fcf00cf7b22e182997880e18aca457f87e5d15dc6317dc14a86c1ae`  
		Last Modified: Fri, 17 Feb 2023 19:27:46 GMT  
		Size: 6.8 MB (6837985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed2afdad37784c9d3b93c945609a13ecdd55631705cf83cb74a416a54cd6d59`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0330887b1b5a53dbbbfeaa3505efce14086c3b37d7b19f49f65cdb72635945`  
		Last Modified: Fri, 17 Feb 2023 19:27:53 GMT  
		Size: 51.5 MB (51515987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80940587188609f4389885878942a63a5623e006a5f7ea447a0b9f70b0efbb`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912126ed1f1507596677091c7debeb69fa8f734f90bfff7fdceaf81b0514a316`  
		Last Modified: Fri, 17 Feb 2023 19:27:45 GMT  
		Size: 2.8 KB (2821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e99ecc41a14e2556e24e59a4e08ee920ce7670de3500b95683311c33c75185e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102770484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca16d80b8cd89f1a1d43bb22374270341450c5eb9b7133570ba0d3b3f3cfc43`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:02:59 GMT
ENV DOCKER_VERSION=23.0.1
# Fri, 10 Feb 2023 22:03:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 10 Feb 2023 22:03:02 GMT
ENV DOCKER_BUILDX_VERSION=0.10.2
# Fri, 10 Feb 2023 22:03:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-amd64'; 			sha256='ee5a5e3ebf5e5c73ac840993720bd1e72c4beb3b4ee9e85e2d6b4364cac87d89'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v6'; 			sha256='4d7c2e9eaed303306b40e0505577f4c7088c99f048a5870dd133cb7ad2336bd6'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm-v7'; 			sha256='d74936a4e4e9266aeca66e6a545ed99d83753b4901e0f5210e7646c987591974'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-arm64'; 			sha256='5f6c706833221cd2cae267ac8612c1809f9d7e8f3fe87707ae86cb695c560cd9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-ppc64le'; 			sha256='fe55ae43e009b4523523575f500257d7dafeb0aa637392b1853676b8a7a55b7b'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-riscv64'; 			sha256='b57cd352329baebca4cc8102806927de3f5402fff16f6f6e4a2e48080434472b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.2/buildx-v0.10.2.linux-s390x'; 			sha256='9a3be43a3a6902617a8224b41177a840e1a638597a27d7b7c2d558adb8be3a24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 10 Feb 2023 22:03:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 10 Feb 2023 22:03:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 10 Feb 2023 22:03:14 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 10 Feb 2023 22:03:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 10 Feb 2023 22:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:14 GMT
CMD ["sh"]
# Fri, 10 Feb 2023 22:03:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 10 Feb 2023 22:03:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 10 Feb 2023 22:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 10 Feb 2023 22:03:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 10 Feb 2023 22:03:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 10 Feb 2023 22:03:24 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 10 Feb 2023 22:03:24 GMT
VOLUME [/var/lib/docker]
# Fri, 10 Feb 2023 22:03:24 GMT
EXPOSE 2375 2376
# Fri, 10 Feb 2023 22:03:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:24 GMT
CMD []
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17073343af35b787a7b38fb171d8f0db63e76ec0cfa52e88f96e0a1a010826cc`  
		Last Modified: Fri, 10 Feb 2023 22:04:54 GMT  
		Size: 15.3 MB (15294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3be24006a004facfcd423a3a0758410ed38fe195642c3dbb0187171758fa40`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 14.4 MB (14436885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619343e2ca69426fe3f8247980a492d489868b6755397932ff4d0b426b2bdaa6`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 13.8 MB (13819068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972b1255ded6d58a7c25c0059d9cbdc2c013813bb220345b20d472a9e1f5c163`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9ec2dd46813a0f5eb3b33a9e861173565cb59fbbf2cc1f25b4dc516ebae2d`  
		Last Modified: Fri, 10 Feb 2023 22:04:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59409be232ad90490b28a2902a5a1ebd40f2eebe11f86d43f26183db2be9acb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde982b24cbd0d9873420b01582b109b291689ffab7a3957b8a5a378de546ff0`  
		Last Modified: Fri, 10 Feb 2023 22:05:10 GMT  
		Size: 7.0 MB (6991147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108f202a64fbf14fe58738b0fd55069d139b1e9244b0413b835409174d84bb9`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651bf7e96c9add2bbd91612c904d037f3f71fd0aaf7d06111a259cab274fc04`  
		Last Modified: Fri, 10 Feb 2023 22:05:14 GMT  
		Size: 46.9 MB (46922881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fbe955a5008d9b47a8ffe736eff4aafc2432a742ee3c3a45a472ac5104a2bd`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8ede8f32330827bc234a746551ac9a2169cf1ddd1d42d00a2006a153035ea3`  
		Last Modified: Fri, 10 Feb 2023 22:05:09 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:6f834f3715ec6b13edce4e396ab6efc5fd776d928401644ef9ced439d5eae364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1547; amd64
	-	windows version 10.0.17763.4010; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:bd18955fd7e4876bd05f686f9d45c67cc80dac0addce95d3177682bdf55c72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull docker@sha256:9768c86daedde5016e133668786b8afadfa3bdedbdd1f5ba55ff2294a8bb0e9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1980839162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d1d5436246620e8f83217b9a949d5fbafdc8a9c6948d83421902b6f936879f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Wed, 15 Feb 2023 22:41:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:35:24 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:35:25 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:35:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:37:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5753d4956d637f7e88bedf0b91260e724500d9fa9b91c0a9ed419263659a9a`  
		Last Modified: Thu, 16 Feb 2023 00:28:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec720058b47d0684c0cd4510fc0ecbd46e9190c17f7c384e1910dace8de10`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 512.2 KB (512156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a8e915a2701c0e02f201505f49d9481048ead72d2ee2c0dd790d451a613d99`  
		Last Modified: Thu, 16 Feb 2023 02:41:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ad533a3d1e6f9e7897ec28017fda70a620a474bb54333f5de4368b1fed55e`  
		Last Modified: Thu, 16 Feb 2023 02:41:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee39a3ffbd5de02c04b8d5cd1936fbe508f48b0a2bce51b5529fe2e4b778e211`  
		Last Modified: Thu, 16 Feb 2023 02:41:08 GMT  
		Size: 17.4 MB (17365009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:69b86145f5a384fe0215f4ec0bd5e56c2c206fea0adbfbf65be51136b1ddf849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull docker@sha256:27ed1b2d4e80dc82b9382c47f412649c1f7f049ba7b7f6d3b52ad684115d9d4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1697716897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a42315e37f397d9ac2a1de5bbe4b93ab1dbe7aa5f06fd89066ea76c87b087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Wed, 15 Feb 2023 22:37:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Feb 2023 02:33:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Feb 2023 02:33:14 GMT
ENV DOCKER_VERSION=23.0.1
# Thu, 16 Feb 2023 02:33:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.1.zip
# Thu, 16 Feb 2023 02:33:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c63a3d1906c0f8f7ca38587ab5f1c84160f9127cce25fb7f57d8a60dc7008`  
		Last Modified: Thu, 16 Feb 2023 00:26:46 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31c0ce3f337b044901163fed3eab931c5230b0243d3265fb3aa74a4d5a2aa6`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 769.3 KB (769272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51b56ea7059583d8fe1903f5de83b8c6d63f3fa7b4d176a2f26c16b906126b`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed573751146c58c393640a63fb38000810c63142ad820fb830bbebcd7c6ae10d`  
		Last Modified: Thu, 16 Feb 2023 02:40:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe1ffaf0244dbbe02c5b6f219ea1eaab5304a297feeab32750eb3f502f8c9bd`  
		Last Modified: Thu, 16 Feb 2023 02:40:53 GMT  
		Size: 17.6 MB (17597003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
