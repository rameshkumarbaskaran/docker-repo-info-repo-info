## `bonita:latest`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
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
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
