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
$ docker pull bonita@sha256:187a7c2eb7dda0b54fabf93bacbf9b7894466300981aad413466fb0a644d8b0f
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
$ docker pull bonita@sha256:caa2e952837a8f37202e38cfa9f22493197dd1a3577c7c38dcb9cc6344fbab9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226406107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e62a714a53e7673058851ffc6aff4be42a13a463ea89e89fea490ee867bf78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:45:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:45:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:45:39 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:45:39 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:46:21 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:46:22 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:46:23 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:46:24 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:46:25 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 03:46:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 03:46:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 03:46:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:46:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:31 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 03:46:32 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:46:34 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 03:46:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 03:46:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 03:46:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 03:46:48 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:46:50 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:46:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1293d5ef41ac474158c344a703ad2e4b1d3cc1086db95b5a0d51518714362c51`  
		Last Modified: Wed, 02 Feb 2022 03:50:30 GMT  
		Size: 85.7 MB (85703333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6191e74b124b9400a4f5c57d32ee0ff7bcf853d927f43939d87cda4a65135c0`  
		Last Modified: Wed, 02 Feb 2022 03:50:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f9eb3c9a7312036549f74c84994db03b4ed54b7b3ee5cc1d1268e5d53ab831`  
		Last Modified: Wed, 02 Feb 2022 03:50:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5352c9473118239827d56f70fd75fbd6f6a8025bd99e3382d3fd7b6427f9b9`  
		Last Modified: Wed, 02 Feb 2022 03:50:17 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2456278e509cc5c96311271bf8bf26c81e2f8fddeabe4b6b9d1e1d5a516b4945`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6fe5e155a20708bacc56139615325d04f5682b29e96322680394edd34da6b`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353d8ef97cc1b966a265fcb4b001a5061f4f1eab84e9a3c03d7568c831c2bc2`  
		Last Modified: Wed, 02 Feb 2022 03:50:50 GMT  
		Size: 116.4 MB (116415399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683992409b89a55cd62e3dee64330e89c520d14d571d64db9ecb574f1d2280c2`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 1.7 KB (1684 bytes)  
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
$ docker pull bonita@sha256:05eb7ed4fffad4ee0f95a1d3b5cb62fbd4e8a027b67c161958d900ac23288810
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
$ docker pull bonita@sha256:1d8ec4448a4b96ba25218c57f1b3b56b5829e8bfad147c9d6ec85884a563cb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224097593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6630b2134154c946ccacddf67df0ee57c876af89274cd74719e3c60d6be61b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:48:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:59 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:49:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:49:23 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:49:23 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:49:24 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:49:25 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:49:26 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:49:27 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:49:28 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 03:49:29 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 03:49:30 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 03:49:31 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:49:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:34 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:49:36 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 03:49:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 03:49:44 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 03:49:45 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:49:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:49:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:49:48 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70234f375dfc7552903a976870d3630a9fffe6364c0e00b93861bae3573050`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 85.7 MB (85703453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38463bd41867f3e10e65a084c65e77045dc4afcbe144b4b9c4f30072821b8e`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8b185635319d5e319829095f04b2f8128a12a077f5013a8b2acd9c52a83a8`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4902c51a8f3c51ed0722f35cfedc3393337d44dd9dfcafe30c1685c42a382d`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 929.4 KB (929412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffad56017642341e3b408c3b8b334661581c7e926e980129c5ba24e219a965`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c659beb7cfa91a3ee3776b9d35a7ca934d6349d87a72617af702bdb6e9538`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ddd3dc89b01bc60d8d1dd80972d613cfe63a713c066fa415f19eb7693bad9`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7139bd23502b90f348736815e15fdf7885674662c1b63074bee2cf33f80d5`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
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
$ docker pull bonita@sha256:05eb7ed4fffad4ee0f95a1d3b5cb62fbd4e8a027b67c161958d900ac23288810
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
$ docker pull bonita@sha256:1d8ec4448a4b96ba25218c57f1b3b56b5829e8bfad147c9d6ec85884a563cb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224097593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6630b2134154c946ccacddf67df0ee57c876af89274cd74719e3c60d6be61b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:48:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:59 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:49:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:49:23 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:49:23 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:49:24 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:49:25 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:49:26 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:49:27 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:49:28 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 03:49:29 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 03:49:30 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 03:49:31 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:49:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:34 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:49:36 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 03:49:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 03:49:44 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 03:49:45 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:49:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:49:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:49:48 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70234f375dfc7552903a976870d3630a9fffe6364c0e00b93861bae3573050`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 85.7 MB (85703453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38463bd41867f3e10e65a084c65e77045dc4afcbe144b4b9c4f30072821b8e`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8b185635319d5e319829095f04b2f8128a12a077f5013a8b2acd9c52a83a8`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4902c51a8f3c51ed0722f35cfedc3393337d44dd9dfcafe30c1685c42a382d`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 929.4 KB (929412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffad56017642341e3b408c3b8b334661581c7e926e980129c5ba24e219a965`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c659beb7cfa91a3ee3776b9d35a7ca934d6349d87a72617af702bdb6e9538`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ddd3dc89b01bc60d8d1dd80972d613cfe63a713c066fa415f19eb7693bad9`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7139bd23502b90f348736815e15fdf7885674662c1b63074bee2cf33f80d5`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
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
$ docker pull bonita@sha256:3626d1b790e83657843a55824890d46f160bfed7b743d412069be034a8d6832d
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
$ docker pull bonita@sha256:c8f838d5f70db012392467c2e1b04d41e918577dc8ad9560150c9fe397d30083
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223338481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8689fa494b491f4052c26cd0db7a965eb80ea0665eaa2fdca8d0757e98490bb9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:45:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:45:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:45:39 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:45:39 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:45:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:45:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:45:42 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:45:43 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 03:45:44 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 03:45:45 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 03:45:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:45:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 03:45:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 03:45:49 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:45:51 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 03:45:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 03:45:58 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 03:45:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 03:46:00 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:46:02 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:46:02 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:46:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1293d5ef41ac474158c344a703ad2e4b1d3cc1086db95b5a0d51518714362c51`  
		Last Modified: Wed, 02 Feb 2022 03:50:30 GMT  
		Size: 85.7 MB (85703333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6191e74b124b9400a4f5c57d32ee0ff7bcf853d927f43939d87cda4a65135c0`  
		Last Modified: Wed, 02 Feb 2022 03:50:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f9eb3c9a7312036549f74c84994db03b4ed54b7b3ee5cc1d1268e5d53ab831`  
		Last Modified: Wed, 02 Feb 2022 03:50:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5352c9473118239827d56f70fd75fbd6f6a8025bd99e3382d3fd7b6427f9b9`  
		Last Modified: Wed, 02 Feb 2022 03:50:17 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd3f9306665498c949b8372cb2c52d6536771bb58eb5967580d7ddb0f2316f4`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07100e3e83bdf9cd7dcfa1a3f968548bc30786ae200a6cb6d3b3a2d5e9cafe04`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f936d12396586c187f9d9b38f1da23689f3b2cc7ec4571376feb8f51737e31`  
		Last Modified: Wed, 02 Feb 2022 03:50:23 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f4089d7ddd6745bdd3fdb8e0a72669d3564ff059bb70a0a8695315adb2ad0`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
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
$ docker pull bonita@sha256:3626d1b790e83657843a55824890d46f160bfed7b743d412069be034a8d6832d
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
$ docker pull bonita@sha256:c8f838d5f70db012392467c2e1b04d41e918577dc8ad9560150c9fe397d30083
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223338481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8689fa494b491f4052c26cd0db7a965eb80ea0665eaa2fdca8d0757e98490bb9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:45:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:45:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:45:39 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:45:39 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:45:40 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:45:41 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:45:42 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:45:43 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 02 Feb 2022 03:45:44 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 02 Feb 2022 03:45:45 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 03:45:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:45:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 02 Feb 2022 03:45:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 03:45:49 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:45:51 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 02 Feb 2022 03:45:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 02 Feb 2022 03:45:58 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 03:45:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 03:46:00 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:46:02 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:46:02 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:46:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1293d5ef41ac474158c344a703ad2e4b1d3cc1086db95b5a0d51518714362c51`  
		Last Modified: Wed, 02 Feb 2022 03:50:30 GMT  
		Size: 85.7 MB (85703333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6191e74b124b9400a4f5c57d32ee0ff7bcf853d927f43939d87cda4a65135c0`  
		Last Modified: Wed, 02 Feb 2022 03:50:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f9eb3c9a7312036549f74c84994db03b4ed54b7b3ee5cc1d1268e5d53ab831`  
		Last Modified: Wed, 02 Feb 2022 03:50:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5352c9473118239827d56f70fd75fbd6f6a8025bd99e3382d3fd7b6427f9b9`  
		Last Modified: Wed, 02 Feb 2022 03:50:17 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd3f9306665498c949b8372cb2c52d6536771bb58eb5967580d7ddb0f2316f4`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07100e3e83bdf9cd7dcfa1a3f968548bc30786ae200a6cb6d3b3a2d5e9cafe04`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f936d12396586c187f9d9b38f1da23689f3b2cc7ec4571376feb8f51737e31`  
		Last Modified: Wed, 02 Feb 2022 03:50:23 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3f4089d7ddd6745bdd3fdb8e0a72669d3564ff059bb70a0a8695315adb2ad0`  
		Last Modified: Wed, 02 Feb 2022 03:50:16 GMT  
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
$ docker pull bonita@sha256:187a7c2eb7dda0b54fabf93bacbf9b7894466300981aad413466fb0a644d8b0f
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
$ docker pull bonita@sha256:caa2e952837a8f37202e38cfa9f22493197dd1a3577c7c38dcb9cc6344fbab9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226406107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e62a714a53e7673058851ffc6aff4be42a13a463ea89e89fea490ee867bf78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:45:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:45:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:45:39 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:45:39 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:46:21 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:46:22 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:46:23 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:46:24 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:46:25 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 03:46:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 03:46:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 03:46:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:46:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:31 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 03:46:32 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:46:34 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 03:46:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 03:46:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 03:46:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 03:46:48 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:46:50 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:46:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1293d5ef41ac474158c344a703ad2e4b1d3cc1086db95b5a0d51518714362c51`  
		Last Modified: Wed, 02 Feb 2022 03:50:30 GMT  
		Size: 85.7 MB (85703333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6191e74b124b9400a4f5c57d32ee0ff7bcf853d927f43939d87cda4a65135c0`  
		Last Modified: Wed, 02 Feb 2022 03:50:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f9eb3c9a7312036549f74c84994db03b4ed54b7b3ee5cc1d1268e5d53ab831`  
		Last Modified: Wed, 02 Feb 2022 03:50:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5352c9473118239827d56f70fd75fbd6f6a8025bd99e3382d3fd7b6427f9b9`  
		Last Modified: Wed, 02 Feb 2022 03:50:17 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2456278e509cc5c96311271bf8bf26c81e2f8fddeabe4b6b9d1e1d5a516b4945`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6fe5e155a20708bacc56139615325d04f5682b29e96322680394edd34da6b`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353d8ef97cc1b966a265fcb4b001a5061f4f1eab84e9a3c03d7568c831c2bc2`  
		Last Modified: Wed, 02 Feb 2022 03:50:50 GMT  
		Size: 116.4 MB (116415399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683992409b89a55cd62e3dee64330e89c520d14d571d64db9ecb574f1d2280c2`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 1.7 KB (1684 bytes)  
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
$ docker pull bonita@sha256:187a7c2eb7dda0b54fabf93bacbf9b7894466300981aad413466fb0a644d8b0f
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
$ docker pull bonita@sha256:caa2e952837a8f37202e38cfa9f22493197dd1a3577c7c38dcb9cc6344fbab9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226406107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e62a714a53e7673058851ffc6aff4be42a13a463ea89e89fea490ee867bf78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:45:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:45:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:45:39 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:45:39 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:46:21 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:46:22 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:46:23 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:46:24 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:46:25 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 02 Feb 2022 03:46:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 02 Feb 2022 03:46:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 02 Feb 2022 03:46:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:46:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 02 Feb 2022 03:46:31 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 02 Feb 2022 03:46:32 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:46:34 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 02 Feb 2022 03:46:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 02 Feb 2022 03:46:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 02 Feb 2022 03:46:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 02 Feb 2022 03:46:48 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:46:50 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:46:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1293d5ef41ac474158c344a703ad2e4b1d3cc1086db95b5a0d51518714362c51`  
		Last Modified: Wed, 02 Feb 2022 03:50:30 GMT  
		Size: 85.7 MB (85703333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6191e74b124b9400a4f5c57d32ee0ff7bcf853d927f43939d87cda4a65135c0`  
		Last Modified: Wed, 02 Feb 2022 03:50:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f9eb3c9a7312036549f74c84994db03b4ed54b7b3ee5cc1d1268e5d53ab831`  
		Last Modified: Wed, 02 Feb 2022 03:50:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5352c9473118239827d56f70fd75fbd6f6a8025bd99e3382d3fd7b6427f9b9`  
		Last Modified: Wed, 02 Feb 2022 03:50:17 GMT  
		Size: 546.9 KB (546946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2456278e509cc5c96311271bf8bf26c81e2f8fddeabe4b6b9d1e1d5a516b4945`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6fe5e155a20708bacc56139615325d04f5682b29e96322680394edd34da6b`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353d8ef97cc1b966a265fcb4b001a5061f4f1eab84e9a3c03d7568c831c2bc2`  
		Last Modified: Wed, 02 Feb 2022 03:50:50 GMT  
		Size: 116.4 MB (116415399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683992409b89a55cd62e3dee64330e89c520d14d571d64db9ecb574f1d2280c2`  
		Last Modified: Wed, 02 Feb 2022 03:50:41 GMT  
		Size: 1.7 KB (1684 bytes)  
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
$ docker pull bonita@sha256:05eb7ed4fffad4ee0f95a1d3b5cb62fbd4e8a027b67c161958d900ac23288810
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
$ docker pull bonita@sha256:1d8ec4448a4b96ba25218c57f1b3b56b5829e8bfad147c9d6ec85884a563cb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224097593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6630b2134154c946ccacddf67df0ee57c876af89274cd74719e3c60d6be61b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:48:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:59 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:49:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:49:23 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:49:23 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:49:24 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:49:25 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:49:26 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:49:27 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:49:28 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 03:49:29 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 03:49:30 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 03:49:31 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:49:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:34 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:49:36 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 03:49:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 03:49:44 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 03:49:45 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:49:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:49:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:49:48 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70234f375dfc7552903a976870d3630a9fffe6364c0e00b93861bae3573050`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 85.7 MB (85703453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38463bd41867f3e10e65a084c65e77045dc4afcbe144b4b9c4f30072821b8e`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8b185635319d5e319829095f04b2f8128a12a077f5013a8b2acd9c52a83a8`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4902c51a8f3c51ed0722f35cfedc3393337d44dd9dfcafe30c1685c42a382d`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 929.4 KB (929412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffad56017642341e3b408c3b8b334661581c7e926e980129c5ba24e219a965`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c659beb7cfa91a3ee3776b9d35a7ca934d6349d87a72617af702bdb6e9538`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ddd3dc89b01bc60d8d1dd80972d613cfe63a713c066fa415f19eb7693bad9`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7139bd23502b90f348736815e15fdf7885674662c1b63074bee2cf33f80d5`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
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
$ docker pull bonita@sha256:05eb7ed4fffad4ee0f95a1d3b5cb62fbd4e8a027b67c161958d900ac23288810
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
$ docker pull bonita@sha256:1d8ec4448a4b96ba25218c57f1b3b56b5829e8bfad147c9d6ec85884a563cb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224097593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6630b2134154c946ccacddf67df0ee57c876af89274cd74719e3c60d6be61b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:48:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:59 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:49:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:49:23 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:49:23 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:49:24 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:49:25 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:49:26 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:49:27 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:49:28 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 03:49:29 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 03:49:30 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 03:49:31 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:49:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:34 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:49:36 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 03:49:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 03:49:44 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 03:49:45 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:49:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:49:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:49:48 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70234f375dfc7552903a976870d3630a9fffe6364c0e00b93861bae3573050`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 85.7 MB (85703453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38463bd41867f3e10e65a084c65e77045dc4afcbe144b4b9c4f30072821b8e`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8b185635319d5e319829095f04b2f8128a12a077f5013a8b2acd9c52a83a8`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4902c51a8f3c51ed0722f35cfedc3393337d44dd9dfcafe30c1685c42a382d`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 929.4 KB (929412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffad56017642341e3b408c3b8b334661581c7e926e980129c5ba24e219a965`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c659beb7cfa91a3ee3776b9d35a7ca934d6349d87a72617af702bdb6e9538`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ddd3dc89b01bc60d8d1dd80972d613cfe63a713c066fa415f19eb7693bad9`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7139bd23502b90f348736815e15fdf7885674662c1b63074bee2cf33f80d5`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
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
$ docker pull bonita@sha256:05eb7ed4fffad4ee0f95a1d3b5cb62fbd4e8a027b67c161958d900ac23288810
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
$ docker pull bonita@sha256:1d8ec4448a4b96ba25218c57f1b3b56b5829e8bfad147c9d6ec85884a563cb2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224097593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6630b2134154c946ccacddf67df0ee57c876af89274cd74719e3c60d6be61b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:42:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 02 Feb 2022 03:48:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:59 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 02 Feb 2022 03:49:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 02 Feb 2022 03:49:23 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 02 Feb 2022 03:49:23 GMT
ARG BONITA_VERSION
# Wed, 02 Feb 2022 03:49:24 GMT
ARG BRANDING_VERSION
# Wed, 02 Feb 2022 03:49:25 GMT
ARG BONITA_SHA256
# Wed, 02 Feb 2022 03:49:26 GMT
ARG BASE_URL
# Wed, 02 Feb 2022 03:49:27 GMT
ARG BONITA_URL
# Wed, 02 Feb 2022 03:49:28 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 02 Feb 2022 03:49:29 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 02 Feb 2022 03:49:30 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 02 Feb 2022 03:49:31 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 02 Feb 2022 03:49:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 02 Feb 2022 03:49:34 GMT
RUN mkdir /opt/files
# Wed, 02 Feb 2022 03:49:36 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 02 Feb 2022 03:49:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 02 Feb 2022 03:49:44 GMT
ENV HTTP_API=false
# Wed, 02 Feb 2022 03:49:45 GMT
VOLUME [/opt/bonita]
# Wed, 02 Feb 2022 03:49:47 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 02 Feb 2022 03:49:47 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 03:49:48 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e70234f375dfc7552903a976870d3630a9fffe6364c0e00b93861bae3573050`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 85.7 MB (85703453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea38463bd41867f3e10e65a084c65e77045dc4afcbe144b4b9c4f30072821b8e`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8b185635319d5e319829095f04b2f8128a12a077f5013a8b2acd9c52a83a8`  
		Last Modified: Wed, 02 Feb 2022 03:51:06 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4902c51a8f3c51ed0722f35cfedc3393337d44dd9dfcafe30c1685c42a382d`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 929.4 KB (929412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffad56017642341e3b408c3b8b334661581c7e926e980129c5ba24e219a965`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c659beb7cfa91a3ee3776b9d35a7ca934d6349d87a72617af702bdb6e9538`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ddd3dc89b01bc60d8d1dd80972d613cfe63a713c066fa415f19eb7693bad9`  
		Last Modified: Wed, 02 Feb 2022 03:51:17 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d7139bd23502b90f348736815e15fdf7885674662c1b63074bee2cf33f80d5`  
		Last Modified: Wed, 02 Feb 2022 03:51:04 GMT  
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
