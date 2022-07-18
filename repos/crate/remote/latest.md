## `crate:latest`

```console
$ docker pull crate@sha256:75b1b5cf9503041e5503ba55192656df55507c501d7dfbbc9164ab21d9a88bc4
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
$ docker pull crate@sha256:f65e95b04cc200518ef9ccf3eaa5c7e41acd58bf4b694962925db87af3408d49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 MB (668948921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53199102ef7a130acdf77852e75e4920db56a0608394971769531bd2ba428e3`
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
# Mon, 18 Jul 2022 17:42:45 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.0.tar.gz.asc crate-5.0.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.0.tar.gz.asc     && tar -xf crate-5.0.0.tar.gz -C /crate --strip-components=1     && rm crate-5.0.0.tar.gz
# Mon, 18 Jul 2022 17:42:49 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 18 Jul 2022 17:42:50 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 17:42:50 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 Jul 2022 17:42:52 GMT
RUN mkdir -p /data/data /data/log
# Mon, 18 Jul 2022 17:42:52 GMT
VOLUME [/data]
# Mon, 18 Jul 2022 17:42:53 GMT
WORKDIR /data
# Mon, 18 Jul 2022 17:42:54 GMT
EXPOSE 4200 4300 5432
# Mon, 18 Jul 2022 17:42:56 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 18 Jul 2022 17:42:57 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 18 Jul 2022 17:42:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-07-13T09:51:35.203197 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.0
# Mon, 18 Jul 2022 17:42:59 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 18 Jul 2022 17:42:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 17:43:00 GMT
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
	-	`sha256:16d6397259ac7b792bd8991b398a79880b657f2093721b5230b8e8d8a1534a72`  
		Last Modified: Mon, 18 Jul 2022 17:44:45 GMT  
		Size: 214.8 MB (214800767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22042fab7a6a4d78896e3fc484654f66a1e36bf2fb220b76929fb5d0d7417e`  
		Last Modified: Mon, 18 Jul 2022 17:44:23 GMT  
		Size: 1.7 MB (1709341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc8bae8af589e2b3e3822b73d1bcae31df1f71958c2747b57c6e16f454b529`  
		Last Modified: Mon, 18 Jul 2022 17:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e7494dfcba9e41b9cc8d53508f5915ce86afb8cfd0e4423a55719e6503e08f`  
		Last Modified: Mon, 18 Jul 2022 17:44:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1f84ae4d4a756942389c899f7f5bb73c38598a85bbfccaee73211b7218b8b2`  
		Last Modified: Mon, 18 Jul 2022 17:44:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ab81af010799e06aa6c7216550cfd1afcce4e9e390a7205bb8616fe8f1024e`  
		Last Modified: Mon, 18 Jul 2022 17:44:23 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
