## `crate:latest`

```console
$ docker pull crate@sha256:542b9de0c230dfe4cea4babfa342c3465f4df101a97e82b0986336a166f79832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:9578962499fc4bf036c2978e3108987b556f4557cfa9093a096a9dc858395d77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277468494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73da05c8bdfc04167bc12661ced7d422963a24310b03e381d612e84101da5a46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 19:19:57 GMT
ADD file:bb680be7279e885f13401f2d43d5f3a04e577d5358a84c769a7bedf7a4891531 in / 
# Tue, 11 Apr 2023 19:19:58 GMT
CMD ["/bin/bash"]
# Fri, 14 Apr 2023 21:51:31 GMT
RUN microdnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && microdnf clean all     && rm -rf /var/cache/yum
# Fri, 14 Apr 2023 21:51:53 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.3.0.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.3.0.tar.gz.asc crate-5.3.0.tar.gz     && rm -rf "$GNUPGHOME" crate-5.3.0.tar.gz.asc     && tar -xf crate-5.3.0.tar.gz -C /crate --strip-components=1     && rm crate-5.3.0.tar.gz
# Fri, 14 Apr 2023 21:51:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Fri, 14 Apr 2023 21:51:58 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Apr 2023 21:51:58 GMT
ENV CRATE_HEAP_SIZE=512M
# Fri, 14 Apr 2023 21:51:59 GMT
RUN mkdir -p /data/data /data/log
# Fri, 14 Apr 2023 21:51:59 GMT
VOLUME [/data]
# Fri, 14 Apr 2023 21:51:59 GMT
WORKDIR /data
# Fri, 14 Apr 2023 21:51:59 GMT
EXPOSE 4200 4300 5432
# Fri, 14 Apr 2023 21:51:59 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Fri, 14 Apr 2023 21:51:59 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Fri, 14 Apr 2023 21:51:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-04T15:04:59.126585 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.3.0
# Fri, 14 Apr 2023 21:51:59 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Fri, 14 Apr 2023 21:51:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Apr 2023 21:51:59 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f587440817f7c56198a3cc9df5d654dd56b5394b2a2a83cf5e2fb635046f2f9`  
		Last Modified: Tue, 11 Apr 2023 19:21:15 GMT  
		Size: 33.5 MB (33467186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b97aefb6e6d3b744fe84d6f5149e898a47563ccc4db07bbd90f3d1b0174a2d`  
		Last Modified: Fri, 14 Apr 2023 21:52:18 GMT  
		Size: 14.8 MB (14824560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbb604bcbab3de99f71519a657d82145cb3f23171f1ee9183c4c3473e7245ce`  
		Last Modified: Fri, 14 Apr 2023 21:52:31 GMT  
		Size: 227.3 MB (227317743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0606117830f475881dfa7794de89790ccf02926ee1d4b640e13dc43e4e22bf`  
		Last Modified: Fri, 14 Apr 2023 21:52:14 GMT  
		Size: 1.9 MB (1857120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051dbacd53d77acac3cb2779f706e670b3d9fc9124b176237bfa8bc2658320c1`  
		Last Modified: Fri, 14 Apr 2023 21:52:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92edd0ba6435e48db4f6ba103f9fca5b1e9302d0ac2f8e965c85cab3d7338149`  
		Last Modified: Fri, 14 Apr 2023 21:52:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790aca4b4e1fc2a572672f5e232be434f2de9c6856829b3ffad380f1a8e7a15`  
		Last Modified: Fri, 14 Apr 2023 21:52:14 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10e743b1eb7795a2222ac1c17b8d43e6a93f84b8964986b10e07f9449446989`  
		Last Modified: Fri, 14 Apr 2023 21:52:13 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:b2cd329fc48c2ff5445d4560ae947564420fc55db37e528357365698310c124f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303426631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cce886f489a0b26e0a0a546c2daecb3ebed543c6c5dcc66adf22d84b4b058cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 11 Apr 2023 20:06:33 GMT
ADD file:389251b1d16989bef7dd304f924df38271d5e1140aca5e6a76aca2a98db3914b in / 
# Tue, 11 Apr 2023 20:06:35 GMT
CMD ["/bin/bash"]
# Tue, 11 Apr 2023 20:23:16 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python3 python3-pip     && yum clean all     && rm -rf /var/cache/yum
# Wed, 12 Apr 2023 19:24:30 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.2.6.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.2.6.tar.gz.asc crate-5.2.6.tar.gz     && rm -rf "$GNUPGHOME" crate-5.2.6.tar.gz.asc     && tar -xf crate-5.2.6.tar.gz -C /crate --strip-components=1     && rm crate-5.2.6.tar.gz
# Wed, 12 Apr 2023 19:24:34 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.29.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.29.0.asc crash_standalone_0.29.0     && rm -rf "$GNUPGHOME" crash_standalone_0.29.0.asc     && mv crash_standalone_0.29.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 12 Apr 2023 19:24:35 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 19:24:35 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 12 Apr 2023 19:24:35 GMT
RUN mkdir -p /data/data /data/log
# Wed, 12 Apr 2023 19:24:35 GMT
VOLUME [/data]
# Wed, 12 Apr 2023 19:24:35 GMT
WORKDIR /data
# Wed, 12 Apr 2023 19:24:35 GMT
EXPOSE 4200 4300 5432
# Wed, 12 Apr 2023 19:24:35 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 12 Apr 2023 19:24:36 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 12 Apr 2023 19:24:36 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2023-04-04T08:45:48.121205 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.2.6
# Wed, 12 Apr 2023 19:24:36 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 12 Apr 2023 19:24:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 19:24:36 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:8bdbb90acb62176a24ad70eb522992bed0fbe2c7a53633cc96327b2ec7fa80cc`  
		Last Modified: Tue, 11 Apr 2023 20:07:38 GMT  
		Size: 68.3 MB (68265081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467cf7edb3b9c6580c686624142f9e30588104828318064248595eb719e98539`  
		Last Modified: Tue, 11 Apr 2023 20:23:58 GMT  
		Size: 7.4 MB (7446001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214e6f8c21a7f549f7f9522dc668d9afa8eddfbcdff16b2768522961b03e7191`  
		Last Modified: Wed, 12 Apr 2023 19:25:08 GMT  
		Size: 225.9 MB (225856544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b00917f5db375842be6901b98e1fd9a64220def41b26fd062737b2530eabd8`  
		Last Modified: Wed, 12 Apr 2023 19:24:53 GMT  
		Size: 1.9 MB (1857122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d96a0a3c32879486eb87465085870437051b7c741e7c0a6ae49e66e1705df`  
		Last Modified: Wed, 12 Apr 2023 19:24:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ae2be876aa966b99ca05bd564d6d4a0e56fb52577edfbffa47d094268b8f08`  
		Last Modified: Wed, 12 Apr 2023 19:24:52 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce4b41a3ee697a992c0da59a73006308d0a9f6e7b26c8e3cd68a7b3c3bea562`  
		Last Modified: Wed, 12 Apr 2023 19:24:52 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569a9dcc15b4fa06d4751a2d26c7537b0f6a4cd7ead883d1927586ddd8af071e`  
		Last Modified: Wed, 12 Apr 2023 19:24:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
