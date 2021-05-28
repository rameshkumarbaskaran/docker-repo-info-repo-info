<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:7.10`](#bonita710)
-	[`bonita:7.10.6`](#bonita7106)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:8113752c97289f12d5d55a4e76badbecb7c359a78cc17e72f54ff755029c9b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:63f4da2e997b34d49a2bc949131f22223da06951022c91c2f36c5a0067689284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237166322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcec19c862fafa66ff6c77648e515c0271302e57956fd0eec416c9f6be53cef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BRANDING_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 19 May 2021 20:14:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:27 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:27 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 19 May 2021 20:14:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:34 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:35 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde9f1c4141e1669d1a0e2519d764cad7f449449982e491985dd53b630ad8bd7`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb97c41865a896652c4cede2d5eb40e68da7d6e09d9fa3687a91aaca1538818`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422680249022a137b3ee3c7e55fcb17684b964168027efde3fdc99ba54eaab0`  
		Last Modified: Wed, 19 May 2021 20:15:55 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadf73b07057fbe22df11b5d3bcb82de5833d388cc7a037acf64b761fc4845b2`  
		Last Modified: Wed, 19 May 2021 20:15:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7fd673d2147f65e83f33920d8a59aad589b5ec0e5a6dffa4a3b092609f0893e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226259506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41b78a5cb1419c42fcb5a82ce7874885509252b7f76ec699d6c83dd5874983`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BRANDING_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:21 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:21 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 27 May 2021 20:29:21 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 27 May 2021 20:29:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:24 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:24 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 27 May 2021 20:29:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:30 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:30 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:30 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff64345f45a7c6f5a0e5440d74097431a65977231dd433a1727a61cdda9cd45b`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7109a355f58af2dcd3a27abb6bad4308dc7c02c0f6ca9652e506efc5578be3`  
		Last Modified: Thu, 27 May 2021 20:30:57 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce827a5d52f64fcfbc814d6395f915dab4391cc44f353a5495a0bbfe6ecad03c`  
		Last Modified: Thu, 27 May 2021 20:31:03 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fababb011508b77f359f5a90341eb8910ffe50b464820efa2dd41a3873ddc6a`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:09da2c521e70bac97002559c1ffe9aa27945133ad024f1b4dcaf09045d8fa1fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233771062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61d43b322fa845c74b454e498eacf30dfe3dc8c8f6ffe8ea879a1a9f20788d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:43:33 GMT
