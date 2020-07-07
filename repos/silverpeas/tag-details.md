<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1`](#silverpeas61)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:5dffbe40ff044cd2936b75d1d8aa0ae65a03184f6d004a5a807de4286d034efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:e5eb0e73cdd736de30f7f3c7f8a5a6d18b6249a643fb0d343085d5d374f05045
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1011604944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f9ce03d5e29068d68979d5bbc228872e8b58b905b336478f8d711edf983d1`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 02:49:35 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 07 Jul 2020 02:49:35 GMT
ENV TERM=xterm
# Tue, 07 Jul 2020 02:51:46 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 07 Jul 2020 02:51:48 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 07 Jul 2020 02:51:50 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 07 Jul 2020 02:51:50 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 07 Jul 2020 02:51:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 07 Jul 2020 02:51:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Jul 2020 02:51:54 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 07 Jul 2020 02:51:54 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Jul 2020 02:51:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Jul 2020 02:51:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 07 Jul 2020 02:51:55 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 07 Jul 2020 02:51:56 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 07 Jul 2020 02:51:56 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 07 Jul 2020 02:51:56 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Tue, 07 Jul 2020 02:51:56 GMT
ENV WILDFLY_VERSION=10.1.0
# Tue, 07 Jul 2020 02:51:56 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Tue, 07 Jul 2020 02:52:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 07 Jul 2020 02:52:07 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Tue, 07 Jul 2020 02:52:07 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 07 Jul 2020 02:52:07 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Tue, 07 Jul 2020 02:52:08 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 07 Jul 2020 02:54:47 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Tue, 07 Jul 2020 02:54:47 GMT
EXPOSE 8000 9990
# Tue, 07 Jul 2020 02:54:48 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Tue, 07 Jul 2020 02:54:48 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9903b279ee1621f252b2e4d22362601e7e8349d11e4a8f784a174e89c73ab`  
		Last Modified: Tue, 07 Jul 2020 02:57:04 GMT  
		Size: 206.3 MB (206260677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e0c02142b1cf8bb0e23507d67c02f48f409de0a7179f0e28af0b169ad35f2`  
		Last Modified: Tue, 07 Jul 2020 02:56:30 GMT  
		Size: 4.0 MB (3994022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1f6b4fa75ed0bd4d5bd831a51f11a962d8802516e643d944ded17eebc19eb0`  
		Last Modified: Tue, 07 Jul 2020 02:56:30 GMT  
		Size: 7.1 MB (7146611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae0f71ee759d3c92ad1acfe37d0d2bbbc05c2dc0363ff6b9f807fec877675ea`  
		Last Modified: Tue, 07 Jul 2020 02:56:27 GMT  
		Size: 845.4 KB (845416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f65a09bb9725222622658466b73b5a5a31d4f674759af24b22fd17ea2f11070`  
		Last Modified: Tue, 07 Jul 2020 02:56:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d669f58cf5b00daf264f93f03f9cdbfe3099f38445d874c78cefef5ff7f72fc`  
		Last Modified: Tue, 07 Jul 2020 02:56:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8803510cecec56c58dfb536ab43e1bd98e0515fd91fdea482c1cba03c43bdb9`  
		Last Modified: Tue, 07 Jul 2020 02:56:37 GMT  
		Size: 144.3 MB (144284437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82327aeb4e21f7ce71d0e5fe0a6733c5babbfb94d624948905df984a7df46cc`  
		Last Modified: Tue, 07 Jul 2020 02:56:26 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e3b17281e1c6758dd1b1a351a7bf8ac60e6a2a52575c02a1aa778fd9bdf2bc`  
		Last Modified: Tue, 07 Jul 2020 02:56:25 GMT  
		Size: 808.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00337460f0cb13e0cd8a6696bdf77643cdb1f5f08184af708e892bc32927d598`  
		Last Modified: Tue, 07 Jul 2020 02:56:26 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9743ba366792beb725d9936b9320df57174763fd86553b873a80aa156b828`  
		Last Modified: Tue, 07 Jul 2020 02:57:05 GMT  
		Size: 604.7 MB (604696123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1`

```console
$ docker pull silverpeas@sha256:58a4ee9535081e9c7da6fa9926e6de4dda24028aa19a23eca949d35161339407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.1` - linux; amd64

```console
$ docker pull silverpeas@sha256:d450741216f7c4fd71e736679e026a0aef3e4ee719a2a1dbe124e3316eb6a84e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1437801964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c8c0052ebb48c66fc2bf46bd910e9ccc9c2dd4ed0f5c99b5d901d01021c6c6`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 02:42:13 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 07 Jul 2020 02:42:14 GMT
ENV TERM=xterm
# Tue, 07 Jul 2020 02:46:35 GMT
RUN apt-get update && apt-get install -y     wget     vim     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 07 Jul 2020 02:46:38 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 07 Jul 2020 02:46:41 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 07 Jul 2020 02:46:42 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 07 Jul 2020 02:46:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:49 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 07 Jul 2020 02:46:52 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 07 Jul 2020 02:46:52 GMT
ENV SILVERPEAS_VERSION=6.1
# Tue, 07 Jul 2020 02:46:52 GMT
ENV WILDFLY_VERSION=18.0.1
# Tue, 07 Jul 2020 02:46:52 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1 build=2
# Tue, 07 Jul 2020 02:47:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Tue, 07 Jul 2020 02:47:06 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Tue, 07 Jul 2020 02:47:07 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 07 Jul 2020 02:49:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && mv ../migrations/db/h2/busCore/up040/alter-table.sql ../migrations/db/h2/busCore/up040/alter_table.sql   && rm ../log/build-*   && touch .install
# Tue, 07 Jul 2020 02:49:20 GMT
EXPOSE 8000 9990
# Tue, 07 Jul 2020 02:49:21 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 07 Jul 2020 02:49:21 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74044e3c9a31dfa12d088435f45ffbec344baeb62d89b57ed1cf6276f52a58c4`  
		Last Modified: Tue, 07 Jul 2020 02:56:21 GMT  
		Size: 489.4 MB (489386033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5b728c8110ec585f73877ee9bd4616aa211b8df30e5e6973434fe547de1eae`  
		Last Modified: Tue, 07 Jul 2020 02:55:01 GMT  
		Size: 4.0 MB (3994002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a64856858143fa1f6409757658cc69c8b68cf1429fbc1fd746d14028358acc`  
		Last Modified: Tue, 07 Jul 2020 02:55:02 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552962c04d8b43d1bad93a1316e85aac4206b49fd4af1e66190eca6912148307`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 490.7 KB (490693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe49bf272ada5639ae6756c1b09499d4f16388946ee0433d8d62d922ca7c1c9`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65162ac9be845cf810e7ec6837cf78695962aa55adc5f21f291b6c5d247cf177`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f102229bb5efaff38887998aa5315ed2f6820674f32984d375864313180bb`  
		Last Modified: Tue, 07 Jul 2020 02:55:15 GMT  
		Size: 190.5 MB (190469479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6754b14ce7eee946b1b21b1a2700b78d1fcca94a4d761e20e0d74da276b30e58`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1de2509e9cb1d2b9c3249bf7b514b6d2119842d502e2ebe9b36cbab8ea6dea`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737c56d12dfdc9a07cc1a8d73be22333d69509db0c073b478e874b4f119c8cc1`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607e71e12dcb6cf66a807bdc376644f7a0398da26fd55eb851663007a0036fc8`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6896dc1d005a37f22e2b4401f10820078eadf52c83fbde4e7284d74b2e2747c7`  
		Last Modified: Tue, 07 Jul 2020 02:55:49 GMT  
		Size: 719.6 MB (719579855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:58a4ee9535081e9c7da6fa9926e6de4dda24028aa19a23eca949d35161339407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:d450741216f7c4fd71e736679e026a0aef3e4ee719a2a1dbe124e3316eb6a84e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1437801964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c8c0052ebb48c66fc2bf46bd910e9ccc9c2dd4ed0f5c99b5d901d01021c6c6`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 02:42:13 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 07 Jul 2020 02:42:14 GMT
ENV TERM=xterm
# Tue, 07 Jul 2020 02:46:35 GMT
RUN apt-get update && apt-get install -y     wget     vim     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 07 Jul 2020 02:46:38 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 07 Jul 2020 02:46:41 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 07 Jul 2020 02:46:42 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 07 Jul 2020 02:46:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:49 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:50 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 07 Jul 2020 02:46:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 07 Jul 2020 02:46:51 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 07 Jul 2020 02:46:52 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 07 Jul 2020 02:46:52 GMT
ENV SILVERPEAS_VERSION=6.1
# Tue, 07 Jul 2020 02:46:52 GMT
ENV WILDFLY_VERSION=18.0.1
# Tue, 07 Jul 2020 02:46:52 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1 build=2
# Tue, 07 Jul 2020 02:47:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Tue, 07 Jul 2020 02:47:06 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 07 Jul 2020 02:47:06 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Tue, 07 Jul 2020 02:47:07 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 07 Jul 2020 02:49:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && mv ../migrations/db/h2/busCore/up040/alter-table.sql ../migrations/db/h2/busCore/up040/alter_table.sql   && rm ../log/build-*   && touch .install
# Tue, 07 Jul 2020 02:49:20 GMT
EXPOSE 8000 9990
# Tue, 07 Jul 2020 02:49:21 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 07 Jul 2020 02:49:21 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74044e3c9a31dfa12d088435f45ffbec344baeb62d89b57ed1cf6276f52a58c4`  
		Last Modified: Tue, 07 Jul 2020 02:56:21 GMT  
		Size: 489.4 MB (489386033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5b728c8110ec585f73877ee9bd4616aa211b8df30e5e6973434fe547de1eae`  
		Last Modified: Tue, 07 Jul 2020 02:55:01 GMT  
		Size: 4.0 MB (3994002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a64856858143fa1f6409757658cc69c8b68cf1429fbc1fd746d14028358acc`  
		Last Modified: Tue, 07 Jul 2020 02:55:02 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552962c04d8b43d1bad93a1316e85aac4206b49fd4af1e66190eca6912148307`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 490.7 KB (490693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe49bf272ada5639ae6756c1b09499d4f16388946ee0433d8d62d922ca7c1c9`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65162ac9be845cf810e7ec6837cf78695962aa55adc5f21f291b6c5d247cf177`  
		Last Modified: Tue, 07 Jul 2020 02:54:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f102229bb5efaff38887998aa5315ed2f6820674f32984d375864313180bb`  
		Last Modified: Tue, 07 Jul 2020 02:55:15 GMT  
		Size: 190.5 MB (190469479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6754b14ce7eee946b1b21b1a2700b78d1fcca94a4d761e20e0d74da276b30e58`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1de2509e9cb1d2b9c3249bf7b514b6d2119842d502e2ebe9b36cbab8ea6dea`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737c56d12dfdc9a07cc1a8d73be22333d69509db0c073b478e874b4f119c8cc1`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607e71e12dcb6cf66a807bdc376644f7a0398da26fd55eb851663007a0036fc8`  
		Last Modified: Tue, 07 Jul 2020 02:54:58 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6896dc1d005a37f22e2b4401f10820078eadf52c83fbde4e7284d74b2e2747c7`  
		Last Modified: Tue, 07 Jul 2020 02:55:49 GMT  
		Size: 719.6 MB (719579855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
