<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:d997aa9ad816ea5d6c1458d42eaced9b6ca06c3d8ebf1c6162b4058909c11ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:4c28435d9e29513ff0f7daecfec61544df34fa974e831e25f931c60d73940ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237485947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cc15457b62c1ba8644edcb7278542a9f91ee4c2e6f59e0453a0b97647f392`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:45:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:45:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:45:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 18:45:51 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:52 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 18:45:53 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:45:53 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 18:45:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 18:46:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 18:46:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 18:46:01 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50e772b503a53e97f96f1c7602b04e6dee66044b4115a656657015cc8dd0b7`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 93.8 MB (93843076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26eb43ae80cdb0d32344078dcc9a34e5168ec38544ca6ec2d6a570c0bd22c8`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60cd03e6c4f2bb07959adeb37f665329f44d70461b01bb7e4a7f2e4a33c361`  
		Last Modified: Tue, 02 Aug 2022 18:47:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3baeb6788537273b4b4ea7b4ca7add2abb8b81aca7a21c8f20cb5c658d097fe`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139969e8126173a3227b1abe266a8119550d2a8bbb2d1a65c3ffe36da819411`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7ca1df3999ff9027299abbcb37e390c0e998fedf8167460080fa1458573f53`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95336ada909617a31482b70af8d5f5e51498eb4e30afa6cbae66ca5e0049968`  
		Last Modified: Tue, 02 Aug 2022 18:47:37 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed438aef59d48263abab0591f1e5f4be92ead54ccb43b8c1c57c1b5facec9769`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:7bc1335543046a6dd7d06f090955a3204bfed48ecfc8f4b9899f43dff86454f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234088437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e17431b963d1f161f609c17ebccad1f36e19e05ab17fd6f3906a210a8933e1a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:07:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:07:24 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:07:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:07:29 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:07:59 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:08:01 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 03 Aug 2022 05:08:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:04 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 03 Aug 2022 05:08:05 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:08:05 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 03 Aug 2022 05:08:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 03 Aug 2022 05:08:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 03 Aug 2022 05:08:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 03 Aug 2022 05:08:20 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:08:20 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:08:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:08:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b31369e09324837ebcfe71c796fbc549f88dff24cc1111dd1a16adef432b2`  
		Last Modified: Wed, 03 Aug 2022 05:11:36 GMT  
		Size: 86.7 MB (86745371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748c9dadd8a0ae7fa27991cf4bfdd58f04af324f0ecb1bb513f416b7e2cdd1`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae7e6c915ca7eeb44d03e192578649098bd7556054f054274cf6a5110db5ab`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68eee231caf7c472a13cdb9165a2dd3731d6f29c9ee664da8021a6750e31a16`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41304b336aa347d94138569466e2b1eb8c69a0af1acc02ea20b6acab57f62ff3`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb024cfbce69a96adef142a44361e6337d45372520471dedcdd0491ed3a9065`  
		Last Modified: Wed, 03 Aug 2022 05:11:49 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88affdd254787a75dcba51b39ff4cd09c2e806100ccd0856d9d38f9dc46637e`  
		Last Modified: Wed, 03 Aug 2022 05:11:58 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac4c679d1130e257a063b79b900758a532da3c6ec664dc5caa9642a3d6ceb9`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:21202e332caf9ad62f42241d93eebf061ec29a30335aeb393a0cfaa3764ab113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:1388ad814f4f35bf67df229b9c51eec3bf07ceed47d60e9bc299c9440f61150a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235221886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a04f6ce33e1510259cfe5c41c4375e8860cd6bf9eab5745ba885d600b90cd0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:46:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:46:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:46:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 18:46:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:46:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:33 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:46:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 18:46:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 18:46:43 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 18:46:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:44 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec60a66b5ad49a9fc5ae72d2d837c3ead083a79a8cd775cd816ffcd70f66262a`  
		Last Modified: Tue, 02 Aug 2022 18:48:04 GMT  
		Size: 93.8 MB (93846025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48581e1ff3b8c4cc198e8a64401742ad31d1974f84b6787966cc26dcc8f0ce`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad1f5d5e2b55f54ef10f24a0743b24d7acabb3694ba9063fcbabae51b7db121`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483cc6170e8dc85ef8cf416062b65510b66e77cd0a095fca1860fbba19afcaa5`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 930.5 KB (930474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b3f18eb96ef9c253503172278278db98c924179a86195ca8709ad357a672d0`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfacd6f1616f2ee9ac5804a9f2a77020d21adabf4951755fecc916f939cf03f6`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec6677533059e6e25a9e3104dd0244cf6414f60ad33469ed5f5211f591ed151`  
		Last Modified: Tue, 02 Aug 2022 18:47:56 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef62cc2ef2cfab90a2571aa6ca98cd9f41131681af5d812aa2ef10b2745b4d57`  
		Last Modified: Tue, 02 Aug 2022 18:47:49 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:104bd22f729718e53913546312a87feece478baf9906574ec4601102a26b34f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231753607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032e61e16b0c4ae75a45441568ab1bee2357887dba582bf24c07d60e1a08a02e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:09:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:09:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:09:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:09:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 03 Aug 2022 05:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:09:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:28 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:09:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 03 Aug 2022 05:09:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 03 Aug 2022 05:09:44 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:09:46 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:09:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:09:48 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:09:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475e316bd9acaa47733ba1107b4f62f103b220d02f6598f876eb8f11a65191c4`  
		Last Modified: Wed, 03 Aug 2022 05:12:37 GMT  
		Size: 86.7 MB (86745403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc81ca2381301f3b0aa03ce612a7a53264aaa54898500b4580193ee3b5787eaf`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd97ed69e27f69c0cfcb6be5f7da1ec7ab6de99afdeed6f63a0438917c9db0`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd51f93d71b36667276e184462a195757d3dda83290d91a4ab6ad70da4506006`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 831.6 KB (831576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50442e8686d94b53f39d0e83a1f10bc50a1fec4b2232b7d6653e6c8a295fe47`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f40705227a8a5b89d9458fa24e75d8749de068b98429a42b7d7f544601812d3`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d8b2a17aaa7d141b1a0b768b50528eecf323a6dc5aed713a24f990b93d6ae4`  
		Last Modified: Wed, 03 Aug 2022 05:12:25 GMT  
		Size: 113.7 MB (113727950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b03d035ea68677c4bc02fea9b835cf9c48e5198a6a7ef597140e15cff2714c`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:21202e332caf9ad62f42241d93eebf061ec29a30335aeb393a0cfaa3764ab113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:1388ad814f4f35bf67df229b9c51eec3bf07ceed47d60e9bc299c9440f61150a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235221886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a04f6ce33e1510259cfe5c41c4375e8860cd6bf9eab5745ba885d600b90cd0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:46:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:46:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:46:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 18:46:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:46:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:33 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:46:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 18:46:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 18:46:43 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 18:46:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:44 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec60a66b5ad49a9fc5ae72d2d837c3ead083a79a8cd775cd816ffcd70f66262a`  
		Last Modified: Tue, 02 Aug 2022 18:48:04 GMT  
		Size: 93.8 MB (93846025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48581e1ff3b8c4cc198e8a64401742ad31d1974f84b6787966cc26dcc8f0ce`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad1f5d5e2b55f54ef10f24a0743b24d7acabb3694ba9063fcbabae51b7db121`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483cc6170e8dc85ef8cf416062b65510b66e77cd0a095fca1860fbba19afcaa5`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 930.5 KB (930474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b3f18eb96ef9c253503172278278db98c924179a86195ca8709ad357a672d0`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfacd6f1616f2ee9ac5804a9f2a77020d21adabf4951755fecc916f939cf03f6`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec6677533059e6e25a9e3104dd0244cf6414f60ad33469ed5f5211f591ed151`  
		Last Modified: Tue, 02 Aug 2022 18:47:56 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef62cc2ef2cfab90a2571aa6ca98cd9f41131681af5d812aa2ef10b2745b4d57`  
		Last Modified: Tue, 02 Aug 2022 18:47:49 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:104bd22f729718e53913546312a87feece478baf9906574ec4601102a26b34f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231753607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032e61e16b0c4ae75a45441568ab1bee2357887dba582bf24c07d60e1a08a02e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:09:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:09:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:09:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:09:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 03 Aug 2022 05:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:09:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:28 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:09:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 03 Aug 2022 05:09:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 03 Aug 2022 05:09:44 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:09:46 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:09:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:09:48 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:09:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475e316bd9acaa47733ba1107b4f62f103b220d02f6598f876eb8f11a65191c4`  
		Last Modified: Wed, 03 Aug 2022 05:12:37 GMT  
		Size: 86.7 MB (86745403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc81ca2381301f3b0aa03ce612a7a53264aaa54898500b4580193ee3b5787eaf`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd97ed69e27f69c0cfcb6be5f7da1ec7ab6de99afdeed6f63a0438917c9db0`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd51f93d71b36667276e184462a195757d3dda83290d91a4ab6ad70da4506006`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 831.6 KB (831576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50442e8686d94b53f39d0e83a1f10bc50a1fec4b2232b7d6653e6c8a295fe47`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f40705227a8a5b89d9458fa24e75d8749de068b98429a42b7d7f544601812d3`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d8b2a17aaa7d141b1a0b768b50528eecf323a6dc5aed713a24f990b93d6ae4`  
		Last Modified: Wed, 03 Aug 2022 05:12:25 GMT  
		Size: 113.7 MB (113727950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b03d035ea68677c4bc02fea9b835cf9c48e5198a6a7ef597140e15cff2714c`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:11602f6ed9f49abed20683f1159d264c7a6154282ad3f111208195152e278a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:48760e95c35390b2f492b6559173e8657c8090ecf1addac2e6d5321b8766abb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176141080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92d51b64fd81e2820bf03fd32b01e26ff31e7afb71e0f380075780c9f9b9f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 05:09:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:10:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 03 Aug 2022 05:10:08 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:10:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 03 Aug 2022 05:10:12 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:10:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:14 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:10:14 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 03 Aug 2022 05:10:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 03 Aug 2022 05:10:28 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_PASSWORD=
# Wed, 03 Aug 2022 05:10:29 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 03 Aug 2022 05:10:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 03 Aug 2022 05:10:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 03 Aug 2022 05:10:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 03 Aug 2022 05:10:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 03 Aug 2022 05:10:32 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 03 Aug 2022 05:10:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 03 Aug 2022 05:10:33 GMT
EXPOSE 8080 9000
# Wed, 03 Aug 2022 05:10:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 03 Aug 2022 05:10:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe7f2bfe5410564aa1d74ccdf5603a737a00741e3f8dc84dc84c28bb8f1a58f`  
		Last Modified: Wed, 03 Aug 2022 05:13:14 GMT  
		Size: 56.6 MB (56628611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b8084c78560f49de74a1058aa78d78c6a33ec20f4eb201815dfa9c0e2b1ff`  
		Last Modified: Wed, 03 Aug 2022 05:13:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a124e0c3c91ead8397c5d4f2810e2f574cd5b9af598a679a798928575165`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f1fdf212a0809b9ec41ba55e07a03ce48470dd631703579e78a56a77a63cf8`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec537158f98211470b7015d0c8ca91221c3ff8b7e18f153c6c339747fcc9002`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 3.0 KB (3035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30501a7752eaf75497ee5c0684eb0ea40f814bf87c77dace4d269de932ee059d`  
		Last Modified: Wed, 03 Aug 2022 05:13:09 GMT  
		Size: 116.7 MB (116690803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b1e9e5d6b48d6b433d918804c917f0e2f3c3b5a049ec7ad373b4045e5180a`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:11602f6ed9f49abed20683f1159d264c7a6154282ad3f111208195152e278a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:48760e95c35390b2f492b6559173e8657c8090ecf1addac2e6d5321b8766abb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176141080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92d51b64fd81e2820bf03fd32b01e26ff31e7afb71e0f380075780c9f9b9f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 05:09:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:10:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 03 Aug 2022 05:10:08 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:10:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 03 Aug 2022 05:10:12 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:10:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:14 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:10:14 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 03 Aug 2022 05:10:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 03 Aug 2022 05:10:28 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_PASSWORD=
# Wed, 03 Aug 2022 05:10:29 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 03 Aug 2022 05:10:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 03 Aug 2022 05:10:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 03 Aug 2022 05:10:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 03 Aug 2022 05:10:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 03 Aug 2022 05:10:32 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 03 Aug 2022 05:10:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 03 Aug 2022 05:10:33 GMT
EXPOSE 8080 9000
# Wed, 03 Aug 2022 05:10:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 03 Aug 2022 05:10:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe7f2bfe5410564aa1d74ccdf5603a737a00741e3f8dc84dc84c28bb8f1a58f`  
		Last Modified: Wed, 03 Aug 2022 05:13:14 GMT  
		Size: 56.6 MB (56628611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b8084c78560f49de74a1058aa78d78c6a33ec20f4eb201815dfa9c0e2b1ff`  
		Last Modified: Wed, 03 Aug 2022 05:13:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a124e0c3c91ead8397c5d4f2810e2f574cd5b9af598a679a798928575165`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f1fdf212a0809b9ec41ba55e07a03ce48470dd631703579e78a56a77a63cf8`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec537158f98211470b7015d0c8ca91221c3ff8b7e18f153c6c339747fcc9002`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 3.0 KB (3035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30501a7752eaf75497ee5c0684eb0ea40f814bf87c77dace4d269de932ee059d`  
		Last Modified: Wed, 03 Aug 2022 05:13:09 GMT  
		Size: 116.7 MB (116690803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b1e9e5d6b48d6b433d918804c917f0e2f3c3b5a049ec7ad373b4045e5180a`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:f4aa6b808caeb5998c6591852ae2d74ccb5256fff87b5660e869c6d11f973a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:02c25843148941a2b16711ab605ab4952d7c1852901981edc10a50c92dbdd132
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234418320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06915655aba02e781626a3b39e648d7a1b9501a76f1efb8206eacdd938a4fad0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:45:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:45:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:45:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 18:45:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:45:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 18:45:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 18:45:34 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:45:34 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 18:45:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 18:45:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 18:45:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 18:45:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:45:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:45:43 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:45:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50e772b503a53e97f96f1c7602b04e6dee66044b4115a656657015cc8dd0b7`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 93.8 MB (93843076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26eb43ae80cdb0d32344078dcc9a34e5168ec38544ca6ec2d6a570c0bd22c8`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60cd03e6c4f2bb07959adeb37f665329f44d70461b01bb7e4a7f2e4a33c361`  
		Last Modified: Tue, 02 Aug 2022 18:47:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3baeb6788537273b4b4ea7b4ca7add2abb8b81aca7a21c8f20cb5c658d097fe`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed2d1cc863c23ea8586d2c6539c20cc81c2eb1902d1828f21e31596ca0d0805`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0866043632c88df795dcadb6becec0ed8033f63e8beac4c2e8efab3dfd1baa`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5867343bf3768ae661845f5c164588dd7cd33b40c66447517199c6ff8ff18b59`  
		Last Modified: Tue, 02 Aug 2022 18:47:11 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0818f06db5477f06b6fa1c112b1c9f90ab1feb76255549f24602e506ac70337`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e8a118dff4de791d93f6c11e94b08c9a1164d7181f64c797acf2d91de067a090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223530644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646571e35ae1a4d11e8d547c9a5860e82aefbca8adddfea403ef44603cbac11c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:18 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:19 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:20 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:21 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 17:41:22 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 17:41:23 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:27 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:41:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 17:41:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:41:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:41:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:41:36 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:41:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:41:38 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:41:39 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad50631eb49c8f19312feae82197b8c84c7acda252a4d27c2ee52deb5531d3cc`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f352bba50f5659567c93213547f0571de628a75a84ffd8ff6d7cc7806fd98`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 6.9 KB (6867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6320208c13dc7f0655e4ee6d692280f7cabac4e50f1edb8f7243d23813baaf6`  
		Last Modified: Tue, 02 Aug 2022 17:44:00 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cde75c267c8cce58f6c22396d464208efe6533f6ffe92f17cfe14954b72b00`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:f1b6835a073a81a46f28444e2534b8c554b4837cef54472cd466ae02bc3ac72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231020811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c683fdb6db188b983b33307169630ffaaede4c2ba4ef376e8d93788b7318d2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:07:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:07:24 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:07:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:07:29 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 03 Aug 2022 05:07:31 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:07:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 03 Aug 2022 05:07:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 03 Aug 2022 05:07:34 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:07:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 03 Aug 2022 05:07:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 03 Aug 2022 05:07:47 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 03 Aug 2022 05:07:49 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 03 Aug 2022 05:07:49 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:07:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:07:50 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:07:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b31369e09324837ebcfe71c796fbc549f88dff24cc1111dd1a16adef432b2`  
		Last Modified: Wed, 03 Aug 2022 05:11:36 GMT  
		Size: 86.7 MB (86745371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748c9dadd8a0ae7fa27991cf4bfdd58f04af324f0ecb1bb513f416b7e2cdd1`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae7e6c915ca7eeb44d03e192578649098bd7556054f054274cf6a5110db5ab`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68eee231caf7c472a13cdb9165a2dd3731d6f29c9ee664da8021a6750e31a16`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6deede1e91bf0c3e37964900714cd745fb1f3cdbd22706d3f5e058d724c4331`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89f5b66720d3797e4dd263ba62d1ace42cb45e775549a4176a8697f48881594`  
		Last Modified: Wed, 03 Aug 2022 05:11:14 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002cc7c0dfc3fc754f7713915485de38edf796ebbeb5fb5555a6add812bfd054`  
		Last Modified: Wed, 03 Aug 2022 05:11:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c1bfdb95498694faf74e1957073c05b24c53e0c518a80e2f2e33c0cdab935c`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:f4aa6b808caeb5998c6591852ae2d74ccb5256fff87b5660e869c6d11f973a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:02c25843148941a2b16711ab605ab4952d7c1852901981edc10a50c92dbdd132
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234418320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06915655aba02e781626a3b39e648d7a1b9501a76f1efb8206eacdd938a4fad0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:45:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:45:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:45:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 18:45:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 18:45:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:45:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 18:45:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 18:45:34 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:45:34 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 18:45:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 18:45:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 18:45:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 18:45:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:45:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:45:43 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:45:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50e772b503a53e97f96f1c7602b04e6dee66044b4115a656657015cc8dd0b7`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 93.8 MB (93843076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26eb43ae80cdb0d32344078dcc9a34e5168ec38544ca6ec2d6a570c0bd22c8`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60cd03e6c4f2bb07959adeb37f665329f44d70461b01bb7e4a7f2e4a33c361`  
		Last Modified: Tue, 02 Aug 2022 18:47:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3baeb6788537273b4b4ea7b4ca7add2abb8b81aca7a21c8f20cb5c658d097fe`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed2d1cc863c23ea8586d2c6539c20cc81c2eb1902d1828f21e31596ca0d0805`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0866043632c88df795dcadb6becec0ed8033f63e8beac4c2e8efab3dfd1baa`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5867343bf3768ae661845f5c164588dd7cd33b40c66447517199c6ff8ff18b59`  
		Last Modified: Tue, 02 Aug 2022 18:47:11 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0818f06db5477f06b6fa1c112b1c9f90ab1feb76255549f24602e506ac70337`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e8a118dff4de791d93f6c11e94b08c9a1164d7181f64c797acf2d91de067a090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223530644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646571e35ae1a4d11e8d547c9a5860e82aefbca8adddfea403ef44603cbac11c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:18 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:19 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:20 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:21 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 17:41:22 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 17:41:23 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:27 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:41:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 17:41:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:41:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:41:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:41:36 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:41:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:41:38 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:41:39 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad50631eb49c8f19312feae82197b8c84c7acda252a4d27c2ee52deb5531d3cc`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f352bba50f5659567c93213547f0571de628a75a84ffd8ff6d7cc7806fd98`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 6.9 KB (6867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6320208c13dc7f0655e4ee6d692280f7cabac4e50f1edb8f7243d23813baaf6`  
		Last Modified: Tue, 02 Aug 2022 17:44:00 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cde75c267c8cce58f6c22396d464208efe6533f6ffe92f17cfe14954b72b00`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:f1b6835a073a81a46f28444e2534b8c554b4837cef54472cd466ae02bc3ac72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231020811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c683fdb6db188b983b33307169630ffaaede4c2ba4ef376e8d93788b7318d2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:07:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:07:24 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:07:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:07:29 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 03 Aug 2022 05:07:31 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 03 Aug 2022 05:07:31 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:07:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 03 Aug 2022 05:07:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 03 Aug 2022 05:07:34 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:07:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 03 Aug 2022 05:07:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 03 Aug 2022 05:07:47 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 03 Aug 2022 05:07:49 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 03 Aug 2022 05:07:49 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:07:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:07:50 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:07:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b31369e09324837ebcfe71c796fbc549f88dff24cc1111dd1a16adef432b2`  
		Last Modified: Wed, 03 Aug 2022 05:11:36 GMT  
		Size: 86.7 MB (86745371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748c9dadd8a0ae7fa27991cf4bfdd58f04af324f0ecb1bb513f416b7e2cdd1`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae7e6c915ca7eeb44d03e192578649098bd7556054f054274cf6a5110db5ab`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68eee231caf7c472a13cdb9165a2dd3731d6f29c9ee664da8021a6750e31a16`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6deede1e91bf0c3e37964900714cd745fb1f3cdbd22706d3f5e058d724c4331`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89f5b66720d3797e4dd263ba62d1ace42cb45e775549a4176a8697f48881594`  
		Last Modified: Wed, 03 Aug 2022 05:11:14 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002cc7c0dfc3fc754f7713915485de38edf796ebbeb5fb5555a6add812bfd054`  
		Last Modified: Wed, 03 Aug 2022 05:11:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c1bfdb95498694faf74e1957073c05b24c53e0c518a80e2f2e33c0cdab935c`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:d997aa9ad816ea5d6c1458d42eaced9b6ca06c3d8ebf1c6162b4058909c11ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:4c28435d9e29513ff0f7daecfec61544df34fa974e831e25f931c60d73940ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237485947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cc15457b62c1ba8644edcb7278542a9f91ee4c2e6f59e0453a0b97647f392`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:45:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:45:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:45:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 18:45:51 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:52 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 18:45:53 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:45:53 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 18:45:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 18:46:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 18:46:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 18:46:01 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50e772b503a53e97f96f1c7602b04e6dee66044b4115a656657015cc8dd0b7`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 93.8 MB (93843076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26eb43ae80cdb0d32344078dcc9a34e5168ec38544ca6ec2d6a570c0bd22c8`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60cd03e6c4f2bb07959adeb37f665329f44d70461b01bb7e4a7f2e4a33c361`  
		Last Modified: Tue, 02 Aug 2022 18:47:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3baeb6788537273b4b4ea7b4ca7add2abb8b81aca7a21c8f20cb5c658d097fe`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139969e8126173a3227b1abe266a8119550d2a8bbb2d1a65c3ffe36da819411`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7ca1df3999ff9027299abbcb37e390c0e998fedf8167460080fa1458573f53`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95336ada909617a31482b70af8d5f5e51498eb4e30afa6cbae66ca5e0049968`  
		Last Modified: Tue, 02 Aug 2022 18:47:37 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed438aef59d48263abab0591f1e5f4be92ead54ccb43b8c1c57c1b5facec9769`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:7bc1335543046a6dd7d06f090955a3204bfed48ecfc8f4b9899f43dff86454f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234088437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e17431b963d1f161f609c17ebccad1f36e19e05ab17fd6f3906a210a8933e1a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:07:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:07:24 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:07:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:07:29 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:07:59 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:08:01 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 03 Aug 2022 05:08:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:04 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 03 Aug 2022 05:08:05 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:08:05 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 03 Aug 2022 05:08:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 03 Aug 2022 05:08:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 03 Aug 2022 05:08:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 03 Aug 2022 05:08:20 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:08:20 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:08:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:08:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b31369e09324837ebcfe71c796fbc549f88dff24cc1111dd1a16adef432b2`  
		Last Modified: Wed, 03 Aug 2022 05:11:36 GMT  
		Size: 86.7 MB (86745371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748c9dadd8a0ae7fa27991cf4bfdd58f04af324f0ecb1bb513f416b7e2cdd1`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae7e6c915ca7eeb44d03e192578649098bd7556054f054274cf6a5110db5ab`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68eee231caf7c472a13cdb9165a2dd3731d6f29c9ee664da8021a6750e31a16`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41304b336aa347d94138569466e2b1eb8c69a0af1acc02ea20b6acab57f62ff3`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb024cfbce69a96adef142a44361e6337d45372520471dedcdd0491ed3a9065`  
		Last Modified: Wed, 03 Aug 2022 05:11:49 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88affdd254787a75dcba51b39ff4cd09c2e806100ccd0856d9d38f9dc46637e`  
		Last Modified: Wed, 03 Aug 2022 05:11:58 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac4c679d1130e257a063b79b900758a532da3c6ec664dc5caa9642a3d6ceb9`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:d997aa9ad816ea5d6c1458d42eaced9b6ca06c3d8ebf1c6162b4058909c11ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:4c28435d9e29513ff0f7daecfec61544df34fa974e831e25f931c60d73940ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237485947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cc15457b62c1ba8644edcb7278542a9f91ee4c2e6f59e0453a0b97647f392`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:45:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:45:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:45:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:45:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 18:45:51 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:45:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 18:45:52 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 18:45:53 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:45:53 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 18:45:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 18:46:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 18:46:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 18:46:01 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:01 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:02 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50e772b503a53e97f96f1c7602b04e6dee66044b4115a656657015cc8dd0b7`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 93.8 MB (93843076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad26eb43ae80cdb0d32344078dcc9a34e5168ec38544ca6ec2d6a570c0bd22c8`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60cd03e6c4f2bb07959adeb37f665329f44d70461b01bb7e4a7f2e4a33c361`  
		Last Modified: Tue, 02 Aug 2022 18:47:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3baeb6788537273b4b4ea7b4ca7add2abb8b81aca7a21c8f20cb5c658d097fe`  
		Last Modified: Tue, 02 Aug 2022 18:47:06 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139969e8126173a3227b1abe266a8119550d2a8bbb2d1a65c3ffe36da819411`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7ca1df3999ff9027299abbcb37e390c0e998fedf8167460080fa1458573f53`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95336ada909617a31482b70af8d5f5e51498eb4e30afa6cbae66ca5e0049968`  
		Last Modified: Tue, 02 Aug 2022 18:47:37 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed438aef59d48263abab0591f1e5f4be92ead54ccb43b8c1c57c1b5facec9769`  
		Last Modified: Tue, 02 Aug 2022 18:47:31 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:7bc1335543046a6dd7d06f090955a3204bfed48ecfc8f4b9899f43dff86454f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234088437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e17431b963d1f161f609c17ebccad1f36e19e05ab17fd6f3906a210a8933e1a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:07:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:07:24 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:07:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:07:29 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:07:30 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:07:59 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:08:00 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:08:01 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 03 Aug 2022 05:08:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 03 Aug 2022 05:08:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:08:03 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 03 Aug 2022 05:08:04 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 03 Aug 2022 05:08:05 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:08:05 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 03 Aug 2022 05:08:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 03 Aug 2022 05:08:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 03 Aug 2022 05:08:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 03 Aug 2022 05:08:20 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:08:20 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:08:20 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:08:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5b31369e09324837ebcfe71c796fbc549f88dff24cc1111dd1a16adef432b2`  
		Last Modified: Wed, 03 Aug 2022 05:11:36 GMT  
		Size: 86.7 MB (86745371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2748c9dadd8a0ae7fa27991cf4bfdd58f04af324f0ecb1bb513f416b7e2cdd1`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae7e6c915ca7eeb44d03e192578649098bd7556054f054274cf6a5110db5ab`  
		Last Modified: Wed, 03 Aug 2022 05:11:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68eee231caf7c472a13cdb9165a2dd3731d6f29c9ee664da8021a6750e31a16`  
		Last Modified: Wed, 03 Aug 2022 05:11:15 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41304b336aa347d94138569466e2b1eb8c69a0af1acc02ea20b6acab57f62ff3`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb024cfbce69a96adef142a44361e6337d45372520471dedcdd0491ed3a9065`  
		Last Modified: Wed, 03 Aug 2022 05:11:49 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88affdd254787a75dcba51b39ff4cd09c2e806100ccd0856d9d38f9dc46637e`  
		Last Modified: Wed, 03 Aug 2022 05:11:58 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac4c679d1130e257a063b79b900758a532da3c6ec664dc5caa9642a3d6ceb9`  
		Last Modified: Wed, 03 Aug 2022 05:11:50 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:21202e332caf9ad62f42241d93eebf061ec29a30335aeb393a0cfaa3764ab113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:1388ad814f4f35bf67df229b9c51eec3bf07ceed47d60e9bc299c9440f61150a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235221886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a04f6ce33e1510259cfe5c41c4375e8860cd6bf9eab5745ba885d600b90cd0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:46:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:46:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:46:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 18:46:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:46:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:33 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:46:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 18:46:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 18:46:43 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 18:46:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:44 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec60a66b5ad49a9fc5ae72d2d837c3ead083a79a8cd775cd816ffcd70f66262a`  
		Last Modified: Tue, 02 Aug 2022 18:48:04 GMT  
		Size: 93.8 MB (93846025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48581e1ff3b8c4cc198e8a64401742ad31d1974f84b6787966cc26dcc8f0ce`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad1f5d5e2b55f54ef10f24a0743b24d7acabb3694ba9063fcbabae51b7db121`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483cc6170e8dc85ef8cf416062b65510b66e77cd0a095fca1860fbba19afcaa5`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 930.5 KB (930474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b3f18eb96ef9c253503172278278db98c924179a86195ca8709ad357a672d0`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfacd6f1616f2ee9ac5804a9f2a77020d21adabf4951755fecc916f939cf03f6`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec6677533059e6e25a9e3104dd0244cf6414f60ad33469ed5f5211f591ed151`  
		Last Modified: Tue, 02 Aug 2022 18:47:56 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef62cc2ef2cfab90a2571aa6ca98cd9f41131681af5d812aa2ef10b2745b4d57`  
		Last Modified: Tue, 02 Aug 2022 18:47:49 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:104bd22f729718e53913546312a87feece478baf9906574ec4601102a26b34f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231753607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032e61e16b0c4ae75a45441568ab1bee2357887dba582bf24c07d60e1a08a02e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:09:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:09:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:09:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:09:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 03 Aug 2022 05:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:09:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:28 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:09:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 03 Aug 2022 05:09:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 03 Aug 2022 05:09:44 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:09:46 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:09:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:09:48 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:09:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475e316bd9acaa47733ba1107b4f62f103b220d02f6598f876eb8f11a65191c4`  
		Last Modified: Wed, 03 Aug 2022 05:12:37 GMT  
		Size: 86.7 MB (86745403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc81ca2381301f3b0aa03ce612a7a53264aaa54898500b4580193ee3b5787eaf`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd97ed69e27f69c0cfcb6be5f7da1ec7ab6de99afdeed6f63a0438917c9db0`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd51f93d71b36667276e184462a195757d3dda83290d91a4ab6ad70da4506006`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 831.6 KB (831576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50442e8686d94b53f39d0e83a1f10bc50a1fec4b2232b7d6653e6c8a295fe47`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f40705227a8a5b89d9458fa24e75d8749de068b98429a42b7d7f544601812d3`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d8b2a17aaa7d141b1a0b768b50528eecf323a6dc5aed713a24f990b93d6ae4`  
		Last Modified: Wed, 03 Aug 2022 05:12:25 GMT  
		Size: 113.7 MB (113727950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b03d035ea68677c4bc02fea9b835cf9c48e5198a6a7ef597140e15cff2714c`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:21202e332caf9ad62f42241d93eebf061ec29a30335aeb393a0cfaa3764ab113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:1388ad814f4f35bf67df229b9c51eec3bf07ceed47d60e9bc299c9440f61150a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235221886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a04f6ce33e1510259cfe5c41c4375e8860cd6bf9eab5745ba885d600b90cd0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:43:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 18:46:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 18:46:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 18:46:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 18:46:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 18:46:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 18:46:33 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 18:46:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 18:46:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 18:46:43 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 18:46:43 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 18:46:43 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 18:46:44 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 18:46:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec60a66b5ad49a9fc5ae72d2d837c3ead083a79a8cd775cd816ffcd70f66262a`  
		Last Modified: Tue, 02 Aug 2022 18:48:04 GMT  
		Size: 93.8 MB (93846025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de48581e1ff3b8c4cc198e8a64401742ad31d1974f84b6787966cc26dcc8f0ce`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad1f5d5e2b55f54ef10f24a0743b24d7acabb3694ba9063fcbabae51b7db121`  
		Last Modified: Tue, 02 Aug 2022 18:47:52 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483cc6170e8dc85ef8cf416062b65510b66e77cd0a095fca1860fbba19afcaa5`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 930.5 KB (930474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b3f18eb96ef9c253503172278278db98c924179a86195ca8709ad357a672d0`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfacd6f1616f2ee9ac5804a9f2a77020d21adabf4951755fecc916f939cf03f6`  
		Last Modified: Tue, 02 Aug 2022 18:47:50 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec6677533059e6e25a9e3104dd0244cf6414f60ad33469ed5f5211f591ed151`  
		Last Modified: Tue, 02 Aug 2022 18:47:56 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef62cc2ef2cfab90a2571aa6ca98cd9f41131681af5d812aa2ef10b2745b4d57`  
		Last Modified: Tue, 02 Aug 2022 18:47:49 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:104bd22f729718e53913546312a87feece478baf9906574ec4601102a26b34f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231753607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032e61e16b0c4ae75a45441568ab1bee2357887dba582bf24c07d60e1a08a02e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 05:06:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:09:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 05:09:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:09:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 03 Aug 2022 05:09:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:09:22 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:09:23 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:09:24 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 03 Aug 2022 05:09:25 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 03 Aug 2022 05:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:09:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 03 Aug 2022 05:09:28 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:09:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 03 Aug 2022 05:09:43 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 03 Aug 2022 05:09:44 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:09:46 GMT
VOLUME [/opt/bonita]
# Wed, 03 Aug 2022 05:09:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 03 Aug 2022 05:09:48 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 05:09:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475e316bd9acaa47733ba1107b4f62f103b220d02f6598f876eb8f11a65191c4`  
		Last Modified: Wed, 03 Aug 2022 05:12:37 GMT  
		Size: 86.7 MB (86745403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc81ca2381301f3b0aa03ce612a7a53264aaa54898500b4580193ee3b5787eaf`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd97ed69e27f69c0cfcb6be5f7da1ec7ab6de99afdeed6f63a0438917c9db0`  
		Last Modified: Wed, 03 Aug 2022 05:12:18 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd51f93d71b36667276e184462a195757d3dda83290d91a4ab6ad70da4506006`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 831.6 KB (831576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50442e8686d94b53f39d0e83a1f10bc50a1fec4b2232b7d6653e6c8a295fe47`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f40705227a8a5b89d9458fa24e75d8749de068b98429a42b7d7f544601812d3`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d8b2a17aaa7d141b1a0b768b50528eecf323a6dc5aed713a24f990b93d6ae4`  
		Last Modified: Wed, 03 Aug 2022 05:12:25 GMT  
		Size: 113.7 MB (113727950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b03d035ea68677c4bc02fea9b835cf9c48e5198a6a7ef597140e15cff2714c`  
		Last Modified: Wed, 03 Aug 2022 05:12:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:11602f6ed9f49abed20683f1159d264c7a6154282ad3f111208195152e278a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:48760e95c35390b2f492b6559173e8657c8090ecf1addac2e6d5321b8766abb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176141080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92d51b64fd81e2820bf03fd32b01e26ff31e7afb71e0f380075780c9f9b9f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 05:09:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:10:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 03 Aug 2022 05:10:08 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:10:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 03 Aug 2022 05:10:12 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:10:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:14 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:10:14 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 03 Aug 2022 05:10:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 03 Aug 2022 05:10:28 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_PASSWORD=
# Wed, 03 Aug 2022 05:10:29 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 03 Aug 2022 05:10:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 03 Aug 2022 05:10:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 03 Aug 2022 05:10:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 03 Aug 2022 05:10:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 03 Aug 2022 05:10:32 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 03 Aug 2022 05:10:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 03 Aug 2022 05:10:33 GMT
EXPOSE 8080 9000
# Wed, 03 Aug 2022 05:10:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 03 Aug 2022 05:10:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe7f2bfe5410564aa1d74ccdf5603a737a00741e3f8dc84dc84c28bb8f1a58f`  
		Last Modified: Wed, 03 Aug 2022 05:13:14 GMT  
		Size: 56.6 MB (56628611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b8084c78560f49de74a1058aa78d78c6a33ec20f4eb201815dfa9c0e2b1ff`  
		Last Modified: Wed, 03 Aug 2022 05:13:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a124e0c3c91ead8397c5d4f2810e2f574cd5b9af598a679a798928575165`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f1fdf212a0809b9ec41ba55e07a03ce48470dd631703579e78a56a77a63cf8`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec537158f98211470b7015d0c8ca91221c3ff8b7e18f153c6c339747fcc9002`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 3.0 KB (3035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30501a7752eaf75497ee5c0684eb0ea40f814bf87c77dace4d269de932ee059d`  
		Last Modified: Wed, 03 Aug 2022 05:13:09 GMT  
		Size: 116.7 MB (116690803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b1e9e5d6b48d6b433d918804c917f0e2f3c3b5a049ec7ad373b4045e5180a`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:11602f6ed9f49abed20683f1159d264c7a6154282ad3f111208195152e278a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:48760e95c35390b2f492b6559173e8657c8090ecf1addac2e6d5321b8766abb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176141080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92d51b64fd81e2820bf03fd32b01e26ff31e7afb71e0f380075780c9f9b9f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 05:09:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:10:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 03 Aug 2022 05:10:08 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:10:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 03 Aug 2022 05:10:12 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:10:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:14 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:10:14 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 03 Aug 2022 05:10:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 03 Aug 2022 05:10:28 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_PASSWORD=
# Wed, 03 Aug 2022 05:10:29 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 03 Aug 2022 05:10:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 03 Aug 2022 05:10:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 03 Aug 2022 05:10:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 03 Aug 2022 05:10:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 03 Aug 2022 05:10:32 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 03 Aug 2022 05:10:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 03 Aug 2022 05:10:33 GMT
EXPOSE 8080 9000
# Wed, 03 Aug 2022 05:10:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 03 Aug 2022 05:10:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe7f2bfe5410564aa1d74ccdf5603a737a00741e3f8dc84dc84c28bb8f1a58f`  
		Last Modified: Wed, 03 Aug 2022 05:13:14 GMT  
		Size: 56.6 MB (56628611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b8084c78560f49de74a1058aa78d78c6a33ec20f4eb201815dfa9c0e2b1ff`  
		Last Modified: Wed, 03 Aug 2022 05:13:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a124e0c3c91ead8397c5d4f2810e2f574cd5b9af598a679a798928575165`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f1fdf212a0809b9ec41ba55e07a03ce48470dd631703579e78a56a77a63cf8`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec537158f98211470b7015d0c8ca91221c3ff8b7e18f153c6c339747fcc9002`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 3.0 KB (3035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30501a7752eaf75497ee5c0684eb0ea40f814bf87c77dace4d269de932ee059d`  
		Last Modified: Wed, 03 Aug 2022 05:13:09 GMT  
		Size: 116.7 MB (116690803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b1e9e5d6b48d6b433d918804c917f0e2f3c3b5a049ec7ad373b4045e5180a`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:11602f6ed9f49abed20683f1159d264c7a6154282ad3f111208195152e278a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:48760e95c35390b2f492b6559173e8657c8090ecf1addac2e6d5321b8766abb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176141080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92d51b64fd81e2820bf03fd32b01e26ff31e7afb71e0f380075780c9f9b9f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 05:09:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 03 Aug 2022 05:10:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 03 Aug 2022 05:10:08 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 03 Aug 2022 05:10:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BONITA_VERSION
# Wed, 03 Aug 2022 05:10:09 GMT
ARG BRANDING_VERSION
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BONITA_SHA256
# Wed, 03 Aug 2022 05:10:10 GMT
ARG BASE_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ARG BONITA_URL
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 03 Aug 2022 05:10:11 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 03 Aug 2022 05:10:12 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 03 Aug 2022 05:10:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 03 Aug 2022 05:10:14 GMT
RUN mkdir /opt/files
# Wed, 03 Aug 2022 05:10:14 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 03 Aug 2022 05:10:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 03 Aug 2022 05:10:28 GMT
ENV HTTP_API=false
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 03 Aug 2022 05:10:29 GMT
ENV HTTP_API_PASSWORD=
# Wed, 03 Aug 2022 05:10:29 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 03 Aug 2022 05:10:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 03 Aug 2022 05:10:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 03 Aug 2022 05:10:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 03 Aug 2022 05:10:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 03 Aug 2022 05:10:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 03 Aug 2022 05:10:32 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 03 Aug 2022 05:10:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 03 Aug 2022 05:10:33 GMT
EXPOSE 8080 9000
# Wed, 03 Aug 2022 05:10:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 03 Aug 2022 05:10:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe7f2bfe5410564aa1d74ccdf5603a737a00741e3f8dc84dc84c28bb8f1a58f`  
		Last Modified: Wed, 03 Aug 2022 05:13:14 GMT  
		Size: 56.6 MB (56628611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b8084c78560f49de74a1058aa78d78c6a33ec20f4eb201815dfa9c0e2b1ff`  
		Last Modified: Wed, 03 Aug 2022 05:13:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a124e0c3c91ead8397c5d4f2810e2f574cd5b9af598a679a798928575165`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f1fdf212a0809b9ec41ba55e07a03ce48470dd631703579e78a56a77a63cf8`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec537158f98211470b7015d0c8ca91221c3ff8b7e18f153c6c339747fcc9002`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 3.0 KB (3035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30501a7752eaf75497ee5c0684eb0ea40f814bf87c77dace4d269de932ee059d`  
		Last Modified: Wed, 03 Aug 2022 05:13:09 GMT  
		Size: 116.7 MB (116690803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b1e9e5d6b48d6b433d918804c917f0e2f3c3b5a049ec7ad373b4045e5180a`  
		Last Modified: Wed, 03 Aug 2022 05:12:58 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
