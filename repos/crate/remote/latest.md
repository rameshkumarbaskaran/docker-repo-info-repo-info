## `crate:latest`

```console
$ docker pull crate@sha256:f9ba56b418964bf6736cfdb9f66f2cf68cdd90305cabd066fd9b6c08292ef2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:460a85d8888e4955ee942cd5871e0c1645053110752a869a96af4cde6ca48e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324751510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f173a79e7f82c0f7c0899f0b694ea14be06e91955b5d6d9aa2a7abd8ee91bf8`
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
# Wed, 16 Mar 2022 00:23:53 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.1.tar.gz.asc crate-4.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.1.tar.gz.asc     && tar -xf crate-4.7.1.tar.gz -C /crate --strip-components=1     && rm crate-4.7.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:24:25 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:24:25 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:24:25 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:24:26 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:24:26 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:24:26 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:24:26 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:24:26 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:24:26 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:24:26 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T16:30:11.824373 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.1
# Wed, 16 Mar 2022 00:24:26 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:24:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:24:26 GMT
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
	-	`sha256:8f77f0d18bdc11c68a11bc644e13201dd629f2c66e5ef3478f992650e7bf6590`  
		Last Modified: Wed, 16 Mar 2022 00:27:21 GMT  
		Size: 247.1 MB (247068013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d967b63911224866915a50dfe0a474f374da6660e736614074227f3fbc52250`  
		Last Modified: Wed, 16 Mar 2022 00:26:59 GMT  
		Size: 1.6 MB (1582198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0179ddcc992ef7de07c187731e346bdd54d6437907b9331b446a7130de76ef`  
		Last Modified: Wed, 16 Mar 2022 00:26:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f3f518b0ebba12b35e2bacef78080928cf9d576076f51b71525f242692ef9c`  
		Last Modified: Wed, 16 Mar 2022 00:26:59 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f5ace285a2c62a6dd4ff7f4ff1f424a1fec3dffc8213f01af30cac554ded7a`  
		Last Modified: Wed, 16 Mar 2022 00:27:00 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a516f1a94d04e4baf277e0d5dad6ceb176fe6b64d3992f6ebe22940ead6622fa`  
		Last Modified: Wed, 16 Mar 2022 00:26:59 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:99e9f7eeb1a701fda3117cbe6dc7d50d064a0f6eebc4e1346bc3ea74d68b4f26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.1 MB (353061515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0758dea32fc3945f22508d10fcff5dda2db90bc6d3d53e6d6c10432456000b40`
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
# Wed, 16 Mar 2022 00:46:04 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.7.1.tar.gz.asc crate-4.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.7.1.tar.gz.asc     && tar -xf crate-4.7.1.tar.gz -C /crate --strip-components=1     && rm crate-4.7.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 16 Mar 2022 00:46:43 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 16 Mar 2022 00:46:43 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Mar 2022 00:46:44 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 16 Mar 2022 00:46:46 GMT
RUN mkdir -p /data/data /data/log
# Wed, 16 Mar 2022 00:46:46 GMT
VOLUME [/data]
# Wed, 16 Mar 2022 00:46:47 GMT
WORKDIR /data
# Wed, 16 Mar 2022 00:46:48 GMT
EXPOSE 4200 4300 5432
# Wed, 16 Mar 2022 00:46:50 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 16 Mar 2022 00:46:51 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 16 Mar 2022 00:46:51 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2022-03-10T16:30:11.824373 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.7.1
# Wed, 16 Mar 2022 00:46:53 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 16 Mar 2022 00:46:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Mar 2022 00:46:54 GMT
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
	-	`sha256:b0ca9816a1aba631dd98a433c6070d9cd6bc22c2f4ab68c69258ba070898860c`  
		Last Modified: Wed, 16 Mar 2022 00:50:49 GMT  
		Size: 243.1 MB (243101933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a58c88c94759b27d57067b30ae59a6469d51f77511e21a6cc3efdb6c543173`  
		Last Modified: Wed, 16 Mar 2022 00:50:24 GMT  
		Size: 1.6 MB (1580578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b79b859b4c8cb1651b5bd7a329efbf1abc3073bd2efd940ea78b5947bdd6fbf`  
		Last Modified: Wed, 16 Mar 2022 00:50:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75da89ebc54d6d04c289cfc14fbf751af4466837cfa0fd35ddc925d4a120565`  
		Last Modified: Wed, 16 Mar 2022 00:50:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dcffb4d03a51f238dd95a23f58c2691a6f5a92e23aaf5950e0df38280d2bb4`  
		Last Modified: Wed, 16 Mar 2022 00:50:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6a83957f8a29287b5964214e7eaaf1ed4ee01bd5ebe48bacffe8ac0e217e27`  
		Last Modified: Wed, 16 Mar 2022 00:50:23 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
