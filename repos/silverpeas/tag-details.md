<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.2.3-b1`](#silverpeas623-b1)
-	[`silverpeas:6.3`](#silverpeas63)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.2.3-b1`

```console
$ docker pull silverpeas@sha256:092e4dccb16a635100311ac702b05ae096e5a78269770779c19a047f79a13f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.3-b1` - linux; amd64

```console
$ docker pull silverpeas@sha256:11964f3160736463e9604b0cddb2538e949c6758f8723ace44b1fb2c4bd0a922
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1898134040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9eadedcebdcb97e46c3ac50f45adccea90084faa31bdafbd6504b8aa61d7118`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:36:15 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 05 Oct 2022 18:36:16 GMT
ENV TERM=xterm
# Wed, 05 Oct 2022 18:42:01 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 05 Oct 2022 18:42:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 05 Oct 2022 18:42:17 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 05 Oct 2022 18:42:17 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 05 Oct 2022 18:42:59 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Wed, 05 Oct 2022 18:42:59 GMT
ENV WILDFLY_VERSION=20.0.1
# Thu, 13 Oct 2022 18:38:26 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=2
# Thu, 13 Oct 2022 18:44:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 13 Oct 2022 18:44:06 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 13 Oct 2022 18:44:06 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 13 Oct 2022 18:44:06 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Oct 2022 18:44:06 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Thu, 13 Oct 2022 18:44:06 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 13 Oct 2022 18:47:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 13 Oct 2022 18:47:04 GMT
EXPOSE 8000 9990
# Thu, 13 Oct 2022 18:47:04 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Oct 2022 18:47:05 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3616069e3d96458d5ae23a0fe5849f26a27039e2b509db5c3e1bb4846a89fe2`  
		Last Modified: Wed, 05 Oct 2022 18:48:52 GMT  
		Size: 911.0 MB (911034394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72d8ed6bbbecb5619cb889c2e33e15823a00e40dc320700789d0e0e817a35e1`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 4.0 MB (3994068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4a9c7a34660475e7fec439784a9ce153444d6a944fa5b31cdaaf074ea27a80`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e99a4a2dabe2f8e959e9175b3527960f7eabbc5113f41a4d1a415ba4e0a8b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 2.5 MB (2534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037141e721092f2ec13934c502a6c55d7fe464a9d8efa768153e4b37e7bf5e8`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef56f6bfe76859720619bdf9adef48ce4e8faecdd59956f4ebbb5b15ea84fe4b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9bb9a1ef91b94eb6aeb5fada8620b6e1ebb97a17640c5c571bd78c23080aa`  
		Last Modified: Thu, 13 Oct 2022 18:48:26 GMT  
		Size: 196.8 MB (196774059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d1c7d1f35b702a8f7e39470dc3a403654342b3a18f675160b7f1dc1cc027e1`  
		Last Modified: Thu, 13 Oct 2022 18:48:14 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7be2e48f9a0d03af23f6fbf0967bc0153efc71e2c766d786048b69fa4d0fbfc`  
		Last Modified: Thu, 13 Oct 2022 18:48:13 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ec292897c50521da98541bf582db1bfd13724d5e026934cb087d42ccc903f`  
		Last Modified: Thu, 13 Oct 2022 18:48:13 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2867e687a3f26d9d3bcb861c2be49d2f79f1d201a2af5145af517712205310be`  
		Last Modified: Thu, 13 Oct 2022 18:48:13 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2080bef684c1b8b9733567978409c19a25331e0eca4abcdcef3a6a9821a23ea2`  
		Last Modified: Thu, 13 Oct 2022 18:48:50 GMT  
		Size: 748.1 MB (748073353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.3`

```console
$ docker pull silverpeas@sha256:635877186aea3c570a36db787cd83e9e24942c3a1afcff27798dd03365c6e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:bec6bea06f451b774cf130b1477eb26f07e8bd71bec98b27788bab59fdf3ba3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928342391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c50c3d268cf6981da0bd25ccf795b7d581d141cd2d64553b4fc451358cc0a`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:36:15 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 05 Oct 2022 18:36:16 GMT
ENV TERM=xterm
# Wed, 05 Oct 2022 18:42:01 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 05 Oct 2022 18:42:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 05 Oct 2022 18:42:17 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 05 Oct 2022 18:42:17 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 13 Oct 2022 18:28:48 GMT
ENV SILVERPEAS_VERSION=6.3
# Thu, 13 Oct 2022 18:28:48 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 13 Oct 2022 18:28:48 GMT
LABEL name=Silverpeas 6.3 description=Image to install and to run Silverpeas 6.3 vendor=Silverpeas version=6.3 build=1
# Thu, 13 Oct 2022 18:35:46 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 13 Oct 2022 18:35:46 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 13 Oct 2022 18:35:46 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 13 Oct 2022 18:35:47 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Oct 2022 18:35:47 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Thu, 13 Oct 2022 18:35:47 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 13 Oct 2022 18:38:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 13 Oct 2022 18:38:21 GMT
EXPOSE 8000 9990
# Thu, 13 Oct 2022 18:38:21 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Oct 2022 18:38:21 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3616069e3d96458d5ae23a0fe5849f26a27039e2b509db5c3e1bb4846a89fe2`  
		Last Modified: Wed, 05 Oct 2022 18:48:52 GMT  
		Size: 911.0 MB (911034394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72d8ed6bbbecb5619cb889c2e33e15823a00e40dc320700789d0e0e817a35e1`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 4.0 MB (3994068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4a9c7a34660475e7fec439784a9ce153444d6a944fa5b31cdaaf074ea27a80`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e99a4a2dabe2f8e959e9175b3527960f7eabbc5113f41a4d1a415ba4e0a8b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 2.5 MB (2534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037141e721092f2ec13934c502a6c55d7fe464a9d8efa768153e4b37e7bf5e8`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef56f6bfe76859720619bdf9adef48ce4e8faecdd59956f4ebbb5b15ea84fe4b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391587da9da25cd966eb63ac6e6bcab07b538acacda19033e6529dc300c19a9`  
		Last Modified: Thu, 13 Oct 2022 18:47:44 GMT  
		Size: 217.8 MB (217842819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ed411d33fd2fc34ccfe489fb500fa970eded495e614493127ccee0b066a1fd`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426e37e9d29bba0d500a03825073a9672b6272f346730b65a36c37ee38b7f382`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdb8c959f566c38c10bd7dc44a1e1788f6deb836ad4e7385594bb74563385e1`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fe2a7ae45c6273c4a1e72f64141498ac457bedf82d46540aa17c5a2cec2476`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb35618554c9d147de2b04f34117337bf3bfed72b61be54f6d422a0a634db4d`  
		Last Modified: Thu, 13 Oct 2022 18:48:02 GMT  
		Size: 757.2 MB (757212945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:635877186aea3c570a36db787cd83e9e24942c3a1afcff27798dd03365c6e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:bec6bea06f451b774cf130b1477eb26f07e8bd71bec98b27788bab59fdf3ba3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928342391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c50c3d268cf6981da0bd25ccf795b7d581d141cd2d64553b4fc451358cc0a`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:36:15 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 05 Oct 2022 18:36:16 GMT
ENV TERM=xterm
# Wed, 05 Oct 2022 18:42:01 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 05 Oct 2022 18:42:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 05 Oct 2022 18:42:17 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 05 Oct 2022 18:42:17 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:57 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 05 Oct 2022 18:42:58 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 05 Oct 2022 18:42:58 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 13 Oct 2022 18:28:48 GMT
ENV SILVERPEAS_VERSION=6.3
# Thu, 13 Oct 2022 18:28:48 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 13 Oct 2022 18:28:48 GMT
LABEL name=Silverpeas 6.3 description=Image to install and to run Silverpeas 6.3 vendor=Silverpeas version=6.3 build=1
# Thu, 13 Oct 2022 18:35:46 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 13 Oct 2022 18:35:46 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 13 Oct 2022 18:35:46 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 13 Oct 2022 18:35:47 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 13 Oct 2022 18:35:47 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Thu, 13 Oct 2022 18:35:47 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 13 Oct 2022 18:38:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 13 Oct 2022 18:38:21 GMT
EXPOSE 8000 9990
# Thu, 13 Oct 2022 18:38:21 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 13 Oct 2022 18:38:21 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3616069e3d96458d5ae23a0fe5849f26a27039e2b509db5c3e1bb4846a89fe2`  
		Last Modified: Wed, 05 Oct 2022 18:48:52 GMT  
		Size: 911.0 MB (911034394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72d8ed6bbbecb5619cb889c2e33e15823a00e40dc320700789d0e0e817a35e1`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 4.0 MB (3994068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4a9c7a34660475e7fec439784a9ce153444d6a944fa5b31cdaaf074ea27a80`  
		Last Modified: Wed, 05 Oct 2022 18:47:20 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e99a4a2dabe2f8e959e9175b3527960f7eabbc5113f41a4d1a415ba4e0a8b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 2.5 MB (2534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037141e721092f2ec13934c502a6c55d7fe464a9d8efa768153e4b37e7bf5e8`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef56f6bfe76859720619bdf9adef48ce4e8faecdd59956f4ebbb5b15ea84fe4b`  
		Last Modified: Wed, 05 Oct 2022 18:47:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1391587da9da25cd966eb63ac6e6bcab07b538acacda19033e6529dc300c19a9`  
		Last Modified: Thu, 13 Oct 2022 18:47:44 GMT  
		Size: 217.8 MB (217842819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ed411d33fd2fc34ccfe489fb500fa970eded495e614493127ccee0b066a1fd`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426e37e9d29bba0d500a03825073a9672b6272f346730b65a36c37ee38b7f382`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdb8c959f566c38c10bd7dc44a1e1788f6deb836ad4e7385594bb74563385e1`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fe2a7ae45c6273c4a1e72f64141498ac457bedf82d46540aa17c5a2cec2476`  
		Last Modified: Thu, 13 Oct 2022 18:47:26 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb35618554c9d147de2b04f34117337bf3bfed72b61be54f6d422a0a634db4d`  
		Last Modified: Thu, 13 Oct 2022 18:48:02 GMT  
		Size: 757.2 MB (757212945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
