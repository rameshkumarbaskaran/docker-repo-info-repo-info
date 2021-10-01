<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.3`](#silverpeas613)
-	[`silverpeas:6.2.1`](#silverpeas621)
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
$ docker pull silverpeas@sha256:5c00c5dcc0488f49fab9cb135abdbfe5869559754aa25e70456f91bc6d4bf225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.1.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:aafc6f12a87115c85b4841089c20d547607aeab5320387fd5a7066a2feac432b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426527378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fd9b83484ffec91ddb6c43842084bdb3088b9e47a9faa9a84bbef28c38c322`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:39:43 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 01 Oct 2021 06:39:43 GMT
ENV TERM=xterm
# Fri, 01 Oct 2021 06:46:35 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 01 Oct 2021 06:46:43 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 01 Oct 2021 06:46:48 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 01 Oct 2021 06:46:48 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 01 Oct 2021 06:46:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 01 Oct 2021 06:46:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Oct 2021 06:46:51 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 01 Oct 2021 06:46:51 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 06:46:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 01 Oct 2021 06:46:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 01 Oct 2021 06:46:53 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 01 Oct 2021 06:46:53 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 01 Oct 2021 06:46:53 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 01 Oct 2021 06:46:54 GMT
ENV SILVERPEAS_VERSION=6.1.3
# Fri, 01 Oct 2021 06:46:54 GMT
ENV WILDFLY_VERSION=18.0.1
# Fri, 01 Oct 2021 06:46:54 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.3 build=1
# Fri, 01 Oct 2021 06:47:06 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 01 Oct 2021 06:47:06 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 01 Oct 2021 06:47:07 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 01 Oct 2021 06:47:07 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Fri, 01 Oct 2021 06:47:07 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 01 Oct 2021 06:49:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 01 Oct 2021 06:49:15 GMT
EXPOSE 8000 9990
# Fri, 01 Oct 2021 06:49:15 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 01 Oct 2021 06:49:16 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce7ee3ef1a33565f839bcf009b3c75d659e9d924e52681bdd1a22da22fdc14a`  
		Last Modified: Fri, 01 Oct 2021 06:52:38 GMT  
		Size: 481.4 MB (481434072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59a7786b48cde3d9ca14992177d08b30380c1d94e3694a1b0762dd835c38613`  
		Last Modified: Fri, 01 Oct 2021 06:51:35 GMT  
		Size: 4.0 MB (3994087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5167bb41abe70ae0b9d3fcbc9d7c75f59b6b2caf59aadf6ee21696c9f496550`  
		Last Modified: Fri, 01 Oct 2021 06:51:35 GMT  
		Size: 7.1 MB (7146659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce84ec10b80deb7767df032ac556c88216eaf15543185e9a5afff3ad6d2b693`  
		Last Modified: Fri, 01 Oct 2021 06:51:32 GMT  
		Size: 490.7 KB (490685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f513859d07e6989fe48216e07bb460687b7c360dc809fb2d7ca8898a2a9cb25`  
		Last Modified: Fri, 01 Oct 2021 06:51:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecbc9d2ad5d663f2af43733e9b0e0bbca75d45eb3f8601fab02b888663e4cae`  
		Last Modified: Fri, 01 Oct 2021 06:51:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6d7beadfe3050a9fb4958f0b53e9ebe6e52b9ac9f0bc5e6b8b7b61785e0f76`  
		Last Modified: Fri, 01 Oct 2021 06:51:42 GMT  
		Size: 190.5 MB (190469435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026d202040a0768bc993914864b06b1b19980098131db9fd1275b4a9816b2bf2`  
		Last Modified: Fri, 01 Oct 2021 06:51:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d252facd361dbc316ffee6430f3327c47f64438bf2b621eab143bab570717635`  
		Last Modified: Fri, 01 Oct 2021 06:51:29 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84e3914595700845c370bbac8e4a3175f8b6645c4d5160fef543d77fe20c303`  
		Last Modified: Fri, 01 Oct 2021 06:51:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150e11337453b8d7a306b9d0332b7e5985fc1ffab7a15b8cf2088db748ca88a`  
		Last Modified: Fri, 01 Oct 2021 06:52:06 GMT  
		Size: 716.3 MB (716285444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2.1`

```console
$ docker pull silverpeas@sha256:d8fdc921cb24863b421544048b4ef46e09cdd1b834060a9e9f589858382d4a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.1` - linux; amd64

```console
$ docker pull silverpeas@sha256:91ffd59123c279c61c363bcf6c295c9c116078563c049ea49f7fadfcfc542c53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1889275877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d260dcce790ab3ff8a7b595c2b840fdd00a8e39af023b6f3d4783f93bcd90`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:29:59 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 01 Oct 2021 06:29:59 GMT
ENV TERM=xterm
# Fri, 01 Oct 2021 06:36:35 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 01 Oct 2021 06:36:41 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 01 Oct 2021 06:36:45 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 01 Oct 2021 06:36:45 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 01 Oct 2021 06:37:26 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 01 Oct 2021 06:37:27 GMT
ENV SILVERPEAS_VERSION=6.2.1
# Fri, 01 Oct 2021 06:37:27 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 01 Oct 2021 06:37:27 GMT
LABEL name=Silverpeas 6.2.1 description=Image to install and to run Silverpeas 6.2.1 vendor=Silverpeas version=6.2.1 build=1
# Fri, 01 Oct 2021 06:37:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 01 Oct 2021 06:37:40 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 01 Oct 2021 06:39:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 01 Oct 2021 06:39:38 GMT
EXPOSE 8000 9990
# Fri, 01 Oct 2021 06:39:39 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 01 Oct 2021 06:39:39 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87657892a756e765471e8d310ef28332c0e5c09f3a236c6429813264c272f644`  
		Last Modified: Fri, 01 Oct 2021 06:51:18 GMT  
		Size: 909.8 MB (909794022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456eb94b3b35c43931270f9dfce05235cbb8497ca0f8b9a4494ad2c3b20b7e20`  
		Last Modified: Fri, 01 Oct 2021 06:49:45 GMT  
		Size: 4.0 MB (3994073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061bd4f0d99eec1e4fe6d9eb7a4b7d861bdeffc3e807429554e09b15dcadcb79`  
		Last Modified: Fri, 01 Oct 2021 06:49:45 GMT  
		Size: 7.1 MB (7146643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8ead08b2c990583db58b9022adf3101f0648111cc47ec47c4e096677c6394`  
		Last Modified: Fri, 01 Oct 2021 06:49:42 GMT  
		Size: 2.5 MB (2534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20078b2f1be999abc507898e00c6fc00cbf5da4b6c6bcbd4450d5b7534f9dd2e`  
		Last Modified: Fri, 01 Oct 2021 06:49:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533fda7bcc54d7b95fb43a0ae6213d95d6e4ac5fe8dd21b551940bd42e9ab5`  
		Last Modified: Fri, 01 Oct 2021 06:49:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0a2a29c322ffd9ef401c8c8778de2270520aa788d7fb1ef36713490acd2ce`  
		Last Modified: Fri, 01 Oct 2021 06:49:54 GMT  
		Size: 196.8 MB (196774119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33a6724f40371d22f055f757341e72bf0bee70392e6382c2dbed8c1de3cba9`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adb8cae6db9f27a420f88916299ff60d5f44ef99adeefbaca99b9a52712ef5`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 662.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e50be5d98446508d079217c657d88f2edf98c5ac204be1c3ae6a66500d469`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22564bb561689c6e69d6a708b33f57c373ae1193e82dc7dc9b8b6973c2a60377`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcdb2a215fe0d386e6cba2feafc648a541812051259f9cb2b2e64b9271538f3`  
		Last Modified: Fri, 01 Oct 2021 06:50:17 GMT  
		Size: 740.5 MB (740461034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:d8fdc921cb24863b421544048b4ef46e09cdd1b834060a9e9f589858382d4a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:91ffd59123c279c61c363bcf6c295c9c116078563c049ea49f7fadfcfc542c53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1889275877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d260dcce790ab3ff8a7b595c2b840fdd00a8e39af023b6f3d4783f93bcd90`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:29:59 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 01 Oct 2021 06:29:59 GMT
ENV TERM=xterm
# Fri, 01 Oct 2021 06:36:35 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 01 Oct 2021 06:36:41 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 01 Oct 2021 06:36:45 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 01 Oct 2021 06:36:45 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:24 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 06:37:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 01 Oct 2021 06:37:26 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 01 Oct 2021 06:37:26 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 01 Oct 2021 06:37:27 GMT
ENV SILVERPEAS_VERSION=6.2.1
# Fri, 01 Oct 2021 06:37:27 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 01 Oct 2021 06:37:27 GMT
LABEL name=Silverpeas 6.2.1 description=Image to install and to run Silverpeas 6.2.1 vendor=Silverpeas version=6.2.1 build=1
# Fri, 01 Oct 2021 06:37:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 01 Oct 2021 06:37:40 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 01 Oct 2021 06:37:40 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 01 Oct 2021 06:39:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 01 Oct 2021 06:39:38 GMT
EXPOSE 8000 9990
# Fri, 01 Oct 2021 06:39:39 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 01 Oct 2021 06:39:39 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87657892a756e765471e8d310ef28332c0e5c09f3a236c6429813264c272f644`  
		Last Modified: Fri, 01 Oct 2021 06:51:18 GMT  
		Size: 909.8 MB (909794022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456eb94b3b35c43931270f9dfce05235cbb8497ca0f8b9a4494ad2c3b20b7e20`  
		Last Modified: Fri, 01 Oct 2021 06:49:45 GMT  
		Size: 4.0 MB (3994073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061bd4f0d99eec1e4fe6d9eb7a4b7d861bdeffc3e807429554e09b15dcadcb79`  
		Last Modified: Fri, 01 Oct 2021 06:49:45 GMT  
		Size: 7.1 MB (7146643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e8ead08b2c990583db58b9022adf3101f0648111cc47ec47c4e096677c6394`  
		Last Modified: Fri, 01 Oct 2021 06:49:42 GMT  
		Size: 2.5 MB (2534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20078b2f1be999abc507898e00c6fc00cbf5da4b6c6bcbd4450d5b7534f9dd2e`  
		Last Modified: Fri, 01 Oct 2021 06:49:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533fda7bcc54d7b95fb43a0ae6213d95d6e4ac5fe8dd21b551940bd42e9ab5`  
		Last Modified: Fri, 01 Oct 2021 06:49:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d0a2a29c322ffd9ef401c8c8778de2270520aa788d7fb1ef36713490acd2ce`  
		Last Modified: Fri, 01 Oct 2021 06:49:54 GMT  
		Size: 196.8 MB (196774119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33a6724f40371d22f055f757341e72bf0bee70392e6382c2dbed8c1de3cba9`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adb8cae6db9f27a420f88916299ff60d5f44ef99adeefbaca99b9a52712ef5`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 662.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e50be5d98446508d079217c657d88f2edf98c5ac204be1c3ae6a66500d469`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22564bb561689c6e69d6a708b33f57c373ae1193e82dc7dc9b8b6973c2a60377`  
		Last Modified: Fri, 01 Oct 2021 06:49:39 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcdb2a215fe0d386e6cba2feafc648a541812051259f9cb2b2e64b9271538f3`  
		Last Modified: Fri, 01 Oct 2021 06:50:17 GMT  
		Size: 740.5 MB (740461034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
