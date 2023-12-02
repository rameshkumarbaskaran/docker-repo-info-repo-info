<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.2.3-b1`](#silverpeas623-b1)
-	[`silverpeas:6.3.2`](#silverpeas632)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.2.3-b1`

```console
$ docker pull silverpeas@sha256:3e464db3c4439d59d93cc64db90a5faca2991b3822012ee2cc9684169516e5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.3-b1` - linux; amd64

```console
$ docker pull silverpeas@sha256:73ee7aff6f5e1afda1bc3d4330cf3fa8d6d82c4b94ea45c36415f2f944d36702
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1749466797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24893ed1267e51dbcbf3759406cbb2f6fa747d2b36414faa4f19527b1edf44a7`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:31:30 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 02 Dec 2023 06:31:30 GMT
ENV TERM=xterm
# Sat, 02 Dec 2023 06:40:33 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 02 Dec 2023 06:40:42 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 02 Dec 2023 06:40:47 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 02 Dec 2023 06:40:47 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 02 Dec 2023 06:41:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 02 Dec 2023 06:45:54 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Sat, 02 Dec 2023 06:45:54 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 02 Dec 2023 06:45:54 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=2
# Sat, 02 Dec 2023 06:47:31 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 02 Dec 2023 06:47:31 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 02 Dec 2023 06:47:31 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 02 Dec 2023 06:47:32 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 02 Dec 2023 06:47:32 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 02 Dec 2023 06:47:32 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 02 Dec 2023 06:51:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 02 Dec 2023 06:51:08 GMT
EXPOSE 8000 9990
# Sat, 02 Dec 2023 06:51:08 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 02 Dec 2023 06:51:09 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df5608df20cb6a703c4c249d37ee7202a913bf956332c7e3b6fa49ac8ddbc57`  
		Last Modified: Sat, 02 Dec 2023 06:52:49 GMT  
		Size: 762.4 MB (762357323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2cc1d8ab965ebf39cd37a6290af75654fe271367532df5e5ca3d7d33bbb3cc`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 4.0 MB (3994076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae6ed185b7f7a10fef3c653721c6270545c578b643affff73b1776c538a1839`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d04e77484d5dc6e0cf6a722e2b32b1c88c573ec9517e8375ba5144dab5b2d7`  
		Last Modified: Sat, 02 Dec 2023 06:51:27 GMT  
		Size: 2.5 MB (2534355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911599266d2a70fdd860cdea1db05ba2b1de3420824bcc4ede99ace6d090ae2e`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e689f539cf2cfd5c3216446f9b13acad7e32785f8cd653492cd72b51ba5134`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66cddbebfdce2cfe4aa651a009db0390794eb542b8b9ade87b822db3cf7e03`  
		Last Modified: Sat, 02 Dec 2023 06:53:10 GMT  
		Size: 196.8 MB (196774137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001d0f7f7ca2f689c0ac0a2b635c7aa3399a6f2ba13395a3083f5656e771938`  
		Last Modified: Sat, 02 Dec 2023 06:52:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126810ce38d5ea7ee5ed39e420f961b37659835f97ffdb37f1eff6e66d1c4df6`  
		Last Modified: Sat, 02 Dec 2023 06:52:58 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1c024eb0e9648a5663d4da85e25d02733cf2c3d379c3ca8fa1fd2e5fd5d593`  
		Last Modified: Sat, 02 Dec 2023 06:52:58 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b0c1cf468412ce173cef8769df074ac293125458d6d4fd6d975e5216e70da2`  
		Last Modified: Sat, 02 Dec 2023 06:52:58 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f34530288a7790f62b51104336bee1806d8648a1b72172dd1ce4eafe5984a9`  
		Last Modified: Sat, 02 Dec 2023 06:53:29 GMT  
		Size: 748.1 MB (748073517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.3.2`

```console
$ docker pull silverpeas@sha256:42475e8faeec1fa1d5eeca936035f929358271c8d35f8b80eabec062c25bc5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:fa749736e2b2ad66de32d55a75c0cbe8d1b32199ba319ddf2f897d0df7af8244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1780878926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1799ad33ee7415aa483fab6576592803080cc7fba6619de2828655b93c41bdd`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:31:30 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 02 Dec 2023 06:31:30 GMT
ENV TERM=xterm
# Sat, 02 Dec 2023 06:40:33 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 02 Dec 2023 06:40:42 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 02 Dec 2023 06:40:47 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 02 Dec 2023 06:40:47 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 02 Dec 2023 06:41:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 02 Dec 2023 06:41:27 GMT
ENV SILVERPEAS_VERSION=6.3.2
# Sat, 02 Dec 2023 06:41:27 GMT
ENV WILDFLY_VERSION=26.1.1
# Sat, 02 Dec 2023 06:41:27 GMT
LABEL name=Silverpeas 6.3.2 description=Image to install and to run Silverpeas 6.3.2 vendor=Silverpeas version=6.3.2 build=1
# Sat, 02 Dec 2023 06:42:24 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 02 Dec 2023 06:42:25 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 02 Dec 2023 06:45:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 02 Dec 2023 06:45:38 GMT
EXPOSE 8000 9990
# Sat, 02 Dec 2023 06:45:38 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 02 Dec 2023 06:45:39 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df5608df20cb6a703c4c249d37ee7202a913bf956332c7e3b6fa49ac8ddbc57`  
		Last Modified: Sat, 02 Dec 2023 06:52:49 GMT  
		Size: 762.4 MB (762357323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2cc1d8ab965ebf39cd37a6290af75654fe271367532df5e5ca3d7d33bbb3cc`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 4.0 MB (3994076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae6ed185b7f7a10fef3c653721c6270545c578b643affff73b1776c538a1839`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d04e77484d5dc6e0cf6a722e2b32b1c88c573ec9517e8375ba5144dab5b2d7`  
		Last Modified: Sat, 02 Dec 2023 06:51:27 GMT  
		Size: 2.5 MB (2534355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911599266d2a70fdd860cdea1db05ba2b1de3420824bcc4ede99ace6d090ae2e`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e689f539cf2cfd5c3216446f9b13acad7e32785f8cd653492cd72b51ba5134`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3166cc4117bad85edaf65084992ad5d5422cd7655489935be9c7da3cd4521`  
		Last Modified: Sat, 02 Dec 2023 06:51:37 GMT  
		Size: 217.8 MB (217842782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a67e252b48e7f3c3b7eb63e1161a05fc847c3e5c3822a45f773ea1659371c51`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e5a42b217b7667307279a8cace9765c8736a8eff10450187f05fa8dae6b08`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffab6771b34963924b33978c14458aec48b805cc35bf3f9bf30a40a72dc6e83`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f85e188af7a4755179319083749746f6e16eea777965fc1cdefdaa0c0b6590`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53017da9d5f02a5d8dca80699240be494adcf901bfd600d580578a87f166bb79`  
		Last Modified: Sat, 02 Dec 2023 06:51:59 GMT  
		Size: 758.4 MB (758416991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:42475e8faeec1fa1d5eeca936035f929358271c8d35f8b80eabec062c25bc5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:fa749736e2b2ad66de32d55a75c0cbe8d1b32199ba319ddf2f897d0df7af8244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1780878926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1799ad33ee7415aa483fab6576592803080cc7fba6619de2828655b93c41bdd`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:31:30 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 02 Dec 2023 06:31:30 GMT
ENV TERM=xterm
# Sat, 02 Dec 2023 06:40:33 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 02 Dec 2023 06:40:42 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 02 Dec 2023 06:40:47 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 02 Dec 2023 06:40:47 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:25 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 02 Dec 2023 06:41:26 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 02 Dec 2023 06:41:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 02 Dec 2023 06:41:27 GMT
ENV SILVERPEAS_VERSION=6.3.2
# Sat, 02 Dec 2023 06:41:27 GMT
ENV WILDFLY_VERSION=26.1.1
# Sat, 02 Dec 2023 06:41:27 GMT
LABEL name=Silverpeas 6.3.2 description=Image to install and to run Silverpeas 6.3.2 vendor=Silverpeas version=6.3.2 build=1
# Sat, 02 Dec 2023 06:42:24 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 02 Dec 2023 06:42:25 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 02 Dec 2023 06:42:25 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 02 Dec 2023 06:45:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 02 Dec 2023 06:45:38 GMT
EXPOSE 8000 9990
# Sat, 02 Dec 2023 06:45:38 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 02 Dec 2023 06:45:39 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df5608df20cb6a703c4c249d37ee7202a913bf956332c7e3b6fa49ac8ddbc57`  
		Last Modified: Sat, 02 Dec 2023 06:52:49 GMT  
		Size: 762.4 MB (762357323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2cc1d8ab965ebf39cd37a6290af75654fe271367532df5e5ca3d7d33bbb3cc`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 4.0 MB (3994076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae6ed185b7f7a10fef3c653721c6270545c578b643affff73b1776c538a1839`  
		Last Modified: Sat, 02 Dec 2023 06:51:29 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d04e77484d5dc6e0cf6a722e2b32b1c88c573ec9517e8375ba5144dab5b2d7`  
		Last Modified: Sat, 02 Dec 2023 06:51:27 GMT  
		Size: 2.5 MB (2534355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911599266d2a70fdd860cdea1db05ba2b1de3420824bcc4ede99ace6d090ae2e`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e689f539cf2cfd5c3216446f9b13acad7e32785f8cd653492cd72b51ba5134`  
		Last Modified: Sat, 02 Dec 2023 06:51:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be3166cc4117bad85edaf65084992ad5d5422cd7655489935be9c7da3cd4521`  
		Last Modified: Sat, 02 Dec 2023 06:51:37 GMT  
		Size: 217.8 MB (217842782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a67e252b48e7f3c3b7eb63e1161a05fc847c3e5c3822a45f773ea1659371c51`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e5a42b217b7667307279a8cace9765c8736a8eff10450187f05fa8dae6b08`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffab6771b34963924b33978c14458aec48b805cc35bf3f9bf30a40a72dc6e83`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f85e188af7a4755179319083749746f6e16eea777965fc1cdefdaa0c0b6590`  
		Last Modified: Sat, 02 Dec 2023 06:51:24 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53017da9d5f02a5d8dca80699240be494adcf901bfd600d580578a87f166bb79`  
		Last Modified: Sat, 02 Dec 2023 06:51:59 GMT  
		Size: 758.4 MB (758416991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
