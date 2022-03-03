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
$ docker pull bonita@sha256:f90b996094c163daf8d142ed67e49cb90729573c08e2e6703b439667e0dc2982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:2446fcfec1b243b1d2d0c9360822126baab9432e9ed52533d6c48657e9fe60be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237286084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6c5c788a3ddd47244b9a2844ce9193aabab1f1db6216ed03dcfb8c6995ac0d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:39:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:14 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:39:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:39:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 02:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:18 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 02:40:19 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:40:19 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 02:40:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 02:40:27 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 02:40:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 02:40:29 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:40:29 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:40:29 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:40:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044e23419ca0e43e6fecfcb0515bbccab5f41e982b101da29c464f96b646bdc`  
		Last Modified: Wed, 02 Feb 2022 02:42:27 GMT  
		Size: 93.6 MB (93574810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60db9d203f5f76d59678a1a4295e97ccdbd6a66400e918dbd8c048807efda8`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed581736e8b15f5b41de5f07ee7144b921d1290ea3f600c0e539f263cf731`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f7fd3a9def33f20814b658f1917a6fe3dcd088fd8c6df0511c54424d6ee85`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 577.0 KB (576968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1827c54cfdd609fadfe2df166f06063edc95c4746907a1b70ccbfd5b25663a`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e209580a6bf40fbfd2324faab1fe9bd2bf1b7fe55d82a6ac71112c0c1921404`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59350fc87038e213f7f86f61e5446eb9e53c380ce9ba336b1835a78c9bcfc5fd`  
		Last Modified: Wed, 02 Feb 2022 02:42:43 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6e3980454f2abae4ed52d36ad1d9e9d13b9273e3224c0486f642ebfce362`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2066dca96e4f4647ecbe609a789e197dcc086a19dd63f2cecb4ca79ae6707d4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4d39e62ef02e33d41f9427c4f2111d753dcabeebe36ed287027551e5d6ef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:33:32 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:33:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:34:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:34:08 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:35:58 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:36:02 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:36:06 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:36:08 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:36:11 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 05:36:14 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 05:36:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 05:36:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:36:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 05:36:41 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:36:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 05:36:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 05:37:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 05:37:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 05:37:13 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:37:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:37:20 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:37:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab912dfde482c15eeb22ec553c885d93db8b95da6f478202623564bb6ef2c05e`  
		Last Modified: Wed, 02 Feb 2022 05:43:45 GMT  
		Size: 86.5 MB (86479745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7425e0fa30a0552894f031fe9447332167edcd4f64beec827a637728cc5954`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4e1c9a3ea59b9bc10a9d7c5956fc58f1e011e493a117ea85b2d52ddfe4587e`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da87b58465df753a5aa2a1fd530d1561aca7fafb6814cade4733b967ceb5727a`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 546.8 KB (546763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdab6c8b00f381df7ce83c450554c0d92a3adc8342b040e2d453a4072e5389d`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46232dded6fa2b3de8fd7541eb0a49cabdb8027473a76dc1733c4114342a2831`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4604256a31a618edbef87b0c9d75f956da4c4edf7174a462395852e2c53600f`  
		Last Modified: Wed, 02 Feb 2022 05:44:06 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c95b4622066a1f19b1d56ece20d5817f80b2b79e760620c15d4baf0d15cf77`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:b3ffab677c9c1c3aa387fccacd489119e35eb1303ab14fe28cd9cbbd866c4cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:218ec8c1762e2f4893a1cc3ae2f34ed0ac341537ebae27a3b2f9e9a4331e6af0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235022718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93680445524e0366f8d1a7fddc295d2c968cf323d472ff60c34cfa2c1224753`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:40:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:40:57 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:40:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:41:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 02:41:42 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:43 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:41:43 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 02:41:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 02:41:52 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 02:41:52 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:41:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:41:53 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:41:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09705134738ba93189ba91cf47cb5857e447803e1fe449c0f9c62b095f4b3575`  
		Last Modified: Wed, 02 Feb 2022 02:43:11 GMT  
		Size: 93.6 MB (93576296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb34bd913c92ceb4d5b890b8eb9e9d1d95d530b6f9bdacc26bccfb6968e92fa`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7eca31c2223e358fd2c5454d04a277305035dbbc3b6c1edc62b3a542a9ce6`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcd9df171506ab78d08cbb912e97b796835e0fdf50302f0fd1d3ae0a9df616`  
		Last Modified: Wed, 02 Feb 2022 02:42:56 GMT  
		Size: 1.0 MB (1003226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897510d063c555822224e7b348e3a374b92efb0712ae36970033b66e5e50c043`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c327f87401721a474fb1450b9b9b029de39f64894cb1ab40ab363ec7a00976d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bf768f0463e236f09158b3014bfc47ee4da453238dcad559a1d6e2d93f1ac`  
		Last Modified: Wed, 02 Feb 2022 02:43:03 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b82ddcdfa2a37394648dee167594ef7710b3132574931cc3a3c47d85c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:f547618e577f5e7864426802ae9e2468d5dd4df66af86d3fa4095730e3838093
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db09f32a93d62ce3fc6190971e87f703edd26601351a06d49a076291293aa3b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:40:51 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:40:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:41:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:41:37 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:41:39 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:41:41 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:41:44 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:41:45 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:41:47 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 05:41:50 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 05:41:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 05:41:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:41:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:41:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:42:04 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:42:05 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 05:42:22 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 05:42:27 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 05:42:32 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:42:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:42:39 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:42:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6c5e13fc634b945560856b4b770a13b4c2d9ec8cdc0d3371f9dc6c1bb006b`  
		Last Modified: Wed, 02 Feb 2022 05:44:41 GMT  
		Size: 86.5 MB (86479807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb39f80a278e91fbf96a6ef913c0b4cb2278f22b774411d3fe1592473acdc20a`  
		Last Modified: Wed, 02 Feb 2022 05:44:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96026ac7348521858a0d36592644de87eb366671a9a82bbefcaae9da39dedcbe`  
		Last Modified: Wed, 02 Feb 2022 05:44:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f07ab73a61ea35f2f53eefd23b9f6b34d3bce096c8df05c6e089fd610bfe2`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 904.2 KB (904219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2972db5847b1f36c36d1b998b69091082c5f360a92d8860a2d66fd99c4b3dc03`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18a925914c9c7cfd0f044a0bf66226e38d5131d7aaf05c3ec068e54752383e`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a885ed01e06a6eaab1f19e836f7878d2b8b89708d42b042d76100522deb4c3c1`  
		Last Modified: Wed, 02 Feb 2022 05:44:34 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36ef935bb77a4368c76ef3a2aaf169d911961fc46b633359a09af60c051667`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:b3ffab677c9c1c3aa387fccacd489119e35eb1303ab14fe28cd9cbbd866c4cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:218ec8c1762e2f4893a1cc3ae2f34ed0ac341537ebae27a3b2f9e9a4331e6af0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235022718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93680445524e0366f8d1a7fddc295d2c968cf323d472ff60c34cfa2c1224753`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:40:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:40:57 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:40:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:41:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 02:41:42 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:43 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:41:43 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 02:41:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 02:41:52 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 02:41:52 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:41:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:41:53 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:41:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09705134738ba93189ba91cf47cb5857e447803e1fe449c0f9c62b095f4b3575`  
		Last Modified: Wed, 02 Feb 2022 02:43:11 GMT  
		Size: 93.6 MB (93576296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb34bd913c92ceb4d5b890b8eb9e9d1d95d530b6f9bdacc26bccfb6968e92fa`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7eca31c2223e358fd2c5454d04a277305035dbbc3b6c1edc62b3a542a9ce6`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcd9df171506ab78d08cbb912e97b796835e0fdf50302f0fd1d3ae0a9df616`  
		Last Modified: Wed, 02 Feb 2022 02:42:56 GMT  
		Size: 1.0 MB (1003226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897510d063c555822224e7b348e3a374b92efb0712ae36970033b66e5e50c043`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c327f87401721a474fb1450b9b9b029de39f64894cb1ab40ab363ec7a00976d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bf768f0463e236f09158b3014bfc47ee4da453238dcad559a1d6e2d93f1ac`  
		Last Modified: Wed, 02 Feb 2022 02:43:03 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b82ddcdfa2a37394648dee167594ef7710b3132574931cc3a3c47d85c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:f547618e577f5e7864426802ae9e2468d5dd4df66af86d3fa4095730e3838093
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db09f32a93d62ce3fc6190971e87f703edd26601351a06d49a076291293aa3b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:40:51 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:40:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:41:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:41:37 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:41:39 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:41:41 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:41:44 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:41:45 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:41:47 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 05:41:50 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 05:41:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 05:41:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:41:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:41:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:42:04 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:42:05 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 05:42:22 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 05:42:27 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 05:42:32 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:42:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:42:39 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:42:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6c5e13fc634b945560856b4b770a13b4c2d9ec8cdc0d3371f9dc6c1bb006b`  
		Last Modified: Wed, 02 Feb 2022 05:44:41 GMT  
		Size: 86.5 MB (86479807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb39f80a278e91fbf96a6ef913c0b4cb2278f22b774411d3fe1592473acdc20a`  
		Last Modified: Wed, 02 Feb 2022 05:44:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96026ac7348521858a0d36592644de87eb366671a9a82bbefcaae9da39dedcbe`  
		Last Modified: Wed, 02 Feb 2022 05:44:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f07ab73a61ea35f2f53eefd23b9f6b34d3bce096c8df05c6e089fd610bfe2`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 904.2 KB (904219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2972db5847b1f36c36d1b998b69091082c5f360a92d8860a2d66fd99c4b3dc03`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18a925914c9c7cfd0f044a0bf66226e38d5131d7aaf05c3ec068e54752383e`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a885ed01e06a6eaab1f19e836f7878d2b8b89708d42b042d76100522deb4c3c1`  
		Last Modified: Wed, 02 Feb 2022 05:44:34 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36ef935bb77a4368c76ef3a2aaf169d911961fc46b633359a09af60c051667`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:7ca174e6352d9d53be3801df5ad2931183788a329e921c7218fa46455497883e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:9061e912c4d506555ab0a36e8b1b7cf2c0494a9be38b19b918071fe0454a5470
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234218456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf8b5f466cee6a8b73a85167787f5513dec8f2458ee2e8cd7c122a06dbffd04`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:39:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:14 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:39:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:39:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:39:59 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:39:59 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:39:59 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 02:39:59 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 02:39:59 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 02:40:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:40:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 02:40:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 02:40:01 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:40:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 02:40:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 02:40:09 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 02:40:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 02:40:11 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:40:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:40:11 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:40:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044e23419ca0e43e6fecfcb0515bbccab5f41e982b101da29c464f96b646bdc`  
		Last Modified: Wed, 02 Feb 2022 02:42:27 GMT  
		Size: 93.6 MB (93574810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60db9d203f5f76d59678a1a4295e97ccdbd6a66400e918dbd8c048807efda8`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed581736e8b15f5b41de5f07ee7144b921d1290ea3f600c0e539f263cf731`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f7fd3a9def33f20814b658f1917a6fe3dcd088fd8c6df0511c54424d6ee85`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 577.0 KB (576968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997964ccf842c959491177c5c705ea913da717833c89b2360f1fd41aaa92c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee292d7753cd041dbb7ecada3d6a24576d96ae44aeb8695781438d04b27a16e`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8283cd69e6f52cbc3e4cfe77b490c1af7f9aeb27ac1c5af8c75a26d2c1fc6f`  
		Last Modified: Wed, 02 Feb 2022 02:42:18 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9021f16d4ce346b698cebf102144bf3df997d168266df117bf70eedd02155c`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6a81cc6c2253c285486f29e734599ccfd5b77751dbc0ce9e91781661d942aca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223334084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1829b38d779f8ecae6f13f0f1b1d910b61f7f82f3ae70a05fc3ce5f9066063b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:04 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:06 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:07 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:00:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:13 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:15 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:00:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:21 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:23 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:25 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9de10c001f237ee55abd3ee02745208923c66fca86dc47b426d70f40739f9c3`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d842f2e1f3898318118be910214bed49eef1fc50293e521740463c02bcb9d`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 6.9 KB (6870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30155b02834c5698b9f82c9103ca30c01979f28263d67af5cdb1e7d87e43af47`  
		Last Modified: Thu, 03 Mar 2022 20:03:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2b92809091e6d9c115b9597a33bd765c67a66d2c0ae867c45fd63bbe23734c`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:fd29d7bb3324e8a2ed00271574e03373436010d44d7b97d1d70bf6ed801b72a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230822820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6afaeed3a96e3afe33488c0cd269f1cbf188d3ff1b926ade39e7a58c0f6a36`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:33:32 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:33:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:34:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:34:08 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:34:11 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:34:15 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:34:18 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:34:21 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 05:34:25 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 05:34:29 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 05:34:33 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:34:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 05:34:45 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 05:34:54 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:34:56 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 05:35:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 05:35:24 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 05:35:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 05:35:36 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:35:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:35:40 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:35:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab912dfde482c15eeb22ec553c885d93db8b95da6f478202623564bb6ef2c05e`  
		Last Modified: Wed, 02 Feb 2022 05:43:45 GMT  
		Size: 86.5 MB (86479745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7425e0fa30a0552894f031fe9447332167edcd4f64beec827a637728cc5954`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4e1c9a3ea59b9bc10a9d7c5956fc58f1e011e493a117ea85b2d52ddfe4587e`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da87b58465df753a5aa2a1fd530d1561aca7fafb6814cade4733b967ceb5727a`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 546.8 KB (546763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1c22e14ce55f3455312a6409337d43fc6f550972d1f60fd06b767639ffc7e8`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25743ab7b3c7c84fd18f8d255ebfdcdbb2a7212044f417906545864244f556b`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d53bd0d555ac4da5707c84fa3955c69121dedd1cb3e7c34c0fc93946ac45795`  
		Last Modified: Wed, 02 Feb 2022 05:43:36 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9754ead671231e4976ebfd07fe6f0ebf386fa9dbfb444c9d52d486644ed2352`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:7ca174e6352d9d53be3801df5ad2931183788a329e921c7218fa46455497883e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:9061e912c4d506555ab0a36e8b1b7cf2c0494a9be38b19b918071fe0454a5470
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234218456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf8b5f466cee6a8b73a85167787f5513dec8f2458ee2e8cd7c122a06dbffd04`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:39:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:14 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:39:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:39:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:39:59 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:39:59 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:39:59 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 02:39:59 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 02:39:59 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 02:40:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:40:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 02:40:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 02:40:01 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:40:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 02:40:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 02:40:09 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 02:40:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 02:40:11 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:40:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:40:11 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:40:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044e23419ca0e43e6fecfcb0515bbccab5f41e982b101da29c464f96b646bdc`  
		Last Modified: Wed, 02 Feb 2022 02:42:27 GMT  
		Size: 93.6 MB (93574810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60db9d203f5f76d59678a1a4295e97ccdbd6a66400e918dbd8c048807efda8`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed581736e8b15f5b41de5f07ee7144b921d1290ea3f600c0e539f263cf731`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f7fd3a9def33f20814b658f1917a6fe3dcd088fd8c6df0511c54424d6ee85`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 577.0 KB (576968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e997964ccf842c959491177c5c705ea913da717833c89b2360f1fd41aaa92c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee292d7753cd041dbb7ecada3d6a24576d96ae44aeb8695781438d04b27a16e`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8283cd69e6f52cbc3e4cfe77b490c1af7f9aeb27ac1c5af8c75a26d2c1fc6f`  
		Last Modified: Wed, 02 Feb 2022 02:42:18 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9021f16d4ce346b698cebf102144bf3df997d168266df117bf70eedd02155c`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6a81cc6c2253c285486f29e734599ccfd5b77751dbc0ce9e91781661d942aca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223334084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1829b38d779f8ecae6f13f0f1b1d910b61f7f82f3ae70a05fc3ce5f9066063b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:04 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:06 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:07 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:00:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:13 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:15 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:00:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:21 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:23 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:25 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9de10c001f237ee55abd3ee02745208923c66fca86dc47b426d70f40739f9c3`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d842f2e1f3898318118be910214bed49eef1fc50293e521740463c02bcb9d`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 6.9 KB (6870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30155b02834c5698b9f82c9103ca30c01979f28263d67af5cdb1e7d87e43af47`  
		Last Modified: Thu, 03 Mar 2022 20:03:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2b92809091e6d9c115b9597a33bd765c67a66d2c0ae867c45fd63bbe23734c`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:fd29d7bb3324e8a2ed00271574e03373436010d44d7b97d1d70bf6ed801b72a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230822820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6afaeed3a96e3afe33488c0cd269f1cbf188d3ff1b926ade39e7a58c0f6a36`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:33:32 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:33:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:34:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:34:08 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:34:11 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:34:15 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:34:18 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:34:21 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 05:34:25 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 05:34:29 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 05:34:33 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:34:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 05:34:45 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 05:34:54 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:34:56 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 05:35:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 05:35:24 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 05:35:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 05:35:36 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:35:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:35:40 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:35:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab912dfde482c15eeb22ec553c885d93db8b95da6f478202623564bb6ef2c05e`  
		Last Modified: Wed, 02 Feb 2022 05:43:45 GMT  
		Size: 86.5 MB (86479745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7425e0fa30a0552894f031fe9447332167edcd4f64beec827a637728cc5954`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4e1c9a3ea59b9bc10a9d7c5956fc58f1e011e493a117ea85b2d52ddfe4587e`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da87b58465df753a5aa2a1fd530d1561aca7fafb6814cade4733b967ceb5727a`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 546.8 KB (546763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1c22e14ce55f3455312a6409337d43fc6f550972d1f60fd06b767639ffc7e8`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25743ab7b3c7c84fd18f8d255ebfdcdbb2a7212044f417906545864244f556b`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d53bd0d555ac4da5707c84fa3955c69121dedd1cb3e7c34c0fc93946ac45795`  
		Last Modified: Wed, 02 Feb 2022 05:43:36 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9754ead671231e4976ebfd07fe6f0ebf386fa9dbfb444c9d52d486644ed2352`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:f90b996094c163daf8d142ed67e49cb90729573c08e2e6703b439667e0dc2982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:2446fcfec1b243b1d2d0c9360822126baab9432e9ed52533d6c48657e9fe60be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237286084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6c5c788a3ddd47244b9a2844ce9193aabab1f1db6216ed03dcfb8c6995ac0d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:39:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:14 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:39:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:39:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 02:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:18 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 02:40:19 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:40:19 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 02:40:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 02:40:27 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 02:40:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 02:40:29 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:40:29 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:40:29 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:40:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044e23419ca0e43e6fecfcb0515bbccab5f41e982b101da29c464f96b646bdc`  
		Last Modified: Wed, 02 Feb 2022 02:42:27 GMT  
		Size: 93.6 MB (93574810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60db9d203f5f76d59678a1a4295e97ccdbd6a66400e918dbd8c048807efda8`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed581736e8b15f5b41de5f07ee7144b921d1290ea3f600c0e539f263cf731`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f7fd3a9def33f20814b658f1917a6fe3dcd088fd8c6df0511c54424d6ee85`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 577.0 KB (576968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1827c54cfdd609fadfe2df166f06063edc95c4746907a1b70ccbfd5b25663a`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e209580a6bf40fbfd2324faab1fe9bd2bf1b7fe55d82a6ac71112c0c1921404`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59350fc87038e213f7f86f61e5446eb9e53c380ce9ba336b1835a78c9bcfc5fd`  
		Last Modified: Wed, 02 Feb 2022 02:42:43 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6e3980454f2abae4ed52d36ad1d9e9d13b9273e3224c0486f642ebfce362`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:2066dca96e4f4647ecbe609a789e197dcc086a19dd63f2cecb4ca79ae6707d4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4d39e62ef02e33d41f9427c4f2111d753dcabeebe36ed287027551e5d6ef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:33:32 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:33:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:34:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:34:08 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:35:58 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:36:02 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:36:06 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:36:08 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:36:11 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 05:36:14 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 05:36:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 05:36:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:36:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 05:36:41 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:36:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 05:36:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 05:37:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 05:37:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 05:37:13 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:37:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:37:20 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:37:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab912dfde482c15eeb22ec553c885d93db8b95da6f478202623564bb6ef2c05e`  
		Last Modified: Wed, 02 Feb 2022 05:43:45 GMT  
		Size: 86.5 MB (86479745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7425e0fa30a0552894f031fe9447332167edcd4f64beec827a637728cc5954`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4e1c9a3ea59b9bc10a9d7c5956fc58f1e011e493a117ea85b2d52ddfe4587e`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da87b58465df753a5aa2a1fd530d1561aca7fafb6814cade4733b967ceb5727a`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 546.8 KB (546763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdab6c8b00f381df7ce83c450554c0d92a3adc8342b040e2d453a4072e5389d`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46232dded6fa2b3de8fd7541eb0a49cabdb8027473a76dc1733c4114342a2831`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4604256a31a618edbef87b0c9d75f956da4c4edf7174a462395852e2c53600f`  
		Last Modified: Wed, 02 Feb 2022 05:44:06 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c95b4622066a1f19b1d56ece20d5817f80b2b79e760620c15d4baf0d15cf77`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:f90b996094c163daf8d142ed67e49cb90729573c08e2e6703b439667e0dc2982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:2446fcfec1b243b1d2d0c9360822126baab9432e9ed52533d6c48657e9fe60be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237286084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6c5c788a3ddd47244b9a2844ce9193aabab1f1db6216ed03dcfb8c6995ac0d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:39:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:14 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:39:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:39:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:39:58 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:40:15 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 02:40:16 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 02:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:40:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 02:40:18 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 02:40:19 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:40:19 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 02:40:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 02:40:27 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 02:40:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 02:40:29 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:40:29 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:40:29 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:40:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6044e23419ca0e43e6fecfcb0515bbccab5f41e982b101da29c464f96b646bdc`  
		Last Modified: Wed, 02 Feb 2022 02:42:27 GMT  
		Size: 93.6 MB (93574810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab60db9d203f5f76d59678a1a4295e97ccdbd6a66400e918dbd8c048807efda8`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed581736e8b15f5b41de5f07ee7144b921d1290ea3f600c0e539f263cf731`  
		Last Modified: Wed, 02 Feb 2022 02:42:14 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54f7fd3a9def33f20814b658f1917a6fe3dcd088fd8c6df0511c54424d6ee85`  
		Last Modified: Wed, 02 Feb 2022 02:42:12 GMT  
		Size: 577.0 KB (576968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1827c54cfdd609fadfe2df166f06063edc95c4746907a1b70ccbfd5b25663a`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e209580a6bf40fbfd2324faab1fe9bd2bf1b7fe55d82a6ac71112c0c1921404`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59350fc87038e213f7f86f61e5446eb9e53c380ce9ba336b1835a78c9bcfc5fd`  
		Last Modified: Wed, 02 Feb 2022 02:42:43 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a6e3980454f2abae4ed52d36ad1d9e9d13b9273e3224c0486f642ebfce362`  
		Last Modified: Wed, 02 Feb 2022 02:42:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2066dca96e4f4647ecbe609a789e197dcc086a19dd63f2cecb4ca79ae6707d4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb4d39e62ef02e33d41f9427c4f2111d753dcabeebe36ed287027551e5d6ef0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:33:32 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:33:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:34:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:34:08 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:35:58 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:36:02 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:36:06 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:36:08 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:36:11 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 05:36:14 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 05:36:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 05:36:21 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:36:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 05:36:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 05:36:41 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:36:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 05:36:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 05:37:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 05:37:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 05:37:13 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:37:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:37:20 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:37:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab912dfde482c15eeb22ec553c885d93db8b95da6f478202623564bb6ef2c05e`  
		Last Modified: Wed, 02 Feb 2022 05:43:45 GMT  
		Size: 86.5 MB (86479745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7425e0fa30a0552894f031fe9447332167edcd4f64beec827a637728cc5954`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4e1c9a3ea59b9bc10a9d7c5956fc58f1e011e493a117ea85b2d52ddfe4587e`  
		Last Modified: Wed, 02 Feb 2022 05:43:29 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da87b58465df753a5aa2a1fd530d1561aca7fafb6814cade4733b967ceb5727a`  
		Last Modified: Wed, 02 Feb 2022 05:43:26 GMT  
		Size: 546.8 KB (546763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdab6c8b00f381df7ce83c450554c0d92a3adc8342b040e2d453a4072e5389d`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46232dded6fa2b3de8fd7541eb0a49cabdb8027473a76dc1733c4114342a2831`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4604256a31a618edbef87b0c9d75f956da4c4edf7174a462395852e2c53600f`  
		Last Modified: Wed, 02 Feb 2022 05:44:06 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c95b4622066a1f19b1d56ece20d5817f80b2b79e760620c15d4baf0d15cf77`  
		Last Modified: Wed, 02 Feb 2022 05:43:57 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:b3ffab677c9c1c3aa387fccacd489119e35eb1303ab14fe28cd9cbbd866c4cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:218ec8c1762e2f4893a1cc3ae2f34ed0ac341537ebae27a3b2f9e9a4331e6af0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235022718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93680445524e0366f8d1a7fddc295d2c968cf323d472ff60c34cfa2c1224753`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:40:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:40:57 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:40:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:41:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 02:41:42 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:43 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:41:43 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 02:41:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 02:41:52 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 02:41:52 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:41:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:41:53 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:41:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09705134738ba93189ba91cf47cb5857e447803e1fe449c0f9c62b095f4b3575`  
		Last Modified: Wed, 02 Feb 2022 02:43:11 GMT  
		Size: 93.6 MB (93576296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb34bd913c92ceb4d5b890b8eb9e9d1d95d530b6f9bdacc26bccfb6968e92fa`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7eca31c2223e358fd2c5454d04a277305035dbbc3b6c1edc62b3a542a9ce6`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcd9df171506ab78d08cbb912e97b796835e0fdf50302f0fd1d3ae0a9df616`  
		Last Modified: Wed, 02 Feb 2022 02:42:56 GMT  
		Size: 1.0 MB (1003226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897510d063c555822224e7b348e3a374b92efb0712ae36970033b66e5e50c043`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c327f87401721a474fb1450b9b9b029de39f64894cb1ab40ab363ec7a00976d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bf768f0463e236f09158b3014bfc47ee4da453238dcad559a1d6e2d93f1ac`  
		Last Modified: Wed, 02 Feb 2022 02:43:03 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b82ddcdfa2a37394648dee167594ef7710b3132574931cc3a3c47d85c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:f547618e577f5e7864426802ae9e2468d5dd4df66af86d3fa4095730e3838093
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db09f32a93d62ce3fc6190971e87f703edd26601351a06d49a076291293aa3b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:40:51 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:40:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:41:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:41:37 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:41:39 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:41:41 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:41:44 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:41:45 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:41:47 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 05:41:50 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 05:41:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 05:41:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:41:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:41:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:42:04 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:42:05 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 05:42:22 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 05:42:27 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 05:42:32 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:42:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:42:39 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:42:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6c5e13fc634b945560856b4b770a13b4c2d9ec8cdc0d3371f9dc6c1bb006b`  
		Last Modified: Wed, 02 Feb 2022 05:44:41 GMT  
		Size: 86.5 MB (86479807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb39f80a278e91fbf96a6ef913c0b4cb2278f22b774411d3fe1592473acdc20a`  
		Last Modified: Wed, 02 Feb 2022 05:44:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96026ac7348521858a0d36592644de87eb366671a9a82bbefcaae9da39dedcbe`  
		Last Modified: Wed, 02 Feb 2022 05:44:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f07ab73a61ea35f2f53eefd23b9f6b34d3bce096c8df05c6e089fd610bfe2`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 904.2 KB (904219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2972db5847b1f36c36d1b998b69091082c5f360a92d8860a2d66fd99c4b3dc03`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18a925914c9c7cfd0f044a0bf66226e38d5131d7aaf05c3ec068e54752383e`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a885ed01e06a6eaab1f19e836f7878d2b8b89708d42b042d76100522deb4c3c1`  
		Last Modified: Wed, 02 Feb 2022 05:44:34 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36ef935bb77a4368c76ef3a2aaf169d911961fc46b633359a09af60c051667`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:b3ffab677c9c1c3aa387fccacd489119e35eb1303ab14fe28cd9cbbd866c4cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:218ec8c1762e2f4893a1cc3ae2f34ed0ac341537ebae27a3b2f9e9a4331e6af0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235022718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93680445524e0366f8d1a7fddc295d2c968cf323d472ff60c34cfa2c1224753`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:40:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:40:57 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:40:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:41:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 02:41:42 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:43 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:41:43 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 02:41:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 02:41:52 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 02:41:52 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:41:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:41:53 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:41:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09705134738ba93189ba91cf47cb5857e447803e1fe449c0f9c62b095f4b3575`  
		Last Modified: Wed, 02 Feb 2022 02:43:11 GMT  
		Size: 93.6 MB (93576296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb34bd913c92ceb4d5b890b8eb9e9d1d95d530b6f9bdacc26bccfb6968e92fa`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7eca31c2223e358fd2c5454d04a277305035dbbc3b6c1edc62b3a542a9ce6`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcd9df171506ab78d08cbb912e97b796835e0fdf50302f0fd1d3ae0a9df616`  
		Last Modified: Wed, 02 Feb 2022 02:42:56 GMT  
		Size: 1.0 MB (1003226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897510d063c555822224e7b348e3a374b92efb0712ae36970033b66e5e50c043`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c327f87401721a474fb1450b9b9b029de39f64894cb1ab40ab363ec7a00976d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bf768f0463e236f09158b3014bfc47ee4da453238dcad559a1d6e2d93f1ac`  
		Last Modified: Wed, 02 Feb 2022 02:43:03 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b82ddcdfa2a37394648dee167594ef7710b3132574931cc3a3c47d85c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:f547618e577f5e7864426802ae9e2468d5dd4df66af86d3fa4095730e3838093
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db09f32a93d62ce3fc6190971e87f703edd26601351a06d49a076291293aa3b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:40:51 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:40:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:41:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:41:37 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:41:39 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:41:41 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:41:44 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:41:45 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:41:47 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 05:41:50 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 05:41:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 05:41:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:41:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:41:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:42:04 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:42:05 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 05:42:22 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 05:42:27 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 05:42:32 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:42:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:42:39 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:42:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6c5e13fc634b945560856b4b770a13b4c2d9ec8cdc0d3371f9dc6c1bb006b`  
		Last Modified: Wed, 02 Feb 2022 05:44:41 GMT  
		Size: 86.5 MB (86479807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb39f80a278e91fbf96a6ef913c0b4cb2278f22b774411d3fe1592473acdc20a`  
		Last Modified: Wed, 02 Feb 2022 05:44:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96026ac7348521858a0d36592644de87eb366671a9a82bbefcaae9da39dedcbe`  
		Last Modified: Wed, 02 Feb 2022 05:44:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f07ab73a61ea35f2f53eefd23b9f6b34d3bce096c8df05c6e089fd610bfe2`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 904.2 KB (904219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2972db5847b1f36c36d1b998b69091082c5f360a92d8860a2d66fd99c4b3dc03`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18a925914c9c7cfd0f044a0bf66226e38d5131d7aaf05c3ec068e54752383e`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a885ed01e06a6eaab1f19e836f7878d2b8b89708d42b042d76100522deb4c3c1`  
		Last Modified: Wed, 02 Feb 2022 05:44:34 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36ef935bb77a4368c76ef3a2aaf169d911961fc46b633359a09af60c051667`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:b3ffab677c9c1c3aa387fccacd489119e35eb1303ab14fe28cd9cbbd866c4cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:218ec8c1762e2f4893a1cc3ae2f34ed0ac341537ebae27a3b2f9e9a4331e6af0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235022718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93680445524e0366f8d1a7fddc295d2c968cf323d472ff60c34cfa2c1224753`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:37:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 02:40:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:40:57 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 02:40:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 02:41:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 02:41:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 02:41:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 02:41:42 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 02:41:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 02:41:43 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 02:41:43 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 02:41:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 02:41:52 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 02:41:52 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 02:41:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 02:41:53 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 02:41:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09705134738ba93189ba91cf47cb5857e447803e1fe449c0f9c62b095f4b3575`  
		Last Modified: Wed, 02 Feb 2022 02:43:11 GMT  
		Size: 93.6 MB (93576296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb34bd913c92ceb4d5b890b8eb9e9d1d95d530b6f9bdacc26bccfb6968e92fa`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7eca31c2223e358fd2c5454d04a277305035dbbc3b6c1edc62b3a542a9ce6`  
		Last Modified: Wed, 02 Feb 2022 02:42:57 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcd9df171506ab78d08cbb912e97b796835e0fdf50302f0fd1d3ae0a9df616`  
		Last Modified: Wed, 02 Feb 2022 02:42:56 GMT  
		Size: 1.0 MB (1003226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897510d063c555822224e7b348e3a374b92efb0712ae36970033b66e5e50c043`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c327f87401721a474fb1450b9b9b029de39f64894cb1ab40ab363ec7a00976d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137bf768f0463e236f09158b3014bfc47ee4da453238dcad559a1d6e2d93f1ac`  
		Last Modified: Wed, 02 Feb 2022 02:43:03 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b82ddcdfa2a37394648dee167594ef7710b3132574931cc3a3c47d85c6d`  
		Last Modified: Wed, 02 Feb 2022 02:42:55 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:f547618e577f5e7864426802ae9e2468d5dd4df66af86d3fa4095730e3838093
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db09f32a93d62ce3fc6190971e87f703edd26601351a06d49a076291293aa3b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:30:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 05:40:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:40:51 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 05:40:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 05:41:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 05:41:37 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 05:41:39 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 05:41:41 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 05:41:44 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 05:41:45 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 05:41:47 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 05:41:50 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 05:41:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 05:41:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:41:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 05:41:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 05:42:04 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 05:42:05 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 05:42:22 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 05:42:27 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 05:42:32 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 05:42:34 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 05:42:39 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 05:42:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b6c5e13fc634b945560856b4b770a13b4c2d9ec8cdc0d3371f9dc6c1bb006b`  
		Last Modified: Wed, 02 Feb 2022 05:44:41 GMT  
		Size: 86.5 MB (86479807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb39f80a278e91fbf96a6ef913c0b4cb2278f22b774411d3fe1592473acdc20a`  
		Last Modified: Wed, 02 Feb 2022 05:44:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96026ac7348521858a0d36592644de87eb366671a9a82bbefcaae9da39dedcbe`  
		Last Modified: Wed, 02 Feb 2022 05:44:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f07ab73a61ea35f2f53eefd23b9f6b34d3bce096c8df05c6e089fd610bfe2`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 904.2 KB (904219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2972db5847b1f36c36d1b998b69091082c5f360a92d8860a2d66fd99c4b3dc03`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c18a925914c9c7cfd0f044a0bf66226e38d5131d7aaf05c3ec068e54752383e`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a885ed01e06a6eaab1f19e836f7878d2b8b89708d42b042d76100522deb4c3c1`  
		Last Modified: Wed, 02 Feb 2022 05:44:34 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36ef935bb77a4368c76ef3a2aaf169d911961fc46b633359a09af60c051667`  
		Last Modified: Wed, 02 Feb 2022 05:44:23 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
