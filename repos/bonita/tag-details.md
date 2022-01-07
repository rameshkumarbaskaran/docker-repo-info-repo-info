<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:b1a5edc48538324d9258f9293d1fceef277b233d60a1647c5445f7dd59c5cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:ebc8ed86516521fb7edbd1c57902ce5a1beb1d4a285a03bd2a46553938dcfc34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237283638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e686edce26811e11a8d97473d4234ef8fb283555b0b4e202d773f0ad4bb51b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:44:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:44:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:44:22 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:44:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:44:48 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:44:51 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:44:51 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:44:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:44:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:45:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:45:01 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:02 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f3786c0c40f6e8deb47a2475ea53f4977287ebe714a44d44f950aaeec98ba`  
		Last Modified: Fri, 07 Jan 2022 02:46:34 GMT  
		Size: 93.6 MB (93575399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661c522eadbab3f8f5ac630a7b61d0c75a436d97338298d029bad643809963a`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027782aea31321bb35d0f16a41c0b7207dcfbd88616de57459b062f409c5ecf3`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a02a08a1262d5108da96ace50d5ec3d318977c3a3c315a9da633d57653637d`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 577.0 KB (576963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb230869d25418bb417be80a7509bdafd7de12adab466a6c5b17dea712383139`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6956864b7724141a69ce62391a3d8d74b4546843b335af20b52817e65d788d9`  
		Last Modified: Fri, 07 Jan 2022 02:46:46 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3ecf350694a1d2de08afd09a7311d0ecdefca39df5c7fc611b9e7c07f0913c`  
		Last Modified: Fri, 07 Jan 2022 02:46:55 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4e8317f722de18d2d67e8d6dad91fbe8f8e36f355d93af5c6521bfc79db8f`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b47e16e82e4e8a2c94492e3a6d28f4e471f8ba9abc6b3380272f67ad088a0cb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226403449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8b9ffa0aa4b699cce26760edcb675c11f323cd2e592238acdb443b8614c30c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:12:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:12:24 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:12:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:12:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:12:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:13:10 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:13:11 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:13:12 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:13:13 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:13:14 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:13:15 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:13:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:13:17 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:13:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:13:21 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:13:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:13:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:13:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:13:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:13:32 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:13:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:13:34 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:13:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca822e6ba2fafa543991c7a6a40f34c01cc87fe3901534e562deb088176d7493`  
		Last Modified: Fri, 07 Jan 2022 02:15:44 GMT  
		Size: 85.7 MB (85703479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c51cef86fe6d8c848b23bf9356efd72d40eb9309423f30fb15cbc4c2742b45`  
		Last Modified: Fri, 07 Jan 2022 02:15:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51d8356f23b73c45579abe97c2e7ae9fea11535c8a366b335e028731fdcc83`  
		Last Modified: Fri, 07 Jan 2022 02:15:32 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1503bacdf75977cb3264983f76442c8a2cce1ef3523605d38ea96570902981`  
		Last Modified: Fri, 07 Jan 2022 02:15:30 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed14de4751c7e19603293038d3df64d993cb9d3d11f701dee5c99be24e969176`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2056d740f0a61d6cfbc612462f1f2bfc55803aabfa51d83a0c69e01e381430da`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ba6429c757c2825161ef4d1df346c4a723c950961988d2608a8fd4e35a7bc`  
		Last Modified: Fri, 07 Jan 2022 02:16:02 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995da71b9130454ebc7011f734b6911ae7ea272154ef258fc2d2baa7a3e0f360`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:8a1a525c2c2e7beca13cc133237b601136b7141d8994537779ec62de26402c7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233884822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1465b0f318d405395a9dddc053e84a1ca55ab0c1d0edbba80800535d446ada`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:13:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:13:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:13:42 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:13:44 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:14:37 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:14:39 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:14:41 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:14:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:14:43 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 04:14:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 04:14:46 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 04:14:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:14:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 04:15:01 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:15:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 04:15:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 04:15:16 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 04:15:21 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 04:15:22 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:15:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:15:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:15:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021461f957d0a6e3f436e80b22505497253d416b8de7e64b503b2ae5cfc8b76c`  
		Last Modified: Fri, 07 Jan 2022 04:19:33 GMT  
		Size: 86.5 MB (86479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b895c91ae5d42e185f36f5fa073cd75a72944978257a5a64cae9c4ea7a4f`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54e78cf28365c09fbdb80b2e00abd87c867f776e402bac6564fc4ab9409b3d`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518bfcc9e3ac9a0b5f936518df882fd5bd1d3007bca5c4a342e8ba78cc10c27`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fd7b363bb63768a93a8b709c099ff8aa1e1b83dccdaf975acc5bbadf353e3`  
		Last Modified: Fri, 07 Jan 2022 04:19:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9058a307703d690c23fc19ff9047c587446b7ecc91950bf35337b26f4c30c0`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f58774110fb6da4ef751fdcbd8e0b18a7ba6ae4036b986aebb26a5e04e1733a`  
		Last Modified: Fri, 07 Jan 2022 04:19:53 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89f578acd0e5c94cc8d4ef274d052711102192734d1ed63e66a1cc0cc0a318a`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:cab0d69387d03c075ccc40cc4d016ff8bd154806ab1e16b17ade51306c315239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:ed211d8966e81479a0de35d88067abc19128f5115f4ed0a18583d0109418c320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f34dfd6f06c782fe12de949e94a95aec280a87fede53c2ecf93bdd31c1415`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:45:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:45:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:45:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:45:41 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:45:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:45:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:44 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:45:45 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:45:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:45:57 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:45:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:58 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97708e1be04f300190a6447eb5701bf6136bde08c7fc9d2f100554dee600862f`  
		Last Modified: Fri, 07 Jan 2022 02:47:23 GMT  
		Size: 93.6 MB (93576944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccaf14419ce16922f1fadc9c0cfca941583821338487070f248663793e6a60`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee464fd0cad364188182240e3445e5ef7d60fcd8b054ea0f81f87bf26f2c1512`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30817fa401eb65a7fe63940c50cc18df1e57394daaec77595f0084faaa94d9b`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.0 MB (1003220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd02559b7c70dc211f68f796d7deef9233732d34de4041ea0e1b352b27736ef`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35076f161983cdfb4a547a85ce068f58dc441047b1ccc6cd3f1db1afbd64a40`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec320074cb8322b6f32e97f7fd43f3e74bceb2525a35c4d4003827d7891d876f`  
		Last Modified: Fri, 07 Jan 2022 02:47:15 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f49324ac46378dd042d253b551c923c11f94b0f5328e3e242837544501e19`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e7dc23c1c127163649ca01a096ffa92d034bf77da4f1f174af5c8ddb4f83e870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224094739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561be5fff3a0045b486baa9db80b475e8c51bacf50e62007dd73a619477d8922`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:14:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:14:24 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:14:25 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:14:26 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:14:27 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:14:28 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:14:29 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:14:30 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:14:31 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:14:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:14:33 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:14:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:36 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:14:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:14:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:14:46 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:14:47 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:14:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:14:50 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:14:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cc759bf42029a19e7ddfcc42dc0db85ecb4bd43c89e8e3e1e0f7498cff516`  
		Last Modified: Fri, 07 Jan 2022 02:16:30 GMT  
		Size: 85.7 MB (85703427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0cfcb5c10e4b2dc1bab617e8c29a34bb963f3e9ffa94e92c6c38f3bebeb04`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61837014e57970f4f06446a4c60d4f3cf530889c0fc449e3b4d758d8d4179c78`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b8055c41250c722a929d047034ec9405cb0ee956a0be28f44d1e97a044f3a`  
		Last Modified: Fri, 07 Jan 2022 02:16:17 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a9192b771b82b241d0bd13fa7ec48f7748732d4ea523071d6380c9054e1bb0`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8817c2a9b0f82e4e5e851a7431064c1dbfea617a62b83d8ff82852c72ece60`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f424b7e4fabf4819c12d14f9e2f95f08ca015a46b0be6e7cbc551ab9bd7eb5`  
		Last Modified: Fri, 07 Jan 2022 02:16:29 GMT  
		Size: 113.7 MB (113727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a990cce3d3807e01700ddcaf1423e46f68f4b5444f90731f8c07548b71962`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:462037663020c39d729f14460e7722f341e0931da832994512b8c39fb5b7b2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231551208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6432d865bfea5c9c7afba043dac44f7319a5527bee30dfb5be2f06c8240536`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:17:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:17:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:17:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:17:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:17:39 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:17:41 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:17:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:17:43 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:17:45 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 04:17:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 04:17:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 04:17:50 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:17:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:57 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:17:58 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 04:18:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 04:18:16 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 04:18:20 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:18:21 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:18:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:18:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb44345bd8b045c9d533fdd1307670dc3124100b34086b62e2d012367a9f47`  
		Last Modified: Fri, 07 Jan 2022 04:20:26 GMT  
		Size: 86.5 MB (86479514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dc5e14b9bd708430308d858539ec01f542e93120293f822ac3892ae6fda958`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1f21c8a4422e0c32d01df760d570c9a5309b085da20b79a9b1656f5edec49`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14e56a49876e7f8fad5bb0be5d8de168febc3c1dad5233c3873dd3f5b89466`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e576677d41fe97c01699d81c674a1d6ef2a174a86149d0c5b2749e5c7a5ca`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62c2cef2b599c80293c3920ffd3de1bac1117c96b801f47133c6d4068e48bd`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a056e1bfe547d7c3f62376f0f1783af91416edc53c838bf23579e91f259377`  
		Last Modified: Fri, 07 Jan 2022 04:20:19 GMT  
		Size: 113.7 MB (113727929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935338738903998b02f65580d162454b0484c90e6bb100aed85304b1c7067f3a`  
		Last Modified: Fri, 07 Jan 2022 04:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:cab0d69387d03c075ccc40cc4d016ff8bd154806ab1e16b17ade51306c315239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:ed211d8966e81479a0de35d88067abc19128f5115f4ed0a18583d0109418c320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f34dfd6f06c782fe12de949e94a95aec280a87fede53c2ecf93bdd31c1415`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:45:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:45:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:45:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:45:41 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:45:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:45:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:44 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:45:45 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:45:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:45:57 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:45:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:58 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97708e1be04f300190a6447eb5701bf6136bde08c7fc9d2f100554dee600862f`  
		Last Modified: Fri, 07 Jan 2022 02:47:23 GMT  
		Size: 93.6 MB (93576944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccaf14419ce16922f1fadc9c0cfca941583821338487070f248663793e6a60`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee464fd0cad364188182240e3445e5ef7d60fcd8b054ea0f81f87bf26f2c1512`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30817fa401eb65a7fe63940c50cc18df1e57394daaec77595f0084faaa94d9b`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.0 MB (1003220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd02559b7c70dc211f68f796d7deef9233732d34de4041ea0e1b352b27736ef`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35076f161983cdfb4a547a85ce068f58dc441047b1ccc6cd3f1db1afbd64a40`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec320074cb8322b6f32e97f7fd43f3e74bceb2525a35c4d4003827d7891d876f`  
		Last Modified: Fri, 07 Jan 2022 02:47:15 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f49324ac46378dd042d253b551c923c11f94b0f5328e3e242837544501e19`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e7dc23c1c127163649ca01a096ffa92d034bf77da4f1f174af5c8ddb4f83e870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224094739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561be5fff3a0045b486baa9db80b475e8c51bacf50e62007dd73a619477d8922`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:14:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:14:24 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:14:25 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:14:26 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:14:27 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:14:28 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:14:29 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:14:30 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:14:31 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:14:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:14:33 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:14:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:36 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:14:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:14:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:14:46 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:14:47 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:14:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:14:50 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:14:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cc759bf42029a19e7ddfcc42dc0db85ecb4bd43c89e8e3e1e0f7498cff516`  
		Last Modified: Fri, 07 Jan 2022 02:16:30 GMT  
		Size: 85.7 MB (85703427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0cfcb5c10e4b2dc1bab617e8c29a34bb963f3e9ffa94e92c6c38f3bebeb04`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61837014e57970f4f06446a4c60d4f3cf530889c0fc449e3b4d758d8d4179c78`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b8055c41250c722a929d047034ec9405cb0ee956a0be28f44d1e97a044f3a`  
		Last Modified: Fri, 07 Jan 2022 02:16:17 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a9192b771b82b241d0bd13fa7ec48f7748732d4ea523071d6380c9054e1bb0`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8817c2a9b0f82e4e5e851a7431064c1dbfea617a62b83d8ff82852c72ece60`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f424b7e4fabf4819c12d14f9e2f95f08ca015a46b0be6e7cbc551ab9bd7eb5`  
		Last Modified: Fri, 07 Jan 2022 02:16:29 GMT  
		Size: 113.7 MB (113727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a990cce3d3807e01700ddcaf1423e46f68f4b5444f90731f8c07548b71962`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:462037663020c39d729f14460e7722f341e0931da832994512b8c39fb5b7b2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231551208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6432d865bfea5c9c7afba043dac44f7319a5527bee30dfb5be2f06c8240536`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:17:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:17:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:17:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:17:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:17:39 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:17:41 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:17:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:17:43 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:17:45 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 04:17:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 04:17:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 04:17:50 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:17:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:57 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:17:58 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 04:18:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 04:18:16 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 04:18:20 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:18:21 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:18:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:18:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb44345bd8b045c9d533fdd1307670dc3124100b34086b62e2d012367a9f47`  
		Last Modified: Fri, 07 Jan 2022 04:20:26 GMT  
		Size: 86.5 MB (86479514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dc5e14b9bd708430308d858539ec01f542e93120293f822ac3892ae6fda958`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1f21c8a4422e0c32d01df760d570c9a5309b085da20b79a9b1656f5edec49`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14e56a49876e7f8fad5bb0be5d8de168febc3c1dad5233c3873dd3f5b89466`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e576677d41fe97c01699d81c674a1d6ef2a174a86149d0c5b2749e5c7a5ca`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62c2cef2b599c80293c3920ffd3de1bac1117c96b801f47133c6d4068e48bd`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a056e1bfe547d7c3f62376f0f1783af91416edc53c838bf23579e91f259377`  
		Last Modified: Fri, 07 Jan 2022 04:20:19 GMT  
		Size: 113.7 MB (113727929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935338738903998b02f65580d162454b0484c90e6bb100aed85304b1c7067f3a`  
		Last Modified: Fri, 07 Jan 2022 04:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:6bb6589a958c6ace85f8076ba84e8c63ba6eaffec52d401331cd6b6bc0f42b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:98e0e3e7aa16d4dfc285a125c8496cb46655940ee2a9328da767fdcba05a188b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234216005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84b704b9e129bdc8b4934ffdd0cee3b5a26d462fe758e6f1c6a00e8a91e7210`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:44:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:44:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:44:22 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:44:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:44:32 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 02:44:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:44:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:44:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:44:34 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:44:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 02:44:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:44:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:44:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:44:43 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:44:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:44:43 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:44:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f3786c0c40f6e8deb47a2475ea53f4977287ebe714a44d44f950aaeec98ba`  
		Last Modified: Fri, 07 Jan 2022 02:46:34 GMT  
		Size: 93.6 MB (93575399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661c522eadbab3f8f5ac630a7b61d0c75a436d97338298d029bad643809963a`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027782aea31321bb35d0f16a41c0b7207dcfbd88616de57459b062f409c5ecf3`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a02a08a1262d5108da96ace50d5ec3d318977c3a3c315a9da633d57653637d`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 577.0 KB (576963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12007faa78bb7892635b508938bce7aeb43d7c80c07af46c8be65ad114012518`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93641292ec66a3d8043cd840dc7ada2d25a982650a41c7062bbd91a77ed94c2d`  
		Last Modified: Fri, 07 Jan 2022 02:46:18 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223b515b5a52b97c3ddef3e70d87d99c98d399283b3d24fa44d93b18c94b2f81`  
		Last Modified: Fri, 07 Jan 2022 02:46:25 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb5d13f1a335b24f04ea63997e7ddc1d22f9e2e05a8a52271b5f91a32ce5370`  
		Last Modified: Fri, 07 Jan 2022 02:46:18 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d3ee3eb5641255a86ca14018afa77ff5902d1fcefd82f0f26dd74956dbd15265
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223335813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dde139c075cb4260d81c7306b783777bbbef6397631e231b6efca7ab6f8bfcf`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:12:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:12:24 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:12:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:12:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:12:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:12:38 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:12:39 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:12:40 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:12:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 02:12:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 02:12:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:12:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:12:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:12:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:12:47 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:12:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 02:12:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:12:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:12:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:12:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:12:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:12:59 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:13:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca822e6ba2fafa543991c7a6a40f34c01cc87fe3901534e562deb088176d7493`  
		Last Modified: Fri, 07 Jan 2022 02:15:44 GMT  
		Size: 85.7 MB (85703479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c51cef86fe6d8c848b23bf9356efd72d40eb9309423f30fb15cbc4c2742b45`  
		Last Modified: Fri, 07 Jan 2022 02:15:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51d8356f23b73c45579abe97c2e7ae9fea11535c8a366b335e028731fdcc83`  
		Last Modified: Fri, 07 Jan 2022 02:15:32 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1503bacdf75977cb3264983f76442c8a2cce1ef3523605d38ea96570902981`  
		Last Modified: Fri, 07 Jan 2022 02:15:30 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4621397c0386db7be7d982a11223465cd931b9b00e319d060e58eabe52a8cc19`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ca03608759134b55f8473ca1c9d04ec285ccd4b7c3ddc75b065c5320e40a62`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 6.9 KB (6866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdd5c5c44aed2cf2ae10040ac9ed80019474236306bf8b0018724a929914454`  
		Last Modified: Fri, 07 Jan 2022 02:15:38 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb5cab595b9cc0699ca6085f8b01a292d60fbeb28bcb1c19d8389d7814bbf1`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:025e232d3abad1f5ac55f104ab170f61934dbc4134fc7bfe7de06988aaeddc77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230817201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4c4e2f0cf300294bd2f2a8ad70845f1a7d64e998fc1e5b4c4a22dd4010cb5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:13:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:13:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:13:42 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:13:44 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:13:45 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:13:47 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:13:48 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:13:49 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 04:13:50 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 04:13:52 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 04:13:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:13:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 04:13:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 04:14:01 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:14:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 04:14:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 04:14:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 04:14:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 04:14:24 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:14:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:14:27 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:14:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021461f957d0a6e3f436e80b22505497253d416b8de7e64b503b2ae5cfc8b76c`  
		Last Modified: Fri, 07 Jan 2022 04:19:33 GMT  
		Size: 86.5 MB (86479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b895c91ae5d42e185f36f5fa073cd75a72944978257a5a64cae9c4ea7a4f`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54e78cf28365c09fbdb80b2e00abd87c867f776e402bac6564fc4ab9409b3d`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518bfcc9e3ac9a0b5f936518df882fd5bd1d3007bca5c4a342e8ba78cc10c27`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bb33401f3bc0ec5dc04e56ed38872ea6b48d0f5fdee2059a16c7b729640937`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47492c3c8db33e696d7834db9535f50f4caa4d2d3617c7748640f36011230e20`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a55d53978319ff37148a408a36cee4c9b56228f0c29329de121dafdacaa9f44`  
		Last Modified: Fri, 07 Jan 2022 04:19:22 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cde6981b21356ca980ba8b38e21e59acd2b06f1b7df3435e5a0b9781f98231`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:6bb6589a958c6ace85f8076ba84e8c63ba6eaffec52d401331cd6b6bc0f42b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:98e0e3e7aa16d4dfc285a125c8496cb46655940ee2a9328da767fdcba05a188b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234216005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84b704b9e129bdc8b4934ffdd0cee3b5a26d462fe758e6f1c6a00e8a91e7210`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:44:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:44:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:44:22 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:44:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:44:32 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 02:44:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:44:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:44:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:44:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:44:34 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:44:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 02:44:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:44:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:44:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:44:43 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:44:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:44:43 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:44:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f3786c0c40f6e8deb47a2475ea53f4977287ebe714a44d44f950aaeec98ba`  
		Last Modified: Fri, 07 Jan 2022 02:46:34 GMT  
		Size: 93.6 MB (93575399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661c522eadbab3f8f5ac630a7b61d0c75a436d97338298d029bad643809963a`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027782aea31321bb35d0f16a41c0b7207dcfbd88616de57459b062f409c5ecf3`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a02a08a1262d5108da96ace50d5ec3d318977c3a3c315a9da633d57653637d`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 577.0 KB (576963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12007faa78bb7892635b508938bce7aeb43d7c80c07af46c8be65ad114012518`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93641292ec66a3d8043cd840dc7ada2d25a982650a41c7062bbd91a77ed94c2d`  
		Last Modified: Fri, 07 Jan 2022 02:46:18 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223b515b5a52b97c3ddef3e70d87d99c98d399283b3d24fa44d93b18c94b2f81`  
		Last Modified: Fri, 07 Jan 2022 02:46:25 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb5d13f1a335b24f04ea63997e7ddc1d22f9e2e05a8a52271b5f91a32ce5370`  
		Last Modified: Fri, 07 Jan 2022 02:46:18 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d3ee3eb5641255a86ca14018afa77ff5902d1fcefd82f0f26dd74956dbd15265
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223335813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dde139c075cb4260d81c7306b783777bbbef6397631e231b6efca7ab6f8bfcf`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:12:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:12:24 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:12:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:12:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:12:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:12:38 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:12:39 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:12:40 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:12:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 02:12:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 02:12:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:12:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:12:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 02:12:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:12:47 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:12:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 02:12:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:12:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:12:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:12:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:12:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:12:59 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:13:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca822e6ba2fafa543991c7a6a40f34c01cc87fe3901534e562deb088176d7493`  
		Last Modified: Fri, 07 Jan 2022 02:15:44 GMT  
		Size: 85.7 MB (85703479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c51cef86fe6d8c848b23bf9356efd72d40eb9309423f30fb15cbc4c2742b45`  
		Last Modified: Fri, 07 Jan 2022 02:15:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51d8356f23b73c45579abe97c2e7ae9fea11535c8a366b335e028731fdcc83`  
		Last Modified: Fri, 07 Jan 2022 02:15:32 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1503bacdf75977cb3264983f76442c8a2cce1ef3523605d38ea96570902981`  
		Last Modified: Fri, 07 Jan 2022 02:15:30 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4621397c0386db7be7d982a11223465cd931b9b00e319d060e58eabe52a8cc19`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ca03608759134b55f8473ca1c9d04ec285ccd4b7c3ddc75b065c5320e40a62`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 6.9 KB (6866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdd5c5c44aed2cf2ae10040ac9ed80019474236306bf8b0018724a929914454`  
		Last Modified: Fri, 07 Jan 2022 02:15:38 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb5cab595b9cc0699ca6085f8b01a292d60fbeb28bcb1c19d8389d7814bbf1`  
		Last Modified: Fri, 07 Jan 2022 02:15:29 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:025e232d3abad1f5ac55f104ab170f61934dbc4134fc7bfe7de06988aaeddc77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230817201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4c4e2f0cf300294bd2f2a8ad70845f1a7d64e998fc1e5b4c4a22dd4010cb5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:13:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:13:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:13:42 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:13:44 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:13:45 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:13:47 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:13:48 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:13:49 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 07 Jan 2022 04:13:50 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 07 Jan 2022 04:13:52 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 04:13:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:13:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 07 Jan 2022 04:13:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 04:14:01 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:14:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 07 Jan 2022 04:14:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 07 Jan 2022 04:14:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 04:14:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 04:14:24 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:14:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:14:27 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:14:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021461f957d0a6e3f436e80b22505497253d416b8de7e64b503b2ae5cfc8b76c`  
		Last Modified: Fri, 07 Jan 2022 04:19:33 GMT  
		Size: 86.5 MB (86479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b895c91ae5d42e185f36f5fa073cd75a72944978257a5a64cae9c4ea7a4f`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54e78cf28365c09fbdb80b2e00abd87c867f776e402bac6564fc4ab9409b3d`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518bfcc9e3ac9a0b5f936518df882fd5bd1d3007bca5c4a342e8ba78cc10c27`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bb33401f3bc0ec5dc04e56ed38872ea6b48d0f5fdee2059a16c7b729640937`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47492c3c8db33e696d7834db9535f50f4caa4d2d3617c7748640f36011230e20`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a55d53978319ff37148a408a36cee4c9b56228f0c29329de121dafdacaa9f44`  
		Last Modified: Fri, 07 Jan 2022 04:19:22 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cde6981b21356ca980ba8b38e21e59acd2b06f1b7df3435e5a0b9781f98231`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:b1a5edc48538324d9258f9293d1fceef277b233d60a1647c5445f7dd59c5cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:ebc8ed86516521fb7edbd1c57902ce5a1beb1d4a285a03bd2a46553938dcfc34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237283638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e686edce26811e11a8d97473d4234ef8fb283555b0b4e202d773f0ad4bb51b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:44:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:44:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:44:22 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:44:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:44:48 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:44:51 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:44:51 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:44:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:44:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:45:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:45:01 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:02 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f3786c0c40f6e8deb47a2475ea53f4977287ebe714a44d44f950aaeec98ba`  
		Last Modified: Fri, 07 Jan 2022 02:46:34 GMT  
		Size: 93.6 MB (93575399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661c522eadbab3f8f5ac630a7b61d0c75a436d97338298d029bad643809963a`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027782aea31321bb35d0f16a41c0b7207dcfbd88616de57459b062f409c5ecf3`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a02a08a1262d5108da96ace50d5ec3d318977c3a3c315a9da633d57653637d`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 577.0 KB (576963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb230869d25418bb417be80a7509bdafd7de12adab466a6c5b17dea712383139`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6956864b7724141a69ce62391a3d8d74b4546843b335af20b52817e65d788d9`  
		Last Modified: Fri, 07 Jan 2022 02:46:46 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3ecf350694a1d2de08afd09a7311d0ecdefca39df5c7fc611b9e7c07f0913c`  
		Last Modified: Fri, 07 Jan 2022 02:46:55 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4e8317f722de18d2d67e8d6dad91fbe8f8e36f355d93af5c6521bfc79db8f`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b47e16e82e4e8a2c94492e3a6d28f4e471f8ba9abc6b3380272f67ad088a0cb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226403449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8b9ffa0aa4b699cce26760edcb675c11f323cd2e592238acdb443b8614c30c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:12:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:12:24 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:12:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:12:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:12:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:13:10 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:13:11 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:13:12 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:13:13 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:13:14 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:13:15 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:13:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:13:17 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:13:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:13:21 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:13:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:13:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:13:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:13:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:13:32 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:13:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:13:34 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:13:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca822e6ba2fafa543991c7a6a40f34c01cc87fe3901534e562deb088176d7493`  
		Last Modified: Fri, 07 Jan 2022 02:15:44 GMT  
		Size: 85.7 MB (85703479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c51cef86fe6d8c848b23bf9356efd72d40eb9309423f30fb15cbc4c2742b45`  
		Last Modified: Fri, 07 Jan 2022 02:15:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51d8356f23b73c45579abe97c2e7ae9fea11535c8a366b335e028731fdcc83`  
		Last Modified: Fri, 07 Jan 2022 02:15:32 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1503bacdf75977cb3264983f76442c8a2cce1ef3523605d38ea96570902981`  
		Last Modified: Fri, 07 Jan 2022 02:15:30 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed14de4751c7e19603293038d3df64d993cb9d3d11f701dee5c99be24e969176`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2056d740f0a61d6cfbc612462f1f2bfc55803aabfa51d83a0c69e01e381430da`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ba6429c757c2825161ef4d1df346c4a723c950961988d2608a8fd4e35a7bc`  
		Last Modified: Fri, 07 Jan 2022 02:16:02 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995da71b9130454ebc7011f734b6911ae7ea272154ef258fc2d2baa7a3e0f360`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:8a1a525c2c2e7beca13cc133237b601136b7141d8994537779ec62de26402c7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233884822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1465b0f318d405395a9dddc053e84a1ca55ab0c1d0edbba80800535d446ada`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:13:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:13:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:13:42 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:13:44 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:14:37 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:14:39 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:14:41 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:14:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:14:43 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 04:14:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 04:14:46 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 04:14:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:14:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 04:15:01 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:15:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 04:15:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 04:15:16 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 04:15:21 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 04:15:22 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:15:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:15:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:15:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021461f957d0a6e3f436e80b22505497253d416b8de7e64b503b2ae5cfc8b76c`  
		Last Modified: Fri, 07 Jan 2022 04:19:33 GMT  
		Size: 86.5 MB (86479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b895c91ae5d42e185f36f5fa073cd75a72944978257a5a64cae9c4ea7a4f`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54e78cf28365c09fbdb80b2e00abd87c867f776e402bac6564fc4ab9409b3d`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518bfcc9e3ac9a0b5f936518df882fd5bd1d3007bca5c4a342e8ba78cc10c27`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fd7b363bb63768a93a8b709c099ff8aa1e1b83dccdaf975acc5bbadf353e3`  
		Last Modified: Fri, 07 Jan 2022 04:19:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9058a307703d690c23fc19ff9047c587446b7ecc91950bf35337b26f4c30c0`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f58774110fb6da4ef751fdcbd8e0b18a7ba6ae4036b986aebb26a5e04e1733a`  
		Last Modified: Fri, 07 Jan 2022 04:19:53 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89f578acd0e5c94cc8d4ef274d052711102192734d1ed63e66a1cc0cc0a318a`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:b1a5edc48538324d9258f9293d1fceef277b233d60a1647c5445f7dd59c5cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:ebc8ed86516521fb7edbd1c57902ce5a1beb1d4a285a03bd2a46553938dcfc34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237283638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e686edce26811e11a8d97473d4234ef8fb283555b0b4e202d773f0ad4bb51b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:44:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:44:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:44:22 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:44:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:44:31 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:44:47 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:44:48 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:44:48 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:44:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:44:50 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:44:51 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:44:51 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:44:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:44:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:45:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:45:01 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:02 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f3786c0c40f6e8deb47a2475ea53f4977287ebe714a44d44f950aaeec98ba`  
		Last Modified: Fri, 07 Jan 2022 02:46:34 GMT  
		Size: 93.6 MB (93575399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661c522eadbab3f8f5ac630a7b61d0c75a436d97338298d029bad643809963a`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027782aea31321bb35d0f16a41c0b7207dcfbd88616de57459b062f409c5ecf3`  
		Last Modified: Fri, 07 Jan 2022 02:46:21 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a02a08a1262d5108da96ace50d5ec3d318977c3a3c315a9da633d57653637d`  
		Last Modified: Fri, 07 Jan 2022 02:46:19 GMT  
		Size: 577.0 KB (576963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb230869d25418bb417be80a7509bdafd7de12adab466a6c5b17dea712383139`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6956864b7724141a69ce62391a3d8d74b4546843b335af20b52817e65d788d9`  
		Last Modified: Fri, 07 Jan 2022 02:46:46 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3ecf350694a1d2de08afd09a7311d0ecdefca39df5c7fc611b9e7c07f0913c`  
		Last Modified: Fri, 07 Jan 2022 02:46:55 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4e8317f722de18d2d67e8d6dad91fbe8f8e36f355d93af5c6521bfc79db8f`  
		Last Modified: Fri, 07 Jan 2022 02:46:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b47e16e82e4e8a2c94492e3a6d28f4e471f8ba9abc6b3380272f67ad088a0cb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226403449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8b9ffa0aa4b699cce26760edcb675c11f323cd2e592238acdb443b8614c30c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:12:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:12:24 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:12:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:12:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:12:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:13:10 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:13:11 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:13:12 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:13:13 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:13:14 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 02:13:15 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 02:13:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 02:13:17 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:13:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 02:13:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 02:13:21 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:13:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 02:13:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 02:13:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 02:13:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 02:13:32 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:13:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:13:34 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:13:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca822e6ba2fafa543991c7a6a40f34c01cc87fe3901534e562deb088176d7493`  
		Last Modified: Fri, 07 Jan 2022 02:15:44 GMT  
		Size: 85.7 MB (85703479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c51cef86fe6d8c848b23bf9356efd72d40eb9309423f30fb15cbc4c2742b45`  
		Last Modified: Fri, 07 Jan 2022 02:15:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d51d8356f23b73c45579abe97c2e7ae9fea11535c8a366b335e028731fdcc83`  
		Last Modified: Fri, 07 Jan 2022 02:15:32 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1503bacdf75977cb3264983f76442c8a2cce1ef3523605d38ea96570902981`  
		Last Modified: Fri, 07 Jan 2022 02:15:30 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed14de4751c7e19603293038d3df64d993cb9d3d11f701dee5c99be24e969176`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2056d740f0a61d6cfbc612462f1f2bfc55803aabfa51d83a0c69e01e381430da`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ba6429c757c2825161ef4d1df346c4a723c950961988d2608a8fd4e35a7bc`  
		Last Modified: Fri, 07 Jan 2022 02:16:02 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995da71b9130454ebc7011f734b6911ae7ea272154ef258fc2d2baa7a3e0f360`  
		Last Modified: Fri, 07 Jan 2022 02:15:55 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:8a1a525c2c2e7beca13cc133237b601136b7141d8994537779ec62de26402c7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233884822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1465b0f318d405395a9dddc053e84a1ca55ab0c1d0edbba80800535d446ada`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:13:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:13:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:13:42 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:13:44 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:14:37 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:14:39 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:14:41 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:14:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:14:43 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 07 Jan 2022 04:14:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 07 Jan 2022 04:14:46 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 07 Jan 2022 04:14:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:14:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 07 Jan 2022 04:14:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 07 Jan 2022 04:15:01 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:15:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 07 Jan 2022 04:15:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 07 Jan 2022 04:15:16 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 07 Jan 2022 04:15:21 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 07 Jan 2022 04:15:22 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:15:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:15:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:15:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021461f957d0a6e3f436e80b22505497253d416b8de7e64b503b2ae5cfc8b76c`  
		Last Modified: Fri, 07 Jan 2022 04:19:33 GMT  
		Size: 86.5 MB (86479470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b895c91ae5d42e185f36f5fa073cd75a72944978257a5a64cae9c4ea7a4f`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d54e78cf28365c09fbdb80b2e00abd87c867f776e402bac6564fc4ab9409b3d`  
		Last Modified: Fri, 07 Jan 2022 04:19:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518bfcc9e3ac9a0b5f936518df882fd5bd1d3007bca5c4a342e8ba78cc10c27`  
		Last Modified: Fri, 07 Jan 2022 04:19:12 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fd7b363bb63768a93a8b709c099ff8aa1e1b83dccdaf975acc5bbadf353e3`  
		Last Modified: Fri, 07 Jan 2022 04:19:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9058a307703d690c23fc19ff9047c587446b7ecc91950bf35337b26f4c30c0`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f58774110fb6da4ef751fdcbd8e0b18a7ba6ae4036b986aebb26a5e04e1733a`  
		Last Modified: Fri, 07 Jan 2022 04:19:53 GMT  
		Size: 116.4 MB (116415404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89f578acd0e5c94cc8d4ef274d052711102192734d1ed63e66a1cc0cc0a318a`  
		Last Modified: Fri, 07 Jan 2022 04:19:45 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:cab0d69387d03c075ccc40cc4d016ff8bd154806ab1e16b17ade51306c315239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:ed211d8966e81479a0de35d88067abc19128f5115f4ed0a18583d0109418c320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f34dfd6f06c782fe12de949e94a95aec280a87fede53c2ecf93bdd31c1415`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:45:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:45:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:45:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:45:41 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:45:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:45:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:44 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:45:45 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:45:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:45:57 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:45:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:58 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97708e1be04f300190a6447eb5701bf6136bde08c7fc9d2f100554dee600862f`  
		Last Modified: Fri, 07 Jan 2022 02:47:23 GMT  
		Size: 93.6 MB (93576944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccaf14419ce16922f1fadc9c0cfca941583821338487070f248663793e6a60`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee464fd0cad364188182240e3445e5ef7d60fcd8b054ea0f81f87bf26f2c1512`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30817fa401eb65a7fe63940c50cc18df1e57394daaec77595f0084faaa94d9b`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.0 MB (1003220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd02559b7c70dc211f68f796d7deef9233732d34de4041ea0e1b352b27736ef`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35076f161983cdfb4a547a85ce068f58dc441047b1ccc6cd3f1db1afbd64a40`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec320074cb8322b6f32e97f7fd43f3e74bceb2525a35c4d4003827d7891d876f`  
		Last Modified: Fri, 07 Jan 2022 02:47:15 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f49324ac46378dd042d253b551c923c11f94b0f5328e3e242837544501e19`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e7dc23c1c127163649ca01a096ffa92d034bf77da4f1f174af5c8ddb4f83e870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224094739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561be5fff3a0045b486baa9db80b475e8c51bacf50e62007dd73a619477d8922`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:14:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:14:24 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:14:25 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:14:26 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:14:27 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:14:28 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:14:29 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:14:30 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:14:31 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:14:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:14:33 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:14:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:36 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:14:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:14:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:14:46 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:14:47 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:14:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:14:50 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:14:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cc759bf42029a19e7ddfcc42dc0db85ecb4bd43c89e8e3e1e0f7498cff516`  
		Last Modified: Fri, 07 Jan 2022 02:16:30 GMT  
		Size: 85.7 MB (85703427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0cfcb5c10e4b2dc1bab617e8c29a34bb963f3e9ffa94e92c6c38f3bebeb04`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61837014e57970f4f06446a4c60d4f3cf530889c0fc449e3b4d758d8d4179c78`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b8055c41250c722a929d047034ec9405cb0ee956a0be28f44d1e97a044f3a`  
		Last Modified: Fri, 07 Jan 2022 02:16:17 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a9192b771b82b241d0bd13fa7ec48f7748732d4ea523071d6380c9054e1bb0`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8817c2a9b0f82e4e5e851a7431064c1dbfea617a62b83d8ff82852c72ece60`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f424b7e4fabf4819c12d14f9e2f95f08ca015a46b0be6e7cbc551ab9bd7eb5`  
		Last Modified: Fri, 07 Jan 2022 02:16:29 GMT  
		Size: 113.7 MB (113727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a990cce3d3807e01700ddcaf1423e46f68f4b5444f90731f8c07548b71962`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:462037663020c39d729f14460e7722f341e0931da832994512b8c39fb5b7b2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231551208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6432d865bfea5c9c7afba043dac44f7319a5527bee30dfb5be2f06c8240536`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:17:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:17:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:17:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:17:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:17:39 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:17:41 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:17:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:17:43 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:17:45 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 04:17:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 04:17:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 04:17:50 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:17:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:57 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:17:58 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 04:18:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 04:18:16 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 04:18:20 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:18:21 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:18:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:18:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb44345bd8b045c9d533fdd1307670dc3124100b34086b62e2d012367a9f47`  
		Last Modified: Fri, 07 Jan 2022 04:20:26 GMT  
		Size: 86.5 MB (86479514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dc5e14b9bd708430308d858539ec01f542e93120293f822ac3892ae6fda958`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1f21c8a4422e0c32d01df760d570c9a5309b085da20b79a9b1656f5edec49`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14e56a49876e7f8fad5bb0be5d8de168febc3c1dad5233c3873dd3f5b89466`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e576677d41fe97c01699d81c674a1d6ef2a174a86149d0c5b2749e5c7a5ca`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62c2cef2b599c80293c3920ffd3de1bac1117c96b801f47133c6d4068e48bd`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a056e1bfe547d7c3f62376f0f1783af91416edc53c838bf23579e91f259377`  
		Last Modified: Fri, 07 Jan 2022 04:20:19 GMT  
		Size: 113.7 MB (113727929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935338738903998b02f65580d162454b0484c90e6bb100aed85304b1c7067f3a`  
		Last Modified: Fri, 07 Jan 2022 04:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:cab0d69387d03c075ccc40cc4d016ff8bd154806ab1e16b17ade51306c315239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:ed211d8966e81479a0de35d88067abc19128f5115f4ed0a18583d0109418c320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f34dfd6f06c782fe12de949e94a95aec280a87fede53c2ecf93bdd31c1415`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:45:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:45:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:45:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:45:41 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:45:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:45:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:44 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:45:45 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:45:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:45:57 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:45:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:58 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97708e1be04f300190a6447eb5701bf6136bde08c7fc9d2f100554dee600862f`  
		Last Modified: Fri, 07 Jan 2022 02:47:23 GMT  
		Size: 93.6 MB (93576944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccaf14419ce16922f1fadc9c0cfca941583821338487070f248663793e6a60`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee464fd0cad364188182240e3445e5ef7d60fcd8b054ea0f81f87bf26f2c1512`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30817fa401eb65a7fe63940c50cc18df1e57394daaec77595f0084faaa94d9b`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.0 MB (1003220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd02559b7c70dc211f68f796d7deef9233732d34de4041ea0e1b352b27736ef`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35076f161983cdfb4a547a85ce068f58dc441047b1ccc6cd3f1db1afbd64a40`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec320074cb8322b6f32e97f7fd43f3e74bceb2525a35c4d4003827d7891d876f`  
		Last Modified: Fri, 07 Jan 2022 02:47:15 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f49324ac46378dd042d253b551c923c11f94b0f5328e3e242837544501e19`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e7dc23c1c127163649ca01a096ffa92d034bf77da4f1f174af5c8ddb4f83e870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224094739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561be5fff3a0045b486baa9db80b475e8c51bacf50e62007dd73a619477d8922`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:14:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:14:24 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:14:25 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:14:26 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:14:27 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:14:28 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:14:29 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:14:30 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:14:31 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:14:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:14:33 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:14:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:36 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:14:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:14:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:14:46 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:14:47 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:14:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:14:50 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:14:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cc759bf42029a19e7ddfcc42dc0db85ecb4bd43c89e8e3e1e0f7498cff516`  
		Last Modified: Fri, 07 Jan 2022 02:16:30 GMT  
		Size: 85.7 MB (85703427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0cfcb5c10e4b2dc1bab617e8c29a34bb963f3e9ffa94e92c6c38f3bebeb04`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61837014e57970f4f06446a4c60d4f3cf530889c0fc449e3b4d758d8d4179c78`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b8055c41250c722a929d047034ec9405cb0ee956a0be28f44d1e97a044f3a`  
		Last Modified: Fri, 07 Jan 2022 02:16:17 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a9192b771b82b241d0bd13fa7ec48f7748732d4ea523071d6380c9054e1bb0`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8817c2a9b0f82e4e5e851a7431064c1dbfea617a62b83d8ff82852c72ece60`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f424b7e4fabf4819c12d14f9e2f95f08ca015a46b0be6e7cbc551ab9bd7eb5`  
		Last Modified: Fri, 07 Jan 2022 02:16:29 GMT  
		Size: 113.7 MB (113727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a990cce3d3807e01700ddcaf1423e46f68f4b5444f90731f8c07548b71962`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:462037663020c39d729f14460e7722f341e0931da832994512b8c39fb5b7b2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231551208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6432d865bfea5c9c7afba043dac44f7319a5527bee30dfb5be2f06c8240536`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:17:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:17:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:17:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:17:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:17:39 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:17:41 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:17:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:17:43 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:17:45 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 04:17:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 04:17:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 04:17:50 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:17:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:57 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:17:58 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 04:18:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 04:18:16 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 04:18:20 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:18:21 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:18:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:18:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb44345bd8b045c9d533fdd1307670dc3124100b34086b62e2d012367a9f47`  
		Last Modified: Fri, 07 Jan 2022 04:20:26 GMT  
		Size: 86.5 MB (86479514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dc5e14b9bd708430308d858539ec01f542e93120293f822ac3892ae6fda958`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1f21c8a4422e0c32d01df760d570c9a5309b085da20b79a9b1656f5edec49`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14e56a49876e7f8fad5bb0be5d8de168febc3c1dad5233c3873dd3f5b89466`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e576677d41fe97c01699d81c674a1d6ef2a174a86149d0c5b2749e5c7a5ca`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62c2cef2b599c80293c3920ffd3de1bac1117c96b801f47133c6d4068e48bd`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a056e1bfe547d7c3f62376f0f1783af91416edc53c838bf23579e91f259377`  
		Last Modified: Fri, 07 Jan 2022 04:20:19 GMT  
		Size: 113.7 MB (113727929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935338738903998b02f65580d162454b0484c90e6bb100aed85304b1c7067f3a`  
		Last Modified: Fri, 07 Jan 2022 04:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:cab0d69387d03c075ccc40cc4d016ff8bd154806ab1e16b17ade51306c315239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:ed211d8966e81479a0de35d88067abc19128f5115f4ed0a18583d0109418c320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f34dfd6f06c782fe12de949e94a95aec280a87fede53c2ecf93bdd31c1415`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:43:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:45:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:45:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:45:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:45:41 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:45:42 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:45:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:45:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:45:44 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:45:45 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:45:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:45:57 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:45:57 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:45:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:45:58 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:45:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97708e1be04f300190a6447eb5701bf6136bde08c7fc9d2f100554dee600862f`  
		Last Modified: Fri, 07 Jan 2022 02:47:23 GMT  
		Size: 93.6 MB (93576944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccaf14419ce16922f1fadc9c0cfca941583821338487070f248663793e6a60`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee464fd0cad364188182240e3445e5ef7d60fcd8b054ea0f81f87bf26f2c1512`  
		Last Modified: Fri, 07 Jan 2022 02:47:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30817fa401eb65a7fe63940c50cc18df1e57394daaec77595f0084faaa94d9b`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.0 MB (1003220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd02559b7c70dc211f68f796d7deef9233732d34de4041ea0e1b352b27736ef`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35076f161983cdfb4a547a85ce068f58dc441047b1ccc6cd3f1db1afbd64a40`  
		Last Modified: Fri, 07 Jan 2022 02:47:07 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec320074cb8322b6f32e97f7fd43f3e74bceb2525a35c4d4003827d7891d876f`  
		Last Modified: Fri, 07 Jan 2022 02:47:15 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f49324ac46378dd042d253b551c923c11f94b0f5328e3e242837544501e19`  
		Last Modified: Fri, 07 Jan 2022 02:47:08 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e7dc23c1c127163649ca01a096ffa92d034bf77da4f1f174af5c8ddb4f83e870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224094739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561be5fff3a0045b486baa9db80b475e8c51bacf50e62007dd73a619477d8922`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:37 GMT
ADD file:def71737de83b2ed2d5ddb5520331ef14ccd496fc11b4f830b79318dd65164a3 in / 
# Fri, 07 Jan 2022 01:53:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:11:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 02:14:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 02:14:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 02:14:24 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 02:14:25 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 02:14:26 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 02:14:27 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 02:14:28 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 02:14:29 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 02:14:30 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 02:14:31 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 02:14:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 02:14:33 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 02:14:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 02:14:36 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 02:14:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 02:14:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 02:14:46 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 02:14:47 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 02:14:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 02:14:50 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 02:14:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:976e4515cbe3bb05d3eaff6aa830f00c2593211ff7600840d5e9a030c803bbee`  
		Last Modified: Fri, 07 Jan 2022 01:55:15 GMT  
		Size: 23.7 MB (23726915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cc759bf42029a19e7ddfcc42dc0db85ecb4bd43c89e8e3e1e0f7498cff516`  
		Last Modified: Fri, 07 Jan 2022 02:16:30 GMT  
		Size: 85.7 MB (85703427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0cfcb5c10e4b2dc1bab617e8c29a34bb963f3e9ffa94e92c6c38f3bebeb04`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61837014e57970f4f06446a4c60d4f3cf530889c0fc449e3b4d758d8d4179c78`  
		Last Modified: Fri, 07 Jan 2022 02:16:19 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b8055c41250c722a929d047034ec9405cb0ee956a0be28f44d1e97a044f3a`  
		Last Modified: Fri, 07 Jan 2022 02:16:17 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a9192b771b82b241d0bd13fa7ec48f7748732d4ea523071d6380c9054e1bb0`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8817c2a9b0f82e4e5e851a7431064c1dbfea617a62b83d8ff82852c72ece60`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f424b7e4fabf4819c12d14f9e2f95f08ca015a46b0be6e7cbc551ab9bd7eb5`  
		Last Modified: Fri, 07 Jan 2022 02:16:29 GMT  
		Size: 113.7 MB (113727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a990cce3d3807e01700ddcaf1423e46f68f4b5444f90731f8c07548b71962`  
		Last Modified: Fri, 07 Jan 2022 02:16:16 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:462037663020c39d729f14460e7722f341e0931da832994512b8c39fb5b7b2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231551208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6432d865bfea5c9c7afba043dac44f7319a5527bee30dfb5be2f06c8240536`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:11:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 07 Jan 2022 04:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:17:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 07 Jan 2022 04:17:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 07 Jan 2022 04:17:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 07 Jan 2022 04:17:37 GMT
ARG BONITA_VERSION
# Fri, 07 Jan 2022 04:17:39 GMT
ARG BRANDING_VERSION
# Fri, 07 Jan 2022 04:17:41 GMT
ARG BONITA_SHA256
# Fri, 07 Jan 2022 04:17:42 GMT
ARG BASE_URL
# Fri, 07 Jan 2022 04:17:43 GMT
ARG BONITA_URL
# Fri, 07 Jan 2022 04:17:45 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 07 Jan 2022 04:17:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 07 Jan 2022 04:17:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 07 Jan 2022 04:17:50 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 07 Jan 2022 04:17:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 07 Jan 2022 04:17:57 GMT
RUN mkdir /opt/files
# Fri, 07 Jan 2022 04:17:58 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 07 Jan 2022 04:18:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 07 Jan 2022 04:18:16 GMT
ENV HTTP_API=false
# Fri, 07 Jan 2022 04:18:20 GMT
VOLUME [/opt/bonita]
# Fri, 07 Jan 2022 04:18:21 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 07 Jan 2022 04:18:24 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 04:18:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb44345bd8b045c9d533fdd1307670dc3124100b34086b62e2d012367a9f47`  
		Last Modified: Fri, 07 Jan 2022 04:20:26 GMT  
		Size: 86.5 MB (86479514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dc5e14b9bd708430308d858539ec01f542e93120293f822ac3892ae6fda958`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1f21c8a4422e0c32d01df760d570c9a5309b085da20b79a9b1656f5edec49`  
		Last Modified: Fri, 07 Jan 2022 04:20:11 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14e56a49876e7f8fad5bb0be5d8de168febc3c1dad5233c3873dd3f5b89466`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e576677d41fe97c01699d81c674a1d6ef2a174a86149d0c5b2749e5c7a5ca`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62c2cef2b599c80293c3920ffd3de1bac1117c96b801f47133c6d4068e48bd`  
		Last Modified: Fri, 07 Jan 2022 04:20:09 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a056e1bfe547d7c3f62376f0f1783af91416edc53c838bf23579e91f259377`  
		Last Modified: Fri, 07 Jan 2022 04:20:19 GMT  
		Size: 113.7 MB (113727929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935338738903998b02f65580d162454b0484c90e6bb100aed85304b1c7067f3a`  
		Last Modified: Fri, 07 Jan 2022 04:20:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
