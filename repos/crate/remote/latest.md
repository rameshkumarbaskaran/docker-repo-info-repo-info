## `crate:latest`

```console
$ docker pull crate@sha256:3da3f761952d46279cb35dd28d33f93fa36cce6cb7fe0dfb5d90e52d73c1d400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:878e27f2a6cade2760a9b65e840e1b095568a4d96625bde5c70e41bb7c2e2e6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370096375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33244aff8840432e394adcda8d92e07cfd3a7b33c63f5c39e51707c93aea3b55`
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
# Mon, 18 Jul 2022 18:28:23 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.0.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.0.0.tar.gz.asc crate-5.0.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.0.0.tar.gz.asc     && tar -xf crate-5.0.0.tar.gz -C /crate --strip-components=1     && rm crate-5.0.0.tar.gz
# Mon, 18 Jul 2022 18:28:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.28.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.28.0.asc crash_standalone_0.28.0     && rm -rf "$GNUPGHOME" crash_standalone_0.28.0.asc     && mv crash_standalone_0.28.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Mon, 18 Jul 2022 18:28:28 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 18:28:28 GMT
ENV CRATE_HEAP_SIZE=512M
# Mon, 18 Jul 2022 18:28:29 GMT
RUN mkdir -p /data/data /data/log
# Mon, 18 Jul 2022 18:28:29 GMT
VOLUME [/data]
# Mon, 18 Jul 2022 18:28:29 GMT
WORKDIR /data
# Mon, 18 Jul 2022 18:28:29 GMT
EXPOSE 4200 4300 5432
# Mon, 18 Jul 2022 18:28:29 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Mon, 18 Jul 2022 18:28:29 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Mon, 18 Jul 2022 18:28:29 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-07-13T09:51:35.203197 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.0.0
# Mon, 18 Jul 2022 18:28:30 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Mon, 18 Jul 2022 18:28:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 18 Jul 2022 18:28:30 GMT
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
	-	`sha256:41571d5ddc0bcdb9c306cc8a6a141b9c0775ba77d4ff170068de855142258a3b`  
		Last Modified: Mon, 18 Jul 2022 18:29:41 GMT  
		Size: 215.9 MB (215944045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78c99a0d78c17ac6f8968ebe72f29720ff288d6818d670bed811c71ace0c177`  
		Last Modified: Mon, 18 Jul 2022 18:29:20 GMT  
		Size: 1.7 MB (1710782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b68135d7d7d87ec0af46c96dab6ed30103e6afd40b86f87a3d0a48874de7eb`  
		Last Modified: Mon, 18 Jul 2022 18:29:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f819b050ed573d7026ea4980dbcb09ae6dea6d71aa10547843bc7a641be467`  
		Last Modified: Mon, 18 Jul 2022 18:29:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cbdcc0e47e7c92f3a1aeec075f36f291905da29ae032e5b9909fec56aa37c5`  
		Last Modified: Mon, 18 Jul 2022 18:29:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c1fdbb351a5f545a661b41ae8f335a06a67a7dcb5214655536549998532ba0`  
		Last Modified: Mon, 18 Jul 2022 18:29:20 GMT  
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
