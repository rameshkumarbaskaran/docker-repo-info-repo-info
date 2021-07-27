## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:735790885dae5d2bb97f6cf82d7312c0e9de87022b994c2e8ddcc98d90639bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:74d2b529225a5a0fc58555f359f024648c68d61036bbc193b280e182b0780014
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884472124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a023d7eaaacd67a3d87986daa82b9f61ff344607dff20f0251997e3d659b32a1`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:21:19 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 27 Jul 2021 01:21:19 GMT
ENV TERM=xterm
# Tue, 27 Jul 2021 01:27:54 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 27 Jul 2021 01:28:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 27 Jul 2021 01:28:05 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 27 Jul 2021 01:28:05 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 27 Jul 2021 01:28:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 27 Jul 2021 01:28:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 27 Jul 2021 01:28:44 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 27 Jul 2021 01:28:44 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 27 Jul 2021 01:28:45 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 27 Jul 2021 01:28:45 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 27 Jul 2021 01:28:46 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 27 Jul 2021 01:28:46 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 27 Jul 2021 01:28:46 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 27 Jul 2021 01:28:46 GMT
ENV SILVERPEAS_VERSION=6.2.1
# Tue, 27 Jul 2021 01:28:46 GMT
ENV WILDFLY_VERSION=20.0.1
# Tue, 27 Jul 2021 01:28:47 GMT
LABEL name=Silverpeas 6.2.1 description=Image to install and to run Silverpeas 6.2.1 vendor=Silverpeas version=6.2.1 build=1
# Tue, 27 Jul 2021 01:29:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 27 Jul 2021 01:29:53 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 27 Jul 2021 01:29:54 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Tue, 27 Jul 2021 01:29:54 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 27 Jul 2021 01:29:54 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Tue, 27 Jul 2021 01:29:54 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 27 Jul 2021 01:33:28 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Tue, 27 Jul 2021 01:33:31 GMT
EXPOSE 8000 9990
# Tue, 27 Jul 2021 01:33:32 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 27 Jul 2021 01:33:32 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b71d2fe7174ae6a9fb01c91e4f3e22ba675561f61fc96b92516a1a6a4840e1`  
		Last Modified: Tue, 27 Jul 2021 02:00:08 GMT  
		Size: 905.0 MB (904990260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33abb19b0f36572d2fd4cf194edd96c246b6fe9b9d5a728f8e40301f010addee`  
		Last Modified: Tue, 27 Jul 2021 01:58:32 GMT  
		Size: 4.0 MB (3994069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c064721c88b65b2ffc7534ae50f974590c339729360f76219e93590033268f0`  
		Last Modified: Tue, 27 Jul 2021 01:58:33 GMT  
		Size: 7.1 MB (7146647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ddc445781e14fd493e44d08a34d7a2dbe75c7dfa82e6ac2aff5dac78957f66`  
		Last Modified: Tue, 27 Jul 2021 01:58:29 GMT  
		Size: 2.5 MB (2534354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dfb4dbaeec94e9fc7ac6bb8db05cca561e667e26a09aaf327edd8fbaec5587`  
		Last Modified: Tue, 27 Jul 2021 01:58:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f381f0f171fdb4676f12f15050fc93ff52bceeb4cdb4314b80cd9f6a19c4e9e`  
		Last Modified: Tue, 27 Jul 2021 01:58:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49307a674f9fef53d22cc97abac044fe666e06a634c6d73aa79e9831658e4740`  
		Last Modified: Tue, 27 Jul 2021 01:58:43 GMT  
		Size: 196.8 MB (196774103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069b47f4d5c543c0adcc0208f42dcb75a3df10f7c6339b52f1999716cc982ab1`  
		Last Modified: Tue, 27 Jul 2021 01:58:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5564fe5d88952c24bd424d76047a6e160722a84dde1a198bb61c6f4353476`  
		Last Modified: Tue, 27 Jul 2021 01:58:26 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a427454c94f7ca76e508cd18f5e9b3c417f422886d16cc921ce98a6e23ae5de7`  
		Last Modified: Tue, 27 Jul 2021 01:58:26 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaede5f7474524986b2c6f94b3c2dafaa7974a53265b689e096a4bc55cdebbc4`  
		Last Modified: Tue, 27 Jul 2021 01:58:26 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceb28ce4515ba8dcd22071283f5952defcafee16adf5325955233d91aa1f32a`  
		Last Modified: Tue, 27 Jul 2021 01:59:04 GMT  
		Size: 740.5 MB (740462042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
