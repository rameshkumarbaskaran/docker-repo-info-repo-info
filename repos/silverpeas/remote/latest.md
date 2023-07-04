## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:f730da0cb490d4a82840aebb38b80b3cb17486410afc0b563df7a6276793b9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:5de4032f3ffe0b2afccb81eda471e226f283cad03fd727d8af3f1c9d6975df63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1779555239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2557c337c94ac2ea08222324a99d40d8b4a21f763c05b93151efc22847d665`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:59:22 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 04 Jul 2023 18:59:22 GMT
ENV TERM=xterm
# Tue, 04 Jul 2023 19:06:53 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 04 Jul 2023 19:07:00 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 04 Jul 2023 19:07:04 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 04 Jul 2023 19:07:04 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 04 Jul 2023 19:07:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 04 Jul 2023 19:07:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 04 Jul 2023 19:07:42 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 04 Jul 2023 19:07:42 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 19:07:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 04 Jul 2023 19:07:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 04 Jul 2023 19:07:43 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 04 Jul 2023 19:07:44 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 04 Jul 2023 19:07:44 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 04 Jul 2023 19:07:44 GMT
ENV SILVERPEAS_VERSION=6.3
# Tue, 04 Jul 2023 19:07:44 GMT
ENV WILDFLY_VERSION=26.1.1
# Tue, 04 Jul 2023 19:07:44 GMT
LABEL name=Silverpeas 6.3 description=Image to install and to run Silverpeas 6.3 vendor=Silverpeas version=6.3 build=1
# Tue, 04 Jul 2023 19:09:06 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 04 Jul 2023 19:09:07 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 04 Jul 2023 19:09:07 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Tue, 04 Jul 2023 19:09:07 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 04 Jul 2023 19:09:07 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Tue, 04 Jul 2023 19:09:07 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 04 Jul 2023 19:11:06 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Tue, 04 Jul 2023 19:11:09 GMT
EXPOSE 8000 9990
# Tue, 04 Jul 2023 19:11:09 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 04 Jul 2023 19:11:09 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f72fe173c8cbb93c829c1f83e91163c6e9b60f35279dd072b166c77fe12131`  
		Last Modified: Tue, 04 Jul 2023 19:16:10 GMT  
		Size: 762.2 MB (762243365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea54ebb4112bfad2d3ab596afe105dc5ebaa8ab1ed1bec9b28432d96912f8b50`  
		Last Modified: Tue, 04 Jul 2023 19:14:50 GMT  
		Size: 4.0 MB (3994071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347b72131b96dd98f484ef228b7be71ced9156ef06d94bebee98fce118b08b57`  
		Last Modified: Tue, 04 Jul 2023 19:14:51 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234ab2dfa158c41ca9bef4e245bd8754add3e69a1b4804b332e05993e9fafb7`  
		Last Modified: Tue, 04 Jul 2023 19:14:48 GMT  
		Size: 2.5 MB (2534354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09a73114ddf5a7c123f871e8eabb58d8a03dddc1172f133a393e7d0d58f057c`  
		Last Modified: Tue, 04 Jul 2023 19:14:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55105ca09f34f22bf91609d92c61c25c6c52775afd66eecae6a69e202474de5`  
		Last Modified: Tue, 04 Jul 2023 19:14:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd8dabfa1205aba7c9d839271c20321bef81cfc39f77cc0237931294c36ea60`  
		Last Modified: Tue, 04 Jul 2023 19:14:59 GMT  
		Size: 217.8 MB (217842826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb20fd1f45fc82c52b08375f94a95969fb87ef1c51c4a5739e27ddd66881ce4`  
		Last Modified: Tue, 04 Jul 2023 19:14:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd285ee05be2455a09e8321077adf775e80807f9c0fbc0ff87c9fa64ad8be33`  
		Last Modified: Tue, 04 Jul 2023 19:14:46 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6438351b3017a0fb3b4ed0a9eb65b741aee70f32c4bf5ff6788c7fef3d9c1962`  
		Last Modified: Tue, 04 Jul 2023 19:14:46 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d2c5628021ab0e97df442dd7b41b1c2e16b45e569a0f6224785ff56074ce`  
		Last Modified: Tue, 04 Jul 2023 19:14:46 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9efeb6c2243fe92687aeafec195156cc7f816626e5b0d975b7b5bce9be4a19`  
		Last Modified: Tue, 04 Jul 2023 19:15:21 GMT  
		Size: 757.2 MB (757211260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
