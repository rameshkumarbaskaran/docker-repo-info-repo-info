## `bonita:latest`

```console
$ docker pull bonita@sha256:cfd04276e7e8fff7294c1a4bb387052fb007a9b0e621c99622ddba0f9a655d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
