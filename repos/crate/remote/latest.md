## `crate:latest`

```console
$ docker pull crate@sha256:599ba05614d34a3513780fac13962bf1c3723a2907ec51e0403777a9b916b051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:1627a8e2e4fa3d621fb82ee16cbcc6ece41f902ca68d07f98ec288b0e69172d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350985313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004cdaadfd54d25698b2c6c5a7d8395cb39042d1a00c629e3de14a8c17c893ff`
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
# Tue, 24 Mar 2020 23:19:55 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.4.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.4.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.4.tar.gz.asc crate-4.1.4.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.4.tar.gz.asc     && tar -xf crate-4.1.4.tar.gz -C /crate --strip-components=1     && rm crate-4.1.4.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 24 Mar 2020 23:19:55 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 24 Mar 2020 23:19:55 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 24 Mar 2020 23:19:58 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 24 Mar 2020 23:19:59 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Mar 2020 23:19:59 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 24 Mar 2020 23:20:00 GMT
RUN mkdir -p /data/data /data/log
# Tue, 24 Mar 2020 23:20:00 GMT
VOLUME [/data]
# Tue, 24 Mar 2020 23:20:00 GMT
WORKDIR /data
# Tue, 24 Mar 2020 23:20:00 GMT
EXPOSE 4200 4300 5432
# Tue, 24 Mar 2020 23:20:00 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 24 Mar 2020 23:20:01 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 24 Mar 2020 23:20:01 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-03-20T11:37:45.220429 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.4
# Tue, 24 Mar 2020 23:20:01 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 24 Mar 2020 23:20:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Mar 2020 23:20:01 GMT
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
	-	`sha256:3a53fc6580d863dc300787f8abe7f3aec9ea5fa0b9162ef0006f25bc47c68da8`  
		Last Modified: Tue, 24 Mar 2020 23:20:27 GMT  
		Size: 77.5 MB (77481783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fdb5ce574afff4d9bc48e418c5c746b279b015331e663fdeeadb7dac448f57`  
		Last Modified: Tue, 24 Mar 2020 23:20:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979fdf3de1dc06bca1c468ed7936ea6679bd13950664c65ec1e7274f5547d4ff`  
		Last Modified: Tue, 24 Mar 2020 23:20:16 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb73e277707e9429986708b4fedb0bc212ac27f47868ee5d0bbabe947709ca`  
		Last Modified: Tue, 24 Mar 2020 23:20:15 GMT  
		Size: 1.3 MB (1294055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9ab38e5cadc75d39dbba980aa0bc8dd04362e8772a82e556212ad3b832e1d2`  
		Last Modified: Tue, 24 Mar 2020 23:20:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60b5292df9c5a712e4130ed626d6a4de48aa0ff9a295cba558eac0b116148b2`  
		Last Modified: Tue, 24 Mar 2020 23:20:15 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46096a9d919ebda16a3d95e208b8a8903f6b5c1d5395bc5d281e0a00b23f52fc`  
		Last Modified: Tue, 24 Mar 2020 23:20:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd7d0076a916d6d468d8cbcd08a37b3baa6b091311e8f61f12d02a9c9c038f9`  
		Last Modified: Tue, 24 Mar 2020 23:20:15 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:4f685723060cfe366068b916eb03cf578c13b580f1d31ce8e081bbcd2212d16e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.5 MB (376519154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee220ddd7668e6b737f0151b642eabb7c53badd0b6c7f79e5ef07945c17b7886`
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
# Tue, 10 Mar 2020 22:40:22 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.3.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.3.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.3.tar.gz.asc crate-4.1.3.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.3.tar.gz.asc     && tar -xf crate-4.1.3.tar.gz -C /crate --strip-components=1     && rm crate-4.1.3.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 10 Mar 2020 22:40:23 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 10 Mar 2020 22:40:24 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 10 Mar 2020 22:40:28 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 10 Mar 2020 22:40:29 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2020 22:40:30 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 10 Mar 2020 22:40:34 GMT
RUN mkdir -p /data/data /data/log
# Tue, 10 Mar 2020 22:40:34 GMT
VOLUME [/data]
# Tue, 10 Mar 2020 22:40:35 GMT
WORKDIR /data
# Tue, 10 Mar 2020 22:40:36 GMT
EXPOSE 4200 4300 5432
# Tue, 10 Mar 2020 22:40:36 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 10 Mar 2020 22:40:37 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 10 Mar 2020 22:40:37 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-03-05T16:12:47.636379 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.3
# Tue, 10 Mar 2020 22:40:38 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 10 Mar 2020 22:40:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2020 22:40:39 GMT
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
	-	`sha256:01c025dc6cae10e94b36345eae35e138b3d898339e1fafc5f1aaf04abf387029`  
		Last Modified: Tue, 10 Mar 2020 22:42:36 GMT  
		Size: 75.2 MB (75176628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fd59b598b1afc1dfc052ee06e3ed3a308f9b17f265f45d0ed5418317b45767`  
		Last Modified: Tue, 10 Mar 2020 22:42:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a29188fe4b021a4a54bfd4c4eccd656a33c8599c5d626b2a5d64ccb2f69c0ce`  
		Last Modified: Tue, 10 Mar 2020 22:42:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843db5a229fae94ebe225592d1b3fb40d23a38234016a09d611b22f8b0d0e2a`  
		Last Modified: Tue, 10 Mar 2020 22:42:21 GMT  
		Size: 1.3 MB (1294047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8640a32f3360eef8222cadc0ff902e6f3790ee8d0fdc5e844ab7ed0ea4dee152`  
		Last Modified: Tue, 10 Mar 2020 22:42:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c1668cf596c3f71fced564351c6301af1ef0bc58ebb1edd70f4e29bd1f5279`  
		Last Modified: Tue, 10 Mar 2020 22:42:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007438d52e9d66e1da7d2546f538ea4a0c333af127388d120d2b1f93384ede40`  
		Last Modified: Tue, 10 Mar 2020 22:42:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29f520775899774c3898bd17958f4d73322c8506f45e94be6955092c72eeccb`  
		Last Modified: Tue, 10 Mar 2020 22:42:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
