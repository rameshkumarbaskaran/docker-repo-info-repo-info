<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.18`](#emqx4418)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.26`](#emqx5026)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.0`](#emqx510)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:b98a8a1b72c69e886e4ff26748286a7c4849717064fc9fdb42b2d86d4024dedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:2b2cf3af1e1fdc946d0400e6ef8bc3f2754ddb861f739c78360c3d39cb253746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8154d287a0cd41ae6f26959af0d5aa9adf0e765d9f5940eae3fde58c3aab944`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 13 Jun 2023 04:05:14 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 13 Jun 2023 04:05:14 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 13 Jun 2023 04:05:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Jun 2023 04:05:19 GMT
WORKDIR /opt/emqx
# Tue, 13 Jun 2023 04:05:19 GMT
USER emqx
# Tue, 13 Jun 2023 04:05:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jun 2023 04:05:19 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Jun 2023 04:05:19 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Jun 2023 04:05:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:05:20 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11ad7fd953a334956026fc08b55abb1625fbaad5c2540a1d531ed566da6f031`  
		Last Modified: Tue, 13 Jun 2023 04:05:47 GMT  
		Size: 2.6 MB (2569638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105da9fef63b5bef345d47ed904190ccb2362f38449341ce80b93b5b72941db`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f883bad9be8bf6dd4cc27edca3cca8ee64f80b3afadab702283823b30d8b01`  
		Last Modified: Tue, 13 Jun 2023 04:05:51 GMT  
		Size: 47.3 MB (47298222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45046c6a3a747679abb1bffe6cd4755e04900a76a30a5369f1ef54700f63440e`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2d08ee2bc416b6f69851a687377881c076764d6010794177a34c576f405d0eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ef632180b6d12a52f16c392ec17886bc0626d84ec46d8a7d1f71cea9b85a0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 04 Jul 2023 03:03:08 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 04 Jul 2023 03:03:09 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 04 Jul 2023 03:03:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 04 Jul 2023 03:03:13 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:13 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 04 Jul 2023 03:03:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3e06c4413e69400a792d7a95cad6d643afdbcdc2f28fdd90e603e2f22e33a7`  
		Last Modified: Tue, 04 Jul 2023 03:03:53 GMT  
		Size: 40.1 MB (40079874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab794d03683cd2393608f40731e4c588dbc7661668e884227ec782c7011921`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:b98a8a1b72c69e886e4ff26748286a7c4849717064fc9fdb42b2d86d4024dedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:2b2cf3af1e1fdc946d0400e6ef8bc3f2754ddb861f739c78360c3d39cb253746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8154d287a0cd41ae6f26959af0d5aa9adf0e765d9f5940eae3fde58c3aab944`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 13 Jun 2023 04:05:14 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 13 Jun 2023 04:05:14 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 13 Jun 2023 04:05:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Jun 2023 04:05:19 GMT
WORKDIR /opt/emqx
# Tue, 13 Jun 2023 04:05:19 GMT
USER emqx
# Tue, 13 Jun 2023 04:05:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jun 2023 04:05:19 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Jun 2023 04:05:19 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Jun 2023 04:05:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:05:20 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11ad7fd953a334956026fc08b55abb1625fbaad5c2540a1d531ed566da6f031`  
		Last Modified: Tue, 13 Jun 2023 04:05:47 GMT  
		Size: 2.6 MB (2569638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105da9fef63b5bef345d47ed904190ccb2362f38449341ce80b93b5b72941db`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f883bad9be8bf6dd4cc27edca3cca8ee64f80b3afadab702283823b30d8b01`  
		Last Modified: Tue, 13 Jun 2023 04:05:51 GMT  
		Size: 47.3 MB (47298222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45046c6a3a747679abb1bffe6cd4755e04900a76a30a5369f1ef54700f63440e`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2d08ee2bc416b6f69851a687377881c076764d6010794177a34c576f405d0eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ef632180b6d12a52f16c392ec17886bc0626d84ec46d8a7d1f71cea9b85a0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 04 Jul 2023 03:03:08 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 04 Jul 2023 03:03:09 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 04 Jul 2023 03:03:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 04 Jul 2023 03:03:13 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:13 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 04 Jul 2023 03:03:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3e06c4413e69400a792d7a95cad6d643afdbcdc2f28fdd90e603e2f22e33a7`  
		Last Modified: Tue, 04 Jul 2023 03:03:53 GMT  
		Size: 40.1 MB (40079874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab794d03683cd2393608f40731e4c588dbc7661668e884227ec782c7011921`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.18`

```console
$ docker pull emqx@sha256:b98a8a1b72c69e886e4ff26748286a7c4849717064fc9fdb42b2d86d4024dedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.18` - linux; amd64

```console
$ docker pull emqx@sha256:2b2cf3af1e1fdc946d0400e6ef8bc3f2754ddb861f739c78360c3d39cb253746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81290481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8154d287a0cd41ae6f26959af0d5aa9adf0e765d9f5940eae3fde58c3aab944`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 13 Jun 2023 04:05:14 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 13 Jun 2023 04:05:14 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 13 Jun 2023 04:05:19 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Jun 2023 04:05:19 GMT
WORKDIR /opt/emqx
# Tue, 13 Jun 2023 04:05:19 GMT
USER emqx
# Tue, 13 Jun 2023 04:05:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jun 2023 04:05:19 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Jun 2023 04:05:19 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Jun 2023 04:05:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:05:20 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11ad7fd953a334956026fc08b55abb1625fbaad5c2540a1d531ed566da6f031`  
		Last Modified: Tue, 13 Jun 2023 04:05:47 GMT  
		Size: 2.6 MB (2569638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105da9fef63b5bef345d47ed904190ccb2362f38449341ce80b93b5b72941db`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f883bad9be8bf6dd4cc27edca3cca8ee64f80b3afadab702283823b30d8b01`  
		Last Modified: Tue, 13 Jun 2023 04:05:51 GMT  
		Size: 47.3 MB (47298222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45046c6a3a747679abb1bffe6cd4755e04900a76a30a5369f1ef54700f63440e`  
		Last Modified: Tue, 13 Jun 2023 04:05:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.18` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2d08ee2bc416b6f69851a687377881c076764d6010794177a34c576f405d0eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ef632180b6d12a52f16c392ec17886bc0626d84ec46d8a7d1f71cea9b85a0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 04 Jul 2023 03:03:08 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 04 Jul 2023 03:03:09 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 04 Jul 2023 03:03:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 04 Jul 2023 03:03:13 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:13 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 04 Jul 2023 03:03:13 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:13 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1428b80937a0eb55c8466779cec4bcf7e31bdcc4fc66b763448cf9d131563`  
		Last Modified: Tue, 04 Jul 2023 03:03:50 GMT  
		Size: 2.6 MB (2559426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa00861c721843ae490a68a90f1db04218b5131cb6b2d6d39618973618f3da3`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3e06c4413e69400a792d7a95cad6d643afdbcdc2f28fdd90e603e2f22e33a7`  
		Last Modified: Tue, 04 Jul 2023 03:03:53 GMT  
		Size: 40.1 MB (40079874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab794d03683cd2393608f40731e4c588dbc7661668e884227ec782c7011921`  
		Last Modified: Tue, 04 Jul 2023 03:03:49 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:0103b6a5e4ea92fbf2529addb640dfcb1a412f2cf071d7dbc76ce9fe97532971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:507df4a6496d9db8803e8886edc3d9249581a12854bd5cfde319c72d51253411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103466216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c982c09d0d71f294aafb75366f9f6735d4f9fe8f32a4c3544ebbe220ae7a10f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 22 Jun 2023 22:41:55 GMT
ENV EMQX_VERSION=5.1.0
# Thu, 22 Jun 2023 22:41:55 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Thu, 22 Jun 2023 22:41:55 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Thu, 22 Jun 2023 22:41:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 22 Jun 2023 22:42:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 22 Jun 2023 22:42:02 GMT
WORKDIR /opt/emqx
# Thu, 22 Jun 2023 22:42:02 GMT
USER emqx
# Thu, 22 Jun 2023 22:42:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 22 Jun 2023 22:42:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 22 Jun 2023 22:42:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 22 Jun 2023 22:42:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 22 Jun 2023 22:42:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a56c0e56b2868b33d9c586817640350cb7cb942ca0d60deb66172f8f0ed22`  
		Last Modified: Thu, 22 Jun 2023 22:42:26 GMT  
		Size: 69.1 MB (69056006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb39c1343b6364d862612ee8268379a05384438048f685f0eded1372ccf5368`  
		Last Modified: Thu, 22 Jun 2023 22:42:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4148afe49e12dc03200209413840898e99aa03b8f5f5bfec85cf44019656642a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93775506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb850920403a69a76452c79aa52766dcb4dbc5c7a8940c2ce4a284a346d2e8b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:33 GMT
ENV EMQX_VERSION=5.1.0
# Tue, 04 Jul 2023 03:03:33 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Tue, 04 Jul 2023 03:03:33 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Tue, 04 Jul 2023 03:03:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:39 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:39 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0ee34f24505f117510ea59fbcce761b0774efa37d970225c044ea801563ef`  
		Last Modified: Tue, 04 Jul 2023 03:04:21 GMT  
		Size: 60.7 MB (60704464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f314df5ec7d54820af1b65139f593fc8c59095734ef557f9116c1a8b42d5ba60`  
		Last Modified: Tue, 04 Jul 2023 03:04:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:b4d82e3633cd8ff740a39cef470bad4609174d3f7efa83b08a5757a93085e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:4c35e0bc1118239811e974dd383eaf13b5c30b80153e0e25ee31aa2d31ead0c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681380b29d8df286b720c20311cc02e83da157bb835b04c42dcda0fd19a43678`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Jun 2023 04:05:28 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 13 Jun 2023 04:05:28 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 13 Jun 2023 04:05:28 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 13 Jun 2023 04:05:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jun 2023 04:05:35 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 13 Jun 2023 04:05:36 GMT
WORKDIR /opt/emqx
# Tue, 13 Jun 2023 04:05:36 GMT
USER emqx
# Tue, 13 Jun 2023 04:05:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jun 2023 04:05:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Jun 2023 04:05:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Jun 2023 04:05:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:05:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297da6d562816a699128e55188d4be62568f5c6d786f78ff6b3241b7338f53cb`  
		Last Modified: Tue, 13 Jun 2023 04:06:08 GMT  
		Size: 67.6 MB (67571866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e7afe3bef593b419b59bbbaff2dabe2a6302a3dc415f0c9599c0e5ec731dee`  
		Last Modified: Tue, 13 Jun 2023 04:06:00 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0abdd21e8a6b3206455cb733eca21c22695b7dc06a98d3a4de5eb999537b0195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db90f1f3fab83ce999d6472a64971ca463afb82097d6b4cdb5da98a3c2f28c0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:22 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 04 Jul 2023 03:03:22 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 04 Jul 2023 03:03:22 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 04 Jul 2023 03:03:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:28 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf20fcfbb7660480c1e5425d2d670e3fc48e00264da9d9a5b0eb282e2472df6`  
		Last Modified: Tue, 04 Jul 2023 03:04:08 GMT  
		Size: 60.0 MB (59989394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03deeecf9242891f89e9ebbde2e0197c04be91ee39569bfcd63a6a3336b20801`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:b4d82e3633cd8ff740a39cef470bad4609174d3f7efa83b08a5757a93085e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:4c35e0bc1118239811e974dd383eaf13b5c30b80153e0e25ee31aa2d31ead0c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681380b29d8df286b720c20311cc02e83da157bb835b04c42dcda0fd19a43678`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Jun 2023 04:05:28 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 13 Jun 2023 04:05:28 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 13 Jun 2023 04:05:28 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 13 Jun 2023 04:05:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jun 2023 04:05:35 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 13 Jun 2023 04:05:36 GMT
WORKDIR /opt/emqx
# Tue, 13 Jun 2023 04:05:36 GMT
USER emqx
# Tue, 13 Jun 2023 04:05:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jun 2023 04:05:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Jun 2023 04:05:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Jun 2023 04:05:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:05:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297da6d562816a699128e55188d4be62568f5c6d786f78ff6b3241b7338f53cb`  
		Last Modified: Tue, 13 Jun 2023 04:06:08 GMT  
		Size: 67.6 MB (67571866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e7afe3bef593b419b59bbbaff2dabe2a6302a3dc415f0c9599c0e5ec731dee`  
		Last Modified: Tue, 13 Jun 2023 04:06:00 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0abdd21e8a6b3206455cb733eca21c22695b7dc06a98d3a4de5eb999537b0195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db90f1f3fab83ce999d6472a64971ca463afb82097d6b4cdb5da98a3c2f28c0d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:22 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 04 Jul 2023 03:03:22 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 04 Jul 2023 03:03:22 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 04 Jul 2023 03:03:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:28 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf20fcfbb7660480c1e5425d2d670e3fc48e00264da9d9a5b0eb282e2472df6`  
		Last Modified: Tue, 04 Jul 2023 03:04:08 GMT  
		Size: 60.0 MB (59989394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03deeecf9242891f89e9ebbde2e0197c04be91ee39569bfcd63a6a3336b20801`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:0103b6a5e4ea92fbf2529addb640dfcb1a412f2cf071d7dbc76ce9fe97532971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:507df4a6496d9db8803e8886edc3d9249581a12854bd5cfde319c72d51253411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103466216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c982c09d0d71f294aafb75366f9f6735d4f9fe8f32a4c3544ebbe220ae7a10f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 22 Jun 2023 22:41:55 GMT
ENV EMQX_VERSION=5.1.0
# Thu, 22 Jun 2023 22:41:55 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Thu, 22 Jun 2023 22:41:55 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Thu, 22 Jun 2023 22:41:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 22 Jun 2023 22:42:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 22 Jun 2023 22:42:02 GMT
WORKDIR /opt/emqx
# Thu, 22 Jun 2023 22:42:02 GMT
USER emqx
# Thu, 22 Jun 2023 22:42:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 22 Jun 2023 22:42:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 22 Jun 2023 22:42:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 22 Jun 2023 22:42:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 22 Jun 2023 22:42:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a56c0e56b2868b33d9c586817640350cb7cb942ca0d60deb66172f8f0ed22`  
		Last Modified: Thu, 22 Jun 2023 22:42:26 GMT  
		Size: 69.1 MB (69056006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb39c1343b6364d862612ee8268379a05384438048f685f0eded1372ccf5368`  
		Last Modified: Thu, 22 Jun 2023 22:42:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4148afe49e12dc03200209413840898e99aa03b8f5f5bfec85cf44019656642a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93775506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb850920403a69a76452c79aa52766dcb4dbc5c7a8940c2ce4a284a346d2e8b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:33 GMT
ENV EMQX_VERSION=5.1.0
# Tue, 04 Jul 2023 03:03:33 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Tue, 04 Jul 2023 03:03:33 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Tue, 04 Jul 2023 03:03:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:39 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:39 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0ee34f24505f117510ea59fbcce761b0774efa37d970225c044ea801563ef`  
		Last Modified: Tue, 04 Jul 2023 03:04:21 GMT  
		Size: 60.7 MB (60704464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f314df5ec7d54820af1b65139f593fc8c59095734ef557f9116c1a8b42d5ba60`  
		Last Modified: Tue, 04 Jul 2023 03:04:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.0`

```console
$ docker pull emqx@sha256:0103b6a5e4ea92fbf2529addb640dfcb1a412f2cf071d7dbc76ce9fe97532971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.0` - linux; amd64

```console
$ docker pull emqx@sha256:507df4a6496d9db8803e8886edc3d9249581a12854bd5cfde319c72d51253411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103466216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c982c09d0d71f294aafb75366f9f6735d4f9fe8f32a4c3544ebbe220ae7a10f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 22 Jun 2023 22:41:55 GMT
ENV EMQX_VERSION=5.1.0
# Thu, 22 Jun 2023 22:41:55 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Thu, 22 Jun 2023 22:41:55 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Thu, 22 Jun 2023 22:41:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 22 Jun 2023 22:42:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 22 Jun 2023 22:42:02 GMT
WORKDIR /opt/emqx
# Thu, 22 Jun 2023 22:42:02 GMT
USER emqx
# Thu, 22 Jun 2023 22:42:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 22 Jun 2023 22:42:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 22 Jun 2023 22:42:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 22 Jun 2023 22:42:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 22 Jun 2023 22:42:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a56c0e56b2868b33d9c586817640350cb7cb942ca0d60deb66172f8f0ed22`  
		Last Modified: Thu, 22 Jun 2023 22:42:26 GMT  
		Size: 69.1 MB (69056006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb39c1343b6364d862612ee8268379a05384438048f685f0eded1372ccf5368`  
		Last Modified: Thu, 22 Jun 2023 22:42:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4148afe49e12dc03200209413840898e99aa03b8f5f5bfec85cf44019656642a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93775506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb850920403a69a76452c79aa52766dcb4dbc5c7a8940c2ce4a284a346d2e8b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:33 GMT
ENV EMQX_VERSION=5.1.0
# Tue, 04 Jul 2023 03:03:33 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Tue, 04 Jul 2023 03:03:33 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Tue, 04 Jul 2023 03:03:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:39 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:39 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0ee34f24505f117510ea59fbcce761b0774efa37d970225c044ea801563ef`  
		Last Modified: Tue, 04 Jul 2023 03:04:21 GMT  
		Size: 60.7 MB (60704464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f314df5ec7d54820af1b65139f593fc8c59095734ef557f9116c1a8b42d5ba60`  
		Last Modified: Tue, 04 Jul 2023 03:04:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:0103b6a5e4ea92fbf2529addb640dfcb1a412f2cf071d7dbc76ce9fe97532971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:507df4a6496d9db8803e8886edc3d9249581a12854bd5cfde319c72d51253411
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103466216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c982c09d0d71f294aafb75366f9f6735d4f9fe8f32a4c3544ebbe220ae7a10f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:05:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:05:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 22 Jun 2023 22:41:55 GMT
ENV EMQX_VERSION=5.1.0
# Thu, 22 Jun 2023 22:41:55 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Thu, 22 Jun 2023 22:41:55 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Thu, 22 Jun 2023 22:41:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 22 Jun 2023 22:42:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 22 Jun 2023 22:42:02 GMT
WORKDIR /opt/emqx
# Thu, 22 Jun 2023 22:42:02 GMT
USER emqx
# Thu, 22 Jun 2023 22:42:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 22 Jun 2023 22:42:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 22 Jun 2023 22:42:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 22 Jun 2023 22:42:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 22 Jun 2023 22:42:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455449c3836673343cfe4a251856a028b9edb7faf316b905d1414568c13634c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 3.0 MB (2987797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e966bf28b5d866b8ef51054ae90093f7819a1ed717f5918ae5fbcbfd8b16a4c`  
		Last Modified: Tue, 13 Jun 2023 04:06:01 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883a56c0e56b2868b33d9c586817640350cb7cb942ca0d60deb66172f8f0ed22`  
		Last Modified: Thu, 22 Jun 2023 22:42:26 GMT  
		Size: 69.1 MB (69056006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb39c1343b6364d862612ee8268379a05384438048f685f0eded1372ccf5368`  
		Last Modified: Thu, 22 Jun 2023 22:42:18 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4148afe49e12dc03200209413840898e99aa03b8f5f5bfec85cf44019656642a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93775506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb850920403a69a76452c79aa52766dcb4dbc5c7a8940c2ce4a284a346d2e8b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:03:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:03:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 04 Jul 2023 03:03:33 GMT
ENV EMQX_VERSION=5.1.0
# Tue, 04 Jul 2023 03:03:33 GMT
ENV AMD64_SHA256=946d8a047c8863afa318abf41be4c265c205d86aa8e6401a39282f02eecbe481
# Tue, 04 Jul 2023 03:03:33 GMT
ENV ARM64_SHA256=9f9ffa019960a6d4a6d60ec0b0f7a45513e326df7667a166aef827d248054940
# Tue, 04 Jul 2023 03:03:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Jul 2023 03:03:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 04 Jul 2023 03:03:39 GMT
WORKDIR /opt/emqx
# Tue, 04 Jul 2023 03:03:39 GMT
USER emqx
# Tue, 04 Jul 2023 03:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Jul 2023 03:03:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 04 Jul 2023 03:03:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 04 Jul 2023 03:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:03:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc212c7c7d61e498e2041ef1be251acbca34483d513266fc40c2b0d41721f61`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 3.0 MB (3003072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aca2cf657bb3bfb3bf3c6675087076999f1bd3e64ffbe99a129c8475d7795`  
		Last Modified: Tue, 04 Jul 2023 03:04:03 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb0ee34f24505f117510ea59fbcce761b0774efa37d970225c044ea801563ef`  
		Last Modified: Tue, 04 Jul 2023 03:04:21 GMT  
		Size: 60.7 MB (60704464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f314df5ec7d54820af1b65139f593fc8c59095734ef557f9116c1a8b42d5ba60`  
		Last Modified: Tue, 04 Jul 2023 03:04:16 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
