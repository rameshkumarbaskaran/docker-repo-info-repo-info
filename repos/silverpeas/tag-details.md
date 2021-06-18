<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.3`](#silverpeas613)
-	[`silverpeas:6.2.1`](#silverpeas621)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:f969484de3c9739d5145664ee2265f3c00cdf6b72e5072378ada903ef31e5f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:5ef70de7fc5a8fda4e5d262f376ff12910393ce2781d18e4d9242af56aae3290
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014923558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0fe5773c74c481da9d067b2704504c16970645e4811b68998709a398c7e990`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 02:55:45 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 18 Jun 2021 02:55:45 GMT
ENV TERM=xterm
# Fri, 18 Jun 2021 02:59:23 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 18 Jun 2021 02:59:28 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 18 Jun 2021 02:59:32 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 18 Jun 2021 02:59:32 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 18 Jun 2021 02:59:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 18 Jun 2021 02:59:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 18 Jun 2021 02:59:35 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 18 Jun 2021 02:59:36 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 02:59:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 18 Jun 2021 02:59:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 18 Jun 2021 02:59:38 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 18 Jun 2021 02:59:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 18 Jun 2021 02:59:38 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 18 Jun 2021 02:59:38 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Fri, 18 Jun 2021 02:59:38 GMT
ENV WILDFLY_VERSION=10.1.0
# Fri, 18 Jun 2021 02:59:39 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Fri, 18 Jun 2021 02:59:58 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 18 Jun 2021 02:59:58 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Fri, 18 Jun 2021 02:59:59 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 18 Jun 2021 02:59:59 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Fri, 18 Jun 2021 02:59:59 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 18 Jun 2021 03:06:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Fri, 18 Jun 2021 03:06:12 GMT
EXPOSE 8000 9990
# Fri, 18 Jun 2021 03:06:13 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Fri, 18 Jun 2021 03:06:13 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d118cc87cf52b53fd1b3cc141ba7bc9121397b185294b0db53a34fe042cea46`  
		Last Modified: Fri, 18 Jun 2021 03:10:31 GMT  
		Size: 207.5 MB (207456151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd04fe4e7236586c978be3fde6fd719b689cf08b556f2e8511a0cfa79cad0656`  
		Last Modified: Fri, 18 Jun 2021 03:10:01 GMT  
		Size: 4.0 MB (3994089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61518036d758e4c58f3f64a744a7e103ed43dd58b352b98d22120ba59214d56`  
		Last Modified: Fri, 18 Jun 2021 03:10:02 GMT  
		Size: 7.1 MB (7146655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c0bc726ebb4d9dfdb54ae20a7cee96ef7954c1a23b58263fbdebb4b9f9380`  
		Last Modified: Fri, 18 Jun 2021 03:09:58 GMT  
		Size: 845.4 KB (845434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacea640ec8e66d314408263d553fd43643718425452f6273767e4d11c214ab2`  
		Last Modified: Fri, 18 Jun 2021 03:09:57 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81a4402d3b510f1d06e07480bb916c6b9155135326ceba80a2809eaf05258b9`  
		Last Modified: Fri, 18 Jun 2021 03:09:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7444b2257cc2c7f47eacca62722621663ce633ef2b2660eb86446ecfc22164`  
		Last Modified: Fri, 18 Jun 2021 03:10:05 GMT  
		Size: 144.3 MB (144284706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e82ed5277996b2db7fcb8a0a3e28b61224969b0b06c10b9499d018c2f017f3`  
		Last Modified: Fri, 18 Jun 2021 03:09:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4a42f00372f9d9efa4aca5b32df4821dec543ea52f2080d82a992def118833`  
		Last Modified: Fri, 18 Jun 2021 03:09:55 GMT  
		Size: 808.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6810f19321b9c4ae821e603e830a58a5e7a255498b231b26e7a433d42e408`  
		Last Modified: Fri, 18 Jun 2021 03:09:55 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c3adf0b3119b138f9a1b5e2a9948e70da9fac4977ef0219c7da2093338889e`  
		Last Modified: Fri, 18 Jun 2021 03:10:28 GMT  
		Size: 604.7 MB (604696226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.3`

```console
$ docker pull silverpeas@sha256:f54ab3fe9f2b36cb1f5c8dc24cd7e90c99a1601c8eea663348d8c0c39e514318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.1.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:32a9fe416208122b4f73427c9b969e3418ba7902d7cced2ecab4daca652a13b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426533829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13f7bebc980ecb84ac10e87470728f8817fc2ec72a862f8e638200f3e1f64f5`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:45:46 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 18 Jun 2021 02:45:46 GMT
ENV TERM=xterm
# Fri, 18 Jun 2021 02:52:50 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 18 Jun 2021 02:52:55 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 18 Jun 2021 02:52:58 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 18 Jun 2021 02:52:59 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 18 Jun 2021 02:53:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 18 Jun 2021 02:53:02 GMT
ENV LANG=en_US.UTF-8
# Fri, 18 Jun 2021 02:53:02 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 18 Jun 2021 02:53:02 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 02:53:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 18 Jun 2021 02:53:04 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 18 Jun 2021 02:53:04 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 18 Jun 2021 02:53:05 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 18 Jun 2021 02:53:05 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 18 Jun 2021 02:53:05 GMT
ENV SILVERPEAS_VERSION=6.1.3
# Fri, 18 Jun 2021 02:53:05 GMT
ENV WILDFLY_VERSION=18.0.1
# Fri, 18 Jun 2021 02:53:05 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.3 build=1
# Fri, 18 Jun 2021 02:53:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 18 Jun 2021 02:53:33 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 18 Jun 2021 02:53:33 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 18 Jun 2021 02:53:34 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Fri, 18 Jun 2021 02:53:34 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 18 Jun 2021 02:55:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 18 Jun 2021 02:55:38 GMT
EXPOSE 8000 9990
# Fri, 18 Jun 2021 02:55:39 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 18 Jun 2021 02:55:39 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec616fe36a1737d4df782723191d8700de8bdafa2a8cc96580d343fdc9a5150d`  
		Last Modified: Fri, 18 Jun 2021 03:09:47 GMT  
		Size: 481.4 MB (481444761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab93068a8b378c023f0a04166e6b4ee23595737bef0ae0e4b9df0c591ada9a`  
		Last Modified: Fri, 18 Jun 2021 03:08:40 GMT  
		Size: 4.0 MB (3994087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4cb6c28e4a841d12b09017a4ca0f99e0cde5b2772968fd69392ebfd5f706eb`  
		Last Modified: Fri, 18 Jun 2021 03:08:41 GMT  
		Size: 7.1 MB (7146666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda4bf1bd0126ed78b81c2cafacd37c48fb7e6575187de0aea40b56e84d7f1d5`  
		Last Modified: Fri, 18 Jun 2021 03:08:37 GMT  
		Size: 490.7 KB (490688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a673db9efddaac66c586437b07c41747943a25038fd23a7d2164f1041bebe0b`  
		Last Modified: Fri, 18 Jun 2021 03:08:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0930eb776b5eeb737b35c6e06c58da22c686f9b8361c5211375ebb124c22c0c9`  
		Last Modified: Fri, 18 Jun 2021 03:08:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c56596d28cf1036780e4b32a7fa0cc2e7a58ff1e05ce6aebb3a82f77b4da741`  
		Last Modified: Fri, 18 Jun 2021 03:08:47 GMT  
		Size: 190.5 MB (190469426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249fe5e70a295d8d176cbea430965b1e13cb7aad8df422943c986d7f19817752`  
		Last Modified: Fri, 18 Jun 2021 03:08:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33f647910409eea1f06d2f2dcebf8a1a5fd28f703e0357345e53cc7d4dcda6c`  
		Last Modified: Fri, 18 Jun 2021 03:08:33 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16adf1cdbafafd71b7824c1cda5ce6848671ff9deb9884bf562824768cd62f3e`  
		Last Modified: Fri, 18 Jun 2021 03:08:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea880cef1676c9fd689b125281b6cf150e33df9b9c6214faa8ed432009b62d1`  
		Last Modified: Fri, 18 Jun 2021 03:09:12 GMT  
		Size: 716.3 MB (716285579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2.1`

```console
$ docker pull silverpeas@sha256:9642ca80ead6dafb94d418a4ec751647e1bd82e0614dc979c1b56f5c35349d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.2.1` - linux; amd64

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
