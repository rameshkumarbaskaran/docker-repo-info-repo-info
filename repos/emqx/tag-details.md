<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.22`](#emqx4322)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.11`](#emqx4411)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.13`](#emqx5013)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:7aea60d41cc8269b545b71ea1f983aa5c939f33f9fecf2ef18e9a4de2c1105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c209b92ca6784e976831f7b96c6dc597b5a530a9cedccdcfa9f776c55b7c186
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca0de599ac2320288f6d2c530a8ccc4b816c6304c690f08c4936e134c4391`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:38 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 13:30:38 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 13:30:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 13:30:46 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
USER emqx
# Wed, 11 Jan 2023 13:30:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:30:47 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 13:30:47 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 13:30:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:30:47 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8afc846b3288c61befe97bcb3990e00d2ade2bdcc5b29cee6ecc6cf58f83d0b`  
		Last Modified: Wed, 11 Jan 2023 13:31:27 GMT  
		Size: 2.6 MB (2559366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb07ee7f97d2a875e8276a1211bdfbd972af93ebe2aa0ab6e970525c8abc389`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083242658c62df8f47a4c19ee4ab5c99b6236e3aa06608cda842391245bafabf`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39409074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969da264a9cf0319066e644051c961d166fcaf3f922c0f4cfb036c325fd8aa61`  
		Last Modified: Wed, 11 Jan 2023 13:31:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:b5cdf96b2f65693708695de630674029da26738a789532e1100b2bcfb148070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:776c7ebd1ad82b0fdb4fb964c7893efc4db5d6dea6fd123c6f0768acf3d3b8dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dddd3a138ab5db23c6729e00989aa22437b88911d6b81aa403c58657dced7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:38 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 03:48:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:48:47 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
USER emqx
# Wed, 11 Jan 2023 03:48:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:48:48 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:48:48 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 03:48:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:48:48 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661145169f684ea6623410a6b2e6bac4fff75dcec9474b51911e88a29706557f`  
		Last Modified: Wed, 11 Jan 2023 03:49:39 GMT  
		Size: 4.6 MB (4612517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebf05a3530c36d245bf6c7e46809202091a05a222150006a341b1a10186a3b2`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee3e26cd384fe26b2d8d4d2e7bd81e7d5510d04394408e3716a9ad3f52cedb3`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b98ad0a8ea4aaf82a5a3a86a56e2d00279b789ed0568c21c210686fdc248f`  
		Last Modified: Wed, 11 Jan 2023 03:49:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:814fe0469ef499119ab3da4a715a032f2ef8d3639d70c1c447e311349046b4b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d80502037f695f13b200e9367996f812703c6f53525becdea880a5eaf44cd7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:20 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 13:30:24 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 13:30:29 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 13:30:29 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:30:29 GMT
USER emqx
# Wed, 11 Jan 2023 13:30:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:30:29 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 13:30:30 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 13:30:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:30:30 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afe26eee17fa1a49cb6f89f853e34d82f13997ca667f6e7407e6b002aeb8473`  
		Last Modified: Wed, 11 Jan 2023 13:31:15 GMT  
		Size: 4.5 MB (4490429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821842eb795b17e8f57e07e9911c56d93351e819eafad5ac0162442932a123b5`  
		Last Modified: Wed, 11 Jan 2023 13:31:18 GMT  
		Size: 36.2 MB (36216048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdbaaafe6992e217a587185c394eebbee7fd486f17316624b53678c62b97191`  
		Last Modified: Wed, 11 Jan 2023 13:31:18 GMT  
		Size: 36.2 MB (36223789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbdc5a38d59ff97d26a19cff31f97490262080c2d1afdcd4ae3309e195993ef`  
		Last Modified: Wed, 11 Jan 2023 13:31:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.22`

```console
$ docker pull emqx@sha256:b5cdf96b2f65693708695de630674029da26738a789532e1100b2bcfb148070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.22` - linux; amd64

```console
$ docker pull emqx@sha256:776c7ebd1ad82b0fdb4fb964c7893efc4db5d6dea6fd123c6f0768acf3d3b8dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dddd3a138ab5db23c6729e00989aa22437b88911d6b81aa403c58657dced7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:38 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 03:48:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:48:47 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
USER emqx
# Wed, 11 Jan 2023 03:48:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:48:48 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:48:48 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 03:48:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:48:48 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661145169f684ea6623410a6b2e6bac4fff75dcec9474b51911e88a29706557f`  
		Last Modified: Wed, 11 Jan 2023 03:49:39 GMT  
		Size: 4.6 MB (4612517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebf05a3530c36d245bf6c7e46809202091a05a222150006a341b1a10186a3b2`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee3e26cd384fe26b2d8d4d2e7bd81e7d5510d04394408e3716a9ad3f52cedb3`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b98ad0a8ea4aaf82a5a3a86a56e2d00279b789ed0568c21c210686fdc248f`  
		Last Modified: Wed, 11 Jan 2023 03:49:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.22` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:814fe0469ef499119ab3da4a715a032f2ef8d3639d70c1c447e311349046b4b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d80502037f695f13b200e9367996f812703c6f53525becdea880a5eaf44cd7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:20 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 13:30:24 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 13:30:29 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 13:30:29 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:30:29 GMT
USER emqx
# Wed, 11 Jan 2023 13:30:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:30:29 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 13:30:30 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 13:30:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:30:30 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afe26eee17fa1a49cb6f89f853e34d82f13997ca667f6e7407e6b002aeb8473`  
		Last Modified: Wed, 11 Jan 2023 13:31:15 GMT  
		Size: 4.5 MB (4490429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821842eb795b17e8f57e07e9911c56d93351e819eafad5ac0162442932a123b5`  
		Last Modified: Wed, 11 Jan 2023 13:31:18 GMT  
		Size: 36.2 MB (36216048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdbaaafe6992e217a587185c394eebbee7fd486f17316624b53678c62b97191`  
		Last Modified: Wed, 11 Jan 2023 13:31:18 GMT  
		Size: 36.2 MB (36223789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbdc5a38d59ff97d26a19cff31f97490262080c2d1afdcd4ae3309e195993ef`  
		Last Modified: Wed, 11 Jan 2023 13:31:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:7aea60d41cc8269b545b71ea1f983aa5c939f33f9fecf2ef18e9a4de2c1105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c209b92ca6784e976831f7b96c6dc597b5a530a9cedccdcfa9f776c55b7c186
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca0de599ac2320288f6d2c530a8ccc4b816c6304c690f08c4936e134c4391`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:38 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 13:30:38 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 13:30:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 13:30:46 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
USER emqx
# Wed, 11 Jan 2023 13:30:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:30:47 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 13:30:47 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 13:30:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:30:47 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8afc846b3288c61befe97bcb3990e00d2ade2bdcc5b29cee6ecc6cf58f83d0b`  
		Last Modified: Wed, 11 Jan 2023 13:31:27 GMT  
		Size: 2.6 MB (2559366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb07ee7f97d2a875e8276a1211bdfbd972af93ebe2aa0ab6e970525c8abc389`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083242658c62df8f47a4c19ee4ab5c99b6236e3aa06608cda842391245bafabf`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39409074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969da264a9cf0319066e644051c961d166fcaf3f922c0f4cfb036c325fd8aa61`  
		Last Modified: Wed, 11 Jan 2023 13:31:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.11`

```console
$ docker pull emqx@sha256:7aea60d41cc8269b545b71ea1f983aa5c939f33f9fecf2ef18e9a4de2c1105a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.11` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.11` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c209b92ca6784e976831f7b96c6dc597b5a530a9cedccdcfa9f776c55b7c186
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca0de599ac2320288f6d2c530a8ccc4b816c6304c690f08c4936e134c4391`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:38 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 13:30:38 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 13:30:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 13:30:46 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:30:47 GMT
USER emqx
# Wed, 11 Jan 2023 13:30:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:30:47 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 13:30:47 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 13:30:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:30:47 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8afc846b3288c61befe97bcb3990e00d2ade2bdcc5b29cee6ecc6cf58f83d0b`  
		Last Modified: Wed, 11 Jan 2023 13:31:27 GMT  
		Size: 2.6 MB (2559366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb07ee7f97d2a875e8276a1211bdfbd972af93ebe2aa0ab6e970525c8abc389`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083242658c62df8f47a4c19ee4ab5c99b6236e3aa06608cda842391245bafabf`  
		Last Modified: Wed, 11 Jan 2023 13:31:30 GMT  
		Size: 39.4 MB (39409074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969da264a9cf0319066e644051c961d166fcaf3f922c0f4cfb036c325fd8aa61`  
		Last Modified: Wed, 11 Jan 2023 13:31:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:33194fdfc4c9904f90a3a7f73e9f6e51d170939ccd77a8a01986f498a7f5ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cac5309974f70ae5eeeb59abff92ac7a3036b2ad9adcd4dffc835abf24e5ccee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614926d26bd930c3065658621e46bfcffe653a8a0b0434985f9985a9a4dd445`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 13:30:55 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 13:30:55 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 13:30:55 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 13:30:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 13:31:00 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 13:31:00 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:31:00 GMT
USER emqx
# Wed, 11 Jan 2023 13:31:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:31:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 13:31:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 13:31:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:31:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc2e1d7e4868b505e10f5031690f64d100e27341b52efe1502538f59eb5c6b`  
		Last Modified: Wed, 11 Jan 2023 13:31:41 GMT  
		Size: 3.0 MB (3002805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7657cfec2c515e4133df88eecfb40ffd2d19a87eacd8fb4643dad7696a6f8ffe`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52121562b602bbc4962dbbe81872592ca827352a8771f60299c567dfc05a5db`  
		Last Modified: Wed, 11 Jan 2023 13:31:46 GMT  
		Size: 58.1 MB (58130370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934191c0fe2be70f8ede503ea5e7ea4707a59d7ff60ea324ebae54fd3af24505`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:33194fdfc4c9904f90a3a7f73e9f6e51d170939ccd77a8a01986f498a7f5ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cac5309974f70ae5eeeb59abff92ac7a3036b2ad9adcd4dffc835abf24e5ccee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614926d26bd930c3065658621e46bfcffe653a8a0b0434985f9985a9a4dd445`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 13:30:55 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 13:30:55 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 13:30:55 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 13:30:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 13:31:00 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 13:31:00 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:31:00 GMT
USER emqx
# Wed, 11 Jan 2023 13:31:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:31:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 13:31:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 13:31:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:31:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc2e1d7e4868b505e10f5031690f64d100e27341b52efe1502538f59eb5c6b`  
		Last Modified: Wed, 11 Jan 2023 13:31:41 GMT  
		Size: 3.0 MB (3002805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7657cfec2c515e4133df88eecfb40ffd2d19a87eacd8fb4643dad7696a6f8ffe`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52121562b602bbc4962dbbe81872592ca827352a8771f60299c567dfc05a5db`  
		Last Modified: Wed, 11 Jan 2023 13:31:46 GMT  
		Size: 58.1 MB (58130370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934191c0fe2be70f8ede503ea5e7ea4707a59d7ff60ea324ebae54fd3af24505`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.13`

```console
$ docker pull emqx@sha256:33194fdfc4c9904f90a3a7f73e9f6e51d170939ccd77a8a01986f498a7f5ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.13` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.13` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cac5309974f70ae5eeeb59abff92ac7a3036b2ad9adcd4dffc835abf24e5ccee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614926d26bd930c3065658621e46bfcffe653a8a0b0434985f9985a9a4dd445`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 13:30:55 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 13:30:55 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 13:30:55 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 13:30:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 13:31:00 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 13:31:00 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:31:00 GMT
USER emqx
# Wed, 11 Jan 2023 13:31:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:31:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 13:31:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 13:31:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:31:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc2e1d7e4868b505e10f5031690f64d100e27341b52efe1502538f59eb5c6b`  
		Last Modified: Wed, 11 Jan 2023 13:31:41 GMT  
		Size: 3.0 MB (3002805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7657cfec2c515e4133df88eecfb40ffd2d19a87eacd8fb4643dad7696a6f8ffe`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52121562b602bbc4962dbbe81872592ca827352a8771f60299c567dfc05a5db`  
		Last Modified: Wed, 11 Jan 2023 13:31:46 GMT  
		Size: 58.1 MB (58130370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934191c0fe2be70f8ede503ea5e7ea4707a59d7ff60ea324ebae54fd3af24505`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:33194fdfc4c9904f90a3a7f73e9f6e51d170939ccd77a8a01986f498a7f5ac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cac5309974f70ae5eeeb59abff92ac7a3036b2ad9adcd4dffc835abf24e5ccee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91183003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614926d26bd930c3065658621e46bfcffe653a8a0b0434985f9985a9a4dd445`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 13:30:55 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 13:30:55 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 13:30:55 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 13:30:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 13:31:00 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 13:31:00 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 13:31:00 GMT
USER emqx
# Wed, 11 Jan 2023 13:31:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 13:31:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 13:31:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 13:31:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 13:31:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc2e1d7e4868b505e10f5031690f64d100e27341b52efe1502538f59eb5c6b`  
		Last Modified: Wed, 11 Jan 2023 13:31:41 GMT  
		Size: 3.0 MB (3002805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7657cfec2c515e4133df88eecfb40ffd2d19a87eacd8fb4643dad7696a6f8ffe`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52121562b602bbc4962dbbe81872592ca827352a8771f60299c567dfc05a5db`  
		Last Modified: Wed, 11 Jan 2023 13:31:46 GMT  
		Size: 58.1 MB (58130370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934191c0fe2be70f8ede503ea5e7ea4707a59d7ff60ea324ebae54fd3af24505`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
