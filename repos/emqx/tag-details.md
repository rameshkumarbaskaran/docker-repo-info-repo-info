<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.18`](#emqx4418)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.24`](#emqx5024)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:48c4aa4c579500d6ff17e7cc28f4cde95e2d43cda4a381b9ebfa4bb3ed6ca0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:48c4aa4c579500d6ff17e7cc28f4cde95e2d43cda4a381b9ebfa4bb3ed6ca0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.18`

```console
$ docker pull emqx@sha256:48c4aa4c579500d6ff17e7cc28f4cde95e2d43cda4a381b9ebfa4bb3ed6ca0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.18` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.18` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8e0d58732509353013c1b904bae07e0329d294ba52c2bd04f53bd25c502d4143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804639c65a2a511d2bed3309d5f86522f6d22dbc8a51e8f139e5fec392650d63`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 18:31:09 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 18:31:09 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 18:31:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 18:31:13 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:13 GMT
USER emqx
# Wed, 03 May 2023 18:31:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 18:31:14 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 18:31:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7f51cc8da6fe6eddb0fd850db3e636cee3e3bf53295f3a92848743419ad42`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 2.6 MB (2559413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3d3ca96bb54f431601711afa294d7451ac1a5e31a4badb232efd929f1c1704`  
		Last Modified: Wed, 03 May 2023 18:31:39 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff06d9350693c4f454f1e9f2ea815a24db1f44dad7dbf3c14cdb68600ef4fecd`  
		Last Modified: Wed, 03 May 2023 18:31:43 GMT  
		Size: 40.1 MB (40079882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb7f52eead47eddb019a9b93e2a9d788bcdace6d6e356c9aef8cecc7990f61`  
		Last Modified: Wed, 03 May 2023 18:31:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:e78ebd69341d015c682e5051157f56c96341985d03844335420ed4c3c34884ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:e78ebd69341d015c682e5051157f56c96341985d03844335420ed4c3c34884ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.24`

```console
$ docker pull emqx@sha256:e78ebd69341d015c682e5051157f56c96341985d03844335420ed4c3c34884ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.24` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.24` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:e78ebd69341d015c682e5051157f56c96341985d03844335420ed4c3c34884ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4b50e10fb46731814c64c2f4895fb915e46bed6a02dbfb2c47f1cc850549541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb178575b71345d1c69f7ed729a26d14a2f31906a357eb0af08e7bdacf1ea59a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:31:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:31:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 18:31:22 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 18:31:22 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 18:31:22 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 18:31:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 18:31:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 18:31:29 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 18:31:29 GMT
USER emqx
# Wed, 03 May 2023 18:31:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 18:31:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 18:31:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 18:31:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 18:31:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a0a959a91944f5ffb31084a10b9b4826a9d805233e915031b76e42b602615`  
		Last Modified: Wed, 03 May 2023 18:31:54 GMT  
		Size: 3.0 MB (3003014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56882cfb1383ca5cd03757133ba3ae8958e9dcda03842b24d3ea7be1a5976eae`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d94cdbd45a137fdd4e9550c9063287635b1f489a5643b0d1ef2b4b97988a0`  
		Last Modified: Wed, 03 May 2023 18:32:00 GMT  
		Size: 68.4 MB (68360168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0135dc909c80db97e23cd34ad7cb67e57fe22c9cc1b3e4fd2bec3168f4446084`  
		Last Modified: Wed, 03 May 2023 18:31:53 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
