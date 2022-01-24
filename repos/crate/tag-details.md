<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `crate`

-	[`crate:4.6`](#crate46)
-	[`crate:4.6.7`](#crate467)
-	[`crate:latest`](#cratelatest)

## `crate:4.6`

```console
$ docker pull crate@sha256:2ec5859d7e8ea39854df0eebe85b4a65ba713e623101634c382c069fe247403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6` - linux; amd64

```console
$ docker pull crate@sha256:255c3b47643e81a805755aaa64cf9360ea4b692d511d430ca93ef0e15cd8efb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333282166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4c40d8f42111730dbac154a8daaf9b092dd4060d41ab55095a8e662502558a`
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
# Mon, 24 Jan 2022 20:58:47 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:59:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:59:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:59:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:59:32 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:59:32 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:59:32 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:59:32 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:59:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:59:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:59:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:59:34 GMT
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
	-	`sha256:77bdfcc915e3d6b46b979bd0efbaf130a1ca62b4b7459b5389cc2a446a09c2a4`  
		Last Modified: Mon, 24 Jan 2022 21:00:15 GMT  
		Size: 255.6 MB (255598668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf083680069f1ae344d9ce89da674fd52aad77271d0e536dbfc438bbc2eb7f`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 1.6 MB (1582201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da95b014bb5dde7754ea770a5a84f70e1ee3a57e7568af1b2f1cb2bf23d736`  
		Last Modified: Mon, 24 Jan 2022 20:59:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b729a7b2b19736b06daf6734a270e598df42325396100d6e97603438aacbf`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd90676ad3d4a672a8aa75cd930205f9484b05a16e6204230dc65b0fd3377a`  
		Last Modified: Mon, 24 Jan 2022 20:59:48 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aac0d94022e8be81274f75ba3ac9d477df89ecb1d8ff77fd6250629ce25935`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e8d5e0d099f503e22c80d4b1bcabf7bdad50135d36e5c25cdafff70ba192a84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362344486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27ea90cd582881b83bf7a75ce1b41f821d0740370eaeff5e4f7072529ed0c4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 24 Jan 2022 20:41:14 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:41:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:41:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:42:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:42:01 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:42:02 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:42:03 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:42:04 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:42:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:42:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:42:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:42:09 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:42:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:42:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d466c5b731363066ebcec54faa2567b513637efc6dea6e245cef9c887e911f`  
		Last Modified: Mon, 24 Jan 2022 20:42:52 GMT  
		Size: 252.4 MB (252384907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7185b6cef7f947ddd78cee3823a6c12ac6ce24c10c17777e75e18d56db93f3c8`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 1.6 MB (1580580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155cb153d99329f5f0c66d656919be7b8e74d75ff6641c59f4138923b000c69b`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5277a481d915e616e6a40f2ff42e2c16e4e3be2445eb618a1e9895326c4d0e`  
		Last Modified: Mon, 24 Jan 2022 20:42:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9766296d413c72e3bafb063d41e89c6579f76e139bf93eec8b765dd5780adcd`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d13da48861a867261a83d9cc5e1a3d117933eca360a1f8772001f6667e9ea7`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:4.6.7`

```console
$ docker pull crate@sha256:2ec5859d7e8ea39854df0eebe85b4a65ba713e623101634c382c069fe247403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:4.6.7` - linux; amd64

```console
$ docker pull crate@sha256:255c3b47643e81a805755aaa64cf9360ea4b692d511d430ca93ef0e15cd8efb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333282166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4c40d8f42111730dbac154a8daaf9b092dd4060d41ab55095a8e662502558a`
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
# Mon, 24 Jan 2022 20:58:47 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:59:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:59:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:59:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:59:32 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:59:32 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:59:32 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:59:32 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:59:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:59:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:59:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:59:34 GMT
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
	-	`sha256:77bdfcc915e3d6b46b979bd0efbaf130a1ca62b4b7459b5389cc2a446a09c2a4`  
		Last Modified: Mon, 24 Jan 2022 21:00:15 GMT  
		Size: 255.6 MB (255598668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf083680069f1ae344d9ce89da674fd52aad77271d0e536dbfc438bbc2eb7f`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 1.6 MB (1582201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da95b014bb5dde7754ea770a5a84f70e1ee3a57e7568af1b2f1cb2bf23d736`  
		Last Modified: Mon, 24 Jan 2022 20:59:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b729a7b2b19736b06daf6734a270e598df42325396100d6e97603438aacbf`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd90676ad3d4a672a8aa75cd930205f9484b05a16e6204230dc65b0fd3377a`  
		Last Modified: Mon, 24 Jan 2022 20:59:48 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aac0d94022e8be81274f75ba3ac9d477df89ecb1d8ff77fd6250629ce25935`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:4.6.7` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e8d5e0d099f503e22c80d4b1bcabf7bdad50135d36e5c25cdafff70ba192a84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362344486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27ea90cd582881b83bf7a75ce1b41f821d0740370eaeff5e4f7072529ed0c4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 24 Jan 2022 20:41:14 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:41:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:41:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:42:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:42:01 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:42:02 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:42:03 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:42:04 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:42:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:42:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:42:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:42:09 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:42:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:42:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d466c5b731363066ebcec54faa2567b513637efc6dea6e245cef9c887e911f`  
		Last Modified: Mon, 24 Jan 2022 20:42:52 GMT  
		Size: 252.4 MB (252384907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7185b6cef7f947ddd78cee3823a6c12ac6ce24c10c17777e75e18d56db93f3c8`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 1.6 MB (1580580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155cb153d99329f5f0c66d656919be7b8e74d75ff6641c59f4138923b000c69b`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5277a481d915e616e6a40f2ff42e2c16e4e3be2445eb618a1e9895326c4d0e`  
		Last Modified: Mon, 24 Jan 2022 20:42:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9766296d413c72e3bafb063d41e89c6579f76e139bf93eec8b765dd5780adcd`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d13da48861a867261a83d9cc5e1a3d117933eca360a1f8772001f6667e9ea7`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `crate:latest`

```console
$ docker pull crate@sha256:2ec5859d7e8ea39854df0eebe85b4a65ba713e623101634c382c069fe247403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:255c3b47643e81a805755aaa64cf9360ea4b692d511d430ca93ef0e15cd8efb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333282166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4c40d8f42111730dbac154a8daaf9b092dd4060d41ab55095a8e662502558a`
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
# Mon, 24 Jan 2022 20:58:47 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:59:31 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:59:31 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:59:31 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:59:32 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:59:32 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:59:32 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:59:32 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:59:33 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:59:33 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:59:33 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:59:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:59:34 GMT
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
	-	`sha256:77bdfcc915e3d6b46b979bd0efbaf130a1ca62b4b7459b5389cc2a446a09c2a4`  
		Last Modified: Mon, 24 Jan 2022 21:00:15 GMT  
		Size: 255.6 MB (255598668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf083680069f1ae344d9ce89da674fd52aad77271d0e536dbfc438bbc2eb7f`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 1.6 MB (1582201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da95b014bb5dde7754ea770a5a84f70e1ee3a57e7568af1b2f1cb2bf23d736`  
		Last Modified: Mon, 24 Jan 2022 20:59:49 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b729a7b2b19736b06daf6734a270e598df42325396100d6e97603438aacbf`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd90676ad3d4a672a8aa75cd930205f9484b05a16e6204230dc65b0fd3377a`  
		Last Modified: Mon, 24 Jan 2022 20:59:48 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aac0d94022e8be81274f75ba3ac9d477df89ecb1d8ff77fd6250629ce25935`  
		Last Modified: Mon, 24 Jan 2022 20:59:47 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e8d5e0d099f503e22c80d4b1bcabf7bdad50135d36e5c25cdafff70ba192a84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362344486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27ea90cd582881b83bf7a75ce1b41f821d0740370eaeff5e4f7072529ed0c4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 17:39:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Mon, 24 Jan 2022 20:41:14 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.6.7.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.6.7.tar.gz.asc crate-4.6.7.tar.gz     && rm -rf "$GNUPGHOME" crate-4.6.7.tar.gz.asc     && tar -xf crate-4.6.7.tar.gz -C /crate --strip-components=1     && rm crate-4.6.7.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Mon, 24 Jan 2022 20:41:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 24 Jan 2022 20:41:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Jan 2022 20:42:00 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 24 Jan 2022 20:42:01 GMT
RUN mkdir -p /data/data /data/log
# Mon, 24 Jan 2022 20:42:02 GMT
VOLUME [/data]
# Mon, 24 Jan 2022 20:42:03 GMT
WORKDIR /data
# Mon, 24 Jan 2022 20:42:04 GMT
EXPOSE 4200 4300 5432
# Mon, 24 Jan 2022 20:42:06 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 24 Jan 2022 20:42:07 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 24 Jan 2022 20:42:07 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-01-19T15:25:26.265468 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.6.7
# Mon, 24 Jan 2022 20:42:09 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 24 Jan 2022 20:42:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 24 Jan 2022 20:42:10 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e276594d35170abf49132218c828dbb53b9fc83765b7a2d3012449d3af249`  
		Last Modified: Fri, 19 Nov 2021 17:52:16 GMT  
		Size: 2.2 KB (2204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d466c5b731363066ebcec54faa2567b513637efc6dea6e245cef9c887e911f`  
		Last Modified: Mon, 24 Jan 2022 20:42:52 GMT  
		Size: 252.4 MB (252384907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7185b6cef7f947ddd78cee3823a6c12ac6ce24c10c17777e75e18d56db93f3c8`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 1.6 MB (1580580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155cb153d99329f5f0c66d656919be7b8e74d75ff6641c59f4138923b000c69b`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5277a481d915e616e6a40f2ff42e2c16e4e3be2445eb618a1e9895326c4d0e`  
		Last Modified: Mon, 24 Jan 2022 20:42:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9766296d413c72e3bafb063d41e89c6579f76e139bf93eec8b765dd5780adcd`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d13da48861a867261a83d9cc5e1a3d117933eca360a1f8772001f6667e9ea7`  
		Last Modified: Mon, 24 Jan 2022 20:42:25 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