ARG BRANDING_VERSION
# Thu, 20 May 2021 00:43:41 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:43:47 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:43:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:44:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 20 May 2021 00:44:12 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 20 May 2021 00:44:17 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 20 May 2021 00:44:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:44:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:44:51 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:44:56 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 20 May 2021 00:45:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 20 May 2021 00:45:39 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:46:05 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:46:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:46:14 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:46:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc9951f8a6e042d6aa4d540a3c257fdc84113e4220e55017795b2f7ab3f2b`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e36ed62d5e55e1a0a7ee290d0eee7d9eebadfa7ed944102b57bbb72a0dd572`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b015e0aea1f89925140ec99156b48900b70ecd46a6fe170c7e58634db6db82d`  
		Last Modified: Thu, 20 May 2021 00:48:08 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55048bca738773475353787939d3fec3a7e0b9f77c543fe7b5cf2aead1f`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:6cbf02da911ac92d6073b37d872f1afae1ffee67f83ce6cb450f94b2dbfff435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:566dad9e189e003b89a292db74bf332bb0a87095fa726ec51f57321b65c10cdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242284249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9948fdc9c248818ebef8318078212ce3940765f8a168019b0221f68a1486a3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:12:00 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 19 May 2021 20:13:18 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:13:20 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:13:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:13:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:13:23 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:13:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:13:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:13:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:13:24 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 19 May 2021 20:13:24 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 19 May 2021 20:13:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:13:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 19 May 2021 20:13:26 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 19 May 2021 20:13:29 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 19 May 2021 20:13:31 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 19 May 2021 20:13:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 19 May 2021 20:13:32 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:13:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 19 May 2021 20:13:33 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 19 May 2021 20:13:33 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:13:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693024d29053f2d150bb5f3b3ccda264ff08a6826dd8a4f2174cb69076b289b7`  
		Last Modified: Wed, 19 May 2021 20:15:10 GMT  
		Size: 117.0 MB (117028565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118948c29b6e1513593d05a4ea3ac36775dbee53f6f708ac10231d2375291499`  
		Last Modified: Wed, 19 May 2021 20:14:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651abb0412851146db66d0fe7a2d1d47b3f9f9902c8c189aaadbf44832cf2623`  
		Last Modified: Wed, 19 May 2021 20:14:51 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87d1b35bb77a0339143c700bedbebf21dda2e87412c5c2026046abe63ef522`  
		Last Modified: Wed, 19 May 2021 20:14:52 GMT  
		Size: 573.0 KB (572999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cabf58783a9f98d846a195434991c110af5022046af04c69016292232f02bd8`  
		Last Modified: Wed, 19 May 2021 20:14:56 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284b0374a2d0768fd8ef2dc33bf690ddc2d848e4ac5dab6559fd750a997af5ae`  
		Last Modified: Wed, 19 May 2021 20:14:51 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da34787771304b4436cd1b380eea367f5b1937fccc1c49b3fd6b0f49fb4a0a`  
		Last Modified: Wed, 19 May 2021 20:14:52 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:1ee9087f31babf5f73e6a9353181d6ab20e9e8d8964c3e82761396afcf5b554a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230965805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e9330e258d04f6510d7640751225eda12ac17b2ba1948bce40f05707289560`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:27:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 27 May 2021 20:28:12 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:14 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:28:16 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:28:16 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:28:16 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:28:17 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:28:17 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 27 May 2021 20:28:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 27 May 2021 20:28:18 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 27 May 2021 20:28:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 27 May 2021 20:28:23 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 27 May 2021 20:28:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 27 May 2021 20:28:24 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:28:24 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 27 May 2021 20:28:24 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 27 May 2021 20:28:24 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:28:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190d40c6f5fe8a6b363738833b2a20223d4cbb5e712ef27346ef6117e96711a8`  
		Last Modified: Thu, 27 May 2021 20:30:16 GMT  
		Size: 108.7 MB (108733632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2665a0a3016d2858fe2062286bec4bdc073ce7f17eabeb0a6e59fed0db3734`  
		Last Modified: Thu, 27 May 2021 20:30:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa767a15e8863c4b774fb02de6b5439ed63166db172c95fdcb42b0f28c26e2`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3b7d5d7d4d6189e0fe9946532bfb02c4e7afe6044e8af1bdac4dfe0aa362e3`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 542.5 KB (542481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abba1bd40515a8b1c80b84d0ca4510426fd3d496ba551bbbb3e25d429c29af75`  
		Last Modified: Thu, 27 May 2021 20:30:04 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c37ec64abddaacb30cfcc915197fe977815f8c9a17b4f8023a17330f0db6299`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a077af30d23f0da3953944b8b000e220b31eacace64b36eee4674880130c86b`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:9a489b0919f8f1c664f1c9ad2c02d0c829cc244e1313865fd1a1b2e3adc6b7b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240247814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5746192bc425b7fcac5324c069409888237e3fe83a9e7c803513bc6f96c480`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:21:56 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 20 May 2021 00:31:59 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:32:12 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:32:31 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:32:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:32:50 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:32:55 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:33:03 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:33:05 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:33:10 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 20 May 2021 00:33:13 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 20 May 2021 00:33:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:33:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 20 May 2021 00:33:33 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 20 May 2021 00:33:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 20 May 2021 00:33:57 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 20 May 2021 00:34:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 20 May 2021 00:34:17 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:34:24 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 20 May 2021 00:34:27 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 20 May 2021 00:34:32 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:34:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d3625bf57aa986338173635f8c468a0b3baebb7cb06bcf800cf33ea59243e`  
		Last Modified: Thu, 20 May 2021 00:47:16 GMT  
		Size: 111.3 MB (111312376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70ddc65d68cd15a96d0138a966744a96e6f5f6d6e421d9e716c9d1fee58b402`  
		Last Modified: Thu, 20 May 2021 00:46:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d173c200e8e4c7d2bb8c65ff705b249d5f79a3169a1f659d604db8783c45d7ea`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c697cbb4143f247d5153cf82bd3730d843468e9b25da63fc50bf22fc560f9662`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8b327423d02ef49d83307155cf593fb3c1714c6ef2a349c5ce4e6a4c8dc556`  
		Last Modified: Thu, 20 May 2021 00:47:00 GMT  
		Size: 98.0 MB (97973964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea1f02f4df72a5e3b6ad0034411153e944bcab25a3794c1ab5fd5f0fd8bc7f`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27f15cf915ec8b010be881a6bab1acf880f036663afbc042282d19259ef8773`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:6cbf02da911ac92d6073b37d872f1afae1ffee67f83ce6cb450f94b2dbfff435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:566dad9e189e003b89a292db74bf332bb0a87095fa726ec51f57321b65c10cdf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242284249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9948fdc9c248818ebef8318078212ce3940765f8a168019b0221f68a1486a3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:12:00 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 19 May 2021 20:13:18 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:13:20 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:13:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:13:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:13:23 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:13:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:13:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:13:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:13:24 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 19 May 2021 20:13:24 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 19 May 2021 20:13:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:13:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 19 May 2021 20:13:26 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 19 May 2021 20:13:29 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 19 May 2021 20:13:31 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 19 May 2021 20:13:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 19 May 2021 20:13:32 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:13:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 19 May 2021 20:13:33 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 19 May 2021 20:13:33 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:13:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693024d29053f2d150bb5f3b3ccda264ff08a6826dd8a4f2174cb69076b289b7`  
		Last Modified: Wed, 19 May 2021 20:15:10 GMT  
		Size: 117.0 MB (117028565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118948c29b6e1513593d05a4ea3ac36775dbee53f6f708ac10231d2375291499`  
		Last Modified: Wed, 19 May 2021 20:14:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651abb0412851146db66d0fe7a2d1d47b3f9f9902c8c189aaadbf44832cf2623`  
		Last Modified: Wed, 19 May 2021 20:14:51 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87d1b35bb77a0339143c700bedbebf21dda2e87412c5c2026046abe63ef522`  
		Last Modified: Wed, 19 May 2021 20:14:52 GMT  
		Size: 573.0 KB (572999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cabf58783a9f98d846a195434991c110af5022046af04c69016292232f02bd8`  
		Last Modified: Wed, 19 May 2021 20:14:56 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284b0374a2d0768fd8ef2dc33bf690ddc2d848e4ac5dab6559fd750a997af5ae`  
		Last Modified: Wed, 19 May 2021 20:14:51 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da34787771304b4436cd1b380eea367f5b1937fccc1c49b3fd6b0f49fb4a0a`  
		Last Modified: Wed, 19 May 2021 20:14:52 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:1ee9087f31babf5f73e6a9353181d6ab20e9e8d8964c3e82761396afcf5b554a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230965805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e9330e258d04f6510d7640751225eda12ac17b2ba1948bce40f05707289560`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:27:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 27 May 2021 20:28:12 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:14 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:28:16 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:28:16 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:28:16 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:28:17 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:28:17 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 27 May 2021 20:28:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:28:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 27 May 2021 20:28:18 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 27 May 2021 20:28:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 27 May 2021 20:28:23 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 27 May 2021 20:28:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 27 May 2021 20:28:24 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:28:24 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 27 May 2021 20:28:24 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 27 May 2021 20:28:24 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:28:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190d40c6f5fe8a6b363738833b2a20223d4cbb5e712ef27346ef6117e96711a8`  
		Last Modified: Thu, 27 May 2021 20:30:16 GMT  
		Size: 108.7 MB (108733632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2665a0a3016d2858fe2062286bec4bdc073ce7f17eabeb0a6e59fed0db3734`  
		Last Modified: Thu, 27 May 2021 20:30:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa767a15e8863c4b774fb02de6b5439ed63166db172c95fdcb42b0f28c26e2`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3b7d5d7d4d6189e0fe9946532bfb02c4e7afe6044e8af1bdac4dfe0aa362e3`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 542.5 KB (542481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abba1bd40515a8b1c80b84d0ca4510426fd3d496ba551bbbb3e25d429c29af75`  
		Last Modified: Thu, 27 May 2021 20:30:04 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c37ec64abddaacb30cfcc915197fe977815f8c9a17b4f8023a17330f0db6299`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a077af30d23f0da3953944b8b000e220b31eacace64b36eee4674880130c86b`  
		Last Modified: Thu, 27 May 2021 20:29:57 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:9a489b0919f8f1c664f1c9ad2c02d0c829cc244e1313865fd1a1b2e3adc6b7b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240247814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5746192bc425b7fcac5324c069409888237e3fe83a9e7c803513bc6f96c480`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:21:56 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 20 May 2021 00:31:59 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:32:12 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:32:31 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:32:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:32:50 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:32:55 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:33:03 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:33:05 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:33:10 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 20 May 2021 00:33:13 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 20 May 2021 00:33:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:33:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 20 May 2021 00:33:33 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 20 May 2021 00:33:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 20 May 2021 00:33:57 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 20 May 2021 00:34:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 20 May 2021 00:34:17 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:34:24 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 20 May 2021 00:34:27 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 20 May 2021 00:34:32 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:34:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d3625bf57aa986338173635f8c468a0b3baebb7cb06bcf800cf33ea59243e`  
		Last Modified: Thu, 20 May 2021 00:47:16 GMT  
		Size: 111.3 MB (111312376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70ddc65d68cd15a96d0138a966744a96e6f5f6d6e421d9e716c9d1fee58b402`  
		Last Modified: Thu, 20 May 2021 00:46:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d173c200e8e4c7d2bb8c65ff705b249d5f79a3169a1f659d604db8783c45d7ea`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 1.9 KB (1938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c697cbb4143f247d5153cf82bd3730d843468e9b25da63fc50bf22fc560f9662`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8b327423d02ef49d83307155cf593fb3c1714c6ef2a349c5ce4e6a4c8dc556`  
		Last Modified: Thu, 20 May 2021 00:47:00 GMT  
		Size: 98.0 MB (97973964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea1f02f4df72a5e3b6ad0034411153e944bcab25a3794c1ab5fd5f0fd8bc7f`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27f15cf915ec8b010be881a6bab1acf880f036663afbc042282d19259ef8773`  
		Last Modified: Thu, 20 May 2021 00:46:52 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:703d7ded266ac0cc7841dd691b965cfb9690d448408f283e52f087a37cf94445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:8a66ed585c556c99a465161c006c4783f93f4ff7c2c08f8bc7469ef0e8ab896d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234098690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9146e6458db0b39838a8b01012e9b5ce576ad722cd5abc837a87be4dc68faec2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:05 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:05 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 19 May 2021 20:14:06 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 19 May 2021 20:14:06 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 19 May 2021 20:14:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 19 May 2021 20:14:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:08 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:08 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 19 May 2021 20:14:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:16 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:16 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:16 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:16 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:16 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad76c13dbf4294d85cb9f1bd96178d0562b14f0a1a3fc6c2f978c43f78e882b`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74adc16fe46a3b302149bbc7b0e9e0f3167f46a8a066ca8ddc78cb019d58d23`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25adf2fd5648226e553a4785509f1517967029db56bcc9c34b7754d1c434f24`  
		Last Modified: Wed, 19 May 2021 20:15:27 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3d611520f7be8a125d4de7cd076ed16bd03222bd307c35d4982fec6a0680ad`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:68c643fe99ddc1eb5c4c23f5420a9cfeb34ff02470f4138d0b0a6ada9c0f0d75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223191874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c5a5bb789478edfc4b59b56f2b3f8d948eb5bf8d1258cbde457764fa6a8e2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:00 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:01 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:01 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 27 May 2021 20:29:01 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 27 May 2021 20:29:01 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 27 May 2021 20:29:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 27 May 2021 20:29:02 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:03 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:03 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 27 May 2021 20:29:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:15 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:15 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:15 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ee77b07d6084a2a0a5ac4243ce65cc037ab6bc12bd0843a0db8f92607391b8`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d1589fb64c24fbf3454a5fb2018cb86e15843dc87cdab0cff5805c97279d5`  
		Last Modified: Thu, 27 May 2021 20:30:28 GMT  
		Size: 6.9 KB (6887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702bbb3f3e14659830072f1bfe85e23e7340a4889962ed8c4d2ac7ae4ce91c3c`  
		Last Modified: Thu, 27 May 2021 20:30:35 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa338e08494855020783507e405774b88b83716bf89a37202e69c508ed2e953a`  
		Last Modified: Thu, 27 May 2021 20:30:28 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:3a0e9f9d2f2bf7a9802924e102b4b30425e5b9e4b9c428b3bcf3612a80916a76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230703426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa05271136d385134506aa3762425496cec715d104f82cbad3b407cacb78fb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:39:50 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:39:54 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:39:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:40:01 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 20 May 2021 00:40:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 20 May 2021 00:40:14 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 20 May 2021 00:40:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:40:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 20 May 2021 00:40:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:41:28 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:41:32 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 20 May 2021 00:41:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 20 May 2021 00:42:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:42:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:43:03 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:43:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:43:13 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:43:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e8feeb8ed1ab8284c5d480339445b621b71d46d2371a16718a04f2e9c5870d`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47243db540c7ff79ad2369746d5b3b1dc08e8b130a680c52b965858c912eb427`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff860e892d5bd2d0645cb8699bffbf6a02456d61d36fabdfc990809b3a7092ac`  
		Last Modified: Thu, 20 May 2021 00:47:37 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543ed613bddec83beb2f35ef640a48a6680f634cd8be353d098a1c933acd76bd`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:703d7ded266ac0cc7841dd691b965cfb9690d448408f283e52f087a37cf94445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:8a66ed585c556c99a465161c006c4783f93f4ff7c2c08f8bc7469ef0e8ab896d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234098690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9146e6458db0b39838a8b01012e9b5ce576ad722cd5abc837a87be4dc68faec2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:05 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:05 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 19 May 2021 20:14:06 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 19 May 2021 20:14:06 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 19 May 2021 20:14:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 19 May 2021 20:14:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:08 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:08 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 19 May 2021 20:14:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:16 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:16 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:16 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:16 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:16 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad76c13dbf4294d85cb9f1bd96178d0562b14f0a1a3fc6c2f978c43f78e882b`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74adc16fe46a3b302149bbc7b0e9e0f3167f46a8a066ca8ddc78cb019d58d23`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25adf2fd5648226e553a4785509f1517967029db56bcc9c34b7754d1c434f24`  
		Last Modified: Wed, 19 May 2021 20:15:27 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3d611520f7be8a125d4de7cd076ed16bd03222bd307c35d4982fec6a0680ad`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:68c643fe99ddc1eb5c4c23f5420a9cfeb34ff02470f4138d0b0a6ada9c0f0d75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223191874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c5a5bb789478edfc4b59b56f2b3f8d948eb5bf8d1258cbde457764fa6a8e2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:00 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:01 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:01 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 27 May 2021 20:29:01 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 27 May 2021 20:29:01 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 27 May 2021 20:29:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 27 May 2021 20:29:02 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:03 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:03 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 27 May 2021 20:29:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:15 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:15 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:15 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ee77b07d6084a2a0a5ac4243ce65cc037ab6bc12bd0843a0db8f92607391b8`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d1589fb64c24fbf3454a5fb2018cb86e15843dc87cdab0cff5805c97279d5`  
		Last Modified: Thu, 27 May 2021 20:30:28 GMT  
		Size: 6.9 KB (6887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702bbb3f3e14659830072f1bfe85e23e7340a4889962ed8c4d2ac7ae4ce91c3c`  
		Last Modified: Thu, 27 May 2021 20:30:35 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa338e08494855020783507e405774b88b83716bf89a37202e69c508ed2e953a`  
		Last Modified: Thu, 27 May 2021 20:30:28 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:3a0e9f9d2f2bf7a9802924e102b4b30425e5b9e4b9c428b3bcf3612a80916a76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230703426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa05271136d385134506aa3762425496cec715d104f82cbad3b407cacb78fb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:39:50 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:39:54 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:39:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:40:01 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 20 May 2021 00:40:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 20 May 2021 00:40:14 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 20 May 2021 00:40:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:40:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 20 May 2021 00:40:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:41:28 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:41:32 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 20 May 2021 00:41:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 20 May 2021 00:42:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:42:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:43:03 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:43:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:43:13 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:43:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e8feeb8ed1ab8284c5d480339445b621b71d46d2371a16718a04f2e9c5870d`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47243db540c7ff79ad2369746d5b3b1dc08e8b130a680c52b965858c912eb427`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff860e892d5bd2d0645cb8699bffbf6a02456d61d36fabdfc990809b3a7092ac`  
		Last Modified: Thu, 20 May 2021 00:47:37 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543ed613bddec83beb2f35ef640a48a6680f634cd8be353d098a1c933acd76bd`  
		Last Modified: Thu, 20 May 2021 00:47:27 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:8113752c97289f12d5d55a4e76badbecb7c359a78cc17e72f54ff755029c9b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:63f4da2e997b34d49a2bc949131f22223da06951022c91c2f36c5a0067689284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237166322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcec19c862fafa66ff6c77648e515c0271302e57956fd0eec416c9f6be53cef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BRANDING_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 19 May 2021 20:14:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:27 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:27 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 19 May 2021 20:14:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:34 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:35 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde9f1c4141e1669d1a0e2519d764cad7f449449982e491985dd53b630ad8bd7`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb97c41865a896652c4cede2d5eb40e68da7d6e09d9fa3687a91aaca1538818`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422680249022a137b3ee3c7e55fcb17684b964168027efde3fdc99ba54eaab0`  
		Last Modified: Wed, 19 May 2021 20:15:55 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadf73b07057fbe22df11b5d3bcb82de5833d388cc7a037acf64b761fc4845b2`  
		Last Modified: Wed, 19 May 2021 20:15:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7fd673d2147f65e83f33920d8a59aad589b5ec0e5a6dffa4a3b092609f0893e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226259506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41b78a5cb1419c42fcb5a82ce7874885509252b7f76ec699d6c83dd5874983`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BRANDING_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:21 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:21 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 27 May 2021 20:29:21 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 27 May 2021 20:29:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:24 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:24 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 27 May 2021 20:29:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:30 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:30 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:30 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff64345f45a7c6f5a0e5440d74097431a65977231dd433a1727a61cdda9cd45b`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7109a355f58af2dcd3a27abb6bad4308dc7c02c0f6ca9652e506efc5578be3`  
		Last Modified: Thu, 27 May 2021 20:30:57 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce827a5d52f64fcfbc814d6395f915dab4391cc44f353a5495a0bbfe6ecad03c`  
		Last Modified: Thu, 27 May 2021 20:31:03 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fababb011508b77f359f5a90341eb8910ffe50b464820efa2dd41a3873ddc6a`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:09da2c521e70bac97002559c1ffe9aa27945133ad024f1b4dcaf09045d8fa1fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233771062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61d43b322fa845c74b454e498eacf30dfe3dc8c8f6ffe8ea879a1a9f20788d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:43:33 GMT
ARG BRANDING_VERSION
# Thu, 20 May 2021 00:43:41 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:43:47 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:43:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:44:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 20 May 2021 00:44:12 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 20 May 2021 00:44:17 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 20 May 2021 00:44:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:44:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:44:51 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:44:56 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 20 May 2021 00:45:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 20 May 2021 00:45:39 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:46:05 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:46:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:46:14 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:46:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc9951f8a6e042d6aa4d540a3c257fdc84113e4220e55017795b2f7ab3f2b`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e36ed62d5e55e1a0a7ee290d0eee7d9eebadfa7ed944102b57bbb72a0dd572`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b015e0aea1f89925140ec99156b48900b70ecd46a6fe170c7e58634db6db82d`  
		Last Modified: Thu, 20 May 2021 00:48:08 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55048bca738773475353787939d3fec3a7e0b9f77c543fe7b5cf2aead1f`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:8113752c97289f12d5d55a4e76badbecb7c359a78cc17e72f54ff755029c9b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:63f4da2e997b34d49a2bc949131f22223da06951022c91c2f36c5a0067689284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237166322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcec19c862fafa66ff6c77648e515c0271302e57956fd0eec416c9f6be53cef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BRANDING_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 19 May 2021 20:14:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:27 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:27 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 19 May 2021 20:14:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:34 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:35 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde9f1c4141e1669d1a0e2519d764cad7f449449982e491985dd53b630ad8bd7`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb97c41865a896652c4cede2d5eb40e68da7d6e09d9fa3687a91aaca1538818`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422680249022a137b3ee3c7e55fcb17684b964168027efde3fdc99ba54eaab0`  
		Last Modified: Wed, 19 May 2021 20:15:55 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadf73b07057fbe22df11b5d3bcb82de5833d388cc7a037acf64b761fc4845b2`  
		Last Modified: Wed, 19 May 2021 20:15:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7fd673d2147f65e83f33920d8a59aad589b5ec0e5a6dffa4a3b092609f0893e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226259506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41b78a5cb1419c42fcb5a82ce7874885509252b7f76ec699d6c83dd5874983`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BRANDING_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:21 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:21 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 27 May 2021 20:29:21 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 27 May 2021 20:29:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:24 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:24 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 27 May 2021 20:29:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:30 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:30 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:30 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff64345f45a7c6f5a0e5440d74097431a65977231dd433a1727a61cdda9cd45b`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7109a355f58af2dcd3a27abb6bad4308dc7c02c0f6ca9652e506efc5578be3`  
		Last Modified: Thu, 27 May 2021 20:30:57 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce827a5d52f64fcfbc814d6395f915dab4391cc44f353a5495a0bbfe6ecad03c`  
		Last Modified: Thu, 27 May 2021 20:31:03 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fababb011508b77f359f5a90341eb8910ffe50b464820efa2dd41a3873ddc6a`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:09da2c521e70bac97002559c1ffe9aa27945133ad024f1b4dcaf09045d8fa1fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233771062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61d43b322fa845c74b454e498eacf30dfe3dc8c8f6ffe8ea879a1a9f20788d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:43:33 GMT
ARG BRANDING_VERSION
# Thu, 20 May 2021 00:43:41 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:43:47 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:43:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:44:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 20 May 2021 00:44:12 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 20 May 2021 00:44:17 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 20 May 2021 00:44:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:44:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:44:51 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:44:56 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 20 May 2021 00:45:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 20 May 2021 00:45:39 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:46:05 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:46:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:46:14 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:46:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc9951f8a6e042d6aa4d540a3c257fdc84113e4220e55017795b2f7ab3f2b`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e36ed62d5e55e1a0a7ee290d0eee7d9eebadfa7ed944102b57bbb72a0dd572`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b015e0aea1f89925140ec99156b48900b70ecd46a6fe170c7e58634db6db82d`  
		Last Modified: Thu, 20 May 2021 00:48:08 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55048bca738773475353787939d3fec3a7e0b9f77c543fe7b5cf2aead1f`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:8113752c97289f12d5d55a4e76badbecb7c359a78cc17e72f54ff755029c9b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:63f4da2e997b34d49a2bc949131f22223da06951022c91c2f36c5a0067689284
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237166322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcec19c862fafa66ff6c77648e515c0271302e57956fd0eec416c9f6be53cef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:13:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 19 May 2021 20:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:14:02 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 19 May 2021 20:14:03 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 19 May 2021 20:14:04 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 19 May 2021 20:14:05 GMT
ARG BONITA_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BRANDING_VERSION
# Wed, 19 May 2021 20:14:23 GMT
ARG BONITA_SHA256
# Wed, 19 May 2021 20:14:24 GMT
ARG BASE_URL
# Wed, 19 May 2021 20:14:24 GMT
ARG BONITA_URL
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 19 May 2021 20:14:24 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 19 May 2021 20:14:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 19 May 2021 20:14:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 19 May 2021 20:14:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 19 May 2021 20:14:27 GMT
RUN mkdir /opt/files
# Wed, 19 May 2021 20:14:27 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 19 May 2021 20:14:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 19 May 2021 20:14:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 19 May 2021 20:14:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 19 May 2021 20:14:34 GMT
VOLUME [/opt/bonita]
# Wed, 19 May 2021 20:14:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 19 May 2021 20:14:35 GMT
EXPOSE 8080
# Wed, 19 May 2021 20:14:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd95924d90b2d84f3ab090bf1dfb25f801417aae360e7b45d7c2faec7a90aed`  
		Last Modified: Wed, 19 May 2021 20:15:37 GMT  
		Size: 93.5 MB (93469711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6bb0a88ee431ba300155aa02a978808d8b1429b4290dfce68a5303ed0d00c8`  
		Last Modified: Wed, 19 May 2021 20:15:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3138c1ebfb5157da1dc313b04355f99852b060b0bc2cafa7e6f92861c8f4a15e`  
		Last Modified: Wed, 19 May 2021 20:15:23 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b8caa7d73e1707afdf7e41d9080a77238037bf5f16cf3feab7bb0e79d45c9`  
		Last Modified: Wed, 19 May 2021 20:15:21 GMT  
		Size: 573.0 KB (573009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde9f1c4141e1669d1a0e2519d764cad7f449449982e491985dd53b630ad8bd7`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb97c41865a896652c4cede2d5eb40e68da7d6e09d9fa3687a91aaca1538818`  
		Last Modified: Wed, 19 May 2021 20:15:48 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422680249022a137b3ee3c7e55fcb17684b964168027efde3fdc99ba54eaab0`  
		Last Modified: Wed, 19 May 2021 20:15:55 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadf73b07057fbe22df11b5d3bcb82de5833d388cc7a037acf64b761fc4845b2`  
		Last Modified: Wed, 19 May 2021 20:15:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7fd673d2147f65e83f33920d8a59aad589b5ec0e5a6dffa4a3b092609f0893e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226259506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a41b78a5cb1419c42fcb5a82ce7874885509252b7f76ec699d6c83dd5874983`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:28:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 27 May 2021 20:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:28:58 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 27 May 2021 20:28:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 27 May 2021 20:29:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 27 May 2021 20:29:00 GMT
ARG BONITA_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BRANDING_VERSION
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_SHA256
# Thu, 27 May 2021 20:29:21 GMT
ARG BASE_URL
# Thu, 27 May 2021 20:29:21 GMT
ARG BONITA_URL
# Thu, 27 May 2021 20:29:21 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 27 May 2021 20:29:21 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 27 May 2021 20:29:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 27 May 2021 20:29:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 27 May 2021 20:29:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 27 May 2021 20:29:24 GMT
RUN mkdir /opt/files
# Thu, 27 May 2021 20:29:24 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 27 May 2021 20:29:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 27 May 2021 20:29:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 27 May 2021 20:29:30 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 27 May 2021 20:29:30 GMT
VOLUME [/opt/bonita]
# Thu, 27 May 2021 20:29:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 27 May 2021 20:29:30 GMT
EXPOSE 8080
# Thu, 27 May 2021 20:29:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24d3bc48537211389cc32ed7a2608133f9d3cc66b1ec8acdd6b8daa783e099`  
		Last Modified: Thu, 27 May 2021 20:30:44 GMT  
		Size: 85.6 MB (85586406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d27f641bfbaff15f7ee3a1700159646c9348e332e6e7f60afdba39453017a32`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf394e777bad6b143f45bc97993c1373c9d7537f48bc5fbf0be23f45970ef39e`  
		Last Modified: Thu, 27 May 2021 20:30:31 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ce58caba06f3d8e1430ecfcc04a9d25e13ff6ce6e2a637fc8ae9c9566ceea`  
		Last Modified: Thu, 27 May 2021 20:30:29 GMT  
		Size: 542.5 KB (542477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff64345f45a7c6f5a0e5440d74097431a65977231dd433a1727a61cdda9cd45b`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7109a355f58af2dcd3a27abb6bad4308dc7c02c0f6ca9652e506efc5578be3`  
		Last Modified: Thu, 27 May 2021 20:30:57 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce827a5d52f64fcfbc814d6395f915dab4391cc44f353a5495a0bbfe6ecad03c`  
		Last Modified: Thu, 27 May 2021 20:31:03 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fababb011508b77f359f5a90341eb8910ffe50b464820efa2dd41a3873ddc6a`  
		Last Modified: Thu, 27 May 2021 20:30:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:09da2c521e70bac97002559c1ffe9aa27945133ad024f1b4dcaf09045d8fa1fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233771062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61d43b322fa845c74b454e498eacf30dfe3dc8c8f6ffe8ea879a1a9f20788d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:34:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 20 May 2021 00:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 May 2021 00:39:13 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 20 May 2021 00:39:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 20 May 2021 00:39:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 20 May 2021 00:39:46 GMT
ARG BONITA_VERSION
# Thu, 20 May 2021 00:43:33 GMT
ARG BRANDING_VERSION
# Thu, 20 May 2021 00:43:41 GMT
ARG BONITA_SHA256
# Thu, 20 May 2021 00:43:47 GMT
ARG BASE_URL
# Thu, 20 May 2021 00:43:58 GMT
ARG BONITA_URL
# Thu, 20 May 2021 00:44:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 20 May 2021 00:44:12 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 20 May 2021 00:44:17 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 20 May 2021 00:44:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 20 May 2021 00:44:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 20 May 2021 00:44:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 20 May 2021 00:44:51 GMT
RUN mkdir /opt/files
# Thu, 20 May 2021 00:44:56 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 20 May 2021 00:45:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 20 May 2021 00:45:39 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 20 May 2021 00:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 20 May 2021 00:46:05 GMT
VOLUME [/opt/bonita]
# Thu, 20 May 2021 00:46:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 20 May 2021 00:46:14 GMT
EXPOSE 8080
# Thu, 20 May 2021 00:46:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9e7ad0f0448e92fb16f76c603aecada15c40889d4f1da5923250604fdc460`  
		Last Modified: Thu, 20 May 2021 00:47:47 GMT  
		Size: 86.4 MB (86394726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff6f34104a98707426da1f362155f111ef7bd4f46193af555901fbe011772b`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7cd99b523b212592de5647eedf6cad7470492839cbd8cb25bd386a5808114`  
		Last Modified: Thu, 20 May 2021 00:47:31 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca56876c96ca39f94c870355914abeb3d9caf5d6f3ccee59ca9329a11528645`  
		Last Modified: Thu, 20 May 2021 00:47:28 GMT  
		Size: 541.9 KB (541868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ebc9951f8a6e042d6aa4d540a3c257fdc84113e4220e55017795b2f7ab3f2b`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e36ed62d5e55e1a0a7ee290d0eee7d9eebadfa7ed944102b57bbb72a0dd572`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b015e0aea1f89925140ec99156b48900b70ecd46a6fe170c7e58634db6db82d`  
		Last Modified: Thu, 20 May 2021 00:48:08 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54f55048bca738773475353787939d3fec3a7e0b9f77c543fe7b5cf2aead1f`  
		Last Modified: Thu, 20 May 2021 00:47:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
