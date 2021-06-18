## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:9642ca80ead6dafb94d418a4ec751647e1bd82e0614dc979c1b56f5c35349d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:d315e16a07f7f1c9df2e1279d1acb17b8f6adbcef71139d7fe4c95b5dd0f3fb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884753002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792bbf46971c27ae04566ad6e719250ed510aa0cb28a09ec42931c67ad8b215c`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:35:17 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 18 Jun 2021 02:35:18 GMT
ENV TERM=xterm
# Fri, 18 Jun 2021 02:41:54 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 18 Jun 2021 02:42:00 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 18 Jun 2021 02:42:04 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 18 Jun 2021 02:42:04 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 18 Jun 2021 02:42:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 18 Jun 2021 02:42:42 GMT
ENV LANG=en_US.UTF-8
# Fri, 18 Jun 2021 02:42:42 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 18 Jun 2021 02:42:43 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 02:42:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 18 Jun 2021 02:42:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 18 Jun 2021 02:42:45 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 18 Jun 2021 02:42:45 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 18 Jun 2021 02:42:45 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 18 Jun 2021 02:42:45 GMT
ENV SILVERPEAS_VERSION=6.2.1
# Fri, 18 Jun 2021 02:42:45 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 18 Jun 2021 02:42:46 GMT
LABEL name=Silverpeas 6.2.1 description=Image to install and to run Silverpeas 6.2.1 vendor=Silverpeas version=6.2.1 build=1
# Fri, 18 Jun 2021 02:43:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 18 Jun 2021 02:43:30 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 18 Jun 2021 02:43:31 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 18 Jun 2021 02:43:31 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 18 Jun 2021 02:43:31 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 18 Jun 2021 02:43:31 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 18 Jun 2021 02:45:31 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 18 Jun 2021 02:45:34 GMT
EXPOSE 8000 9990
# Fri, 18 Jun 2021 02:45:34 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 18 Jun 2021 02:45:34 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8342cfdb9a65978762b4190eaaa26e132d8598c42fe1ccda855a29c45b2ce41e`  
		Last Modified: Fri, 18 Jun 2021 03:08:22 GMT  
		Size: 905.3 MB (905288924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd738ff249fe8a7073aa226465037d9b1deccd8d2d178092c57b8c3a4ddd2487`  
		Last Modified: Fri, 18 Jun 2021 03:06:43 GMT  
		Size: 4.0 MB (3994068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa231ebd5e5b5ad1e145c2b4d77763e0effd87e9afb1895c5c88f1f24b25af7`  
		Last Modified: Fri, 18 Jun 2021 03:06:44 GMT  
		Size: 7.1 MB (7146636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4fec7ecb4732e3b1c29d5f748aa49bbad9dcc4e4df5ff9c9d1102105b1cedf`  
		Last Modified: Fri, 18 Jun 2021 03:06:41 GMT  
		Size: 2.5 MB (2534363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af457fdc910af5a5a204df8c090ff46464cd5a19f893fae5d75fb3ea89b7322b`  
		Last Modified: Fri, 18 Jun 2021 03:06:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3adb85f65a82c8bd2e7e75555d2214b5f58d9fe5cef245d6521ec291649988`  
		Last Modified: Fri, 18 Jun 2021 03:06:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bc4a17a4a0d8f5f39cfc4f17c371d90ded84a780a958e23eb6dba965030f92`  
		Last Modified: Fri, 18 Jun 2021 03:06:53 GMT  
		Size: 196.8 MB (196774017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0bdffb4733196be069ca234d0ab5b6807e1e69b9802c1fad741d2fe28e66c`  
		Last Modified: Fri, 18 Jun 2021 03:06:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d371f8559cf8891e70a6e6903d92d695c6e08f0a3c1a2c994657b96e70879`  
		Last Modified: Fri, 18 Jun 2021 03:06:37 GMT  
		Size: 660.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1462a6f1b82c84a8ff9e8bd4402611d6bd823a5b86127b5328e5810c6031b`  
		Last Modified: Fri, 18 Jun 2021 03:06:37 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cdd37bb0bf92bc2fdf268392dd72baf5f197e3ac41c670b34324ebf27ac953`  
		Last Modified: Fri, 18 Jun 2021 03:06:37 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c11773627fd8f130767a835f7e1e97464845706e759597da37d4c5ef54d2d1`  
		Last Modified: Fri, 18 Jun 2021 03:07:19 GMT  
		Size: 740.5 MB (740458603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
