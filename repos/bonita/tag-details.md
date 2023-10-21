<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:2022.2`](#bonita20222)
-	[`bonita:2022.2-u0`](#bonita20222-u0)
-	[`bonita:2023.1`](#bonita20231)
-	[`bonita:2023.1-u0`](#bonita20231-u0)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:7.15`](#bonita715)
-	[`bonita:7.15.0`](#bonita7150)
-	[`bonita:8.0`](#bonita80)
-	[`bonita:8.0.0`](#bonita800)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:ce650e5acc90966d76ebb0c0968f5d2fe9d1b62d69cae93bdd808bce9f52f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:d3504d49046b6cbb431ec90bb344f254f1a8e0b9736d168e22abcd30ffed7c7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badd28134ec7f563679eee944b08edf0f1687d1f2c778833509d8434f488a0f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:19:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Jun 2023 01:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:20:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Jun 2023 01:20:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Jun 2023 01:20:08 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BRANDING_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_SHA256
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BASE_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Jun 2023 01:20:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
RUN mkdir /opt/files
# Fri, 02 Jun 2023 01:20:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Jun 2023 01:20:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Jun 2023 01:20:16 GMT
ENV HTTP_API=false
# Fri, 02 Jun 2023 01:20:16 GMT
VOLUME [/opt/bonita]
# Fri, 02 Jun 2023 01:20:17 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Jun 2023 01:20:17 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:20:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd66009a2dbd6b13b48c03e620dc0d49a27b5fd5edd522481589da4ec83c526`  
		Last Modified: Fri, 02 Jun 2023 01:20:50 GMT  
		Size: 92.9 MB (92944178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be42761d56458b3876044f47c056acb8beb77ca5b5bad37a9377ae92724a7ac`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bb0bf1a3506f2d3fd5fa116d38b8a133731f7ac253a756e8b48310c57fc73e`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14cd509ef9279b4e10131ecedefb2116b8fb29d8be7e1b1267eb13dfcf74d5b`  
		Last Modified: Fri, 02 Jun 2023 01:20:37 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd80966488eec8a1d3be3122b746c2c605603cc3f7019eb872fd907f6dbae88`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e518b308f8e6b58f7d547b813759d11befdd2ac0bceb06ba3bce753939fb3f`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965e6c2ffddd5132fee5c085f652709db0942fc286553c4601fcf605e7326de`  
		Last Modified: Fri, 02 Jun 2023 01:20:42 GMT  
		Size: 113.7 MB (113727967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69d5b1c719b5e1f5a1477c02c2c69a9ebd8eb6d0b33da3a2c1b8247d10a2a5`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9983867912dae3c0340ff770602729b3b3728753ff40591cf211bcf38007a1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225676099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c63596f96f08e3dbf506c6c90b2929d5eab4dd3ef5ef84cfd25e65fde9644c9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 01 Jun 2023 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:17:02 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 01 Jun 2023 23:17:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 01 Jun 2023 23:17:04 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 01 Jun 2023 23:17:04 GMT
ARG BONITA_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BRANDING_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_SHA256
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BASE_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 01 Jun 2023 23:17:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:06 GMT
RUN mkdir /opt/files
# Thu, 01 Jun 2023 23:17:06 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 01 Jun 2023 23:17:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 01 Jun 2023 23:17:12 GMT
ENV HTTP_API=false
# Thu, 01 Jun 2023 23:17:13 GMT
VOLUME [/opt/bonita]
# Thu, 01 Jun 2023 23:17:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 01 Jun 2023 23:17:14 GMT
EXPOSE 8080
# Thu, 01 Jun 2023 23:17:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cfb67ef19b8d2442c508e04ab003d707b523f2ee8ae03c1ab1442758c12151`  
		Last Modified: Thu, 01 Jun 2023 23:17:52 GMT  
		Size: 87.3 MB (87340452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cad99b019eb859855f0d5c5825fea4757b9db91cc08ca9a3a1f4d4a421af80`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d7c4b0a95b024d8689af7e62cab40303010e087a7907688d123171498db739`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a54bfcbabd0acd81e503fcd692852f94d0aefa37a592ea953045c67950963f5`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 859.6 KB (859575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed5bfbccc4f433c508ec71aeb81d2ab4aff36fed3bf9b0e355adbd42cd498d`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e1d827d0df165a6bc58709c2722e34ec7976e92aec1888870bdc42c3e5567`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23cd8e1319350f37efb6e02fa81d4e29025bf431c34d5bf98127806953fab3`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 113.7 MB (113727966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84800ffb6ef7fb85e38cf09a031bb365b6912b0aa61e2b5218f8f37e2b40850b`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:ee1f85da1a0601a58c08f5b38954b807e58e77f1c15f856c6e65c6d7069d9f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232986008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f8cedb264ee64d6eea033731ad0d9e827931e355389b1670d4603868da35a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 02:35:53 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Sep 2023 02:38:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 02:38:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Sep 2023 02:38:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 16 Sep 2023 02:38:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BONITA_VERSION
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BRANDING_VERSION
# Sat, 16 Sep 2023 02:38:36 GMT
ARG BONITA_SHA256
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BASE_URL
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BONITA_URL
# Sat, 16 Sep 2023 02:38:38 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 16 Sep 2023 02:38:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Sep 2023 02:38:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:42 GMT
RUN mkdir /opt/files
# Sat, 16 Sep 2023 02:38:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 16 Sep 2023 02:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 16 Sep 2023 02:38:57 GMT
ENV HTTP_API=false
# Sat, 16 Sep 2023 02:39:00 GMT
VOLUME [/opt/bonita]
# Sat, 16 Sep 2023 02:39:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 16 Sep 2023 02:39:03 GMT
EXPOSE 8080
# Sat, 16 Sep 2023 02:39:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2be4fb4963c9ca350d079e0a4f8a6af6e5c340f41d8021b993e78df7f93ad064`  
		Last Modified: Fri, 02 Jun 2023 00:21:59 GMT  
		Size: 30.4 MB (30444090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ceefc23d77069ec288df034168091e2b853c1486fed391d1dae80c8dd41319`  
		Last Modified: Sat, 16 Sep 2023 02:39:59 GMT  
		Size: 88.0 MB (87975233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05285767062ecf2a4dbeac7e3b295a6f16b85aaed73b43d053de02361fd4ee9`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85527ce4335f69446508c3a5ec215a176f774bb26f0e289f01f869b03a3f000`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b04b643d05b9d28651f17e0200b452ec28cb6c1a34562fb14ea01d4bf6563e`  
		Last Modified: Sat, 16 Sep 2023 02:39:38 GMT  
		Size: 831.6 KB (831580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58368109f9a398b225bcf828cfe5e4e1872efadae44c7f24b8ea71a490296db6`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba19de21f79dddd4b1496ced7970f008404bb0a6a0207e5d46a86964b546b2f`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65d3fdfff12c9f01cbb893d222cf4ffa59d774f4d34d06769fd273dcfb5d25d`  
		Last Modified: Sat, 16 Sep 2023 02:39:47 GMT  
		Size: 113.7 MB (113727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86765eaed4922054440ad8df162f88c7bb68e20fe40dc037bf19ac523b0f1c`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:ce650e5acc90966d76ebb0c0968f5d2fe9d1b62d69cae93bdd808bce9f52f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:d3504d49046b6cbb431ec90bb344f254f1a8e0b9736d168e22abcd30ffed7c7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badd28134ec7f563679eee944b08edf0f1687d1f2c778833509d8434f488a0f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:19:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Jun 2023 01:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:20:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Jun 2023 01:20:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Jun 2023 01:20:08 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BRANDING_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_SHA256
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BASE_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Jun 2023 01:20:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
RUN mkdir /opt/files
# Fri, 02 Jun 2023 01:20:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Jun 2023 01:20:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Jun 2023 01:20:16 GMT
ENV HTTP_API=false
# Fri, 02 Jun 2023 01:20:16 GMT
VOLUME [/opt/bonita]
# Fri, 02 Jun 2023 01:20:17 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Jun 2023 01:20:17 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:20:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd66009a2dbd6b13b48c03e620dc0d49a27b5fd5edd522481589da4ec83c526`  
		Last Modified: Fri, 02 Jun 2023 01:20:50 GMT  
		Size: 92.9 MB (92944178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be42761d56458b3876044f47c056acb8beb77ca5b5bad37a9377ae92724a7ac`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bb0bf1a3506f2d3fd5fa116d38b8a133731f7ac253a756e8b48310c57fc73e`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14cd509ef9279b4e10131ecedefb2116b8fb29d8be7e1b1267eb13dfcf74d5b`  
		Last Modified: Fri, 02 Jun 2023 01:20:37 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd80966488eec8a1d3be3122b746c2c605603cc3f7019eb872fd907f6dbae88`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e518b308f8e6b58f7d547b813759d11befdd2ac0bceb06ba3bce753939fb3f`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965e6c2ffddd5132fee5c085f652709db0942fc286553c4601fcf605e7326de`  
		Last Modified: Fri, 02 Jun 2023 01:20:42 GMT  
		Size: 113.7 MB (113727967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69d5b1c719b5e1f5a1477c02c2c69a9ebd8eb6d0b33da3a2c1b8247d10a2a5`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9983867912dae3c0340ff770602729b3b3728753ff40591cf211bcf38007a1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225676099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c63596f96f08e3dbf506c6c90b2929d5eab4dd3ef5ef84cfd25e65fde9644c9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 01 Jun 2023 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:17:02 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 01 Jun 2023 23:17:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 01 Jun 2023 23:17:04 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 01 Jun 2023 23:17:04 GMT
ARG BONITA_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BRANDING_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_SHA256
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BASE_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 01 Jun 2023 23:17:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:06 GMT
RUN mkdir /opt/files
# Thu, 01 Jun 2023 23:17:06 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 01 Jun 2023 23:17:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 01 Jun 2023 23:17:12 GMT
ENV HTTP_API=false
# Thu, 01 Jun 2023 23:17:13 GMT
VOLUME [/opt/bonita]
# Thu, 01 Jun 2023 23:17:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 01 Jun 2023 23:17:14 GMT
EXPOSE 8080
# Thu, 01 Jun 2023 23:17:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cfb67ef19b8d2442c508e04ab003d707b523f2ee8ae03c1ab1442758c12151`  
		Last Modified: Thu, 01 Jun 2023 23:17:52 GMT  
		Size: 87.3 MB (87340452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cad99b019eb859855f0d5c5825fea4757b9db91cc08ca9a3a1f4d4a421af80`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d7c4b0a95b024d8689af7e62cab40303010e087a7907688d123171498db739`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a54bfcbabd0acd81e503fcd692852f94d0aefa37a592ea953045c67950963f5`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 859.6 KB (859575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed5bfbccc4f433c508ec71aeb81d2ab4aff36fed3bf9b0e355adbd42cd498d`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e1d827d0df165a6bc58709c2722e34ec7976e92aec1888870bdc42c3e5567`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23cd8e1319350f37efb6e02fa81d4e29025bf431c34d5bf98127806953fab3`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 113.7 MB (113727966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84800ffb6ef7fb85e38cf09a031bb365b6912b0aa61e2b5218f8f37e2b40850b`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:ee1f85da1a0601a58c08f5b38954b807e58e77f1c15f856c6e65c6d7069d9f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232986008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f8cedb264ee64d6eea033731ad0d9e827931e355389b1670d4603868da35a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 02:35:53 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Sep 2023 02:38:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 02:38:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Sep 2023 02:38:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 16 Sep 2023 02:38:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BONITA_VERSION
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BRANDING_VERSION
# Sat, 16 Sep 2023 02:38:36 GMT
ARG BONITA_SHA256
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BASE_URL
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BONITA_URL
# Sat, 16 Sep 2023 02:38:38 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 16 Sep 2023 02:38:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Sep 2023 02:38:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:42 GMT
RUN mkdir /opt/files
# Sat, 16 Sep 2023 02:38:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 16 Sep 2023 02:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 16 Sep 2023 02:38:57 GMT
ENV HTTP_API=false
# Sat, 16 Sep 2023 02:39:00 GMT
VOLUME [/opt/bonita]
# Sat, 16 Sep 2023 02:39:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 16 Sep 2023 02:39:03 GMT
EXPOSE 8080
# Sat, 16 Sep 2023 02:39:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2be4fb4963c9ca350d079e0a4f8a6af6e5c340f41d8021b993e78df7f93ad064`  
		Last Modified: Fri, 02 Jun 2023 00:21:59 GMT  
		Size: 30.4 MB (30444090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ceefc23d77069ec288df034168091e2b853c1486fed391d1dae80c8dd41319`  
		Last Modified: Sat, 16 Sep 2023 02:39:59 GMT  
		Size: 88.0 MB (87975233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05285767062ecf2a4dbeac7e3b295a6f16b85aaed73b43d053de02361fd4ee9`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85527ce4335f69446508c3a5ec215a176f774bb26f0e289f01f869b03a3f000`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b04b643d05b9d28651f17e0200b452ec28cb6c1a34562fb14ea01d4bf6563e`  
		Last Modified: Sat, 16 Sep 2023 02:39:38 GMT  
		Size: 831.6 KB (831580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58368109f9a398b225bcf828cfe5e4e1872efadae44c7f24b8ea71a490296db6`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba19de21f79dddd4b1496ced7970f008404bb0a6a0207e5d46a86964b546b2f`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65d3fdfff12c9f01cbb893d222cf4ffa59d774f4d34d06769fd273dcfb5d25d`  
		Last Modified: Sat, 16 Sep 2023 02:39:47 GMT  
		Size: 113.7 MB (113727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86765eaed4922054440ad8df162f88c7bb68e20fe40dc037bf19ac523b0f1c`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:b91ff1af5aac73b96fbca89ad9df29919486ff91b7b6b71f4fedeea7ab499fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:3cac4180084c8dbf3335b65b9fe7f9db49b1e540bdcc6377ce7b8b87a03df0f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98c7f607f72d0b2c7486fe9dab7f05073280d5e7d98b2f5e3c7b795f06232a8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:08:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:08:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:08:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:08:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:08:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:52 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:08:52 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:08:59 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:08:59 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:08:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:08:59 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:08:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d610034353553f6ca76b74cdd62d0015e40ad583c7f6d503a50ecf08041d8fe9`  
		Last Modified: Sat, 21 Oct 2023 00:09:55 GMT  
		Size: 57.5 MB (57526433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90de5e69792da749c895abc624ab3de43351b491f05f0c4f2356d53ca0833f8`  
		Last Modified: Sat, 21 Oct 2023 00:09:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb032c20af74385a38dd4f1c00cd6214f64989a2b97e5e6ea9ba7cfa72f4810`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d17667756dc950766c0bb7ac800ad21624adb5b4f21966f48a963898e5c928c`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f8c69457bcf98203d907b0c843170b7869d949233dc5a9855db2248b6f90b`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c965fa2f0b980792f8409398d0754b8e7ad27564f34d507874335971c6cc026`  
		Last Modified: Sat, 21 Oct 2023 00:09:52 GMT  
		Size: 116.7 MB (116690773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd546514c9d426bf4ed51809f460045390909c82583b2307348dc746d51fe8`  
		Last Modified: Sat, 21 Oct 2023 00:09:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0ea169d83237eb202306b2cd0a6cc24877890d9d8be482653ec04602e013a856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87e4009484cad5718c8f7655cfd032ea2e2f306bc9d19f914a31ae5a93fdc8a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:21:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:21:14 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:15 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:15 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:21:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:19 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:20 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:20 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:20 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30b04b989feda894ca0b457461e55d9039d0ebde980dc0e5bee386b70675866`  
		Last Modified: Sat, 21 Oct 2023 00:22:14 GMT  
		Size: 56.8 MB (56849162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118902ce787d895d2e785b08904870a93874d9db197dd86081bae5601281bd46`  
		Last Modified: Sat, 21 Oct 2023 00:22:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a4625b1872efa24499c906f30e0bff3d56b7ce2df26c57fd55492e99d3ba7`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cfa9b8a826cfefbdc2a0150c54e94974899aeb3de7ff2b7b22299592851c1`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db461290ead7e14a6b69ae5137cdcd1af2bde66f7f757a6b4c504f8f9469068f`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 3.0 KB (3033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a386c89d0274e585ff30b4d469d155680308286e672aca6b9619b867ec8a67a1`  
		Last Modified: Sat, 21 Oct 2023 00:22:12 GMT  
		Size: 116.7 MB (116690828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82291cca55afe2714decce7bdeca50b6ed3df9a627980ba8c9917136d2820fdf`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:5b72012bd1c8ef23bb6cf5a1c74dcd525fae746206edc86eaa991e645716d2e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13755e0f0e74aab659ec215606fe9e431fdd5acdb2e5b135702a31998ad0b8f`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:50 GMT
ADD file:f730d2cd05a420ffd38548ae1611345fc40a7db59dea5ff41328caa60ee42608 in / 
# Mon, 07 Aug 2023 20:16:51 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:10 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:05:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:05:16 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:05:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:17 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:05:18 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:05:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:05:30 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:05:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:05:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:05:33 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:05:33 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:05:34 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:05:34 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:05:34 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1ecf55aa97fb0011a1c90ffc58e5cb218908bc85a13afe003aea5a46e045ac8`  
		Last Modified: Mon, 07 Aug 2023 20:18:07 GMT  
		Size: 2.8 MB (2812358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0bc661754e9c1a1c7808cd4aebcf9bb233e1e55c5cf2069c72db2eed92b512`  
		Last Modified: Sat, 21 Oct 2023 00:07:38 GMT  
		Size: 53.4 MB (53352378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba5f8131855543f6e63d29e15cd59e81fbbd4033e332bffe35433aa8a3b4f4c`  
		Last Modified: Sat, 21 Oct 2023 00:07:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9b9f1a1513e54f08fec07645bda95581f175dc7e28dfa7ce6cfa5ba40d8408`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b37a74ced68275fd7e18e8e056b7928ea978cfff0e61bc11f6de7370b12c0b`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cab843ca007a6c371937b42451f21fe5a544df927d5b5be512363c031235a5`  
		Last Modified: Sat, 21 Oct 2023 00:07:27 GMT  
		Size: 3.0 KB (3027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e184364fb77c4a7de8e3586962b8abf353afc490da25edcb18b58d5618b37e`  
		Last Modified: Sat, 21 Oct 2023 00:07:35 GMT  
		Size: 116.7 MB (116690767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101ee59bcf89ceff28424997b37ea86d3cbe59a6326e061137ac824534f154c`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:b91ff1af5aac73b96fbca89ad9df29919486ff91b7b6b71f4fedeea7ab499fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:3cac4180084c8dbf3335b65b9fe7f9db49b1e540bdcc6377ce7b8b87a03df0f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98c7f607f72d0b2c7486fe9dab7f05073280d5e7d98b2f5e3c7b795f06232a8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:08:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:08:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:08:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:08:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:08:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:52 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:08:52 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:08:59 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:08:59 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:08:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:08:59 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:08:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d610034353553f6ca76b74cdd62d0015e40ad583c7f6d503a50ecf08041d8fe9`  
		Last Modified: Sat, 21 Oct 2023 00:09:55 GMT  
		Size: 57.5 MB (57526433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90de5e69792da749c895abc624ab3de43351b491f05f0c4f2356d53ca0833f8`  
		Last Modified: Sat, 21 Oct 2023 00:09:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb032c20af74385a38dd4f1c00cd6214f64989a2b97e5e6ea9ba7cfa72f4810`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d17667756dc950766c0bb7ac800ad21624adb5b4f21966f48a963898e5c928c`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f8c69457bcf98203d907b0c843170b7869d949233dc5a9855db2248b6f90b`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c965fa2f0b980792f8409398d0754b8e7ad27564f34d507874335971c6cc026`  
		Last Modified: Sat, 21 Oct 2023 00:09:52 GMT  
		Size: 116.7 MB (116690773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd546514c9d426bf4ed51809f460045390909c82583b2307348dc746d51fe8`  
		Last Modified: Sat, 21 Oct 2023 00:09:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0ea169d83237eb202306b2cd0a6cc24877890d9d8be482653ec04602e013a856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87e4009484cad5718c8f7655cfd032ea2e2f306bc9d19f914a31ae5a93fdc8a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:21:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:21:14 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:15 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:15 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:21:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:19 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:20 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:20 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:20 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30b04b989feda894ca0b457461e55d9039d0ebde980dc0e5bee386b70675866`  
		Last Modified: Sat, 21 Oct 2023 00:22:14 GMT  
		Size: 56.8 MB (56849162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118902ce787d895d2e785b08904870a93874d9db197dd86081bae5601281bd46`  
		Last Modified: Sat, 21 Oct 2023 00:22:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a4625b1872efa24499c906f30e0bff3d56b7ce2df26c57fd55492e99d3ba7`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cfa9b8a826cfefbdc2a0150c54e94974899aeb3de7ff2b7b22299592851c1`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db461290ead7e14a6b69ae5137cdcd1af2bde66f7f757a6b4c504f8f9469068f`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 3.0 KB (3033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a386c89d0274e585ff30b4d469d155680308286e672aca6b9619b867ec8a67a1`  
		Last Modified: Sat, 21 Oct 2023 00:22:12 GMT  
		Size: 116.7 MB (116690828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82291cca55afe2714decce7bdeca50b6ed3df9a627980ba8c9917136d2820fdf`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:5b72012bd1c8ef23bb6cf5a1c74dcd525fae746206edc86eaa991e645716d2e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13755e0f0e74aab659ec215606fe9e431fdd5acdb2e5b135702a31998ad0b8f`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:50 GMT
ADD file:f730d2cd05a420ffd38548ae1611345fc40a7db59dea5ff41328caa60ee42608 in / 
# Mon, 07 Aug 2023 20:16:51 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:10 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:05:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:05:16 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:05:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:17 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:05:18 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:05:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:05:30 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:05:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:05:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:05:33 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:05:33 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:05:34 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:05:34 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:05:34 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1ecf55aa97fb0011a1c90ffc58e5cb218908bc85a13afe003aea5a46e045ac8`  
		Last Modified: Mon, 07 Aug 2023 20:18:07 GMT  
		Size: 2.8 MB (2812358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0bc661754e9c1a1c7808cd4aebcf9bb233e1e55c5cf2069c72db2eed92b512`  
		Last Modified: Sat, 21 Oct 2023 00:07:38 GMT  
		Size: 53.4 MB (53352378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba5f8131855543f6e63d29e15cd59e81fbbd4033e332bffe35433aa8a3b4f4c`  
		Last Modified: Sat, 21 Oct 2023 00:07:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9b9f1a1513e54f08fec07645bda95581f175dc7e28dfa7ce6cfa5ba40d8408`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b37a74ced68275fd7e18e8e056b7928ea978cfff0e61bc11f6de7370b12c0b`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cab843ca007a6c371937b42451f21fe5a544df927d5b5be512363c031235a5`  
		Last Modified: Sat, 21 Oct 2023 00:07:27 GMT  
		Size: 3.0 KB (3027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e184364fb77c4a7de8e3586962b8abf353afc490da25edcb18b58d5618b37e`  
		Last Modified: Sat, 21 Oct 2023 00:07:35 GMT  
		Size: 116.7 MB (116690767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101ee59bcf89ceff28424997b37ea86d3cbe59a6326e061137ac824534f154c`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:c855b569a6906e47cb0120d5e377f93bb13a7b5f4a15cf936de24de7b14fb149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:9397da525b7f910c00a74424fa135de72459d1f5ed3cd21fd26336df09d31874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d766ec513a1b35b5da81c182b9860f45d701389a7f5979cd0cbede490559705`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:09:09 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:10 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:10 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:17 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b97c8d888ae0b04882dd993b35b0850f3e34623d1e12caf16fecc66e9c412`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe37f4b4509cae99169ce632f24a9284f602da93663e74e37693b8d5756576`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c8ec81cf713585c8713461d2bc5ceaf1a54c4e79eae0aa9c0367bba26c0b6c`  
		Last Modified: Sat, 21 Oct 2023 00:10:18 GMT  
		Size: 119.2 MB (119192965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86163c87964ff6d91f03174e9fe98aeec7fa6457c9892a376d8df26f39c5d9`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:62e4c17b4661ca47f2c2733f87ba9695e393ebdd4461b0280eee047de700101d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182788911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0a7be30a91c69ff288330aeabf1f08f5b28a87ddd125509428ea99453bb0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:21:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:30 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:30 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:36 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3d8346a85c75af761fdcbc23eabf4c5d974d79f42d1200705026a6a44c82ce`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de254dfbb0a9f944a5a15b1b242d6cd131fe04faf4a3888f40c630bdef498f86`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 3.0 KB (3043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ed4f93a4567b7947e44839d52ab211805ff0d5f8033b12cc823a7b66b6893`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab2983a108eee39375b91d7771fed9b974c7faef0a63e2594139e6f3d6cfeb`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:70406f5fe89469ed7d59656f3f5e1c3fa7c8cb6ad0d98eee3fcae32df8d6b269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179810504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee1c222dc69b806f62cfeb0878e50a691a83cac4fbc9d9b57d84d88999eb9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:06:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:03 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:03 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:17 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:06:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:06:21 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:06:21 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:06:21 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:06:22 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:06:22 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0504305dcebccee264d838d1aeda4170303fdfee5ac27a24126e510fa10510`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da3285bf8e11449111455f0f577a3ea4f5b48772732be5bfc304dd87880544a`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb56fc9b54d41ce90e0aefae0f913653e1736555ad3253e802652db7515f80ac`  
		Last Modified: Sat, 21 Oct 2023 00:08:01 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff385ca6254ea8200d95868b4ece6077cfeffa8fb914f78c338af50ba9d4fa`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:c855b569a6906e47cb0120d5e377f93bb13a7b5f4a15cf936de24de7b14fb149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:9397da525b7f910c00a74424fa135de72459d1f5ed3cd21fd26336df09d31874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d766ec513a1b35b5da81c182b9860f45d701389a7f5979cd0cbede490559705`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:09:09 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:10 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:10 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:17 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b97c8d888ae0b04882dd993b35b0850f3e34623d1e12caf16fecc66e9c412`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe37f4b4509cae99169ce632f24a9284f602da93663e74e37693b8d5756576`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c8ec81cf713585c8713461d2bc5ceaf1a54c4e79eae0aa9c0367bba26c0b6c`  
		Last Modified: Sat, 21 Oct 2023 00:10:18 GMT  
		Size: 119.2 MB (119192965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86163c87964ff6d91f03174e9fe98aeec7fa6457c9892a376d8df26f39c5d9`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:62e4c17b4661ca47f2c2733f87ba9695e393ebdd4461b0280eee047de700101d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182788911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0a7be30a91c69ff288330aeabf1f08f5b28a87ddd125509428ea99453bb0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:21:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:30 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:30 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:36 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3d8346a85c75af761fdcbc23eabf4c5d974d79f42d1200705026a6a44c82ce`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de254dfbb0a9f944a5a15b1b242d6cd131fe04faf4a3888f40c630bdef498f86`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 3.0 KB (3043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ed4f93a4567b7947e44839d52ab211805ff0d5f8033b12cc823a7b66b6893`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab2983a108eee39375b91d7771fed9b974c7faef0a63e2594139e6f3d6cfeb`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:70406f5fe89469ed7d59656f3f5e1c3fa7c8cb6ad0d98eee3fcae32df8d6b269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179810504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee1c222dc69b806f62cfeb0878e50a691a83cac4fbc9d9b57d84d88999eb9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:06:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:03 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:03 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:17 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:06:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:06:21 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:06:21 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:06:21 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:06:22 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:06:22 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0504305dcebccee264d838d1aeda4170303fdfee5ac27a24126e510fa10510`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da3285bf8e11449111455f0f577a3ea4f5b48772732be5bfc304dd87880544a`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb56fc9b54d41ce90e0aefae0f913653e1736555ad3253e802652db7515f80ac`  
		Last Modified: Sat, 21 Oct 2023 00:08:01 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff385ca6254ea8200d95868b4ece6077cfeffa8fb914f78c338af50ba9d4fa`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:9cc1c79c2e0bfd31844e065735c9de9558b746de0c66a1a08ea01f0ab9b714e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6caa6d987f8bb4d92ac9708cb96892f75922c456f7e23f47fc81831baa5253b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d9138869e854dabe987677c6296b8000a27c0294216ff4f2fc6b5fcdcc0dc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:21:40 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:41 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:46 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:47 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:47 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:47 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:47 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53304663ae778a54e7b372eaa3f9d2c9ec04304676f7d68dbf9ef0e49cec5cd2`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248a924f2d69def64b47e413837d362d23526bd82a2ee8eaa76ef7eb7b3a2a6c`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db246470125490d592da04c556e6c1e6ab48ae698f4c32c4e808e30131fe16c4`  
		Last Modified: Sat, 21 Oct 2023 00:23:03 GMT  
		Size: 118.2 MB (118180306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38e28d52909284903d5d1d54a5f385e20c01dbcfda93424be746cdb87c2b0f`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:9cc1c79c2e0bfd31844e065735c9de9558b746de0c66a1a08ea01f0ab9b714e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6caa6d987f8bb4d92ac9708cb96892f75922c456f7e23f47fc81831baa5253b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d9138869e854dabe987677c6296b8000a27c0294216ff4f2fc6b5fcdcc0dc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:21:40 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:41 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:46 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:47 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:47 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:47 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:47 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53304663ae778a54e7b372eaa3f9d2c9ec04304676f7d68dbf9ef0e49cec5cd2`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248a924f2d69def64b47e413837d362d23526bd82a2ee8eaa76ef7eb7b3a2a6c`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db246470125490d592da04c556e6c1e6ab48ae698f4c32c4e808e30131fe16c4`  
		Last Modified: Sat, 21 Oct 2023 00:23:03 GMT  
		Size: 118.2 MB (118180306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38e28d52909284903d5d1d54a5f385e20c01dbcfda93424be746cdb87c2b0f`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:ce650e5acc90966d76ebb0c0968f5d2fe9d1b62d69cae93bdd808bce9f52f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:d3504d49046b6cbb431ec90bb344f254f1a8e0b9736d168e22abcd30ffed7c7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badd28134ec7f563679eee944b08edf0f1687d1f2c778833509d8434f488a0f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:19:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Jun 2023 01:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:20:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Jun 2023 01:20:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Jun 2023 01:20:08 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BRANDING_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_SHA256
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BASE_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Jun 2023 01:20:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
RUN mkdir /opt/files
# Fri, 02 Jun 2023 01:20:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Jun 2023 01:20:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Jun 2023 01:20:16 GMT
ENV HTTP_API=false
# Fri, 02 Jun 2023 01:20:16 GMT
VOLUME [/opt/bonita]
# Fri, 02 Jun 2023 01:20:17 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Jun 2023 01:20:17 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:20:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd66009a2dbd6b13b48c03e620dc0d49a27b5fd5edd522481589da4ec83c526`  
		Last Modified: Fri, 02 Jun 2023 01:20:50 GMT  
		Size: 92.9 MB (92944178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be42761d56458b3876044f47c056acb8beb77ca5b5bad37a9377ae92724a7ac`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bb0bf1a3506f2d3fd5fa116d38b8a133731f7ac253a756e8b48310c57fc73e`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14cd509ef9279b4e10131ecedefb2116b8fb29d8be7e1b1267eb13dfcf74d5b`  
		Last Modified: Fri, 02 Jun 2023 01:20:37 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd80966488eec8a1d3be3122b746c2c605603cc3f7019eb872fd907f6dbae88`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e518b308f8e6b58f7d547b813759d11befdd2ac0bceb06ba3bce753939fb3f`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965e6c2ffddd5132fee5c085f652709db0942fc286553c4601fcf605e7326de`  
		Last Modified: Fri, 02 Jun 2023 01:20:42 GMT  
		Size: 113.7 MB (113727967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69d5b1c719b5e1f5a1477c02c2c69a9ebd8eb6d0b33da3a2c1b8247d10a2a5`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9983867912dae3c0340ff770602729b3b3728753ff40591cf211bcf38007a1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225676099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c63596f96f08e3dbf506c6c90b2929d5eab4dd3ef5ef84cfd25e65fde9644c9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 01 Jun 2023 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:17:02 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 01 Jun 2023 23:17:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 01 Jun 2023 23:17:04 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 01 Jun 2023 23:17:04 GMT
ARG BONITA_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BRANDING_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_SHA256
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BASE_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 01 Jun 2023 23:17:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:06 GMT
RUN mkdir /opt/files
# Thu, 01 Jun 2023 23:17:06 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 01 Jun 2023 23:17:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 01 Jun 2023 23:17:12 GMT
ENV HTTP_API=false
# Thu, 01 Jun 2023 23:17:13 GMT
VOLUME [/opt/bonita]
# Thu, 01 Jun 2023 23:17:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 01 Jun 2023 23:17:14 GMT
EXPOSE 8080
# Thu, 01 Jun 2023 23:17:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cfb67ef19b8d2442c508e04ab003d707b523f2ee8ae03c1ab1442758c12151`  
		Last Modified: Thu, 01 Jun 2023 23:17:52 GMT  
		Size: 87.3 MB (87340452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cad99b019eb859855f0d5c5825fea4757b9db91cc08ca9a3a1f4d4a421af80`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d7c4b0a95b024d8689af7e62cab40303010e087a7907688d123171498db739`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a54bfcbabd0acd81e503fcd692852f94d0aefa37a592ea953045c67950963f5`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 859.6 KB (859575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed5bfbccc4f433c508ec71aeb81d2ab4aff36fed3bf9b0e355adbd42cd498d`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e1d827d0df165a6bc58709c2722e34ec7976e92aec1888870bdc42c3e5567`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23cd8e1319350f37efb6e02fa81d4e29025bf431c34d5bf98127806953fab3`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 113.7 MB (113727966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84800ffb6ef7fb85e38cf09a031bb365b6912b0aa61e2b5218f8f37e2b40850b`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:ee1f85da1a0601a58c08f5b38954b807e58e77f1c15f856c6e65c6d7069d9f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232986008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f8cedb264ee64d6eea033731ad0d9e827931e355389b1670d4603868da35a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 02:35:53 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Sep 2023 02:38:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 02:38:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Sep 2023 02:38:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 16 Sep 2023 02:38:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BONITA_VERSION
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BRANDING_VERSION
# Sat, 16 Sep 2023 02:38:36 GMT
ARG BONITA_SHA256
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BASE_URL
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BONITA_URL
# Sat, 16 Sep 2023 02:38:38 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 16 Sep 2023 02:38:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Sep 2023 02:38:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:42 GMT
RUN mkdir /opt/files
# Sat, 16 Sep 2023 02:38:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 16 Sep 2023 02:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 16 Sep 2023 02:38:57 GMT
ENV HTTP_API=false
# Sat, 16 Sep 2023 02:39:00 GMT
VOLUME [/opt/bonita]
# Sat, 16 Sep 2023 02:39:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 16 Sep 2023 02:39:03 GMT
EXPOSE 8080
# Sat, 16 Sep 2023 02:39:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2be4fb4963c9ca350d079e0a4f8a6af6e5c340f41d8021b993e78df7f93ad064`  
		Last Modified: Fri, 02 Jun 2023 00:21:59 GMT  
		Size: 30.4 MB (30444090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ceefc23d77069ec288df034168091e2b853c1486fed391d1dae80c8dd41319`  
		Last Modified: Sat, 16 Sep 2023 02:39:59 GMT  
		Size: 88.0 MB (87975233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05285767062ecf2a4dbeac7e3b295a6f16b85aaed73b43d053de02361fd4ee9`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85527ce4335f69446508c3a5ec215a176f774bb26f0e289f01f869b03a3f000`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b04b643d05b9d28651f17e0200b452ec28cb6c1a34562fb14ea01d4bf6563e`  
		Last Modified: Sat, 16 Sep 2023 02:39:38 GMT  
		Size: 831.6 KB (831580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58368109f9a398b225bcf828cfe5e4e1872efadae44c7f24b8ea71a490296db6`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba19de21f79dddd4b1496ced7970f008404bb0a6a0207e5d46a86964b546b2f`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65d3fdfff12c9f01cbb893d222cf4ffa59d774f4d34d06769fd273dcfb5d25d`  
		Last Modified: Sat, 16 Sep 2023 02:39:47 GMT  
		Size: 113.7 MB (113727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86765eaed4922054440ad8df162f88c7bb68e20fe40dc037bf19ac523b0f1c`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:ce650e5acc90966d76ebb0c0968f5d2fe9d1b62d69cae93bdd808bce9f52f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:d3504d49046b6cbb431ec90bb344f254f1a8e0b9736d168e22abcd30ffed7c7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badd28134ec7f563679eee944b08edf0f1687d1f2c778833509d8434f488a0f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:19:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Jun 2023 01:20:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:20:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Jun 2023 01:20:05 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Jun 2023 01:20:08 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BRANDING_VERSION
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_SHA256
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BASE_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ARG BONITA_URL
# Fri, 02 Jun 2023 01:20:08 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Jun 2023 01:20:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Jun 2023 01:20:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Jun 2023 01:20:09 GMT
RUN mkdir /opt/files
# Fri, 02 Jun 2023 01:20:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Jun 2023 01:20:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Jun 2023 01:20:16 GMT
ENV HTTP_API=false
# Fri, 02 Jun 2023 01:20:16 GMT
VOLUME [/opt/bonita]
# Fri, 02 Jun 2023 01:20:17 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Jun 2023 01:20:17 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:20:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd66009a2dbd6b13b48c03e620dc0d49a27b5fd5edd522481589da4ec83c526`  
		Last Modified: Fri, 02 Jun 2023 01:20:50 GMT  
		Size: 92.9 MB (92944178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be42761d56458b3876044f47c056acb8beb77ca5b5bad37a9377ae92724a7ac`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bb0bf1a3506f2d3fd5fa116d38b8a133731f7ac253a756e8b48310c57fc73e`  
		Last Modified: Fri, 02 Jun 2023 01:20:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14cd509ef9279b4e10131ecedefb2116b8fb29d8be7e1b1267eb13dfcf74d5b`  
		Last Modified: Fri, 02 Jun 2023 01:20:37 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd80966488eec8a1d3be3122b746c2c605603cc3f7019eb872fd907f6dbae88`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e518b308f8e6b58f7d547b813759d11befdd2ac0bceb06ba3bce753939fb3f`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6965e6c2ffddd5132fee5c085f652709db0942fc286553c4601fcf605e7326de`  
		Last Modified: Fri, 02 Jun 2023 01:20:42 GMT  
		Size: 113.7 MB (113727967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc69d5b1c719b5e1f5a1477c02c2c69a9ebd8eb6d0b33da3a2c1b8247d10a2a5`  
		Last Modified: Fri, 02 Jun 2023 01:20:36 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9983867912dae3c0340ff770602729b3b3728753ff40591cf211bcf38007a1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225676099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c63596f96f08e3dbf506c6c90b2929d5eab4dd3ef5ef84cfd25e65fde9644c9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 01 Jun 2023 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:17:02 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 01 Jun 2023 23:17:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 01 Jun 2023 23:17:04 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 01 Jun 2023 23:17:04 GMT
ARG BONITA_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BRANDING_VERSION
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_SHA256
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BASE_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ARG BONITA_URL
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 01 Jun 2023 23:17:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 01 Jun 2023 23:17:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 01 Jun 2023 23:17:06 GMT
RUN mkdir /opt/files
# Thu, 01 Jun 2023 23:17:06 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 01 Jun 2023 23:17:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 01 Jun 2023 23:17:12 GMT
ENV HTTP_API=false
# Thu, 01 Jun 2023 23:17:13 GMT
VOLUME [/opt/bonita]
# Thu, 01 Jun 2023 23:17:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 01 Jun 2023 23:17:14 GMT
EXPOSE 8080
# Thu, 01 Jun 2023 23:17:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cfb67ef19b8d2442c508e04ab003d707b523f2ee8ae03c1ab1442758c12151`  
		Last Modified: Thu, 01 Jun 2023 23:17:52 GMT  
		Size: 87.3 MB (87340452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cad99b019eb859855f0d5c5825fea4757b9db91cc08ca9a3a1f4d4a421af80`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d7c4b0a95b024d8689af7e62cab40303010e087a7907688d123171498db739`  
		Last Modified: Thu, 01 Jun 2023 23:17:43 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a54bfcbabd0acd81e503fcd692852f94d0aefa37a592ea953045c67950963f5`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 859.6 KB (859575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ed5bfbccc4f433c508ec71aeb81d2ab4aff36fed3bf9b0e355adbd42cd498d`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48e1d827d0df165a6bc58709c2722e34ec7976e92aec1888870bdc42c3e5567`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23cd8e1319350f37efb6e02fa81d4e29025bf431c34d5bf98127806953fab3`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 113.7 MB (113727966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84800ffb6ef7fb85e38cf09a031bb365b6912b0aa61e2b5218f8f37e2b40850b`  
		Last Modified: Thu, 01 Jun 2023 23:17:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:ee1f85da1a0601a58c08f5b38954b807e58e77f1c15f856c6e65c6d7069d9f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232986008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f8cedb264ee64d6eea033731ad0d9e827931e355389b1670d4603868da35a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
# Sat, 16 Sep 2023 02:35:53 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Sep 2023 02:38:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 16 Sep 2023 02:38:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Sep 2023 02:38:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 16 Sep 2023 02:38:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BONITA_VERSION
# Sat, 16 Sep 2023 02:38:35 GMT
ARG BRANDING_VERSION
# Sat, 16 Sep 2023 02:38:36 GMT
ARG BONITA_SHA256
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BASE_URL
# Sat, 16 Sep 2023 02:38:37 GMT
ARG BONITA_URL
# Sat, 16 Sep 2023 02:38:38 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 16 Sep 2023 02:38:39 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 16 Sep 2023 02:38:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Sep 2023 02:38:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 16 Sep 2023 02:38:42 GMT
RUN mkdir /opt/files
# Sat, 16 Sep 2023 02:38:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 16 Sep 2023 02:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 16 Sep 2023 02:38:57 GMT
ENV HTTP_API=false
# Sat, 16 Sep 2023 02:39:00 GMT
VOLUME [/opt/bonita]
# Sat, 16 Sep 2023 02:39:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 16 Sep 2023 02:39:03 GMT
EXPOSE 8080
# Sat, 16 Sep 2023 02:39:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:2be4fb4963c9ca350d079e0a4f8a6af6e5c340f41d8021b993e78df7f93ad064`  
		Last Modified: Fri, 02 Jun 2023 00:21:59 GMT  
		Size: 30.4 MB (30444090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ceefc23d77069ec288df034168091e2b853c1486fed391d1dae80c8dd41319`  
		Last Modified: Sat, 16 Sep 2023 02:39:59 GMT  
		Size: 88.0 MB (87975233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05285767062ecf2a4dbeac7e3b295a6f16b85aaed73b43d053de02361fd4ee9`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85527ce4335f69446508c3a5ec215a176f774bb26f0e289f01f869b03a3f000`  
		Last Modified: Sat, 16 Sep 2023 02:39:40 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b04b643d05b9d28651f17e0200b452ec28cb6c1a34562fb14ea01d4bf6563e`  
		Last Modified: Sat, 16 Sep 2023 02:39:38 GMT  
		Size: 831.6 KB (831580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58368109f9a398b225bcf828cfe5e4e1872efadae44c7f24b8ea71a490296db6`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba19de21f79dddd4b1496ced7970f008404bb0a6a0207e5d46a86964b546b2f`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65d3fdfff12c9f01cbb893d222cf4ffa59d774f4d34d06769fd273dcfb5d25d`  
		Last Modified: Sat, 16 Sep 2023 02:39:47 GMT  
		Size: 113.7 MB (113727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86765eaed4922054440ad8df162f88c7bb68e20fe40dc037bf19ac523b0f1c`  
		Last Modified: Sat, 16 Sep 2023 02:39:37 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:b91ff1af5aac73b96fbca89ad9df29919486ff91b7b6b71f4fedeea7ab499fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:3cac4180084c8dbf3335b65b9fe7f9db49b1e540bdcc6377ce7b8b87a03df0f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98c7f607f72d0b2c7486fe9dab7f05073280d5e7d98b2f5e3c7b795f06232a8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:08:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:08:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:08:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:08:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:08:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:52 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:08:52 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:08:59 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:08:59 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:08:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:08:59 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:08:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d610034353553f6ca76b74cdd62d0015e40ad583c7f6d503a50ecf08041d8fe9`  
		Last Modified: Sat, 21 Oct 2023 00:09:55 GMT  
		Size: 57.5 MB (57526433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90de5e69792da749c895abc624ab3de43351b491f05f0c4f2356d53ca0833f8`  
		Last Modified: Sat, 21 Oct 2023 00:09:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb032c20af74385a38dd4f1c00cd6214f64989a2b97e5e6ea9ba7cfa72f4810`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d17667756dc950766c0bb7ac800ad21624adb5b4f21966f48a963898e5c928c`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f8c69457bcf98203d907b0c843170b7869d949233dc5a9855db2248b6f90b`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c965fa2f0b980792f8409398d0754b8e7ad27564f34d507874335971c6cc026`  
		Last Modified: Sat, 21 Oct 2023 00:09:52 GMT  
		Size: 116.7 MB (116690773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd546514c9d426bf4ed51809f460045390909c82583b2307348dc746d51fe8`  
		Last Modified: Sat, 21 Oct 2023 00:09:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0ea169d83237eb202306b2cd0a6cc24877890d9d8be482653ec04602e013a856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87e4009484cad5718c8f7655cfd032ea2e2f306bc9d19f914a31ae5a93fdc8a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:21:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:21:14 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:15 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:15 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:21:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:19 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:20 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:20 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:20 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30b04b989feda894ca0b457461e55d9039d0ebde980dc0e5bee386b70675866`  
		Last Modified: Sat, 21 Oct 2023 00:22:14 GMT  
		Size: 56.8 MB (56849162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118902ce787d895d2e785b08904870a93874d9db197dd86081bae5601281bd46`  
		Last Modified: Sat, 21 Oct 2023 00:22:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a4625b1872efa24499c906f30e0bff3d56b7ce2df26c57fd55492e99d3ba7`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cfa9b8a826cfefbdc2a0150c54e94974899aeb3de7ff2b7b22299592851c1`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db461290ead7e14a6b69ae5137cdcd1af2bde66f7f757a6b4c504f8f9469068f`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 3.0 KB (3033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a386c89d0274e585ff30b4d469d155680308286e672aca6b9619b867ec8a67a1`  
		Last Modified: Sat, 21 Oct 2023 00:22:12 GMT  
		Size: 116.7 MB (116690828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82291cca55afe2714decce7bdeca50b6ed3df9a627980ba8c9917136d2820fdf`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:5b72012bd1c8ef23bb6cf5a1c74dcd525fae746206edc86eaa991e645716d2e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13755e0f0e74aab659ec215606fe9e431fdd5acdb2e5b135702a31998ad0b8f`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:50 GMT
ADD file:f730d2cd05a420ffd38548ae1611345fc40a7db59dea5ff41328caa60ee42608 in / 
# Mon, 07 Aug 2023 20:16:51 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:10 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:05:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:05:16 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:05:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:17 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:05:18 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:05:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:05:30 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:05:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:05:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:05:33 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:05:33 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:05:34 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:05:34 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:05:34 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1ecf55aa97fb0011a1c90ffc58e5cb218908bc85a13afe003aea5a46e045ac8`  
		Last Modified: Mon, 07 Aug 2023 20:18:07 GMT  
		Size: 2.8 MB (2812358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0bc661754e9c1a1c7808cd4aebcf9bb233e1e55c5cf2069c72db2eed92b512`  
		Last Modified: Sat, 21 Oct 2023 00:07:38 GMT  
		Size: 53.4 MB (53352378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba5f8131855543f6e63d29e15cd59e81fbbd4033e332bffe35433aa8a3b4f4c`  
		Last Modified: Sat, 21 Oct 2023 00:07:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9b9f1a1513e54f08fec07645bda95581f175dc7e28dfa7ce6cfa5ba40d8408`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b37a74ced68275fd7e18e8e056b7928ea978cfff0e61bc11f6de7370b12c0b`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cab843ca007a6c371937b42451f21fe5a544df927d5b5be512363c031235a5`  
		Last Modified: Sat, 21 Oct 2023 00:07:27 GMT  
		Size: 3.0 KB (3027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e184364fb77c4a7de8e3586962b8abf353afc490da25edcb18b58d5618b37e`  
		Last Modified: Sat, 21 Oct 2023 00:07:35 GMT  
		Size: 116.7 MB (116690767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101ee59bcf89ceff28424997b37ea86d3cbe59a6326e061137ac824534f154c`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:b91ff1af5aac73b96fbca89ad9df29919486ff91b7b6b71f4fedeea7ab499fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:3cac4180084c8dbf3335b65b9fe7f9db49b1e540bdcc6377ce7b8b87a03df0f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98c7f607f72d0b2c7486fe9dab7f05073280d5e7d98b2f5e3c7b795f06232a8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:08:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:08:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:08:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:08:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:08:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:08:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:08:52 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:08:52 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:08:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:08:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:08:59 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:08:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:08:59 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:08:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:08:59 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:08:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d610034353553f6ca76b74cdd62d0015e40ad583c7f6d503a50ecf08041d8fe9`  
		Last Modified: Sat, 21 Oct 2023 00:09:55 GMT  
		Size: 57.5 MB (57526433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90de5e69792da749c895abc624ab3de43351b491f05f0c4f2356d53ca0833f8`  
		Last Modified: Sat, 21 Oct 2023 00:09:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb032c20af74385a38dd4f1c00cd6214f64989a2b97e5e6ea9ba7cfa72f4810`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d17667756dc950766c0bb7ac800ad21624adb5b4f21966f48a963898e5c928c`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f8c69457bcf98203d907b0c843170b7869d949233dc5a9855db2248b6f90b`  
		Last Modified: Sat, 21 Oct 2023 00:09:46 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c965fa2f0b980792f8409398d0754b8e7ad27564f34d507874335971c6cc026`  
		Last Modified: Sat, 21 Oct 2023 00:09:52 GMT  
		Size: 116.7 MB (116690773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fd546514c9d426bf4ed51809f460045390909c82583b2307348dc746d51fe8`  
		Last Modified: Sat, 21 Oct 2023 00:09:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0ea169d83237eb202306b2cd0a6cc24877890d9d8be482653ec04602e013a856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87e4009484cad5718c8f7655cfd032ea2e2f306bc9d19f914a31ae5a93fdc8a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:21:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:13 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:21:14 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:21:15 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:15 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:21:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:19 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:19 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:20 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:20 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:20 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30b04b989feda894ca0b457461e55d9039d0ebde980dc0e5bee386b70675866`  
		Last Modified: Sat, 21 Oct 2023 00:22:14 GMT  
		Size: 56.8 MB (56849162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118902ce787d895d2e785b08904870a93874d9db197dd86081bae5601281bd46`  
		Last Modified: Sat, 21 Oct 2023 00:22:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a4625b1872efa24499c906f30e0bff3d56b7ce2df26c57fd55492e99d3ba7`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cfa9b8a826cfefbdc2a0150c54e94974899aeb3de7ff2b7b22299592851c1`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db461290ead7e14a6b69ae5137cdcd1af2bde66f7f757a6b4c504f8f9469068f`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 3.0 KB (3033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a386c89d0274e585ff30b4d469d155680308286e672aca6b9619b867ec8a67a1`  
		Last Modified: Sat, 21 Oct 2023 00:22:12 GMT  
		Size: 116.7 MB (116690828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82291cca55afe2714decce7bdeca50b6ed3df9a627980ba8c9917136d2820fdf`  
		Last Modified: Sat, 21 Oct 2023 00:22:05 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:5b72012bd1c8ef23bb6cf5a1c74dcd525fae746206edc86eaa991e645716d2e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13755e0f0e74aab659ec215606fe9e431fdd5acdb2e5b135702a31998ad0b8f`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:50 GMT
ADD file:f730d2cd05a420ffd38548ae1611345fc40a7db59dea5ff41328caa60ee42608 in / 
# Mon, 07 Aug 2023 20:16:51 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:10 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 21 Oct 2023 00:05:13 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:13 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:14 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 21 Oct 2023 00:05:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 21 Oct 2023 00:05:16 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:05:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 21 Oct 2023 00:05:17 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:05:18 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 21 Oct 2023 00:05:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:05:30 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:05:30 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:05:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:05:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:05:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:05:33 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:05:33 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:05:33 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:05:34 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:05:34 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:05:34 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f1ecf55aa97fb0011a1c90ffc58e5cb218908bc85a13afe003aea5a46e045ac8`  
		Last Modified: Mon, 07 Aug 2023 20:18:07 GMT  
		Size: 2.8 MB (2812358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0bc661754e9c1a1c7808cd4aebcf9bb233e1e55c5cf2069c72db2eed92b512`  
		Last Modified: Sat, 21 Oct 2023 00:07:38 GMT  
		Size: 53.4 MB (53352378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba5f8131855543f6e63d29e15cd59e81fbbd4033e332bffe35433aa8a3b4f4c`  
		Last Modified: Sat, 21 Oct 2023 00:07:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9b9f1a1513e54f08fec07645bda95581f175dc7e28dfa7ce6cfa5ba40d8408`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b37a74ced68275fd7e18e8e056b7928ea978cfff0e61bc11f6de7370b12c0b`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cab843ca007a6c371937b42451f21fe5a544df927d5b5be512363c031235a5`  
		Last Modified: Sat, 21 Oct 2023 00:07:27 GMT  
		Size: 3.0 KB (3027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e184364fb77c4a7de8e3586962b8abf353afc490da25edcb18b58d5618b37e`  
		Last Modified: Sat, 21 Oct 2023 00:07:35 GMT  
		Size: 116.7 MB (116690767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101ee59bcf89ceff28424997b37ea86d3cbe59a6326e061137ac824534f154c`  
		Last Modified: Sat, 21 Oct 2023 00:07:28 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15`

```console
$ docker pull bonita@sha256:c855b569a6906e47cb0120d5e377f93bb13a7b5f4a15cf936de24de7b14fb149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:9397da525b7f910c00a74424fa135de72459d1f5ed3cd21fd26336df09d31874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d766ec513a1b35b5da81c182b9860f45d701389a7f5979cd0cbede490559705`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:09:09 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:10 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:10 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:17 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b97c8d888ae0b04882dd993b35b0850f3e34623d1e12caf16fecc66e9c412`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe37f4b4509cae99169ce632f24a9284f602da93663e74e37693b8d5756576`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c8ec81cf713585c8713461d2bc5ceaf1a54c4e79eae0aa9c0367bba26c0b6c`  
		Last Modified: Sat, 21 Oct 2023 00:10:18 GMT  
		Size: 119.2 MB (119192965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86163c87964ff6d91f03174e9fe98aeec7fa6457c9892a376d8df26f39c5d9`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:62e4c17b4661ca47f2c2733f87ba9695e393ebdd4461b0280eee047de700101d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182788911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0a7be30a91c69ff288330aeabf1f08f5b28a87ddd125509428ea99453bb0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:21:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:30 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:30 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:36 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3d8346a85c75af761fdcbc23eabf4c5d974d79f42d1200705026a6a44c82ce`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de254dfbb0a9f944a5a15b1b242d6cd131fe04faf4a3888f40c630bdef498f86`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 3.0 KB (3043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ed4f93a4567b7947e44839d52ab211805ff0d5f8033b12cc823a7b66b6893`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab2983a108eee39375b91d7771fed9b974c7faef0a63e2594139e6f3d6cfeb`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:70406f5fe89469ed7d59656f3f5e1c3fa7c8cb6ad0d98eee3fcae32df8d6b269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179810504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee1c222dc69b806f62cfeb0878e50a691a83cac4fbc9d9b57d84d88999eb9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:06:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:03 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:03 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:17 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:06:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:06:21 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:06:21 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:06:21 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:06:22 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:06:22 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0504305dcebccee264d838d1aeda4170303fdfee5ac27a24126e510fa10510`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da3285bf8e11449111455f0f577a3ea4f5b48772732be5bfc304dd87880544a`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb56fc9b54d41ce90e0aefae0f913653e1736555ad3253e802652db7515f80ac`  
		Last Modified: Sat, 21 Oct 2023 00:08:01 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff385ca6254ea8200d95868b4ece6077cfeffa8fb914f78c338af50ba9d4fa`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:c855b569a6906e47cb0120d5e377f93bb13a7b5f4a15cf936de24de7b14fb149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:9397da525b7f910c00a74424fa135de72459d1f5ed3cd21fd26336df09d31874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d766ec513a1b35b5da81c182b9860f45d701389a7f5979cd0cbede490559705`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:09:09 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:09:10 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:10 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:17 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b97c8d888ae0b04882dd993b35b0850f3e34623d1e12caf16fecc66e9c412`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe37f4b4509cae99169ce632f24a9284f602da93663e74e37693b8d5756576`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c8ec81cf713585c8713461d2bc5ceaf1a54c4e79eae0aa9c0367bba26c0b6c`  
		Last Modified: Sat, 21 Oct 2023 00:10:18 GMT  
		Size: 119.2 MB (119192965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86163c87964ff6d91f03174e9fe98aeec7fa6457c9892a376d8df26f39c5d9`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:62e4c17b4661ca47f2c2733f87ba9695e393ebdd4461b0280eee047de700101d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182788911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0a7be30a91c69ff288330aeabf1f08f5b28a87ddd125509428ea99453bb0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:21:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:21:30 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:30 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:36 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3d8346a85c75af761fdcbc23eabf4c5d974d79f42d1200705026a6a44c82ce`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de254dfbb0a9f944a5a15b1b242d6cd131fe04faf4a3888f40c630bdef498f86`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 3.0 KB (3043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026ed4f93a4567b7947e44839d52ab211805ff0d5f8033b12cc823a7b66b6893`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab2983a108eee39375b91d7771fed9b974c7faef0a63e2594139e6f3d6cfeb`  
		Last Modified: Sat, 21 Oct 2023 00:22:29 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:70406f5fe89469ed7d59656f3f5e1c3fa7c8cb6ad0d98eee3fcae32df8d6b269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179810504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee1c222dc69b806f62cfeb0878e50a691a83cac4fbc9d9b57d84d88999eb9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 21 Oct 2023 00:06:00 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 21 Oct 2023 00:06:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 21 Oct 2023 00:06:03 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:03 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:16 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:17 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:17 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:06:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:06:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:06:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:06:21 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:06:21 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:06:21 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:06:21 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:06:22 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:06:22 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0504305dcebccee264d838d1aeda4170303fdfee5ac27a24126e510fa10510`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da3285bf8e11449111455f0f577a3ea4f5b48772732be5bfc304dd87880544a`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb56fc9b54d41ce90e0aefae0f913653e1736555ad3253e802652db7515f80ac`  
		Last Modified: Sat, 21 Oct 2023 00:08:01 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff385ca6254ea8200d95868b4ece6077cfeffa8fb914f78c338af50ba9d4fa`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0`

```console
$ docker pull bonita@sha256:9cc1c79c2e0bfd31844e065735c9de9558b746de0c66a1a08ea01f0ab9b714e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6caa6d987f8bb4d92ac9708cb96892f75922c456f7e23f47fc81831baa5253b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d9138869e854dabe987677c6296b8000a27c0294216ff4f2fc6b5fcdcc0dc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:21:40 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:41 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:46 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:47 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:47 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:47 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:47 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53304663ae778a54e7b372eaa3f9d2c9ec04304676f7d68dbf9ef0e49cec5cd2`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248a924f2d69def64b47e413837d362d23526bd82a2ee8eaa76ef7eb7b3a2a6c`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db246470125490d592da04c556e6c1e6ab48ae698f4c32c4e808e30131fe16c4`  
		Last Modified: Sat, 21 Oct 2023 00:23:03 GMT  
		Size: 118.2 MB (118180306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38e28d52909284903d5d1d54a5f385e20c01dbcfda93424be746cdb87c2b0f`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:9cc1c79c2e0bfd31844e065735c9de9558b746de0c66a1a08ea01f0ab9b714e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6caa6d987f8bb4d92ac9708cb96892f75922c456f7e23f47fc81831baa5253b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d9138869e854dabe987677c6296b8000a27c0294216ff4f2fc6b5fcdcc0dc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:21:40 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:41 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:46 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:47 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:47 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:47 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:47 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53304663ae778a54e7b372eaa3f9d2c9ec04304676f7d68dbf9ef0e49cec5cd2`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248a924f2d69def64b47e413837d362d23526bd82a2ee8eaa76ef7eb7b3a2a6c`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db246470125490d592da04c556e6c1e6ab48ae698f4c32c4e808e30131fe16c4`  
		Last Modified: Sat, 21 Oct 2023 00:23:03 GMT  
		Size: 118.2 MB (118180306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38e28d52909284903d5d1d54a5f385e20c01dbcfda93424be746cdb87c2b0f`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:9cc1c79c2e0bfd31844e065735c9de9558b746de0c66a1a08ea01f0ab9b714e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6caa6d987f8bb4d92ac9708cb96892f75922c456f7e23f47fc81831baa5253b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4d9138869e854dabe987677c6296b8000a27c0294216ff4f2fc6b5fcdcc0dc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:21:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:21:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:21:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:21:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:21:29 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:21:40 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:21:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:21:41 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:21:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:21:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:21:46 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:21:46 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:21:46 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:21:46 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:21:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:21:47 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:21:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:21:47 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:21:47 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:21:47 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5f2835c66f8ead0f5ac5004ac32b980310222426b764281faaba6d90a5bb1`  
		Last Modified: Sat, 21 Oct 2023 00:22:37 GMT  
		Size: 60.9 MB (60877871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560756194c1b347782438a0185cd65088a3571276f3c32c35de55f05d8caf37e`  
		Last Modified: Sat, 21 Oct 2023 00:22:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef831cf3e75e32ffa733657ecd5633e1f9365b368892c21a1858996d28d5cd3`  
		Last Modified: Sat, 21 Oct 2023 00:22:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53304663ae778a54e7b372eaa3f9d2c9ec04304676f7d68dbf9ef0e49cec5cd2`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248a924f2d69def64b47e413837d362d23526bd82a2ee8eaa76ef7eb7b3a2a6c`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db246470125490d592da04c556e6c1e6ab48ae698f4c32c4e808e30131fe16c4`  
		Last Modified: Sat, 21 Oct 2023 00:23:03 GMT  
		Size: 118.2 MB (118180306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38e28d52909284903d5d1d54a5f385e20c01dbcfda93424be746cdb87c2b0f`  
		Last Modified: Sat, 21 Oct 2023 00:22:53 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
