<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.6`](#crate46)
-	[`crate:4.6.8`](#crate468)
-	[`crate:4.7`](#crate47)
-	[`crate:4.7.3`](#crate473)
-	[`crate:4.8`](#crate48)
-	[`crate:4.8.1`](#crate481)
-	[`crate:latest`](#cratelatest)

## `crate:4.6`

```console
$ docker pull crate@sha256:64fd5119f66e902498610152dba07a27363df1f193d22730175bb8b09ee883b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6` - linux; amd64

```console
$ docker pull crate@sha256:93632109a3539c26ed9a5b3f8697a4c375893fb70aea87b3953d76002a7e3fe3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333298491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489ec3cd90eda191854db4fa2f2b6fcfd796bed07ef007d4ce6ce274e0325e96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 16 Mar 2022 00:26:02 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.8.tar.gz.asc crate-4.6.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.8.tar.gz.asc     && tar -xf crate-4.6.8.tar.gz -C /crate --strip-components=1     && rm crate-4.6.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:26:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:26:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:26:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:26:36 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:26:36 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:26:36 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:26:36 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:26:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:26:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:26:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T10:39:18.218424 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.8
# Wed, 16 Mar 2022 00:26:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:26:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:26:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eb0e6af56c8c0900122db7a6808def673a4ceecdb95b699f9ca0078c52c074`  
		Last Modified: Wed, 16 Mar 2022 00:27:56 GMT  
		Size: 255.6 MB (255614996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86f3db1f86fd161c20ebd210b3b5324dd3ab8647233685c86b30c4bcbf25d33`  
		Last Modified: Wed, 16 Mar 2022 00:27:34 GMT  
		Size: 1.6 MB (1582197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f230a107ddd6d942339256630c7882c616d8960b4103de7b877bfbf888f07876`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e6a74bfead1f8a250143d841bef006617d5313413d2cafc929cfce7d4bd7df`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fce1768c7c5213b32777c5c631168cc1f348b7dd4c81383a44e6cd8f8cdaeeb`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac286d124317b0d806c8fa98acf5372ffd61dc6c920f9dab724e15879a207fd`  
		Last Modified: Wed, 16 Mar 2022 00:27:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a1c139662f1d9a0097994f00cfa81eec166a5db241942e491d5d2539238ad521
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362344650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b09b5df3b440fa883c5fb4c85438824fe354dc0c4d903c66059a09dc06572a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 14 Feb 2022 20:17:55 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 16 Mar 2022 00:49:00 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.8.tar.gz.asc crate-4.6.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.8.tar.gz.asc     && tar -xf crate-4.6.8.tar.gz -C /crate --strip-components=1     && rm crate-4.6.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:49:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:49:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:49:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:49:43 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:49:44 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:49:45 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:49:46 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:49:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:49:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:49:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T10:39:18.218424 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.8
# Wed, 16 Mar 2022 00:49:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:49:52 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54c55dc24d3cbebabdd223dbc4e51f5c147fad4f356562dd4a5c4fdb5a4ed4c`  
		Last Modified: Mon, 14 Feb 2022 20:24:02 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18494ee0116ddb7fc6d9a1ff0335ba763062815df80185b5a5881aa9f266f226`  
		Last Modified: Wed, 16 Mar 2022 00:51:34 GMT  
		Size: 252.4 MB (252385074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509ed3a573490ccb5e418acdc43a7fbcb30905113697e37b13362f68ddbdb308`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 1.6 MB (1580569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91af8584979695159a69fea1700f6771ac062c62f31760a3e0e3d6ad9fa6b0e`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb27b132f0d22f02542f83d53b087e79125b50d5fdc16092e8d75451ad1ec93`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd025c87bb8bb650250fe19913d0a21aa214a45d5109d79391a1ab7e975792b`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3982a4830b74dae916cc3e004fe05c1b44addb345a6fa47d2705dabfadb6717`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.6.8`

```console
$ docker pull crate@sha256:64fd5119f66e902498610152dba07a27363df1f193d22730175bb8b09ee883b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6.8` - linux; amd64

```console
$ docker pull crate@sha256:93632109a3539c26ed9a5b3f8697a4c375893fb70aea87b3953d76002a7e3fe3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333298491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489ec3cd90eda191854db4fa2f2b6fcfd796bed07ef007d4ce6ce274e0325e96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:37:51 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 16 Mar 2022 00:26:02 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.8.tar.gz.asc crate-4.6.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.8.tar.gz.asc     && tar -xf crate-4.6.8.tar.gz -C /crate --strip-components=1     && rm crate-4.6.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:26:35 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:26:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:26:36 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:26:36 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:26:36 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:26:36 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:26:36 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:26:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:26:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:26:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T10:39:18.218424 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.8
# Wed, 16 Mar 2022 00:26:37 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:26:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:26:37 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b4c75f30c9b7afb780c16245b96bddad3d255e679114717859265250a0f64`  
		Last Modified: Wed, 15 Sep 2021 18:46:27 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eb0e6af56c8c0900122db7a6808def673a4ceecdb95b699f9ca0078c52c074`  
		Last Modified: Wed, 16 Mar 2022 00:27:56 GMT  
		Size: 255.6 MB (255614996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86f3db1f86fd161c20ebd210b3b5324dd3ab8647233685c86b30c4bcbf25d33`  
		Last Modified: Wed, 16 Mar 2022 00:27:34 GMT  
		Size: 1.6 MB (1582197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f230a107ddd6d942339256630c7882c616d8960b4103de7b877bfbf888f07876`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e6a74bfead1f8a250143d841bef006617d5313413d2cafc929cfce7d4bd7df`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fce1768c7c5213b32777c5c631168cc1f348b7dd4c81383a44e6cd8f8cdaeeb`  
		Last Modified: Wed, 16 Mar 2022 00:27:33 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac286d124317b0d806c8fa98acf5372ffd61dc6c920f9dab724e15879a207fd`  
		Last Modified: Wed, 16 Mar 2022 00:27:34 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:a1c139662f1d9a0097994f00cfa81eec166a5db241942e491d5d2539238ad521
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362344650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b09b5df3b440fa883c5fb4c85438824fe354dc0c4d903c66059a09dc06572a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Mon, 14 Feb 2022 20:17:55 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 16 Mar 2022 00:49:00 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.8.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.8.tar.gz.asc crate-4.6.8.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.8.tar.gz.asc     && tar -xf crate-4.6.8.tar.gz -C /crate --strip-components=1     && rm crate-4.6.8.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:49:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:49:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:49:42 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:49:43 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:49:44 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:49:45 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:49:46 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:49:48 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:49:49 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:49:49 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T10:39:18.218424 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.8
# Wed, 16 Mar 2022 00:49:51 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:49:52 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54c55dc24d3cbebabdd223dbc4e51f5c147fad4f356562dd4a5c4fdb5a4ed4c`  
		Last Modified: Mon, 14 Feb 2022 20:24:02 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18494ee0116ddb7fc6d9a1ff0335ba763062815df80185b5a5881aa9f266f226`  
		Last Modified: Wed, 16 Mar 2022 00:51:34 GMT  
		Size: 252.4 MB (252385074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509ed3a573490ccb5e418acdc43a7fbcb30905113697e37b13362f68ddbdb308`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 1.6 MB (1580569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91af8584979695159a69fea1700f6771ac062c62f31760a3e0e3d6ad9fa6b0e`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb27b132f0d22f02542f83d53b087e79125b50d5fdc16092e8d75451ad1ec93`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd025c87bb8bb650250fe19913d0a21aa214a45d5109d79391a1ab7e975792b`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3982a4830b74dae916cc3e004fe05c1b44addb345a6fa47d2705dabfadb6717`  
		Last Modified: Wed, 16 Mar 2022 00:51:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.7`

```console
$ docker pull crate@sha256:2078450066279764db4bca22840fd0fbd5cc45167577205fbcfa37d571a3a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.7` - linux; amd64

```console
$ docker pull crate@sha256:43fb05ab45d1e9cd343b586b04ea608e6ba6577a989d2131e27631df2bb427d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378498279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894a71bc691be6203a9910f8294c22c5e8914e451ddaaea4a33d5eca38e26f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 02:19:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:46 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:46 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:46 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:46 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 02:19:47 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6b95f3386f2cd7959b406edc0cf7f12f9e8bef49197782fbb7b4689900524`  
		Last Modified: Wed, 01 Jun 2022 02:20:56 GMT  
		Size: 224.3 MB (224345961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dcdaf46f2cda8f038a6b5733adbaf57a7df63e555ac6bc200924a995417a3e`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 1.7 MB (1710770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d0adbec4d92e5eef0118b814d2c672aa63b0f68bb582aab2ee58877400bce9`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557505f940c3fe820fbf57a025f486a625df83940521bf3509da94e12b9f62a`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659873cff32f66bb0e2825b6f27d7cfa7b276aabdae7bd9c921fd11fc91753b`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0eb1fcd3de4227b7b4bd74a1f49d85f03e9ea1a5a7a1b2dd882364ef2be1e1`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6e5201e139fa9aebec01518fdcd2fc2c0bebf722f2de31b9bbaee31ac51a2b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677268672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231cf819dd48ee73009f86e05906351cfaeae24dbd0239087f57578234ea4ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:30:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 03:30:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:30:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:30:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:30:21 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:30:22 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:30:23 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:30:23 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:30:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:30:26 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:30:26 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 03:30:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:30:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:30:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a0546c53970e90c42dd06edca1fc95130796e58ffaef91bac0c74f560e18b0`  
		Last Modified: Wed, 01 Jun 2022 03:32:14 GMT  
		Size: 223.1 MB (223120525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6b93b24ed17c5809c900abbcb49ca625ffaaacf3282098013e96830de40359`  
		Last Modified: Wed, 01 Jun 2022 03:31:51 GMT  
		Size: 1.7 MB (1709338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2dc37ac1d8de177c73a57e7b9f755df1a30c2037ab362d94924202c6c67975`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b518f803547ff7d4156632269149131ca438cd16d70dc2059f22bc6e025537a`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef8e7842badd444824bf4ba171e7c3f29823d4487e2079f9d5cd71fc94ac0f`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc0735067d3a7caa3c2087750e9bfbbc644d19ab81c27800f6ebe2a1ec27242`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.7.3`

```console
$ docker pull crate@sha256:2078450066279764db4bca22840fd0fbd5cc45167577205fbcfa37d571a3a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.7.3` - linux; amd64

```console
$ docker pull crate@sha256:43fb05ab45d1e9cd343b586b04ea608e6ba6577a989d2131e27631df2bb427d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378498279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894a71bc691be6203a9910f8294c22c5e8914e451ddaaea4a33d5eca38e26f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:42 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 02:19:45 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:45 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:45 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:46 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:46 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:46 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:46 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 02:19:47 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:47 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c6b95f3386f2cd7959b406edc0cf7f12f9e8bef49197782fbb7b4689900524`  
		Last Modified: Wed, 01 Jun 2022 02:20:56 GMT  
		Size: 224.3 MB (224345961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dcdaf46f2cda8f038a6b5733adbaf57a7df63e555ac6bc200924a995417a3e`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 1.7 MB (1710770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d0adbec4d92e5eef0118b814d2c672aa63b0f68bb582aab2ee58877400bce9`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4557505f940c3fe820fbf57a025f486a625df83940521bf3509da94e12b9f62a`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659873cff32f66bb0e2825b6f27d7cfa7b276aabdae7bd9c921fd11fc91753b`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0eb1fcd3de4227b7b4bd74a1f49d85f03e9ea1a5a7a1b2dd882364ef2be1e1`  
		Last Modified: Wed, 01 Jun 2022 02:20:37 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.7.3` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:6e5201e139fa9aebec01518fdcd2fc2c0bebf722f2de31b9bbaee31ac51a2b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677268672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231cf819dd48ee73009f86e05906351cfaeae24dbd0239087f57578234ea4ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:30:15 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.3.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.3.tar.gz.asc crate-4.7.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.3.tar.gz.asc     && tar -xf crate-4.7.3.tar.gz -C /crate --strip-components=1     && rm crate-4.7.3.tar.gz
# Wed, 01 Jun 2022 03:30:18 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:30:19 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:30:20 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:30:21 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:30:22 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:30:23 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:30:23 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:30:25 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:30:26 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:30:26 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-24T15:45:34.917877 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.3
# Wed, 01 Jun 2022 03:30:28 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:30:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:30:29 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a0546c53970e90c42dd06edca1fc95130796e58ffaef91bac0c74f560e18b0`  
		Last Modified: Wed, 01 Jun 2022 03:32:14 GMT  
		Size: 223.1 MB (223120525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6b93b24ed17c5809c900abbcb49ca625ffaaacf3282098013e96830de40359`  
		Last Modified: Wed, 01 Jun 2022 03:31:51 GMT  
		Size: 1.7 MB (1709338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2dc37ac1d8de177c73a57e7b9f755df1a30c2037ab362d94924202c6c67975`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b518f803547ff7d4156632269149131ca438cd16d70dc2059f22bc6e025537a`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef8e7842badd444824bf4ba171e7c3f29823d4487e2079f9d5cd71fc94ac0f`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc0735067d3a7caa3c2087750e9bfbbc644d19ab81c27800f6ebe2a1ec27242`  
		Last Modified: Wed, 01 Jun 2022 03:31:50 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8`

```console
$ docker pull crate@sha256:3661461bfd871ccf66100fbe7ca5342e6abf9c348395c4c56c71d6b41f5d0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8` - linux; amd64

```console
$ docker pull crate@sha256:9b504acc4e67da77fc4ebdff6b3c00af673d9172c18e8da7553cabf2d26e365b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362901740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a652fdf58152ab1a9b53bc282709c7839066460615808a3ddd80b255cf6f33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 02:19:05 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:05 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:05 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:06 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:06 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:06 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:06 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 02:19:07 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12cef03cf54f5d5cc5f6030ee0ed20c888aa2208e6898b414790ba73c1d1d53`  
		Last Modified: Wed, 01 Jun 2022 02:20:22 GMT  
		Size: 208.7 MB (208749426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864eb8f7e84d0be375f1d6108f0a645400dc100b58a01378d2674854f75e5db5`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 1.7 MB (1710771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c0c3be1457b3fcf8cdfb0887c3cd24b18db53c8d425d06b804378bddbe64ac`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80df7d6531f57c4316b0e9ced200043fc096a12b4cf769fb9743f69715f26d5`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04f65f9fe26177b637b9ad885830b95dc0bceb8e2980cbc10fd7b250c1e781f`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00997a6aeff0fc3103dba65a109dbefe61131d3662e784abedbd20c4d331d4c`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:629e9d4fcb291c8f6cf00a58eaeb1d0ec5b40acc40d23d68295259e4b74455d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.7 MB (661679206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf944ce8f3aac92915b67a349ebb6c8779a415a908e9af461b3f8fd1df0a2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:29:12 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 03:29:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:29:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:29:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:29:19 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:29:20 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:29:20 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:29:21 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:29:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:29:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:29:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 03:29:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:29:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:29:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0020adfb8551b4d34503851b4c3e9702aa9cd8f9d66d82b767401167f2a2b1`  
		Last Modified: Wed, 01 Jun 2022 03:31:22 GMT  
		Size: 207.5 MB (207531052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b0bcd34db8c20d657739129db407d4b3e21ff6bab0d40d68f2c234e19c2b10`  
		Last Modified: Wed, 01 Jun 2022 03:30:58 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89735b8826cae6e244413c3eba24bfd507477645513852b52ca8a120650442`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4759785519253d15082e7826a7b4b4e84edd87b95be3a25d093c1989a8d6bb`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d71954f81cc2cca54473ae472e5f52523f4122739b5232a6bc3f5b873d35c4`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafda819f9e879b584a5d9cbc7499d4b3fdf97fd8a49534c45a0d2b9f6524964`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.8.1`

```console
$ docker pull crate@sha256:3661461bfd871ccf66100fbe7ca5342e6abf9c348395c4c56c71d6b41f5d0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.8.1` - linux; amd64

```console
$ docker pull crate@sha256:9b504acc4e67da77fc4ebdff6b3c00af673d9172c18e8da7553cabf2d26e365b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362901740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a652fdf58152ab1a9b53bc282709c7839066460615808a3ddd80b255cf6f33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 02:19:05 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:05 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:05 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:06 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:06 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:06 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:06 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 02:19:07 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12cef03cf54f5d5cc5f6030ee0ed20c888aa2208e6898b414790ba73c1d1d53`  
		Last Modified: Wed, 01 Jun 2022 02:20:22 GMT  
		Size: 208.7 MB (208749426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864eb8f7e84d0be375f1d6108f0a645400dc100b58a01378d2674854f75e5db5`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 1.7 MB (1710771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c0c3be1457b3fcf8cdfb0887c3cd24b18db53c8d425d06b804378bddbe64ac`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80df7d6531f57c4316b0e9ced200043fc096a12b4cf769fb9743f69715f26d5`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04f65f9fe26177b637b9ad885830b95dc0bceb8e2980cbc10fd7b250c1e781f`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00997a6aeff0fc3103dba65a109dbefe61131d3662e784abedbd20c4d331d4c`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.8.1` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:629e9d4fcb291c8f6cf00a58eaeb1d0ec5b40acc40d23d68295259e4b74455d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.7 MB (661679206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf944ce8f3aac92915b67a349ebb6c8779a415a908e9af461b3f8fd1df0a2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:29:12 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 03:29:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:29:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:29:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:29:19 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:29:20 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:29:20 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:29:21 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:29:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:29:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:29:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 03:29:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:29:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:29:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0020adfb8551b4d34503851b4c3e9702aa9cd8f9d66d82b767401167f2a2b1`  
		Last Modified: Wed, 01 Jun 2022 03:31:22 GMT  
		Size: 207.5 MB (207531052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b0bcd34db8c20d657739129db407d4b3e21ff6bab0d40d68f2c234e19c2b10`  
		Last Modified: Wed, 01 Jun 2022 03:30:58 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89735b8826cae6e244413c3eba24bfd507477645513852b52ca8a120650442`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4759785519253d15082e7826a7b4b4e84edd87b95be3a25d093c1989a8d6bb`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d71954f81cc2cca54473ae472e5f52523f4122739b5232a6bc3f5b873d35c4`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafda819f9e879b584a5d9cbc7499d4b3fdf97fd8a49534c45a0d2b9f6524964`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:3661461bfd871ccf66100fbe7ca5342e6abf9c348395c4c56c71d6b41f5d0c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9b504acc4e67da77fc4ebdff6b3c00af673d9172c18e8da7553cabf2d26e365b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362901740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a652fdf58152ab1a9b53bc282709c7839066460615808a3ddd80b255cf6f33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 02:18:37 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 02:19:02 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 02:19:05 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 02:19:05 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 02:19:05 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 02:19:06 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 02:19:06 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 02:19:06 GMT
WORKDIR /data
# Wed, 01 Jun 2022 02:19:06 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 02:19:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 02:19:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 02:19:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 02:19:07 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 02:19:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 02:19:07 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e0278fa73b12c38da522cb3ac5a17a218c02fc4f6a33a9272bd63d6dada`  
		Last Modified: Wed, 01 Jun 2022 02:20:17 GMT  
		Size: 76.3 MB (76342505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12cef03cf54f5d5cc5f6030ee0ed20c888aa2208e6898b414790ba73c1d1d53`  
		Last Modified: Wed, 01 Jun 2022 02:20:22 GMT  
		Size: 208.7 MB (208749426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864eb8f7e84d0be375f1d6108f0a645400dc100b58a01378d2674854f75e5db5`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 1.7 MB (1710771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c0c3be1457b3fcf8cdfb0887c3cd24b18db53c8d425d06b804378bddbe64ac`  
		Last Modified: Wed, 01 Jun 2022 02:20:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80df7d6531f57c4316b0e9ced200043fc096a12b4cf769fb9743f69715f26d5`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04f65f9fe26177b637b9ad885830b95dc0bceb8e2980cbc10fd7b250c1e781f`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00997a6aeff0fc3103dba65a109dbefe61131d3662e784abedbd20c4d331d4c`  
		Last Modified: Wed, 01 Jun 2022 02:20:02 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:629e9d4fcb291c8f6cf00a58eaeb1d0ec5b40acc40d23d68295259e4b74455d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.7 MB (661679206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf944ce8f3aac92915b67a349ebb6c8779a415a908e9af461b3f8fd1df0a2a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 03:28:42 GMT
RUN yum install -y yum-utils deltarpm     && yum makecache     && yum install -y python3 openssl     && yum upgrade -y     && pip3 install "pip>=19,<19.3" --upgrade     && yum clean all     && rm -rf /var/cache/yum
# Wed, 01 Jun 2022 03:29:12 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.8.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.8.1.tar.gz.asc crate-4.8.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.8.1.tar.gz.asc     && tar -xf crate-4.8.1.tar.gz -C /crate --strip-components=1     && rm crate-4.8.1.tar.gz
# Wed, 01 Jun 2022 03:29:16 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 01 Jun 2022 03:29:17 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 03:29:18 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 01 Jun 2022 03:29:19 GMT
RUN mkdir -p /data/data /data/log
# Wed, 01 Jun 2022 03:29:20 GMT
VOLUME [/data]
# Wed, 01 Jun 2022 03:29:20 GMT
WORKDIR /data
# Wed, 01 Jun 2022 03:29:21 GMT
EXPOSE 4200 4300 5432
# Wed, 01 Jun 2022 03:29:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 01 Jun 2022 03:29:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 01 Jun 2022 03:29:24 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-05-25T08:09:52.858318 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.8.1
# Wed, 01 Jun 2022 03:29:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 01 Jun 2022 03:29:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Jun 2022 03:29:27 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6774b23350e9379e8826202f65f1340856dbeb40114cd85b252aca0e38dc8a0`  
		Last Modified: Wed, 01 Jun 2022 03:31:35 GMT  
		Size: 344.1 MB (344062014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0020adfb8551b4d34503851b4c3e9702aa9cd8f9d66d82b767401167f2a2b1`  
		Last Modified: Wed, 01 Jun 2022 03:31:22 GMT  
		Size: 207.5 MB (207531052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b0bcd34db8c20d657739129db407d4b3e21ff6bab0d40d68f2c234e19c2b10`  
		Last Modified: Wed, 01 Jun 2022 03:30:58 GMT  
		Size: 1.7 MB (1709339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89735b8826cae6e244413c3eba24bfd507477645513852b52ca8a120650442`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4759785519253d15082e7826a7b4b4e84edd87b95be3a25d093c1989a8d6bb`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d71954f81cc2cca54473ae472e5f52523f4122739b5232a6bc3f5b873d35c4`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafda819f9e879b584a5d9cbc7499d4b3fdf97fd8a49534c45a0d2b9f6524964`  
		Last Modified: Wed, 01 Jun 2022 03:30:57 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
