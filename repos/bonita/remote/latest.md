## `bonita:latest`

```console
$ docker pull bonita@sha256:a3431853b62272dc92a2aaaa18ca36f361c1b9634db7c3f35573547b493c7ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:55ca1a9d6556fab9f400b6a0565b3c448001e3e3be78d0c50082535b49e46875
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234283153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f010c6ada2daea1e12693d8443503cd20713a6d814b0ffdac584f9fbee6af60b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 20:59:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:00:28 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 21:00:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 21:00:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 21:00:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 21:00:34 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 21:00:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 21:00:39 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 21:00:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 21:00:42 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 21:00:42 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 21:00:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 21:00:42 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 21:00:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d558549b4f088b12d8d7f40183737f64e2b8b1b581e31b0cf6b7ba33c2a098`  
		Last Modified: Fri, 06 Nov 2020 21:01:16 GMT  
		Size: 93.7 MB (93657145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299279f6c2b963e1562e7f9eb3cfc08844ff4d84495b349a6a8480ab82aecf99`  
		Last Modified: Fri, 06 Nov 2020 21:01:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03f489aa47259b29756fe7ac1f4d93e5a96edea681717f708959736293a`  
		Last Modified: Fri, 06 Nov 2020 21:01:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865a4bf2da9c5ec77ebe85db3355479835300324f57ca4192457b8bf80d6b03`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71f3c965e2fe6c75ece21941927f0255357fb223e0daf65e23deb5283a02062`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab813df46746aeb6b728a516026c5a9578c2a73884bf9e386653cc5603844424`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0d6b79b05f0f06e86b2587159296c4e1d5b1eec758ee885e3d2f1fa3e17fc`  
		Last Modified: Fri, 06 Nov 2020 21:01:05 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823aa99640d53270b3a4aa212ea68c84da33931f1acc06fc11db5d7a390aa8c8`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:106a80c8216682511f2d9a6a2058c9ab5f2d56ae7e63c328305b0295dfc7bcae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222609386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93788c20a795fab12f1a2ac04a5fb6b30e50120f784f624ba984392d45118ce`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 21:04:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:04:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:04:55 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 21:04:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 21:05:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 21:05:00 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 21:05:01 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 21:05:02 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 21:05:02 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 21:05:03 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 21:05:03 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 21:05:04 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:05:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 21:05:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:05:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 21:05:08 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 21:05:09 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 21:05:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 21:05:15 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 21:05:18 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 21:05:18 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 21:05:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 21:05:19 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 21:05:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccc47d6559a5f5cea930f2e5d08e93e59740925d521ff132fd9ce1b2b8e2c4c`  
		Last Modified: Fri, 06 Nov 2020 21:05:54 GMT  
		Size: 85.0 MB (84992521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abce4c7f048fe7775408eab733dbeca9bde2ad98a6fffcd68b9cd63c3653c819`  
		Last Modified: Fri, 06 Nov 2020 21:05:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456116fef93e5c00527ab441b37e07cfa8043033934bcf90c1f2225fced33722`  
		Last Modified: Fri, 06 Nov 2020 21:05:33 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a77190de68efde4d58aebca857642d65b3e7eb90861cdd3c2be06bf50b8f75`  
		Last Modified: Fri, 06 Nov 2020 21:05:32 GMT  
		Size: 541.8 KB (541822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fee60e70f6a3e04a603b42ca5308e5641a41de7ab68137c17821a5f98c4ebf5`  
		Last Modified: Fri, 06 Nov 2020 21:05:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374e5efc498aae379e29ca17a04b5cfc6e186e7b25f82ca0e0574fba8fc4c583`  
		Last Modified: Fri, 06 Nov 2020 21:05:32 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6cc8d10b8c0453c40094443963010540c2a47c9508ae7b69136df0fdf0e15`  
		Last Modified: Fri, 06 Nov 2020 21:05:47 GMT  
		Size: 113.3 MB (113340347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b463caea2b21bf6a6f24015c5b864e2b469da6a5ce250ca55b688d29e81e6db`  
		Last Modified: Fri, 06 Nov 2020 21:05:32 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:ad224a8bb29770bd7bd2f1cc15c1e826143aa81f4a0dc3735c10d98c15371673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239218858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742115eac1b29d82ebed955d3f45663bb43de88da5db663ff27bebb26b864dc4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Fri, 02 Oct 2020 21:20:48 GMT
ENV BONITA_VERSION=7.11.2
# Fri, 02 Oct 2020 21:21:01 GMT
ENV BONITA_SHA256=36dca45fed326d700fddc52edc4efe2a14bc1111b2952fc0001047df9cf7a67a
# Fri, 02 Oct 2020 21:21:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Oct 2020 21:21:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.2/BonitaCommunity-7.11.2.zip
# Fri, 02 Oct 2020 21:21:35 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 02 Oct 2020 21:21:53 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:22:11 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:22:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 02 Oct 2020 21:22:34 GMT
VOLUME [/opt/bonita]
# Fri, 02 Oct 2020 21:22:42 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 02 Oct 2020 21:22:46 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 02 Oct 2020 21:22:50 GMT
EXPOSE 8080
# Fri, 02 Oct 2020 21:22:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb9a8374541e94b5f735d7f0fcf5dcb0847b2d4b4a2a9b71ceb42a3183c7920`  
		Last Modified: Fri, 02 Oct 2020 21:23:49 GMT  
		Size: 113.2 MB (113238282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2a0a4126af1d57a14a6f19cfe78d56ba7102784d25c0b6404dc3ed14dbac74`  
		Last Modified: Fri, 02 Oct 2020 21:23:42 GMT  
		Size: 7.7 KB (7662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78625b5911c1a1fe3e37ee04c4494493a856db2698006f27481ad6b802a6ba4`  
		Last Modified: Fri, 02 Oct 2020 21:23:42 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
