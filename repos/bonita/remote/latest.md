## `bonita:latest`

```console
$ docker pull bonita@sha256:d64146b5ac018ad79df77035db816466ef2240a3a3231489ad0addf5e70ad611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:8ba7080a1dfe944cfa3aef310a80d85721b63bec01b8e828b4efa3720b6eb958
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180308041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9859da686fb4ba8fbb20e2bfab0b384a8efea93b24a5a7b1671330434e0a3a4a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:13:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 19 Jul 2022 23:13:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 19 Jul 2022 23:13:20 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 19 Jul 2022 23:13:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_VERSION
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BRANDING_VERSION
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_SHA256
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BASE_URL
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_URL
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 19 Jul 2022 23:13:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:13:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 19 Jul 2022 23:13:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:13:22 GMT
RUN mkdir /opt/files
# Tue, 19 Jul 2022 23:13:22 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 19 Jul 2022 23:13:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API=false
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 19 Jul 2022 23:13:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 19 Jul 2022 23:13:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 19 Jul 2022 23:13:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 19 Jul 2022 23:13:31 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 19 Jul 2022 23:13:31 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 19 Jul 2022 23:13:32 GMT
EXPOSE 8080 9000
# Tue, 19 Jul 2022 23:13:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 19 Jul 2022 23:13:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d6d302c572c7936a2c535df7e3665e4cea12109804d7db2e17c2350483f5c6`  
		Last Modified: Tue, 19 Jul 2022 23:14:04 GMT  
		Size: 60.8 MB (60792590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acef1e43a082930ac2a59ac750fcc44e89eee0d2ee2663ea15276a30a761c112`  
		Last Modified: Tue, 19 Jul 2022 23:13:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753d9cad27595f77612d22db5aff3bf2dd14371b997d3fd09692e97837874620`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d59792a17a7735b2bbce017b4e9d56c1eb02cc888a64de33a280730e0c1acc4`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a3b0241dac6de74f098fc124ba52ca8c4950e9b58a750f986190c73b50250b`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2f50a37fcc52dae6eaf265933b27d626a5e38dc2eca7b657a3062e4225083d`  
		Last Modified: Tue, 19 Jul 2022 23:14:00 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f1095e1b328bb6dfb64e3bc183b9c35afad21a80811146c52cabd8c1251db7`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b14e49b5ca541afa03c868b7617ac3f8bf2dca1217013940b3511bb53ac0fcfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179532890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d20a8d0a49aaa3f2a866b84e75f0470fc28aa3f2723eabb7f4b7762991f6d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:18:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 19 Jul 2022 23:18:53 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 19 Jul 2022 23:18:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 19 Jul 2022 23:18:55 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 19 Jul 2022 23:18:56 GMT
ARG BONITA_VERSION
# Tue, 19 Jul 2022 23:18:57 GMT
ARG BRANDING_VERSION
# Tue, 19 Jul 2022 23:18:58 GMT
ARG BONITA_SHA256
# Tue, 19 Jul 2022 23:18:59 GMT
ARG BASE_URL
# Tue, 19 Jul 2022 23:19:00 GMT
ARG BONITA_URL
# Tue, 19 Jul 2022 23:19:01 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 19 Jul 2022 23:19:02 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 19 Jul 2022 23:19:03 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 19 Jul 2022 23:19:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:19:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 19 Jul 2022 23:19:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:19:07 GMT
RUN mkdir /opt/files
# Tue, 19 Jul 2022 23:19:09 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 19 Jul 2022 23:19:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 19 Jul 2022 23:19:20 GMT
ENV HTTP_API=false
# Tue, 19 Jul 2022 23:19:21 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 19 Jul 2022 23:19:22 GMT
ENV HTTP_API_PASSWORD=
# Tue, 19 Jul 2022 23:19:23 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 19 Jul 2022 23:19:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 19 Jul 2022 23:19:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 19 Jul 2022 23:19:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 19 Jul 2022 23:19:27 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 19 Jul 2022 23:19:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 19 Jul 2022 23:19:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 19 Jul 2022 23:19:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 19 Jul 2022 23:19:31 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 19 Jul 2022 23:19:32 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 19 Jul 2022 23:19:34 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 19 Jul 2022 23:19:34 GMT
EXPOSE 8080 9000
# Tue, 19 Jul 2022 23:19:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 19 Jul 2022 23:19:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a830a9157109fda713d4c8868452f009b89f5a0aa23e35b64a9fd8ffcbeb248e`  
		Last Modified: Tue, 19 Jul 2022 23:20:35 GMT  
		Size: 60.1 MB (60117412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a219e1f74381cab8fbf4b2158f0e0c8cccf2822e3693f1d8bd13ca27bec084`  
		Last Modified: Tue, 19 Jul 2022 23:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3153e8cd70c473bb49cd1568765d6399083f8655ace89dcb743660377256711`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448fd19395d15f1dff4ee9d541ee4a4789a87a8902684e4abe9aec78f7c80696`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932c91b8ca10c2ff283945c7998d94267040c160f86b043a84e8a794c4d09a3a`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 3.0 KB (2999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a76d6481ad87c0f65cbd5bf6740c81fbcf6a2b23c530554ec66556c1515ef34`  
		Last Modified: Tue, 19 Jul 2022 23:20:34 GMT  
		Size: 116.7 MB (116688726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdff38d20f7bc060a65e11bf956a87d603ef22aeceda94be739ea3f0f13bd1c`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 5.4 KB (5395 bytes)  
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
