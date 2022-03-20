<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.3`](#silverpeas613)
-	[`silverpeas:6.2.2`](#silverpeas622)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:b5c9b1df7911d96406247d7fafc0fedda2244be799e6009cfc621ad7be63b0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:0a267954f687c0500c46dfdb31408a6ce073f519d6d94b7d46feb8f752bd7cb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014925313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7219f80b96ae15c804beee33c3e2580723de1295e7a534c385361754e37073`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 02:03:39 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 31 Aug 2021 02:03:39 GMT
ENV TERM=xterm
# Tue, 31 Aug 2021 02:07:33 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 31 Aug 2021 02:07:39 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 31 Aug 2021 02:07:45 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 31 Aug 2021 02:07:45 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 31 Aug 2021 02:07:51 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 31 Aug 2021 02:07:51 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Tue, 31 Aug 2021 02:07:51 GMT
ENV WILDFLY_VERSION=10.1.0
# Tue, 31 Aug 2021 02:07:51 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Tue, 31 Aug 2021 02:08:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Tue, 31 Aug 2021 02:08:10 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 31 Aug 2021 02:15:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Tue, 31 Aug 2021 02:15:32 GMT
EXPOSE 8000 9990
# Tue, 31 Aug 2021 02:15:32 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Tue, 31 Aug 2021 02:15:32 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bab7b2978c6f447f4f11629d5abb18105da46a467b3e7fdad602da38a099a`  
		Last Modified: Tue, 31 Aug 2021 02:19:47 GMT  
		Size: 207.5 MB (207457617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ad3fb77baf164e811362e174b7f55078faddfb5419581e02ee8be4e22c8cb`  
		Last Modified: Tue, 31 Aug 2021 02:19:19 GMT  
		Size: 4.0 MB (3994087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21a02eb15eabcb08194dc549f6d2633401a9f02b70a28c42acfb982a2c0892`  
		Last Modified: Tue, 31 Aug 2021 02:19:19 GMT  
		Size: 7.1 MB (7146644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957309a7c22133ea5da921a9e1c440e5db36c1ef29767922a96d0715144a7f3c`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 845.4 KB (845399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f504f19b2261f336d5fb8ed204508a177d4672a306b41a359f41940d39c67f`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07658715bda815de3e29d8e151f013b1b5ef7fc70e9b567fc532bb8bd19e2c04`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600e097c39adc1a81b28bad70ec252868df7c4824d28038502d09de60f0e340`  
		Last Modified: Tue, 31 Aug 2021 02:19:21 GMT  
		Size: 144.3 MB (144284714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa2533c95124d7f6f1f71e873889eb02fb290464f44877ab8db60dc9c58931f`  
		Last Modified: Tue, 31 Aug 2021 02:19:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a055b4aee299167cc171b4c496a6fa722dc1cafaffba88430008c4671edfd5d6`  
		Last Modified: Tue, 31 Aug 2021 02:19:12 GMT  
		Size: 809.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f3514ac10d9002bc266d0d7d3916e143b49a339e7cc5249b412b4699987d38`  
		Last Modified: Tue, 31 Aug 2021 02:19:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af73964675c4218dd30a52c94723697d58cf2d0cd23cf4a61cb6da0396cf0aa`  
		Last Modified: Tue, 31 Aug 2021 02:19:44 GMT  
		Size: 604.7 MB (604695778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.3`

```console
$ docker pull silverpeas@sha256:e4934da47438c05e50dd7b50db17a7a2915cbd3add7d2e1d792d20928bae8b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.1.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:0e80b932dbc00caff70ab78b77c202993b07b1a2daf39844654e5dc8002c25db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426656582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970e7cc5d0b43bd1ba1be6d7d6b0f2e53a66fcccf346d380f87deedeb636c8bc`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 23:36:53 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 19 Mar 2022 23:36:53 GMT
ENV TERM=xterm
# Sat, 19 Mar 2022 23:42:11 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 19 Mar 2022 23:42:20 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 19 Mar 2022 23:42:25 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 19 Mar 2022 23:42:25 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 19 Mar 2022 23:42:28 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 19 Mar 2022 23:42:28 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 23:42:28 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 19 Mar 2022 23:42:28 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 23:42:28 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 19 Mar 2022 23:42:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 19 Mar 2022 23:42:29 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 19 Mar 2022 23:42:29 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 19 Mar 2022 23:42:29 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 19 Mar 2022 23:42:29 GMT
ENV SILVERPEAS_VERSION=6.1.3
# Sat, 19 Mar 2022 23:42:29 GMT
ENV WILDFLY_VERSION=18.0.1
# Sat, 19 Mar 2022 23:42:29 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.3 build=1
# Sat, 19 Mar 2022 23:43:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 19 Mar 2022 23:43:51 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 19 Mar 2022 23:43:51 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 19 Mar 2022 23:43:51 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Sat, 19 Mar 2022 23:43:51 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 19 Mar 2022 23:46:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 19 Mar 2022 23:46:51 GMT
EXPOSE 8000 9990
# Sat, 19 Mar 2022 23:46:51 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 19 Mar 2022 23:46:51 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfd7d192e873f767b757b6b57594f6b7cefaaf9d9abb6f632e6238ac2a7ab79`  
		Last Modified: Sat, 19 Mar 2022 23:50:08 GMT  
		Size: 481.6 MB (481559556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f27642a84cc6120255c592ff40c801db5509d95659e264a3f2d406fe362bd52`  
		Last Modified: Sat, 19 Mar 2022 23:49:05 GMT  
		Size: 4.0 MB (3994083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550182e2ebb75dcd899d678e364a39a273e92a46d5a337003fb171e089eda3df`  
		Last Modified: Sat, 19 Mar 2022 23:49:05 GMT  
		Size: 7.1 MB (7146668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6b730a7586676d6bb9c8a84f2cc8e5234fe60930ba36439569c543894b3ae`  
		Last Modified: Sat, 19 Mar 2022 23:49:02 GMT  
		Size: 490.7 KB (490687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd87860fd3254d336b4806335c5a7d93b5215ea6c8505fc93a35d54bbb050f2`  
		Last Modified: Sat, 19 Mar 2022 23:49:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826aa849acf96287704939d0c8f04ecb7e2cfb969bd8a9d548f6b26809197ff`  
		Last Modified: Sat, 19 Mar 2022 23:49:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d078fd67a74fc267a5bd494fb198f533c7d9dd883cc8099403768e58846232`  
		Last Modified: Sat, 19 Mar 2022 23:49:11 GMT  
		Size: 190.5 MB (190469457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be58a7973a12e47f2d58a82066bc5b4a5b0acdddf7f18b14d0033f27e1d9dc2`  
		Last Modified: Sat, 19 Mar 2022 23:48:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c9b441f704a8943f62fe6693007b7630aeefd1e906c99494f4a8c30a496a0e`  
		Last Modified: Sat, 19 Mar 2022 23:48:59 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e3d52bd1a23227afffba6151f12d6ed14e7fe0d1552b189fb325d2bbc36e7`  
		Last Modified: Sat, 19 Mar 2022 23:48:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ecde63025f18ca98dc02cbf4f7f5ded4d248f5293117988c5440d6774f47fd`  
		Last Modified: Sat, 19 Mar 2022 23:49:35 GMT  
		Size: 716.3 MB (716285573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2.2`

```console
$ docker pull silverpeas@sha256:d2e80f608c14f63dafdba57fd4f1831f31605fff530ca074de97803e366db93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:0b50871087bcc600206d7812015716545c8fdd4d3177ad4acab1ca78482de737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900001695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c6cd948ac8ede9998f17d727ef5b90ec866e8da580d85b890404b73856952e`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 23:25:15 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 19 Mar 2022 23:25:15 GMT
ENV TERM=xterm
# Sat, 19 Mar 2022 23:32:06 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 19 Mar 2022 23:32:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 19 Mar 2022 23:32:17 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 19 Mar 2022 23:32:17 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 19 Mar 2022 23:32:57 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 19 Mar 2022 23:32:57 GMT
ENV SILVERPEAS_VERSION=6.2.2
# Sat, 19 Mar 2022 23:32:57 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 19 Mar 2022 23:32:57 GMT
LABEL name=Silverpeas 6.2.2 description=Image to install and to run Silverpeas 6.2.2 vendor=Silverpeas version=6.2.2 build=1
# Sat, 19 Mar 2022 23:33:45 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 19 Mar 2022 23:33:46 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 19 Mar 2022 23:36:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 19 Mar 2022 23:36:47 GMT
EXPOSE 8000 9990
# Sat, 19 Mar 2022 23:36:48 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 19 Mar 2022 23:36:48 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d523c11b4a9fcc50b1253f0fb444fda88e1b2506d27eea94a70aa8061150d2d`  
		Last Modified: Sat, 19 Mar 2022 23:48:49 GMT  
		Size: 913.0 MB (912961860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148bf542e8433c85c649b0812b9fea57dac845877eb57e63caaec6fd85678335`  
		Last Modified: Sat, 19 Mar 2022 23:47:15 GMT  
		Size: 4.0 MB (3994071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2098d9ca45a9c6f0f7c8340316e4ed3c7faef4a57426609bc1457a66aca23e`  
		Last Modified: Sat, 19 Mar 2022 23:47:16 GMT  
		Size: 7.1 MB (7146641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7764851c80fc9af9d6fc9990c5b862f6a6b1eda502c50e6f099158634e925ee`  
		Last Modified: Sat, 19 Mar 2022 23:47:13 GMT  
		Size: 2.5 MB (2534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0a396ed4a241f9823a12e69975e995c5ae864ee5ba71e80242016fa9b22c14`  
		Last Modified: Sat, 19 Mar 2022 23:47:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae337a85949e458273b7794d2805af98608a5c53c817b45864f1f2ef80f471`  
		Last Modified: Sat, 19 Mar 2022 23:47:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7127e5629eef4554b58b3ea8a7d2cfd89d7344473ad83c639ba9ff0176e47`  
		Last Modified: Sat, 19 Mar 2022 23:47:25 GMT  
		Size: 196.8 MB (196774068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7646f8e20ff8f5dd3545cc1e189d0e31a37931590ff21500878d86dee9d53e0`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b171c6f7ef56b510a2827e325bc97a5ccc35e5fdac5aef6f2e564cdd11a8ce3`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab9a1c7e5081736a60919be63a0401cbffbf86268f6ccf0e5ac25650612fc3`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c38c3363c4090aeb713752310cf4a30f0fcc09de764f778796ccdd85636bc6`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730270cef94659564bcadacce536af90a58b61e8cb8eaff13ee7ac8c1ab1a971`  
		Last Modified: Sat, 19 Mar 2022 23:47:48 GMT  
		Size: 748.0 MB (748022080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:d2e80f608c14f63dafdba57fd4f1831f31605fff530ca074de97803e366db93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:0b50871087bcc600206d7812015716545c8fdd4d3177ad4acab1ca78482de737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900001695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c6cd948ac8ede9998f17d727ef5b90ec866e8da580d85b890404b73856952e`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 23:25:15 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 19 Mar 2022 23:25:15 GMT
ENV TERM=xterm
# Sat, 19 Mar 2022 23:32:06 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 19 Mar 2022 23:32:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 19 Mar 2022 23:32:17 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 19 Mar 2022 23:32:17 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:55 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 23:32:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 19 Mar 2022 23:32:56 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 19 Mar 2022 23:32:57 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 19 Mar 2022 23:32:57 GMT
ENV SILVERPEAS_VERSION=6.2.2
# Sat, 19 Mar 2022 23:32:57 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 19 Mar 2022 23:32:57 GMT
LABEL name=Silverpeas 6.2.2 description=Image to install and to run Silverpeas 6.2.2 vendor=Silverpeas version=6.2.2 build=1
# Sat, 19 Mar 2022 23:33:45 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 19 Mar 2022 23:33:46 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 19 Mar 2022 23:33:46 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 19 Mar 2022 23:36:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 19 Mar 2022 23:36:47 GMT
EXPOSE 8000 9990
# Sat, 19 Mar 2022 23:36:48 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 19 Mar 2022 23:36:48 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d523c11b4a9fcc50b1253f0fb444fda88e1b2506d27eea94a70aa8061150d2d`  
		Last Modified: Sat, 19 Mar 2022 23:48:49 GMT  
		Size: 913.0 MB (912961860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148bf542e8433c85c649b0812b9fea57dac845877eb57e63caaec6fd85678335`  
		Last Modified: Sat, 19 Mar 2022 23:47:15 GMT  
		Size: 4.0 MB (3994071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2098d9ca45a9c6f0f7c8340316e4ed3c7faef4a57426609bc1457a66aca23e`  
		Last Modified: Sat, 19 Mar 2022 23:47:16 GMT  
		Size: 7.1 MB (7146641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7764851c80fc9af9d6fc9990c5b862f6a6b1eda502c50e6f099158634e925ee`  
		Last Modified: Sat, 19 Mar 2022 23:47:13 GMT  
		Size: 2.5 MB (2534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0a396ed4a241f9823a12e69975e995c5ae864ee5ba71e80242016fa9b22c14`  
		Last Modified: Sat, 19 Mar 2022 23:47:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae337a85949e458273b7794d2805af98608a5c53c817b45864f1f2ef80f471`  
		Last Modified: Sat, 19 Mar 2022 23:47:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7127e5629eef4554b58b3ea8a7d2cfd89d7344473ad83c639ba9ff0176e47`  
		Last Modified: Sat, 19 Mar 2022 23:47:25 GMT  
		Size: 196.8 MB (196774068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7646f8e20ff8f5dd3545cc1e189d0e31a37931590ff21500878d86dee9d53e0`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b171c6f7ef56b510a2827e325bc97a5ccc35e5fdac5aef6f2e564cdd11a8ce3`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab9a1c7e5081736a60919be63a0401cbffbf86268f6ccf0e5ac25650612fc3`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c38c3363c4090aeb713752310cf4a30f0fcc09de764f778796ccdd85636bc6`  
		Last Modified: Sat, 19 Mar 2022 23:47:10 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730270cef94659564bcadacce536af90a58b61e8cb8eaff13ee7ac8c1ab1a971`  
		Last Modified: Sat, 19 Mar 2022 23:47:48 GMT  
		Size: 748.0 MB (748022080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
