<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.22`](#emqx4322)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.11`](#emqx4411)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.11`](#emqx5011)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:deeaeddbaec3e481653ff6c7e490cad2074cdc1f8100b0049ce768291ad8f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:2d23dcc574f9f82154d041a3c9c213f4a7aac829887c5f5104108d4f5b07dee7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127238717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd4b6b7c15dd9777f6d2732b818378ba7e4ac8551f8c4341e9540def0d6b71e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:03:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:51 GMT
ENV EMQX_VERSION=4.4.11
# Tue, 06 Dec 2022 04:03:51 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 06 Dec 2022 04:03:55 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 06 Dec 2022 04:04:01 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:02 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 06 Dec 2022 04:04:02 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:02 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3078ffce5d90ff48d82f12269ab8ab64696808bbda5c548acf2699549e57a18`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 2.6 MB (2571021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00655aeabee69f96756e1946695715aa34d796b40f41401330e62d17227c9720`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 46.6 MB (46617891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a34fe9ad4c37e86ba5473a44e9725a3824ca572a8dcb1acb710672aedd0cd`  
		Last Modified: Tue, 06 Dec 2022 04:05:05 GMT  
		Size: 46.6 MB (46635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fe2652ab31a61b2b21678e07b447848a4114f8483e7fbf17883634f5ea9684`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db311e07a1dbe868f478f416210c3d80ae36f1698ef35144df93452fdb3e18ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111435225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9545e78c631045922aeb537864f74d52e56f4ee9aed57257e02471cc1c43c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:42 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 30 Nov 2022 01:52:42 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 30 Nov 2022 01:52:45 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 30 Nov 2022 01:52:50 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
USER emqx
# Wed, 30 Nov 2022 01:52:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:52:50 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 30 Nov 2022 01:52:50 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 30 Nov 2022 01:52:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:52:50 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78386a1c510620cb84f856900798687f1ea67c708915c4a9a2e60b8f5df15857`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39403596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a6da069cff1af881684d95753d55911ca54eeea95ffa2cee0f9d2a3b3ec7ae`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39409100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28aad18ab154243a8cbc713b374f429ba44b49ef016ca56878375a604e29b74`  
		Last Modified: Wed, 30 Nov 2022 01:53:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:032f9a7b4a747ad6ff6256caa6444b86dc067f8d9b7c718e5b0890beb7093982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:e9de1f4db098d54c04857658afed662a614ff9776a07f43b39a3b691481fecf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcf4ecf3c036cc8186e6c130d3e287718ee121e27c60f4a16528ce2d12f4ef3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:18 GMT
ADD file:30180333dcb9028c0d2776f05042f6f309238b100863a050f3981fb80604e871 in / 
# Tue, 06 Dec 2022 01:21:18 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:03:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:28 GMT
ENV EMQX_VERSION=4.3.22
# Tue, 06 Dec 2022 04:03:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 06 Dec 2022 04:03:38 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:03:39 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:03:39 GMT
USER emqx
# Tue, 06 Dec 2022 04:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:03:39 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 06 Dec 2022 04:03:39 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 06 Dec 2022 04:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:39 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:6eab20599fab240a56b06125a77b4921dd39662d3b9f9008da7306531772a1d0`  
		Last Modified: Tue, 06 Dec 2022 01:25:52 GMT  
		Size: 27.1 MB (27140356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efc79d145ca2cbe713f132cf4472673fb9801bf19d6b4c2fee21fcd7fd4cc33`  
		Last Modified: Tue, 06 Dec 2022 04:04:46 GMT  
		Size: 4.6 MB (4612576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d36f1157ff83e8657409c76b60a35bb2c8240b84728d3beb776b3feb4bac01`  
		Last Modified: Tue, 06 Dec 2022 04:04:50 GMT  
		Size: 36.5 MB (36537227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a1f4aac9aa65875cf351f9feff18afa0bbaf72ec947c707b0bf7511d79f572`  
		Last Modified: Tue, 06 Dec 2022 04:04:50 GMT  
		Size: 36.5 MB (36537362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34029b6a8c1be3b40f57100eca203020d4d599de74b8f1f14fe817c945d92892`  
		Last Modified: Tue, 06 Dec 2022 04:04:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cc61dcf2073c3c0e7c48c3426df5b07fe18c21a19b0fe5f6cbdbc0c643d75fd1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2fc6c8ffa36a6976b6c936af65033e160f87365205ace2e212305da0c50d3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:34 GMT
ADD file:aaead8e4dd08d41c8d1692bbe76b673119289836428e1f713ca550c2468711ac in / 
# Tue, 15 Nov 2022 01:41:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:30 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 30 Nov 2022 01:52:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 30 Nov 2022 01:52:38 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:52:39 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:52:39 GMT
USER emqx
# Wed, 30 Nov 2022 01:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:52:39 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 30 Nov 2022 01:52:39 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 30 Nov 2022 01:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:52:39 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:cc457132e077d684a6cecad3331c35341d814c5d364f3cf24d698a6d8e76d0e7`  
		Last Modified: Tue, 15 Nov 2022 01:45:13 GMT  
		Size: 25.9 MB (25914924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027abecdd5af35e9a16c44518f0617af3a9b80b03d0fac7e90d16f1de3c6100`  
		Last Modified: Tue, 15 Nov 2022 06:13:52 GMT  
		Size: 4.5 MB (4490492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd156f83df550b9c60e06e429f96308123f16fa687c477cde4fb6cd8a7a6ef99`  
		Last Modified: Wed, 30 Nov 2022 01:53:29 GMT  
		Size: 36.2 MB (36216026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abc81371049c42b020f56e5e771f9ad18237fe536d1bd104145b732303cf727`  
		Last Modified: Wed, 30 Nov 2022 01:53:29 GMT  
		Size: 36.2 MB (36223793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5b18e968368274267af0a7369ddcaf359cb15cfd80aade6e5238b4de183f74`  
		Last Modified: Wed, 30 Nov 2022 01:53:26 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.22`

```console
$ docker pull emqx@sha256:032f9a7b4a747ad6ff6256caa6444b86dc067f8d9b7c718e5b0890beb7093982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.22` - linux; amd64

```console
$ docker pull emqx@sha256:e9de1f4db098d54c04857658afed662a614ff9776a07f43b39a3b691481fecf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcf4ecf3c036cc8186e6c130d3e287718ee121e27c60f4a16528ce2d12f4ef3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:18 GMT
ADD file:30180333dcb9028c0d2776f05042f6f309238b100863a050f3981fb80604e871 in / 
# Tue, 06 Dec 2022 01:21:18 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:03:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:28 GMT
ENV EMQX_VERSION=4.3.22
# Tue, 06 Dec 2022 04:03:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 06 Dec 2022 04:03:38 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:03:39 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:03:39 GMT
USER emqx
# Tue, 06 Dec 2022 04:03:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:03:39 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 06 Dec 2022 04:03:39 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 06 Dec 2022 04:03:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:39 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:6eab20599fab240a56b06125a77b4921dd39662d3b9f9008da7306531772a1d0`  
		Last Modified: Tue, 06 Dec 2022 01:25:52 GMT  
		Size: 27.1 MB (27140356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efc79d145ca2cbe713f132cf4472673fb9801bf19d6b4c2fee21fcd7fd4cc33`  
		Last Modified: Tue, 06 Dec 2022 04:04:46 GMT  
		Size: 4.6 MB (4612576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d36f1157ff83e8657409c76b60a35bb2c8240b84728d3beb776b3feb4bac01`  
		Last Modified: Tue, 06 Dec 2022 04:04:50 GMT  
		Size: 36.5 MB (36537227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a1f4aac9aa65875cf351f9feff18afa0bbaf72ec947c707b0bf7511d79f572`  
		Last Modified: Tue, 06 Dec 2022 04:04:50 GMT  
		Size: 36.5 MB (36537362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34029b6a8c1be3b40f57100eca203020d4d599de74b8f1f14fe817c945d92892`  
		Last Modified: Tue, 06 Dec 2022 04:04:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.22` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cc61dcf2073c3c0e7c48c3426df5b07fe18c21a19b0fe5f6cbdbc0c643d75fd1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2fc6c8ffa36a6976b6c936af65033e160f87365205ace2e212305da0c50d3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:34 GMT
ADD file:aaead8e4dd08d41c8d1692bbe76b673119289836428e1f713ca550c2468711ac in / 
# Tue, 15 Nov 2022 01:41:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:30 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 30 Nov 2022 01:52:34 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 30 Nov 2022 01:52:38 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:52:39 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:52:39 GMT
USER emqx
# Wed, 30 Nov 2022 01:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:52:39 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 30 Nov 2022 01:52:39 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 30 Nov 2022 01:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:52:39 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:cc457132e077d684a6cecad3331c35341d814c5d364f3cf24d698a6d8e76d0e7`  
		Last Modified: Tue, 15 Nov 2022 01:45:13 GMT  
		Size: 25.9 MB (25914924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027abecdd5af35e9a16c44518f0617af3a9b80b03d0fac7e90d16f1de3c6100`  
		Last Modified: Tue, 15 Nov 2022 06:13:52 GMT  
		Size: 4.5 MB (4490492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd156f83df550b9c60e06e429f96308123f16fa687c477cde4fb6cd8a7a6ef99`  
		Last Modified: Wed, 30 Nov 2022 01:53:29 GMT  
		Size: 36.2 MB (36216026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abc81371049c42b020f56e5e771f9ad18237fe536d1bd104145b732303cf727`  
		Last Modified: Wed, 30 Nov 2022 01:53:29 GMT  
		Size: 36.2 MB (36223793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5b18e968368274267af0a7369ddcaf359cb15cfd80aade6e5238b4de183f74`  
		Last Modified: Wed, 30 Nov 2022 01:53:26 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:deeaeddbaec3e481653ff6c7e490cad2074cdc1f8100b0049ce768291ad8f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:2d23dcc574f9f82154d041a3c9c213f4a7aac829887c5f5104108d4f5b07dee7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127238717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd4b6b7c15dd9777f6d2732b818378ba7e4ac8551f8c4341e9540def0d6b71e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:03:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:51 GMT
ENV EMQX_VERSION=4.4.11
# Tue, 06 Dec 2022 04:03:51 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 06 Dec 2022 04:03:55 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 06 Dec 2022 04:04:01 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:02 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 06 Dec 2022 04:04:02 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:02 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3078ffce5d90ff48d82f12269ab8ab64696808bbda5c548acf2699549e57a18`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 2.6 MB (2571021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00655aeabee69f96756e1946695715aa34d796b40f41401330e62d17227c9720`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 46.6 MB (46617891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a34fe9ad4c37e86ba5473a44e9725a3824ca572a8dcb1acb710672aedd0cd`  
		Last Modified: Tue, 06 Dec 2022 04:05:05 GMT  
		Size: 46.6 MB (46635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fe2652ab31a61b2b21678e07b447848a4114f8483e7fbf17883634f5ea9684`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db311e07a1dbe868f478f416210c3d80ae36f1698ef35144df93452fdb3e18ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111435225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9545e78c631045922aeb537864f74d52e56f4ee9aed57257e02471cc1c43c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:42 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 30 Nov 2022 01:52:42 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 30 Nov 2022 01:52:45 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 30 Nov 2022 01:52:50 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
USER emqx
# Wed, 30 Nov 2022 01:52:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:52:50 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 30 Nov 2022 01:52:50 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 30 Nov 2022 01:52:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:52:50 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78386a1c510620cb84f856900798687f1ea67c708915c4a9a2e60b8f5df15857`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39403596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a6da069cff1af881684d95753d55911ca54eeea95ffa2cee0f9d2a3b3ec7ae`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39409100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28aad18ab154243a8cbc713b374f429ba44b49ef016ca56878375a604e29b74`  
		Last Modified: Wed, 30 Nov 2022 01:53:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.11`

```console
$ docker pull emqx@sha256:deeaeddbaec3e481653ff6c7e490cad2074cdc1f8100b0049ce768291ad8f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.11` - linux; amd64

```console
$ docker pull emqx@sha256:2d23dcc574f9f82154d041a3c9c213f4a7aac829887c5f5104108d4f5b07dee7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127238717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd4b6b7c15dd9777f6d2732b818378ba7e4ac8551f8c4341e9540def0d6b71e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:03:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:51 GMT
ENV EMQX_VERSION=4.4.11
# Tue, 06 Dec 2022 04:03:51 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 06 Dec 2022 04:03:55 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 06 Dec 2022 04:04:01 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:02 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:02 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 06 Dec 2022 04:04:02 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:02 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3078ffce5d90ff48d82f12269ab8ab64696808bbda5c548acf2699549e57a18`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 2.6 MB (2571021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00655aeabee69f96756e1946695715aa34d796b40f41401330e62d17227c9720`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 46.6 MB (46617891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a34fe9ad4c37e86ba5473a44e9725a3824ca572a8dcb1acb710672aedd0cd`  
		Last Modified: Tue, 06 Dec 2022 04:05:05 GMT  
		Size: 46.6 MB (46635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fe2652ab31a61b2b21678e07b447848a4114f8483e7fbf17883634f5ea9684`  
		Last Modified: Tue, 06 Dec 2022 04:04:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.11` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:db311e07a1dbe868f478f416210c3d80ae36f1698ef35144df93452fdb3e18ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111435225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9545e78c631045922aeb537864f74d52e56f4ee9aed57257e02471cc1c43c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:42 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 30 Nov 2022 01:52:42 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 30 Nov 2022 01:52:45 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 30 Nov 2022 01:52:50 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:52:50 GMT
USER emqx
# Wed, 30 Nov 2022 01:52:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:52:50 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 30 Nov 2022 01:52:50 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 30 Nov 2022 01:52:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:52:50 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78386a1c510620cb84f856900798687f1ea67c708915c4a9a2e60b8f5df15857`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39403596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a6da069cff1af881684d95753d55911ca54eeea95ffa2cee0f9d2a3b3ec7ae`  
		Last Modified: Wed, 30 Nov 2022 01:53:43 GMT  
		Size: 39.4 MB (39409100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28aad18ab154243a8cbc713b374f429ba44b49ef016ca56878375a604e29b74`  
		Last Modified: Wed, 30 Nov 2022 01:53:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:e16fb01aa65825dae3d9b99e5b777386f7c4677c980b23134476eaef547681c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:af67b05efd940d20f7045f890108598695e5432d25844412ac412d2889eeaa5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f3c40783e63508fbe1577dd48615bbbcbacb458793a33bbc80c48810e06c5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:04:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:15 GMT
ENV EMQX_VERSION=5.0.11
# Tue, 06 Dec 2022 04:04:15 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Tue, 06 Dec 2022 04:04:15 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Tue, 06 Dec 2022 04:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Dec 2022 04:04:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 06 Dec 2022 04:04:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:22 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:29 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Dec 2022 04:04:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29e5e20fa16580fcb41964870e6c9d3d48072cc1abdbe98fe1645a15c65e9ec`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.0 MB (2988935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dd9348a5687efee9dadf933fdf1c581bf1533143eb3ce58748acb88502529`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64920995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd74f9c9e7272821472794e054fec92054af29b0a2e630254ff8f3a33fdb09f`  
		Last Modified: Tue, 06 Dec 2022 04:05:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cc6b1ce2d96ed9a20aeaf174adb300c68487487d4a97d95ffb692f30dafae7`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64926015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:36847cbc801d37eafe836c7486f7069e618b168054494a17e6b9108a02c80d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147767210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2c84148e688bdd6a324207d0535c831a0a169d9ac580388ab9659e4f6df89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Wed, 30 Nov 2022 01:52:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:58 GMT
ENV EMQX_VERSION=5.0.11
# Wed, 30 Nov 2022 01:52:58 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Wed, 30 Nov 2022 01:52:58 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Wed, 30 Nov 2022 01:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 30 Nov 2022 01:53:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 30 Nov 2022 01:53:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 30 Nov 2022 01:53:03 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
USER emqx
# Wed, 30 Nov 2022 01:53:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:53:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 30 Nov 2022 01:53:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:53:08 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779afb6670c886761cbd92232fabbfb5460051f084cda020112fd649fd64c9e9`  
		Last Modified: Wed, 30 Nov 2022 01:53:54 GMT  
		Size: 3.0 MB (3004113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c27ff169ec58514bc5b2f6c9432b3c603c0f3c9d900e0f87cf167e7e8216e`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.3 MB (57348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554dd3630b90df5cd7b76d935f8ca60310032deeb91f91555ace233382d57c09`  
		Last Modified: Wed, 30 Nov 2022 01:53:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d390a44da3d80a16d371b5d4fa0e9de4b35bc149a4fcb8c8c13309aa6c6cee`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.4 MB (57353085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:e16fb01aa65825dae3d9b99e5b777386f7c4677c980b23134476eaef547681c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:af67b05efd940d20f7045f890108598695e5432d25844412ac412d2889eeaa5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f3c40783e63508fbe1577dd48615bbbcbacb458793a33bbc80c48810e06c5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:04:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:15 GMT
ENV EMQX_VERSION=5.0.11
# Tue, 06 Dec 2022 04:04:15 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Tue, 06 Dec 2022 04:04:15 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Tue, 06 Dec 2022 04:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Dec 2022 04:04:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 06 Dec 2022 04:04:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:22 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:29 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Dec 2022 04:04:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29e5e20fa16580fcb41964870e6c9d3d48072cc1abdbe98fe1645a15c65e9ec`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.0 MB (2988935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dd9348a5687efee9dadf933fdf1c581bf1533143eb3ce58748acb88502529`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64920995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd74f9c9e7272821472794e054fec92054af29b0a2e630254ff8f3a33fdb09f`  
		Last Modified: Tue, 06 Dec 2022 04:05:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cc6b1ce2d96ed9a20aeaf174adb300c68487487d4a97d95ffb692f30dafae7`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64926015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:36847cbc801d37eafe836c7486f7069e618b168054494a17e6b9108a02c80d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147767210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2c84148e688bdd6a324207d0535c831a0a169d9ac580388ab9659e4f6df89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Wed, 30 Nov 2022 01:52:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:58 GMT
ENV EMQX_VERSION=5.0.11
# Wed, 30 Nov 2022 01:52:58 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Wed, 30 Nov 2022 01:52:58 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Wed, 30 Nov 2022 01:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 30 Nov 2022 01:53:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 30 Nov 2022 01:53:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 30 Nov 2022 01:53:03 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
USER emqx
# Wed, 30 Nov 2022 01:53:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:53:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 30 Nov 2022 01:53:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:53:08 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779afb6670c886761cbd92232fabbfb5460051f084cda020112fd649fd64c9e9`  
		Last Modified: Wed, 30 Nov 2022 01:53:54 GMT  
		Size: 3.0 MB (3004113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c27ff169ec58514bc5b2f6c9432b3c603c0f3c9d900e0f87cf167e7e8216e`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.3 MB (57348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554dd3630b90df5cd7b76d935f8ca60310032deeb91f91555ace233382d57c09`  
		Last Modified: Wed, 30 Nov 2022 01:53:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d390a44da3d80a16d371b5d4fa0e9de4b35bc149a4fcb8c8c13309aa6c6cee`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.4 MB (57353085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.11`

```console
$ docker pull emqx@sha256:e16fb01aa65825dae3d9b99e5b777386f7c4677c980b23134476eaef547681c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.11` - linux; amd64

```console
$ docker pull emqx@sha256:af67b05efd940d20f7045f890108598695e5432d25844412ac412d2889eeaa5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f3c40783e63508fbe1577dd48615bbbcbacb458793a33bbc80c48810e06c5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:04:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:15 GMT
ENV EMQX_VERSION=5.0.11
# Tue, 06 Dec 2022 04:04:15 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Tue, 06 Dec 2022 04:04:15 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Tue, 06 Dec 2022 04:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Dec 2022 04:04:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 06 Dec 2022 04:04:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:22 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:29 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Dec 2022 04:04:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29e5e20fa16580fcb41964870e6c9d3d48072cc1abdbe98fe1645a15c65e9ec`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.0 MB (2988935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dd9348a5687efee9dadf933fdf1c581bf1533143eb3ce58748acb88502529`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64920995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd74f9c9e7272821472794e054fec92054af29b0a2e630254ff8f3a33fdb09f`  
		Last Modified: Tue, 06 Dec 2022 04:05:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cc6b1ce2d96ed9a20aeaf174adb300c68487487d4a97d95ffb692f30dafae7`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64926015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.11` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:36847cbc801d37eafe836c7486f7069e618b168054494a17e6b9108a02c80d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147767210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2c84148e688bdd6a324207d0535c831a0a169d9ac580388ab9659e4f6df89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Wed, 30 Nov 2022 01:52:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:58 GMT
ENV EMQX_VERSION=5.0.11
# Wed, 30 Nov 2022 01:52:58 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Wed, 30 Nov 2022 01:52:58 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Wed, 30 Nov 2022 01:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 30 Nov 2022 01:53:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 30 Nov 2022 01:53:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 30 Nov 2022 01:53:03 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
USER emqx
# Wed, 30 Nov 2022 01:53:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:53:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 30 Nov 2022 01:53:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:53:08 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779afb6670c886761cbd92232fabbfb5460051f084cda020112fd649fd64c9e9`  
		Last Modified: Wed, 30 Nov 2022 01:53:54 GMT  
		Size: 3.0 MB (3004113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c27ff169ec58514bc5b2f6c9432b3c603c0f3c9d900e0f87cf167e7e8216e`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.3 MB (57348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554dd3630b90df5cd7b76d935f8ca60310032deeb91f91555ace233382d57c09`  
		Last Modified: Wed, 30 Nov 2022 01:53:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d390a44da3d80a16d371b5d4fa0e9de4b35bc149a4fcb8c8c13309aa6c6cee`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.4 MB (57353085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:e16fb01aa65825dae3d9b99e5b777386f7c4677c980b23134476eaef547681c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:af67b05efd940d20f7045f890108598695e5432d25844412ac412d2889eeaa5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164249699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f3c40783e63508fbe1577dd48615bbbcbacb458793a33bbc80c48810e06c5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:04:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:15 GMT
ENV EMQX_VERSION=5.0.11
# Tue, 06 Dec 2022 04:04:15 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Tue, 06 Dec 2022 04:04:15 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Tue, 06 Dec 2022 04:04:15 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Dec 2022 04:04:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 06 Dec 2022 04:04:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Dec 2022 04:04:22 GMT
WORKDIR /opt/emqx
# Tue, 06 Dec 2022 04:04:28 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 06 Dec 2022 04:04:29 GMT
USER emqx
# Tue, 06 Dec 2022 04:04:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Dec 2022 04:04:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Dec 2022 04:04:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29e5e20fa16580fcb41964870e6c9d3d48072cc1abdbe98fe1645a15c65e9ec`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.0 MB (2988935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22dd9348a5687efee9dadf933fdf1c581bf1533143eb3ce58748acb88502529`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64920995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd74f9c9e7272821472794e054fec92054af29b0a2e630254ff8f3a33fdb09f`  
		Last Modified: Tue, 06 Dec 2022 04:05:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cc6b1ce2d96ed9a20aeaf174adb300c68487487d4a97d95ffb692f30dafae7`  
		Last Modified: Tue, 06 Dec 2022 04:05:24 GMT  
		Size: 64.9 MB (64926015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:36847cbc801d37eafe836c7486f7069e618b168054494a17e6b9108a02c80d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147767210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d2c84148e688bdd6a324207d0535c831a0a169d9ac580388ab9659e4f6df89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Wed, 30 Nov 2022 01:52:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Nov 2022 01:52:58 GMT
ENV EMQX_VERSION=5.0.11
# Wed, 30 Nov 2022 01:52:58 GMT
ENV AMD64_SHA256=68609fcc1d74be917f9c28c57c14daabccee22361af91b6e98812a35300a1c80
# Wed, 30 Nov 2022 01:52:58 GMT
ENV ARM64_SHA256=f7c7417951beb490ed3a7347b3879db8e9e80ea214c9ef942e777c7136681d31
# Wed, 30 Nov 2022 01:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 30 Nov 2022 01:53:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 30 Nov 2022 01:53:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 30 Nov 2022 01:53:03 GMT
WORKDIR /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 30 Nov 2022 01:53:08 GMT
USER emqx
# Wed, 30 Nov 2022 01:53:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 30 Nov 2022 01:53:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 30 Nov 2022 01:53:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 30 Nov 2022 01:53:08 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779afb6670c886761cbd92232fabbfb5460051f084cda020112fd649fd64c9e9`  
		Last Modified: Wed, 30 Nov 2022 01:53:54 GMT  
		Size: 3.0 MB (3004113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c27ff169ec58514bc5b2f6c9432b3c603c0f3c9d900e0f87cf167e7e8216e`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.3 MB (57348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554dd3630b90df5cd7b76d935f8ca60310032deeb91f91555ace233382d57c09`  
		Last Modified: Wed, 30 Nov 2022 01:53:53 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d390a44da3d80a16d371b5d4fa0e9de4b35bc149a4fcb8c8c13309aa6c6cee`  
		Last Modified: Wed, 30 Nov 2022 01:53:59 GMT  
		Size: 57.4 MB (57353085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
