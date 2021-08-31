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
$ docker pull bonita@sha256:ed7f09603bd263627ea3fe624e1eddfea0aebca1649122c4b0ce364da74fe3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2a6e551a5bd891abe055c5d3d9cdeaf51fd8d396f78c85cfb15615a6ea13d4e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233852199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6637b1b076c10f7d06f93e4de13692ebd64c32e3798b8e5cd4279f111bd2e367`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:18:05 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:18:09 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:18:12 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:18:20 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:18:23 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:18:26 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:18:30 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:18:34 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:18:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:19:02 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:19:03 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:19:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:19:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:19:46 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:19:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:19:57 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:20:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44a6dcceeb84150e152f7d2042a19418478b89434c18c29f816842761aebb84`  
		Last Modified: Tue, 31 Aug 2021 03:21:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709568a28e21e633e7c8714f0d7c15f5da8998019a55ab816fb0b6801fbfd65e`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba285a6b98fd908e3b4653f4ad1e188d38918991721f88d13cdfc321aebca4f8`  
		Last Modified: Tue, 31 Aug 2021 03:21:54 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef0f91abdc722f016ef5cf11495031666b723bca3aec839d977e7340f489dd`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:ac9ff09cce197923c16687c4af8ba94be62c826e0fa3471cf3e5249dd824b64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:e7ea0c4d7c1a3a3a1954ec3826381e73e52fa54b4d6c0594965dcbef4a2084cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242336189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bce3da74ac2ae038e6b299db850dfffd6c5a4eb9d25bae83eef94f62056f35`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:32 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 02:45:36 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:45:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:45:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:45:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 02:45:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 02:45:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 02:45:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 02:45:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:45:56 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113b5338edfef242ba8108e7cb8e73dfbbdd1c6090af0210b1bb470cf177785`  
		Last Modified: Tue, 31 Aug 2021 02:47:50 GMT  
		Size: 117.1 MB (117065422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5051eb4f6d463ec15e9acde49ec92c30499bbba7cd30743a6e4a1b48b97538b7`  
		Last Modified: Tue, 31 Aug 2021 02:47:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1a330f251dad8d1bf94c7f49fa22fa3da9a74b598abc3466905a17d40fd54c`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33969b7d483107e84736e89851c194cac9ddc5b62ecb73feba2d8b77aaf412b`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 576.9 KB (576941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd74c33cee47dc43924561fdedde1c84167377ab0f8d92ede3e4aacebbda7c`  
		Last Modified: Tue, 31 Aug 2021 02:47:36 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc245b5828b0e96f17df0d37e18e7903f836c389c0edaafecdc0a2450ff58c0`  
		Last Modified: Tue, 31 Aug 2021 02:47:31 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ace84dd3eb83050e4bd74047b942de1e98805507776c3d0a0e086c5a6fb01e`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:058e34528958bea10c947b162eecf600fec1bc1561d09e4647591633a8cc8f75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231037775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8fdfea1cfb1d18325253d9fb265fc65948121d71c51b0762a8a65f6e27d5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:00:14 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:00:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:00:43 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:00:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:01:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:01:05 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:07 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:01:07 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:01:08 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79ac9f2e15b1e0bb60576e833601ba7abf9047cd17986fe34125af088e3902c`  
		Last Modified: Tue, 31 Aug 2021 03:03:08 GMT  
		Size: 108.8 MB (108774887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2cec2173ecb52e7fff5803915956bf4805c0d6575874fcc28ef1a12f6efabf`  
		Last Modified: Tue, 31 Aug 2021 03:02:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ead7a73f92e56f59865b34b5ba38099265022a13bb2cf10e8760f6c86cb763`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13592da4eb3367522e3527ff41e7c78d0f2fa95e68b9fe6e51e2427e36ea7470`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 547.0 KB (546966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1631fcb4f15e439779d8957a9ec3575d024b1be12fafb63d2bfed8b34a652`  
		Last Modified: Tue, 31 Aug 2021 03:02:56 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676030f6340ad8828221f37c06d208acb4171ec2b3974453d979009267061816`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c86954ea2dfa0888cdaa430f8f63534d7a8546c307287c07ea8b57718f277ac`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ae6c6450c051c25e61270b1a58b8acdae9c5c0abd9f0bcb5d05b795864300b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b74e981f8d30d34825dd3ce487e3d65a484c148b34f83c95cf71f7c9a5ecd7`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:03:49 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:09:22 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:09:44 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:09:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:10:16 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:10:20 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:10:23 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:10:27 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:10:31 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:10:33 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:10:38 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:10:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:10:43 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:10:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:11:10 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:11:22 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:11:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:11:39 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:11:41 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:11:42 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:11:48 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:11:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add44339faca2d4e791ed66e2cc50a15e7bda3647d29de7ae9628db9a1493fc`  
		Last Modified: Tue, 31 Aug 2021 03:21:03 GMT  
		Size: 111.4 MB (111357716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b827ba8115e75901e84e8190622e4d47dca42d7cdf1b1fe977bcb323235f9b`  
		Last Modified: Tue, 31 Aug 2021 03:20:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffd233d9be9777560e7dd5ad2a212327772e2cc680c97b23a38e50f6efeb5f4`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 1.9 KB (1920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4db659952a332fe2eadf615eaaa663b32956a03131296c855ab00d086a49f9`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 546.7 KB (546736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23195d1ede89cb6aa100ddfbc20aae90b9a811f215921fbf7bb9767d0f8d866c`  
		Last Modified: Tue, 31 Aug 2021 03:20:49 GMT  
		Size: 98.0 MB (97973956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a80c5bdf7ebccef54348c023d7cd195c4bb6c3dbe599a831c0d8cf4bada53f2`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c942391fbaeac4398aa5af8f95bd135bc3f10263ed371efe463398c200793261`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:ac9ff09cce197923c16687c4af8ba94be62c826e0fa3471cf3e5249dd824b64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:e7ea0c4d7c1a3a3a1954ec3826381e73e52fa54b4d6c0594965dcbef4a2084cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242336189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bce3da74ac2ae038e6b299db850dfffd6c5a4eb9d25bae83eef94f62056f35`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:32 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 02:45:36 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:45:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:45:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:45:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 02:45:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 02:45:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 02:45:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 02:45:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:45:56 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113b5338edfef242ba8108e7cb8e73dfbbdd1c6090af0210b1bb470cf177785`  
		Last Modified: Tue, 31 Aug 2021 02:47:50 GMT  
		Size: 117.1 MB (117065422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5051eb4f6d463ec15e9acde49ec92c30499bbba7cd30743a6e4a1b48b97538b7`  
		Last Modified: Tue, 31 Aug 2021 02:47:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1a330f251dad8d1bf94c7f49fa22fa3da9a74b598abc3466905a17d40fd54c`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33969b7d483107e84736e89851c194cac9ddc5b62ecb73feba2d8b77aaf412b`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 576.9 KB (576941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd74c33cee47dc43924561fdedde1c84167377ab0f8d92ede3e4aacebbda7c`  
		Last Modified: Tue, 31 Aug 2021 02:47:36 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc245b5828b0e96f17df0d37e18e7903f836c389c0edaafecdc0a2450ff58c0`  
		Last Modified: Tue, 31 Aug 2021 02:47:31 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ace84dd3eb83050e4bd74047b942de1e98805507776c3d0a0e086c5a6fb01e`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:058e34528958bea10c947b162eecf600fec1bc1561d09e4647591633a8cc8f75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231037775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8fdfea1cfb1d18325253d9fb265fc65948121d71c51b0762a8a65f6e27d5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:00:14 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:00:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:00:43 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:00:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:01:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:01:05 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:07 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:01:07 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:01:08 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79ac9f2e15b1e0bb60576e833601ba7abf9047cd17986fe34125af088e3902c`  
		Last Modified: Tue, 31 Aug 2021 03:03:08 GMT  
		Size: 108.8 MB (108774887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2cec2173ecb52e7fff5803915956bf4805c0d6575874fcc28ef1a12f6efabf`  
		Last Modified: Tue, 31 Aug 2021 03:02:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ead7a73f92e56f59865b34b5ba38099265022a13bb2cf10e8760f6c86cb763`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13592da4eb3367522e3527ff41e7c78d0f2fa95e68b9fe6e51e2427e36ea7470`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 547.0 KB (546966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1631fcb4f15e439779d8957a9ec3575d024b1be12fafb63d2bfed8b34a652`  
		Last Modified: Tue, 31 Aug 2021 03:02:56 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676030f6340ad8828221f37c06d208acb4171ec2b3974453d979009267061816`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c86954ea2dfa0888cdaa430f8f63534d7a8546c307287c07ea8b57718f277ac`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ae6c6450c051c25e61270b1a58b8acdae9c5c0abd9f0bcb5d05b795864300b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b74e981f8d30d34825dd3ce487e3d65a484c148b34f83c95cf71f7c9a5ecd7`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:03:49 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:09:22 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:09:44 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:09:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:10:16 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:10:20 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:10:23 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:10:27 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:10:31 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:10:33 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:10:38 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:10:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:10:43 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:10:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:11:10 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:11:22 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:11:34 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:11:39 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:11:41 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:11:42 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:11:48 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:11:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7add44339faca2d4e791ed66e2cc50a15e7bda3647d29de7ae9628db9a1493fc`  
		Last Modified: Tue, 31 Aug 2021 03:21:03 GMT  
		Size: 111.4 MB (111357716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b827ba8115e75901e84e8190622e4d47dca42d7cdf1b1fe977bcb323235f9b`  
		Last Modified: Tue, 31 Aug 2021 03:20:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffd233d9be9777560e7dd5ad2a212327772e2cc680c97b23a38e50f6efeb5f4`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 1.9 KB (1920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4db659952a332fe2eadf615eaaa663b32956a03131296c855ab00d086a49f9`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 546.7 KB (546736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23195d1ede89cb6aa100ddfbc20aae90b9a811f215921fbf7bb9767d0f8d866c`  
		Last Modified: Tue, 31 Aug 2021 03:20:49 GMT  
		Size: 98.0 MB (97973956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a80c5bdf7ebccef54348c023d7cd195c4bb6c3dbe599a831c0d8cf4bada53f2`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c942391fbaeac4398aa5af8f95bd135bc3f10263ed371efe463398c200793261`  
		Last Modified: Tue, 31 Aug 2021 03:20:41 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:6d471236b9273e1aba818b3fb06c46d9e953784e389d351adc4d5aece9579df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:1d1869fce833de8e5b455a38669094054c8cd09427b5ca357489c62637886919
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234162070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816da2c209ce264b46232c4703e1ad51ffd6693a51b8f262026067a2ac1cba3f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 02:46:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:46:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:46:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 02:46:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:46:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:46:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:46:58 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:46:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:46:58 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:46:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4defe4a6a79231710ca826d99cbc7d1e103e433259c7ea2e2960d29a7f824200`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e0d44bc1f45a9bda2ca8d87d5163a6da184c2fc7e8b8c192cf00f9314a559`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca88238d657d56ad12a125d96bb6cde8dc4e650134227e7aaa7c442e931efb3`  
		Last Modified: Tue, 31 Aug 2021 02:48:07 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44601a6feff337628a9b1fc0da6d32482b96106bc148f45e05207984807ead`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:95092ad6b2bd314cab36257af0043c325bfab189e39dc78cb02fcd9e5decb5aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223269582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a1321edf10188001d0c9cb9f4439c81e564dbf36bb26217f74712e2ab66b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:01:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:01:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:01:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:01:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:01:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:01:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:01:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:01:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a178a891713c7a51d4cf9df12b454d83b92703fb89bdbf33c7f0e529c2c5b506`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53216262cb919a99e340ebd9ef8c55aa355414ecab6ecb78b28ac9150b13a4`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbd659620f4239cc11accb998730ed7530c524c4db16919ddbd8ade6df7b92`  
		Last Modified: Tue, 31 Aug 2021 03:03:32 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e3dded631ffa349cbe1698235d56e07d0aed455a74e3e3221575b1b4d78dda`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:aba9c3174ce3d2f36951dba013b6d3af8f231e695e07659ed37fe8be538f8582
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230784560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14dc7c890827eefb5f79f2d6153f6e19e26684f58e4212278aae56e2ae059b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:16:01 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:16:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:16:09 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:16:14 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:16:17 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:16:20 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:16:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:16:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:16:37 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:16:46 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:16:48 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:17:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:17:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:17:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:17:23 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:17:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:17:30 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:17:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2455a524c6bc2143b839a7531d140e08fb9557b58b83bc39ab745f4f27b35ad4`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ffbec42c83b4a8072a5bdea66efb9e2835f9d5a967ec44332bbfbb1f043429`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976cb44c5c1e4ca88a4f5e3d5e8fd1361b495050ed551041f0b8f0236553410`  
		Last Modified: Tue, 31 Aug 2021 03:21:25 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c74acd6e8d186eb6f6bc7ce65cfbae0348073dce3ad27e6ca6dde039f27bc7`  
		Last Modified: Tue, 31 Aug 2021 03:21:16 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:6d471236b9273e1aba818b3fb06c46d9e953784e389d351adc4d5aece9579df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:1d1869fce833de8e5b455a38669094054c8cd09427b5ca357489c62637886919
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234162070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816da2c209ce264b46232c4703e1ad51ffd6693a51b8f262026067a2ac1cba3f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 02:46:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:46:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:46:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 02:46:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:46:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:46:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:46:58 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:46:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:46:58 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:46:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4defe4a6a79231710ca826d99cbc7d1e103e433259c7ea2e2960d29a7f824200`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e0d44bc1f45a9bda2ca8d87d5163a6da184c2fc7e8b8c192cf00f9314a559`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca88238d657d56ad12a125d96bb6cde8dc4e650134227e7aaa7c442e931efb3`  
		Last Modified: Tue, 31 Aug 2021 02:48:07 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44601a6feff337628a9b1fc0da6d32482b96106bc148f45e05207984807ead`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:95092ad6b2bd314cab36257af0043c325bfab189e39dc78cb02fcd9e5decb5aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223269582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a1321edf10188001d0c9cb9f4439c81e564dbf36bb26217f74712e2ab66b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:01:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:01:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:01:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:01:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:01:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:01:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:01:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:01:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a178a891713c7a51d4cf9df12b454d83b92703fb89bdbf33c7f0e529c2c5b506`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53216262cb919a99e340ebd9ef8c55aa355414ecab6ecb78b28ac9150b13a4`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbd659620f4239cc11accb998730ed7530c524c4db16919ddbd8ade6df7b92`  
		Last Modified: Tue, 31 Aug 2021 03:03:32 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e3dded631ffa349cbe1698235d56e07d0aed455a74e3e3221575b1b4d78dda`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:aba9c3174ce3d2f36951dba013b6d3af8f231e695e07659ed37fe8be538f8582
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230784560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14dc7c890827eefb5f79f2d6153f6e19e26684f58e4212278aae56e2ae059b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:16:01 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:16:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:16:09 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:16:14 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:16:17 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:16:20 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:16:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:16:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:16:37 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:16:46 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:16:48 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:17:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:17:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:17:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:17:23 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:17:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:17:30 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:17:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2455a524c6bc2143b839a7531d140e08fb9557b58b83bc39ab745f4f27b35ad4`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ffbec42c83b4a8072a5bdea66efb9e2835f9d5a967ec44332bbfbb1f043429`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6976cb44c5c1e4ca88a4f5e3d5e8fd1361b495050ed551041f0b8f0236553410`  
		Last Modified: Tue, 31 Aug 2021 03:21:25 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c74acd6e8d186eb6f6bc7ce65cfbae0348073dce3ad27e6ca6dde039f27bc7`  
		Last Modified: Tue, 31 Aug 2021 03:21:16 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:ed7f09603bd263627ea3fe624e1eddfea0aebca1649122c4b0ce364da74fe3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:2a6e551a5bd891abe055c5d3d9cdeaf51fd8d396f78c85cfb15615a6ea13d4e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233852199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6637b1b076c10f7d06f93e4de13692ebd64c32e3798b8e5cd4279f111bd2e367`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:18:05 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:18:09 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:18:12 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:18:20 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:18:23 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:18:26 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:18:30 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:18:34 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:18:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:19:02 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:19:03 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:19:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:19:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:19:46 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:19:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:19:57 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:20:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44a6dcceeb84150e152f7d2042a19418478b89434c18c29f816842761aebb84`  
		Last Modified: Tue, 31 Aug 2021 03:21:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709568a28e21e633e7c8714f0d7c15f5da8998019a55ab816fb0b6801fbfd65e`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba285a6b98fd908e3b4653f4ad1e188d38918991721f88d13cdfc321aebca4f8`  
		Last Modified: Tue, 31 Aug 2021 03:21:54 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef0f91abdc722f016ef5cf11495031666b723bca3aec839d977e7340f489dd`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:ed7f09603bd263627ea3fe624e1eddfea0aebca1649122c4b0ce364da74fe3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2a6e551a5bd891abe055c5d3d9cdeaf51fd8d396f78c85cfb15615a6ea13d4e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233852199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6637b1b076c10f7d06f93e4de13692ebd64c32e3798b8e5cd4279f111bd2e367`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:18:05 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:18:09 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:18:12 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:18:20 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:18:23 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:18:26 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:18:30 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:18:34 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:18:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:19:02 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:19:03 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:19:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:19:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:19:46 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:19:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:19:57 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:20:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44a6dcceeb84150e152f7d2042a19418478b89434c18c29f816842761aebb84`  
		Last Modified: Tue, 31 Aug 2021 03:21:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709568a28e21e633e7c8714f0d7c15f5da8998019a55ab816fb0b6801fbfd65e`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba285a6b98fd908e3b4653f4ad1e188d38918991721f88d13cdfc321aebca4f8`  
		Last Modified: Tue, 31 Aug 2021 03:21:54 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef0f91abdc722f016ef5cf11495031666b723bca3aec839d977e7340f489dd`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:ed7f09603bd263627ea3fe624e1eddfea0aebca1649122c4b0ce364da74fe3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:2a6e551a5bd891abe055c5d3d9cdeaf51fd8d396f78c85cfb15615a6ea13d4e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233852199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6637b1b076c10f7d06f93e4de13692ebd64c32e3798b8e5cd4279f111bd2e367`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:12:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:15:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:15:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:15:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:15:55 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:18:05 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:18:09 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:18:12 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:18:20 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:18:23 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:18:26 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:18:30 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:18:34 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:18:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:18:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:19:02 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:19:03 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:19:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:19:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:19:46 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:19:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:19:57 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:20:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54978ae656d40037cfaec12659d83d17df3f111e5c260f8b00c5dc48967862b`  
		Last Modified: Tue, 31 Aug 2021 03:21:33 GMT  
		Size: 86.4 MB (86441451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe73f6d51a2d50268e599e7d89ba63e3c7ecaeebb9d94462603eade0789a5`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0555b6890c27c06b847697527af8c80b7ab11e7c04f51b2d34afa768079ee3`  
		Last Modified: Tue, 31 Aug 2021 03:21:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2debdb88d2a487637f51a90eddc12512ef172a3f9b78ac28492b922aad94b55`  
		Last Modified: Tue, 31 Aug 2021 03:21:15 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44a6dcceeb84150e152f7d2042a19418478b89434c18c29f816842761aebb84`  
		Last Modified: Tue, 31 Aug 2021 03:21:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709568a28e21e633e7c8714f0d7c15f5da8998019a55ab816fb0b6801fbfd65e`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba285a6b98fd908e3b4653f4ad1e188d38918991721f88d13cdfc321aebca4f8`  
		Last Modified: Tue, 31 Aug 2021 03:21:54 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ef0f91abdc722f016ef5cf11495031666b723bca3aec839d977e7340f489dd`  
		Last Modified: Tue, 31 Aug 2021 03:21:45 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
