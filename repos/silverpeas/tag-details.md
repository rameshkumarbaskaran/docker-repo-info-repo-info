<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.2`](#silverpeas612)
-	[`silverpeas:6.2`](#silverpeas62)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:29ed7eae5dc43acfa523e1e3ba4b7c3f05ee1afe5c51df33b687fc5163610cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:4eadf6433f6de177596a34be08edee6caf4119fe9f8917d23991c0fac884fc3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014326899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251d43938a6d4266f3ed4fa429f6104ab26bc30b19a900d7d4ec9a77bc211775`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:02:56 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 26 Mar 2021 16:02:56 GMT
ENV TERM=xterm
# Fri, 26 Mar 2021 16:06:52 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 26 Mar 2021 16:06:57 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 26 Mar 2021 16:07:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 26 Mar 2021 16:07:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 26 Mar 2021 16:07:04 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 26 Mar 2021 16:07:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Mar 2021 16:07:04 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 26 Mar 2021 16:07:04 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 26 Mar 2021 16:07:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 26 Mar 2021 16:07:06 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 26 Mar 2021 16:07:06 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 26 Mar 2021 16:07:07 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 26 Mar 2021 16:07:07 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 26 Mar 2021 16:07:07 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Fri, 26 Mar 2021 16:07:07 GMT
ENV WILDFLY_VERSION=10.1.0
# Fri, 26 Mar 2021 16:07:07 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Fri, 26 Mar 2021 16:07:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 26 Mar 2021 16:07:22 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Fri, 26 Mar 2021 16:07:22 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 26 Mar 2021 16:07:23 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Fri, 26 Mar 2021 16:07:23 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 26 Mar 2021 16:13:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Fri, 26 Mar 2021 16:13:38 GMT
EXPOSE 8000 9990
# Fri, 26 Mar 2021 16:13:38 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Fri, 26 Mar 2021 16:13:38 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4312eb35e036b0f2cf662aeb9a776b8c4b7c2e74ce8ea9f264669c917f8465`  
		Last Modified: Fri, 26 Mar 2021 16:20:07 GMT  
		Size: 207.4 MB (207394534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93b9acf8412235c484546f4491d83ac6d7b29303cc4323788d4878131860eda`  
		Last Modified: Fri, 26 Mar 2021 16:19:33 GMT  
		Size: 4.0 MB (3994092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca01d0e5a61c433e744af917bd1ea87ef15bb91787052a1d3956d64070da61ff`  
		Last Modified: Fri, 26 Mar 2021 16:19:34 GMT  
		Size: 7.1 MB (7146648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c21bb57513b6fd8fb8c2dae816d318469b6d6f65451a6c3b1999d2a7afbd62d`  
		Last Modified: Fri, 26 Mar 2021 16:19:30 GMT  
		Size: 845.4 KB (845411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d825aeebd42399ee1f1374a9bd4eae7cf06fdcf73f85abd6023f51352c56b854`  
		Last Modified: Fri, 26 Mar 2021 16:19:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aea347a6678602a961f8cdcdfcd25b7aebb37937abb37352522cadb96ec12d`  
		Last Modified: Fri, 26 Mar 2021 16:19:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d2828a332467e269311a4083cba227c494ac0eba88dc333aa1a1b8435e9887`  
		Last Modified: Fri, 26 Mar 2021 16:19:41 GMT  
		Size: 144.3 MB (144284718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a271b4c46c056d377c8d0418efc51b286ee61a525deca602a80aea3f1f65496`  
		Last Modified: Fri, 26 Mar 2021 16:19:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2ff5be4354e12a966ad325834ad990b35db5505c801400dc5521ce64e1b6c8`  
		Last Modified: Fri, 26 Mar 2021 16:19:26 GMT  
		Size: 809.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca67ac550d1090968409453a7b52827ada7df3625966d524dda34aeec852fa30`  
		Last Modified: Fri, 26 Mar 2021 16:19:26 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7610b0d6493c9cf64dce78695d28eb42c260719ee2f4f1fd80ffe558cda85b`  
		Last Modified: Fri, 26 Mar 2021 16:20:05 GMT  
		Size: 604.7 MB (604695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.2`

```console
$ docker pull silverpeas@sha256:b4d73164a3cb29fe7a5f2580c9109a5d1a83c3781745bcc8f45d6eda846ebac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.1.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:7110791e4e808c55f01708be3ac802c486f270e88d4ea6a2e9805fc9ba0e7933
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426676467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47275f8ea59b1270db692b1c7418db3b355dff317c49822a76a2896d7b3bb5f`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 15:50:55 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 26 Mar 2021 15:50:55 GMT
ENV TERM=xterm
# Fri, 26 Mar 2021 15:59:02 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 26 Mar 2021 15:59:07 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 26 Mar 2021 15:59:12 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 26 Mar 2021 15:59:13 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 26 Mar 2021 15:59:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 26 Mar 2021 15:59:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Mar 2021 15:59:19 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 26 Mar 2021 15:59:19 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 26 Mar 2021 15:59:21 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 26 Mar 2021 15:59:23 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 26 Mar 2021 15:59:23 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 26 Mar 2021 15:59:24 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 26 Mar 2021 15:59:24 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 26 Mar 2021 15:59:24 GMT
ENV SILVERPEAS_VERSION=6.1.2
# Fri, 26 Mar 2021 15:59:24 GMT
ENV WILDFLY_VERSION=18.0.1
# Fri, 26 Mar 2021 15:59:25 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.2 build=1
# Fri, 26 Mar 2021 16:00:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 26 Mar 2021 16:00:10 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 26 Mar 2021 16:00:10 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 26 Mar 2021 16:00:11 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Fri, 26 Mar 2021 16:00:11 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 26 Mar 2021 16:02:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 26 Mar 2021 16:02:39 GMT
EXPOSE 8000 9990
# Fri, 26 Mar 2021 16:02:39 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 26 Mar 2021 16:02:40 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c13327cc2f8248bc8c879294e75b80ff22b035d5ae864b03fe11fbf5157e69`  
		Last Modified: Fri, 26 Mar 2021 16:19:17 GMT  
		Size: 481.6 MB (481586708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539f457ca9bcdc4fe69b60b09b6491fc82aa8515aad9c358151f1ab010cc9cb`  
		Last Modified: Fri, 26 Mar 2021 16:17:27 GMT  
		Size: 4.0 MB (3994090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44229316ab9a5e2b9d8c52a7dcf40a3a022a38833f4c4c59cc0b6b36978e91d7`  
		Last Modified: Fri, 26 Mar 2021 16:17:31 GMT  
		Size: 7.1 MB (7146656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b809203ef0414deb9172e72646714f45b6dfe87bc67168bf2d575cf188fedf46`  
		Last Modified: Fri, 26 Mar 2021 16:17:22 GMT  
		Size: 490.7 KB (490695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d16bf2cdc20c30fed6f4be2f24783180110cf605d958e4bce1107fde7ffe1a`  
		Last Modified: Fri, 26 Mar 2021 16:17:22 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fea6fa2bbd473bf20157f0025e2dce2a74dac3af0ce192242c05b4292b2fbad`  
		Last Modified: Fri, 26 Mar 2021 16:17:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca98d1063007b0216facd0dde01f414b0cbd6d2ae4c7ca81dcd3db22a850556`  
		Last Modified: Fri, 26 Mar 2021 16:17:48 GMT  
		Size: 190.5 MB (190469424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4c9314c9a0e8e52cbb6f7d30007585a05facac17e6dabeb7a1c5b938aebe9`  
		Last Modified: Fri, 26 Mar 2021 16:17:19 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ec926909e7a582fedc729e87f4fc41d038ee64064f4810325231704e9413b0`  
		Last Modified: Fri, 26 Mar 2021 16:17:19 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741445dc87f0bc5c8cd42c55a8a13e66a121b39970230c735e6ddcb66a148964`  
		Last Modified: Fri, 26 Mar 2021 16:17:19 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa95fe5418b013045fc94aac315e5d41931af013dfc6a0a57b15b1c325c7e37`  
		Last Modified: Fri, 26 Mar 2021 16:18:40 GMT  
		Size: 716.3 MB (716275150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2`

```console
$ docker pull silverpeas@sha256:b634327d743d37aca860656e77dd72d05ba5d36c2428b9e86cfbdd72d73c1912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:bd7adea54d72addabaa2777f58f9055341076f29742b181d7a956004339f5703
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865910839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f065f6ac66a975f673a383ef9bb2b95bbab042c5ec3c9e055cac60d79ef6c782`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 02:49:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 03 Apr 2021 02:49:10 GMT
ENV TERM=xterm
# Sat, 03 Apr 2021 02:55:46 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 03 Apr 2021 02:55:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 03 Apr 2021 02:55:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 03 Apr 2021 02:55:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 03 Apr 2021 02:56:36 GMT
ENV LANG=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:36 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:37 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 03 Apr 2021 02:56:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 03 Apr 2021 02:56:39 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 03 Apr 2021 02:56:39 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 03 Apr 2021 02:56:39 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 03 Apr 2021 02:56:39 GMT
ENV SILVERPEAS_VERSION=6.2
# Sat, 03 Apr 2021 02:56:39 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 03 Apr 2021 02:56:40 GMT
LABEL name=Silverpeas 6.2 description=Image to install and to run Silverpeas 6.2 vendor=Silverpeas version=6.2 build=1
# Sat, 03 Apr 2021 02:56:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 03 Apr 2021 02:56:56 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 03 Apr 2021 02:56:56 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 03 Apr 2021 02:56:56 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 03 Apr 2021 02:56:57 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 03 Apr 2021 02:56:57 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 03 Apr 2021 02:59:40 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 03 Apr 2021 02:59:43 GMT
EXPOSE 8000 9990
# Sat, 03 Apr 2021 02:59:43 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 03 Apr 2021 02:59:43 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef219aa901abee2afcfdd8795ff2bbdcd551383f7918302b02b3325334aeca7`  
		Last Modified: Sat, 03 Apr 2021 03:01:55 GMT  
		Size: 904.9 MB (904938708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf429164ec0e1b64a8766d8127ede8f1bc63b09326cdf24305c6c80b37694035`  
		Last Modified: Sat, 03 Apr 2021 03:00:14 GMT  
		Size: 4.0 MB (3994069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea6448a7b44d7eed626c4cc2ddeec92911a4e0d1907d0f8151e76a39fde75b3`  
		Last Modified: Sat, 03 Apr 2021 03:00:14 GMT  
		Size: 7.1 MB (7146637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a4e9644e7d857d44266a4a05b4d0a77e9f22ffadd3bc530992986e9cfb226b`  
		Last Modified: Sat, 03 Apr 2021 03:00:11 GMT  
		Size: 2.5 MB (2534357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16d42d196d36f1823743a4b58ed9a87a1b4a912024f2de8bf0942e9952bf4bb`  
		Last Modified: Sat, 03 Apr 2021 03:00:10 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5742117c35dfcb279f4223d895a0d6afc61d45e2ab8a244ec93d076d8ed97864`  
		Last Modified: Sat, 03 Apr 2021 03:00:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b126a5474bb8c3d788147fb38eec3e588f32a101adf49e446f9c5c998e9c7`  
		Last Modified: Sat, 03 Apr 2021 03:00:24 GMT  
		Size: 196.8 MB (196774049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26dae82dae51213e9eb40ae554fd687af2b4617c9b78511c1addaeda05b44d8`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf31578d3024b65375859ff1035236ca7e7119da001cacb1a2417223b2de989`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59243664ebeb231b2a1325fab97167552012f57c0f56727568e020e037110d06`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8d2fd5a00544519bd41bf964653e899f66ff63440af9992aacc4d637d7a72`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c33eba9fcbae9e15c4633f3406f9b02ec3ba5570ba6303f2347a51ca89ce490`  
		Last Modified: Sat, 03 Apr 2021 03:00:47 GMT  
		Size: 722.0 MB (721950265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:b634327d743d37aca860656e77dd72d05ba5d36c2428b9e86cfbdd72d73c1912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:bd7adea54d72addabaa2777f58f9055341076f29742b181d7a956004339f5703
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865910839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f065f6ac66a975f673a383ef9bb2b95bbab042c5ec3c9e055cac60d79ef6c782`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 02:49:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 03 Apr 2021 02:49:10 GMT
ENV TERM=xterm
# Sat, 03 Apr 2021 02:55:46 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 03 Apr 2021 02:55:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 03 Apr 2021 02:55:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 03 Apr 2021 02:55:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 03 Apr 2021 02:56:36 GMT
ENV LANG=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:36 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:37 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 02:56:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 03 Apr 2021 02:56:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 03 Apr 2021 02:56:39 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 03 Apr 2021 02:56:39 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 03 Apr 2021 02:56:39 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 03 Apr 2021 02:56:39 GMT
ENV SILVERPEAS_VERSION=6.2
# Sat, 03 Apr 2021 02:56:39 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 03 Apr 2021 02:56:40 GMT
LABEL name=Silverpeas 6.2 description=Image to install and to run Silverpeas 6.2 vendor=Silverpeas version=6.2 build=1
# Sat, 03 Apr 2021 02:56:55 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 03 Apr 2021 02:56:56 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 03 Apr 2021 02:56:56 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 03 Apr 2021 02:56:56 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 03 Apr 2021 02:56:57 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 03 Apr 2021 02:56:57 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 03 Apr 2021 02:59:40 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 03 Apr 2021 02:59:43 GMT
EXPOSE 8000 9990
# Sat, 03 Apr 2021 02:59:43 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 03 Apr 2021 02:59:43 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef219aa901abee2afcfdd8795ff2bbdcd551383f7918302b02b3325334aeca7`  
		Last Modified: Sat, 03 Apr 2021 03:01:55 GMT  
		Size: 904.9 MB (904938708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf429164ec0e1b64a8766d8127ede8f1bc63b09326cdf24305c6c80b37694035`  
		Last Modified: Sat, 03 Apr 2021 03:00:14 GMT  
		Size: 4.0 MB (3994069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea6448a7b44d7eed626c4cc2ddeec92911a4e0d1907d0f8151e76a39fde75b3`  
		Last Modified: Sat, 03 Apr 2021 03:00:14 GMT  
		Size: 7.1 MB (7146637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a4e9644e7d857d44266a4a05b4d0a77e9f22ffadd3bc530992986e9cfb226b`  
		Last Modified: Sat, 03 Apr 2021 03:00:11 GMT  
		Size: 2.5 MB (2534357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16d42d196d36f1823743a4b58ed9a87a1b4a912024f2de8bf0942e9952bf4bb`  
		Last Modified: Sat, 03 Apr 2021 03:00:10 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5742117c35dfcb279f4223d895a0d6afc61d45e2ab8a244ec93d076d8ed97864`  
		Last Modified: Sat, 03 Apr 2021 03:00:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b126a5474bb8c3d788147fb38eec3e588f32a101adf49e446f9c5c998e9c7`  
		Last Modified: Sat, 03 Apr 2021 03:00:24 GMT  
		Size: 196.8 MB (196774049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26dae82dae51213e9eb40ae554fd687af2b4617c9b78511c1addaeda05b44d8`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf31578d3024b65375859ff1035236ca7e7119da001cacb1a2417223b2de989`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59243664ebeb231b2a1325fab97167552012f57c0f56727568e020e037110d06`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8d2fd5a00544519bd41bf964653e899f66ff63440af9992aacc4d637d7a72`  
		Last Modified: Sat, 03 Apr 2021 03:00:07 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c33eba9fcbae9e15c4633f3406f9b02ec3ba5570ba6303f2347a51ca89ce490`  
		Last Modified: Sat, 03 Apr 2021 03:00:47 GMT  
		Size: 722.0 MB (721950265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
