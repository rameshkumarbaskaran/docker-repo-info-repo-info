<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.3`](#silverpeas613)
-	[`silverpeas:6.2.1`](#silverpeas621)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:110c1f20e802f7cc2bb5b480dffcd9409e071683b549a0c702ead34947f55b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:c3f7fd18e42038e404f3b2fb3272581a7556aa36beaa0e962f182062ba238e49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014926268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5699d68428416d4c2ca74a5539d5546842bbb7c95a53304aa0afa36ccd1d4e2`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 01:45:18 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 27 Jul 2021 01:45:19 GMT
ENV TERM=xterm
# Tue, 27 Jul 2021 01:49:16 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 27 Jul 2021 01:49:22 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 27 Jul 2021 01:49:27 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 27 Jul 2021 01:49:28 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 27 Jul 2021 01:49:33 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 27 Jul 2021 01:49:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 27 Jul 2021 01:49:34 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 27 Jul 2021 01:49:34 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 27 Jul 2021 01:49:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 27 Jul 2021 01:49:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 27 Jul 2021 01:49:38 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 27 Jul 2021 01:49:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 27 Jul 2021 01:49:39 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 27 Jul 2021 01:49:39 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Tue, 27 Jul 2021 01:49:40 GMT
ENV WILDFLY_VERSION=10.1.0
# Tue, 27 Jul 2021 01:49:40 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Tue, 27 Jul 2021 01:49:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 27 Jul 2021 01:49:54 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Tue, 27 Jul 2021 01:49:54 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 27 Jul 2021 01:49:55 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Tue, 27 Jul 2021 01:49:55 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 27 Jul 2021 01:58:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Tue, 27 Jul 2021 01:58:14 GMT
EXPOSE 8000 9990
# Tue, 27 Jul 2021 01:58:14 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Tue, 27 Jul 2021 01:58:14 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29259485236cf95c18f11971ab3387f2f368352d16e69e424df8978d7c03657b`  
		Last Modified: Tue, 27 Jul 2021 02:02:17 GMT  
		Size: 207.5 MB (207458838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405d4b5ad751593403f73aa776ef711d1486b27a43bcb99638b93e7fb2cf1709`  
		Last Modified: Tue, 27 Jul 2021 02:01:47 GMT  
		Size: 4.0 MB (3994089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec4cb4f3c8989e65b93b8bc9f64e6f2e6a22680416aa13b350fec21213b686`  
		Last Modified: Tue, 27 Jul 2021 02:01:48 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8960728d63cc3bdfdc31cb0bf4f3eee0baa2c8ef581b61aeb0d197df07fc6a7c`  
		Last Modified: Tue, 27 Jul 2021 02:01:44 GMT  
		Size: 845.4 KB (845397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0c2254cd189b44a580ce870491862cbf35b3b72d6e7af055bcad77eacce7bb`  
		Last Modified: Tue, 27 Jul 2021 02:01:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6411c4709988008ac57cceb60af6843ea02625a66fdc96ce7599566e8bb09e`  
		Last Modified: Tue, 27 Jul 2021 02:01:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be2f4de7ddd995696d970487ff1c57608e16d9a1fccb52311e617ce7c6b6173`  
		Last Modified: Tue, 27 Jul 2021 02:01:53 GMT  
		Size: 144.3 MB (144284735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85b610db032d9578d4b2771fd06599dfd34ee6af1dacff2efb4e916e7604dc7`  
		Last Modified: Tue, 27 Jul 2021 02:01:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ac5827f81c61904f91e4a09344b016292f00ea7ccaaa95abcfe541950e8d3f`  
		Last Modified: Tue, 27 Jul 2021 02:01:41 GMT  
		Size: 809.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830aae8fcf473766884fb91c2a817cdc5a07a1336213f57f20bc1fd859d02fe8`  
		Last Modified: Tue, 27 Jul 2021 02:01:41 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9baafb4e5846992ee0121550f21a3407cb1a826b06d252157fd7afd5612ae2`  
		Last Modified: Tue, 27 Jul 2021 02:02:11 GMT  
		Size: 604.7 MB (604695676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.3`

```console
$ docker pull silverpeas@sha256:aac6c263cef338a50a595b004e97aa7c4c8c11ae15bf3f339077ab0e5539cc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.1.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:cd510a13ede1fe425df2aa9ab050b633617140c61912704ebbc150d5d56afba2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426543419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0118a899e225c962e49a862be3be268dd55f24f9bb08801c99cadffb031c9a55`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:33:48 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 27 Jul 2021 01:33:48 GMT
ENV TERM=xterm
# Tue, 27 Jul 2021 01:41:21 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 27 Jul 2021 01:41:30 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 27 Jul 2021 01:41:35 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 27 Jul 2021 01:41:36 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 27 Jul 2021 01:41:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 27 Jul 2021 01:41:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 27 Jul 2021 01:41:40 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 27 Jul 2021 01:41:41 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 27 Jul 2021 01:41:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 27 Jul 2021 01:41:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 27 Jul 2021 01:41:44 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 27 Jul 2021 01:41:44 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 27 Jul 2021 01:41:45 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 27 Jul 2021 01:41:45 GMT
ENV SILVERPEAS_VERSION=6.1.3
# Tue, 27 Jul 2021 01:41:45 GMT
ENV WILDFLY_VERSION=18.0.1
# Tue, 27 Jul 2021 01:41:46 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.3 build=1
# Tue, 27 Jul 2021 01:42:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 27 Jul 2021 01:42:04 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 27 Jul 2021 01:42:04 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 27 Jul 2021 01:42:05 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Tue, 27 Jul 2021 01:42:05 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 27 Jul 2021 01:45:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Tue, 27 Jul 2021 01:45:06 GMT
EXPOSE 8000 9990
# Tue, 27 Jul 2021 01:45:07 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 27 Jul 2021 01:45:07 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756768e613b962461ed748c6c592c51a096367219fb9ef584991ddff2855c365`  
		Last Modified: Tue, 27 Jul 2021 02:01:30 GMT  
		Size: 481.4 MB (481444307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35560a09851b4869eb9077d299484715452cc273bcf57c697c6c79b0603414a`  
		Last Modified: Tue, 27 Jul 2021 02:00:29 GMT  
		Size: 4.0 MB (3994083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03783b14e1b864a6cf00296d1c770fadf6b45417e41b3deabd04b28d1cff2a1`  
		Last Modified: Tue, 27 Jul 2021 02:00:28 GMT  
		Size: 7.1 MB (7146664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a4f8d472dcc34c99807aa4b3cbcb5f31eef86e9ee22c8b8b2957f5b4bf470e`  
		Last Modified: Tue, 27 Jul 2021 02:00:24 GMT  
		Size: 490.7 KB (490692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2038b33ba67017085fc73e5c446da04b4b66d799c38cc0f7b803ed3a1d6e04d`  
		Last Modified: Tue, 27 Jul 2021 02:00:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0afa3e9b3a33839bd05f759054e2825856277fcf9e71cdd691eda6999957a86`  
		Last Modified: Tue, 27 Jul 2021 02:00:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31be7edd049f9decd08777b9bb28d607378e5321de10288987013178b817032a`  
		Last Modified: Tue, 27 Jul 2021 02:00:33 GMT  
		Size: 190.5 MB (190469421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36aecc1b98a9f2d3600f42e7399319fcd8ad7114aec762a80fdf05bf6a0c6d4b`  
		Last Modified: Tue, 27 Jul 2021 02:00:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080046b0282cc678779a1287e7b0d8fdd3a24b01e0162d5ef04d166a74aaacac`  
		Last Modified: Tue, 27 Jul 2021 02:00:20 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0f81063e0b5aaadaa6feaa58eee7a9d3821d8109ddc92fe74075b30af2aa9`  
		Last Modified: Tue, 27 Jul 2021 02:00:21 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad077e02cc13c100266b92e7c2c6fcd1e13db1be91b5dff3310fabc1af5dd13`  
		Last Modified: Tue, 27 Jul 2021 02:00:56 GMT  
		Size: 716.3 MB (716287292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2.1`

```console
$ docker pull silverpeas@sha256:735790885dae5d2bb97f6cf82d7312c0e9de87022b994c2e8ddcc98d90639bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.1` - linux; amd64

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
