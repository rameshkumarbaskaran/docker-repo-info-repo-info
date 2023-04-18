<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.17`](#emqx4417)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.23`](#emqx5023)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:3193e36deb1608511904693ff16bbb279ffec8ff0795ac5756b1a3d35ac874a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:777be2ec320c0448e8d4c79dcade7501ae98cf53f256d973f4faa47150d748b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81279221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02879c1b8ec47f99da6f309c6b0b829c3256e60f997d0cb2905851085fde7047`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 12 Apr 2023 00:42:35 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 12 Apr 2023 00:42:35 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 12 Apr 2023 00:42:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 12 Apr 2023 00:42:40 GMT
WORKDIR /opt/emqx
# Wed, 12 Apr 2023 00:42:41 GMT
USER emqx
# Wed, 12 Apr 2023 00:42:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 12 Apr 2023 00:42:41 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 12 Apr 2023 00:42:41 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 12 Apr 2023 00:42:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 00:42:41 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901aaad2c36dc10a256fae9d94810d0bcd1d3732eb3e172f7d18eba970956df`  
		Last Modified: Wed, 12 Apr 2023 00:43:09 GMT  
		Size: 2.6 MB (2569627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f607aa293305bd4722109d3b17853a91b8de9754b42fe37d71be6cf3c9abb42`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d76c9e6de33b4e4930f490339f65388845be0f45ac8c927caa21f8284e91968`  
		Last Modified: Wed, 12 Apr 2023 00:43:13 GMT  
		Size: 47.3 MB (47286153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982eabc32ac02081fb30fb30af3b0b9098324072276786bfe38338b79409aa87`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a6f997e81d50a04ba433686109a70031148c52a8ee5768605ad468eec8fb07d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a7ba17574b3be0da7935a562b2a553595666a86c3b0441689024fe6b5e1d4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 18 Apr 2023 18:39:23 GMT
ENV EMQX_VERSION=4.4.17
# Tue, 18 Apr 2023 18:39:23 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 18 Apr 2023 18:39:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b078cfe835799485748a4d31b4af2a4f7bc696da8f64e22662b46a95bfec74af"; fi;     if [ ${arch} = "arm64" ]; then sha256="4d2cc9d908490d3ba5f6d2d53e0280dee0753783f78f8e6701e5d5c9550e75f4"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 18 Apr 2023 18:39:27 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:27 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:27 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 18 Apr 2023 18:39:27 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4322e90f757b16a8adb2d40ade499d3006e85ca6d83f0eb96ea9691b6871dd`  
		Last Modified: Wed, 12 Apr 2023 01:38:39 GMT  
		Size: 2.6 MB (2559482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071e2b66079e6214608516ff2e6a436738f7da65ae6bb2c5357edcfb8d54a78`  
		Last Modified: Wed, 12 Apr 2023 01:38:38 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b037587ac726ae947e23c5a90c1b664d676bc4ed966e8824782fbb0a43de2`  
		Last Modified: Tue, 18 Apr 2023 18:39:49 GMT  
		Size: 40.1 MB (40079345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecd1cab1d85ea166bf8809c679d6df88f9e1aaa7fcdea562997208abeb7e175`  
		Last Modified: Tue, 18 Apr 2023 18:39:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:3193e36deb1608511904693ff16bbb279ffec8ff0795ac5756b1a3d35ac874a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:777be2ec320c0448e8d4c79dcade7501ae98cf53f256d973f4faa47150d748b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81279221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02879c1b8ec47f99da6f309c6b0b829c3256e60f997d0cb2905851085fde7047`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 12 Apr 2023 00:42:35 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 12 Apr 2023 00:42:35 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 12 Apr 2023 00:42:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 12 Apr 2023 00:42:40 GMT
WORKDIR /opt/emqx
# Wed, 12 Apr 2023 00:42:41 GMT
USER emqx
# Wed, 12 Apr 2023 00:42:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 12 Apr 2023 00:42:41 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 12 Apr 2023 00:42:41 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 12 Apr 2023 00:42:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 00:42:41 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901aaad2c36dc10a256fae9d94810d0bcd1d3732eb3e172f7d18eba970956df`  
		Last Modified: Wed, 12 Apr 2023 00:43:09 GMT  
		Size: 2.6 MB (2569627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f607aa293305bd4722109d3b17853a91b8de9754b42fe37d71be6cf3c9abb42`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d76c9e6de33b4e4930f490339f65388845be0f45ac8c927caa21f8284e91968`  
		Last Modified: Wed, 12 Apr 2023 00:43:13 GMT  
		Size: 47.3 MB (47286153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982eabc32ac02081fb30fb30af3b0b9098324072276786bfe38338b79409aa87`  
		Last Modified: Wed, 12 Apr 2023 00:43:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a6f997e81d50a04ba433686109a70031148c52a8ee5768605ad468eec8fb07d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a7ba17574b3be0da7935a562b2a553595666a86c3b0441689024fe6b5e1d4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 18 Apr 2023 18:39:23 GMT
ENV EMQX_VERSION=4.4.17
# Tue, 18 Apr 2023 18:39:23 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 18 Apr 2023 18:39:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b078cfe835799485748a4d31b4af2a4f7bc696da8f64e22662b46a95bfec74af"; fi;     if [ ${arch} = "arm64" ]; then sha256="4d2cc9d908490d3ba5f6d2d53e0280dee0753783f78f8e6701e5d5c9550e75f4"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 18 Apr 2023 18:39:27 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:27 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:27 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 18 Apr 2023 18:39:27 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4322e90f757b16a8adb2d40ade499d3006e85ca6d83f0eb96ea9691b6871dd`  
		Last Modified: Wed, 12 Apr 2023 01:38:39 GMT  
		Size: 2.6 MB (2559482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071e2b66079e6214608516ff2e6a436738f7da65ae6bb2c5357edcfb8d54a78`  
		Last Modified: Wed, 12 Apr 2023 01:38:38 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b037587ac726ae947e23c5a90c1b664d676bc4ed966e8824782fbb0a43de2`  
		Last Modified: Tue, 18 Apr 2023 18:39:49 GMT  
		Size: 40.1 MB (40079345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecd1cab1d85ea166bf8809c679d6df88f9e1aaa7fcdea562997208abeb7e175`  
		Last Modified: Tue, 18 Apr 2023 18:39:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.17`

```console
$ docker pull emqx@sha256:17135e47d44de7842503a45aa253dfc34a8d8bc38cfa02b8338529eb797b1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `emqx:4.4.17` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a6f997e81d50a04ba433686109a70031148c52a8ee5768605ad468eec8fb07d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a7ba17574b3be0da7935a562b2a553595666a86c3b0441689024fe6b5e1d4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:12 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 18 Apr 2023 18:39:23 GMT
ENV EMQX_VERSION=4.4.17
# Tue, 18 Apr 2023 18:39:23 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 18 Apr 2023 18:39:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="b078cfe835799485748a4d31b4af2a4f7bc696da8f64e22662b46a95bfec74af"; fi;     if [ ${arch} = "arm64" ]; then sha256="4d2cc9d908490d3ba5f6d2d53e0280dee0753783f78f8e6701e5d5c9550e75f4"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 18 Apr 2023 18:39:27 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:27 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:27 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 18 Apr 2023 18:39:27 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4322e90f757b16a8adb2d40ade499d3006e85ca6d83f0eb96ea9691b6871dd`  
		Last Modified: Wed, 12 Apr 2023 01:38:39 GMT  
		Size: 2.6 MB (2559482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071e2b66079e6214608516ff2e6a436738f7da65ae6bb2c5357edcfb8d54a78`  
		Last Modified: Wed, 12 Apr 2023 01:38:38 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b037587ac726ae947e23c5a90c1b664d676bc4ed966e8824782fbb0a43de2`  
		Last Modified: Tue, 18 Apr 2023 18:39:49 GMT  
		Size: 40.1 MB (40079345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecd1cab1d85ea166bf8809c679d6df88f9e1aaa7fcdea562997208abeb7e175`  
		Last Modified: Tue, 18 Apr 2023 18:39:46 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:99a351198514a4c2be6905894236b6d93dbbf6878373c8e22015ca07ee213b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:9999ce104c5ff47fba3a29088e6449d368b589cb65cd44cd1cddf645f89239ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101479847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3901154fdd9011592b8783aa81e2ef5ea7196e52f4033569359c473317229d2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 14 Apr 2023 21:33:21 GMT
ENV EMQX_VERSION=5.0.22
# Fri, 14 Apr 2023 21:33:21 GMT
ENV AMD64_SHA256=f0cdf5da8daf1ba8c2fc12cd7b8aa7e7c084beb62874ac8f4892a03ec6590eaa
# Fri, 14 Apr 2023 21:33:21 GMT
ENV ARM64_SHA256=45ec8810a4d8e3a4ef4ce472a63f8cd7e4676af827989633429007e209c824fe
# Fri, 14 Apr 2023 21:33:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 14 Apr 2023 21:33:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 14 Apr 2023 21:33:27 GMT
WORKDIR /opt/emqx
# Fri, 14 Apr 2023 21:33:27 GMT
USER emqx
# Fri, 14 Apr 2023 21:33:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 14 Apr 2023 21:33:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 14 Apr 2023 21:33:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 14 Apr 2023 21:33:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 14 Apr 2023 21:33:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729b9c39b4f15a7e64f7c885e5c1212726c05149cc47a8fd8856af3d95b1be84`  
		Last Modified: Fri, 14 Apr 2023 21:33:46 GMT  
		Size: 67.1 MB (67068786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca89e9afab43ebadcbafbe65f3ede47d5c72cf8fcd7b06942b9048580ff18d`  
		Last Modified: Fri, 14 Apr 2023 21:33:39 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b20b0908ec021f4ec179fd55b0b1fd1ad2573dfa23b060e333fb695394a561ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bae0c81f826ed909247451fba3ee3518fb415381812dcbbf2209b9d24d3795`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 18 Apr 2023 18:39:29 GMT
ENV EMQX_VERSION=5.0.23
# Tue, 18 Apr 2023 18:39:29 GMT
ENV AMD64_SHA256=66322a18c2c1677d9ee07f44d06410d8b3914782f7b56dceb67c44ab946bc8bd
# Tue, 18 Apr 2023 18:39:29 GMT
ENV ARM64_SHA256=74c0f096fbd8b480f79b45918de83148ba0c1defcf997f268557ed27f85d9159
# Tue, 18 Apr 2023 18:39:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Apr 2023 18:39:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 18 Apr 2023 18:39:35 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:35 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 18 Apr 2023 18:39:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b64e3be9abc32d122bd4b9c6cbdc2adc75085b08f7644acbd1e9a963977cd48`  
		Last Modified: Wed, 12 Apr 2023 01:38:53 GMT  
		Size: 3.0 MB (3002944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b665badbe1ecc88ea2bdc4962042f6412551d166e4bc0bfbfcd3e00d159e605`  
		Last Modified: Wed, 12 Apr 2023 01:38:52 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81826c36e478507e264f8473188bd6a67787268ae42d90ed3468e89afd28f271`  
		Last Modified: Tue, 18 Apr 2023 18:40:06 GMT  
		Size: 69.1 MB (69086004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb58189c390f19b6def2d0a892c2211334d48973166ef7574b3ccb3e5f1f24f0`  
		Last Modified: Tue, 18 Apr 2023 18:39:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:99a351198514a4c2be6905894236b6d93dbbf6878373c8e22015ca07ee213b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:9999ce104c5ff47fba3a29088e6449d368b589cb65cd44cd1cddf645f89239ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101479847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3901154fdd9011592b8783aa81e2ef5ea7196e52f4033569359c473317229d2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 14 Apr 2023 21:33:21 GMT
ENV EMQX_VERSION=5.0.22
# Fri, 14 Apr 2023 21:33:21 GMT
ENV AMD64_SHA256=f0cdf5da8daf1ba8c2fc12cd7b8aa7e7c084beb62874ac8f4892a03ec6590eaa
# Fri, 14 Apr 2023 21:33:21 GMT
ENV ARM64_SHA256=45ec8810a4d8e3a4ef4ce472a63f8cd7e4676af827989633429007e209c824fe
# Fri, 14 Apr 2023 21:33:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 14 Apr 2023 21:33:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 14 Apr 2023 21:33:27 GMT
WORKDIR /opt/emqx
# Fri, 14 Apr 2023 21:33:27 GMT
USER emqx
# Fri, 14 Apr 2023 21:33:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 14 Apr 2023 21:33:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 14 Apr 2023 21:33:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 14 Apr 2023 21:33:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 14 Apr 2023 21:33:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729b9c39b4f15a7e64f7c885e5c1212726c05149cc47a8fd8856af3d95b1be84`  
		Last Modified: Fri, 14 Apr 2023 21:33:46 GMT  
		Size: 67.1 MB (67068786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca89e9afab43ebadcbafbe65f3ede47d5c72cf8fcd7b06942b9048580ff18d`  
		Last Modified: Fri, 14 Apr 2023 21:33:39 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b20b0908ec021f4ec179fd55b0b1fd1ad2573dfa23b060e333fb695394a561ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bae0c81f826ed909247451fba3ee3518fb415381812dcbbf2209b9d24d3795`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 18 Apr 2023 18:39:29 GMT
ENV EMQX_VERSION=5.0.23
# Tue, 18 Apr 2023 18:39:29 GMT
ENV AMD64_SHA256=66322a18c2c1677d9ee07f44d06410d8b3914782f7b56dceb67c44ab946bc8bd
# Tue, 18 Apr 2023 18:39:29 GMT
ENV ARM64_SHA256=74c0f096fbd8b480f79b45918de83148ba0c1defcf997f268557ed27f85d9159
# Tue, 18 Apr 2023 18:39:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Apr 2023 18:39:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 18 Apr 2023 18:39:35 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:35 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 18 Apr 2023 18:39:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b64e3be9abc32d122bd4b9c6cbdc2adc75085b08f7644acbd1e9a963977cd48`  
		Last Modified: Wed, 12 Apr 2023 01:38:53 GMT  
		Size: 3.0 MB (3002944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b665badbe1ecc88ea2bdc4962042f6412551d166e4bc0bfbfcd3e00d159e605`  
		Last Modified: Wed, 12 Apr 2023 01:38:52 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81826c36e478507e264f8473188bd6a67787268ae42d90ed3468e89afd28f271`  
		Last Modified: Tue, 18 Apr 2023 18:40:06 GMT  
		Size: 69.1 MB (69086004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb58189c390f19b6def2d0a892c2211334d48973166ef7574b3ccb3e5f1f24f0`  
		Last Modified: Tue, 18 Apr 2023 18:39:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.23`

```console
$ docker pull emqx@sha256:5631823628adb39b541bf6cf27a817a68c56ac63f3bc0b6d9a73e9fd6e90d927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `emqx:5.0.23` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b20b0908ec021f4ec179fd55b0b1fd1ad2573dfa23b060e333fb695394a561ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bae0c81f826ed909247451fba3ee3518fb415381812dcbbf2209b9d24d3795`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 18 Apr 2023 18:39:29 GMT
ENV EMQX_VERSION=5.0.23
# Tue, 18 Apr 2023 18:39:29 GMT
ENV AMD64_SHA256=66322a18c2c1677d9ee07f44d06410d8b3914782f7b56dceb67c44ab946bc8bd
# Tue, 18 Apr 2023 18:39:29 GMT
ENV ARM64_SHA256=74c0f096fbd8b480f79b45918de83148ba0c1defcf997f268557ed27f85d9159
# Tue, 18 Apr 2023 18:39:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Apr 2023 18:39:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 18 Apr 2023 18:39:35 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:35 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 18 Apr 2023 18:39:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b64e3be9abc32d122bd4b9c6cbdc2adc75085b08f7644acbd1e9a963977cd48`  
		Last Modified: Wed, 12 Apr 2023 01:38:53 GMT  
		Size: 3.0 MB (3002944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b665badbe1ecc88ea2bdc4962042f6412551d166e4bc0bfbfcd3e00d159e605`  
		Last Modified: Wed, 12 Apr 2023 01:38:52 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81826c36e478507e264f8473188bd6a67787268ae42d90ed3468e89afd28f271`  
		Last Modified: Tue, 18 Apr 2023 18:40:06 GMT  
		Size: 69.1 MB (69086004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb58189c390f19b6def2d0a892c2211334d48973166ef7574b3ccb3e5f1f24f0`  
		Last Modified: Tue, 18 Apr 2023 18:39:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:99a351198514a4c2be6905894236b6d93dbbf6878373c8e22015ca07ee213b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:9999ce104c5ff47fba3a29088e6449d368b589cb65cd44cd1cddf645f89239ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101479847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3901154fdd9011592b8783aa81e2ef5ea7196e52f4033569359c473317229d2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:42:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:42:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 14 Apr 2023 21:33:21 GMT
ENV EMQX_VERSION=5.0.22
# Fri, 14 Apr 2023 21:33:21 GMT
ENV AMD64_SHA256=f0cdf5da8daf1ba8c2fc12cd7b8aa7e7c084beb62874ac8f4892a03ec6590eaa
# Fri, 14 Apr 2023 21:33:21 GMT
ENV ARM64_SHA256=45ec8810a4d8e3a4ef4ce472a63f8cd7e4676af827989633429007e209c824fe
# Fri, 14 Apr 2023 21:33:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 14 Apr 2023 21:33:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 14 Apr 2023 21:33:27 GMT
WORKDIR /opt/emqx
# Fri, 14 Apr 2023 21:33:27 GMT
USER emqx
# Fri, 14 Apr 2023 21:33:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 14 Apr 2023 21:33:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 14 Apr 2023 21:33:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 14 Apr 2023 21:33:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 14 Apr 2023 21:33:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f79c821cbd23fa1420033390e2828e0922b8efe06687c960eb7ff40edfbd0d6`  
		Last Modified: Wed, 12 Apr 2023 00:43:23 GMT  
		Size: 3.0 MB (2987825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048c1bdd86f15f4d429d049f898a2d3c0f0732c5b7e68a31b824acae055655d8`  
		Last Modified: Wed, 12 Apr 2023 00:43:22 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729b9c39b4f15a7e64f7c885e5c1212726c05149cc47a8fd8856af3d95b1be84`  
		Last Modified: Fri, 14 Apr 2023 21:33:46 GMT  
		Size: 67.1 MB (67068786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ca89e9afab43ebadcbafbe65f3ede47d5c72cf8fcd7b06942b9048580ff18d`  
		Last Modified: Fri, 14 Apr 2023 21:33:39 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b20b0908ec021f4ec179fd55b0b1fd1ad2573dfa23b060e333fb695394a561ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bae0c81f826ed909247451fba3ee3518fb415381812dcbbf2209b9d24d3795`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:38:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:38:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 18 Apr 2023 18:39:29 GMT
ENV EMQX_VERSION=5.0.23
# Tue, 18 Apr 2023 18:39:29 GMT
ENV AMD64_SHA256=66322a18c2c1677d9ee07f44d06410d8b3914782f7b56dceb67c44ab946bc8bd
# Tue, 18 Apr 2023 18:39:29 GMT
ENV ARM64_SHA256=74c0f096fbd8b480f79b45918de83148ba0c1defcf997f268557ed27f85d9159
# Tue, 18 Apr 2023 18:39:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Apr 2023 18:39:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 18 Apr 2023 18:39:35 GMT
WORKDIR /opt/emqx
# Tue, 18 Apr 2023 18:39:35 GMT
USER emqx
# Tue, 18 Apr 2023 18:39:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Apr 2023 18:39:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 18 Apr 2023 18:39:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 18 Apr 2023 18:39:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Apr 2023 18:39:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b64e3be9abc32d122bd4b9c6cbdc2adc75085b08f7644acbd1e9a963977cd48`  
		Last Modified: Wed, 12 Apr 2023 01:38:53 GMT  
		Size: 3.0 MB (3002944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b665badbe1ecc88ea2bdc4962042f6412551d166e4bc0bfbfcd3e00d159e605`  
		Last Modified: Wed, 12 Apr 2023 01:38:52 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81826c36e478507e264f8473188bd6a67787268ae42d90ed3468e89afd28f271`  
		Last Modified: Tue, 18 Apr 2023 18:40:06 GMT  
		Size: 69.1 MB (69086004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb58189c390f19b6def2d0a892c2211334d48973166ef7574b3ccb3e5f1f24f0`  
		Last Modified: Tue, 18 Apr 2023 18:39:59 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
