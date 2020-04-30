## `crate:latest`

```console
$ docker pull crate@sha256:229b37a084e0501a2db3e31b9b6f3fb5bcae482c4bf0efcad3b18f0ba4b08c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:68a8251e2138cb7186bd2f2c376592029b986a569ec425faa99436a15b634d4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351038692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7b8112dd9380a6bdfbb56f65140a4965fa4e961f4cdcf68ffdffe3ad9e3353`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 Feb 2020 23:25:54 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 05 Feb 2020 23:25:54 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 05 Feb 2020 23:25:55 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 29 Apr 2020 20:19:52 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.5.tar.gz.asc crate-4.1.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.5.tar.gz.asc     && tar -xf crate-4.1.5.tar.gz -C /crate --strip-components=1     && rm crate-4.1.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 29 Apr 2020 20:19:55 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Apr 2020 20:19:55 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2020 20:19:55 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Apr 2020 20:19:56 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Apr 2020 20:19:56 GMT
VOLUME [/data]
# Wed, 29 Apr 2020 20:19:56 GMT
WORKDIR /data
# Wed, 29 Apr 2020 20:19:56 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Apr 2020 20:19:56 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Apr 2020 20:19:57 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Apr 2020 20:19:57 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-04-24T09:34:17.477377 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.5
# Wed, 29 Apr 2020 20:19:57 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 29 Apr 2020 20:19:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Apr 2020 20:19:57 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c132278b93b3443fafff8460382be10690caf0702bc22339ea0dd7b81d5cf8b`  
		Last Modified: Wed, 05 Feb 2020 23:31:07 GMT  
		Size: 196.4 MB (196423227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42807ee70d40e75fddd4f32ee923cedd85714cfe1339b0e13e317438a447e721`  
		Last Modified: Wed, 05 Feb 2020 23:28:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0e8a5e1dc25c1362920a3a1af7aad089113b32eb025ca51fa5e804d47e7019`  
		Last Modified: Wed, 29 Apr 2020 20:20:31 GMT  
		Size: 77.5 MB (77536391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf60ea610411891e4a2bf71dd0a79f09c5fc19f28bfee3c3299e34433493a9d`  
		Last Modified: Wed, 29 Apr 2020 20:20:16 GMT  
		Size: 1.3 MB (1294047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f701890e400eea453f5c5fe566292da59eb6656a679cc954c1a3e2abf31abbb`  
		Last Modified: Wed, 29 Apr 2020 20:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2feb7d0bbe91cff3634e0572c196029bfcad378574167e08e5a9d413d48a2e8b`  
		Last Modified: Wed, 29 Apr 2020 20:20:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f42727e14db9eb8ce06329d228b6ad78ac233066a9406676bfe5e9999b19a6`  
		Last Modified: Wed, 29 Apr 2020 20:20:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a50ef50ef8c12f06038601fcc0bb686f8e5b00323667dc8c1e2f1fe1dda58a5`  
		Last Modified: Wed, 29 Apr 2020 20:20:16 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:e774c3ca17900d70f7cfface29551c479ed90b41416799beb1c5e62b10c90ec7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.6 MB (376607067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deefec3670fc632405ef9c16b136587d6843e615725515a744204d691120ea61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:40:03 GMT
ADD file:8449a578596d0a7b4ce64f74355f602ee47b1a8782058356ae614cdcdf4639fb in / 
# Tue, 12 Nov 2019 00:40:05 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:40:06 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2020 23:45:29 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 Feb 2020 23:46:15 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 05 Feb 2020 23:46:17 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 05 Feb 2020 23:46:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Wed, 29 Apr 2020 20:40:35 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.5.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.5.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.5.tar.gz.asc crate-4.1.5.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.5.tar.gz.asc     && tar -xf crate-4.1.5.tar.gz -C /crate --strip-components=1     && rm crate-4.1.5.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Wed, 29 Apr 2020 20:40:40 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 29 Apr 2020 20:40:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2020 20:40:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 29 Apr 2020 20:40:43 GMT
RUN mkdir -p /data/data /data/log
# Wed, 29 Apr 2020 20:40:43 GMT
VOLUME [/data]
# Wed, 29 Apr 2020 20:40:44 GMT
WORKDIR /data
# Wed, 29 Apr 2020 20:40:45 GMT
EXPOSE 4200 4300 5432
# Wed, 29 Apr 2020 20:40:45 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 29 Apr 2020 20:40:46 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 29 Apr 2020 20:40:46 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-04-24T09:34:17.477377 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.5
# Wed, 29 Apr 2020 20:40:47 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Wed, 29 Apr 2020 20:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Apr 2020 20:40:48 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3f2696f8166ff69dd0c116674b19eebd351ed3fc4111a42dbd57c673601c725d`  
		Last Modified: Tue, 12 Nov 2019 00:40:46 GMT  
		Size: 103.6 MB (103619629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11d48e7bd36dbc63110f197eefe11eb9a4f505370153c386e5938d14144b04`  
		Last Modified: Fri, 07 Feb 2020 17:42:20 GMT  
		Size: 2.3 KB (2262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d6743359dfaf8645137afd31a4552eb3195971517a48fca57593b25250b015`  
		Last Modified: Tue, 18 Feb 2020 22:42:08 GMT  
		Size: 196.4 MB (196423249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf4a3a653abc3f2a5931326c03e9ef927aec2a7ab30aa4fcc311b69d41fa57c`  
		Last Modified: Tue, 18 Feb 2020 22:41:34 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d44db711bd59f380132e443fd0f5d302b918c7403b60ce4015a2c7fd2fdf36`  
		Last Modified: Wed, 29 Apr 2020 20:42:13 GMT  
		Size: 75.3 MB (75265760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61df5e229c88a101b9afb8d177c0c8d99e8fa0dae7c4b0ab96a427f6918ad8d`  
		Last Modified: Wed, 29 Apr 2020 20:41:54 GMT  
		Size: 1.3 MB (1294048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083453394b77103728941617a40356b30d891cc6ff98ede5f99e6872e410c0ad`  
		Last Modified: Wed, 29 Apr 2020 20:41:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64877c49fd0b3a40e79b6dc20c9b94c1c9e5f7d87812f7975a5696ccde3e92f5`  
		Last Modified: Wed, 29 Apr 2020 20:41:54 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2aef3e7905129338d39beed970c46d3caad8bb7b41d8a0894fac1fb5d529f6`  
		Last Modified: Wed, 29 Apr 2020 20:41:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824b6281a2daaf5ced67897db9e0da661280d49740a8a3b980e86573693562d5`  
		Last Modified: Wed, 29 Apr 2020 20:41:53 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
