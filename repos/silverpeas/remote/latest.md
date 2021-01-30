## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:77bdf3ee0d0ef12710d3f85549fb1bbc194dc9248a63c4d4c622a277450988d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:c265766a296947e1d520a3257facfec237d3f97ec3765473d7195e4f095f0b2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875237250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87144512d347fd6cb6e4c240a0dd5cf4b51a715f2cf7a81668d513aab4003f4b`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Sat, 30 Jan 2021 02:41:07 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 30 Jan 2021 02:41:07 GMT
ENV TERM=xterm
# Sat, 30 Jan 2021 02:47:50 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 30 Jan 2021 02:47:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 30 Jan 2021 02:47:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 30 Jan 2021 02:47:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 30 Jan 2021 02:48:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 30 Jan 2021 02:48:42 GMT
ENV LANG=en_US.UTF-8
# Sat, 30 Jan 2021 02:48:42 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 30 Jan 2021 02:48:42 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 30 Jan 2021 02:48:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 30 Jan 2021 02:48:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 30 Jan 2021 02:48:44 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 30 Jan 2021 02:48:44 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 30 Jan 2021 02:48:45 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 30 Jan 2021 02:48:45 GMT
ENV SILVERPEAS_VERSION=6.2
# Sat, 30 Jan 2021 02:48:45 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 30 Jan 2021 02:48:45 GMT
LABEL name=Silverpeas 6.2 description=Image to install and to run Silverpeas 6.2 vendor=Silverpeas version=6.2 build=1
# Sat, 30 Jan 2021 02:48:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 30 Jan 2021 02:48:55 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 30 Jan 2021 02:48:55 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 30 Jan 2021 02:48:55 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 30 Jan 2021 02:48:55 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 30 Jan 2021 02:48:56 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 30 Jan 2021 02:50:47 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 30 Jan 2021 02:50:47 GMT
EXPOSE 8000 9990
# Sat, 30 Jan 2021 02:50:48 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 30 Jan 2021 02:50:48 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dec8e696a81b5781b58b5736ab5b682b638f56b99ba176fd69f5bb3406f02fe`  
		Last Modified: Sat, 30 Jan 2021 02:55:17 GMT  
		Size: 914.3 MB (914265663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e198577ef8af69ff5cbab687daa169641466c9bfb1ecdaef604ef60a9239f979`  
		Last Modified: Sat, 30 Jan 2021 02:53:18 GMT  
		Size: 4.0 MB (3994005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58557ca5362ee0881636d00b1283375d81f56722fa7468504f04947ddfae2738`  
		Last Modified: Sat, 30 Jan 2021 02:53:18 GMT  
		Size: 7.1 MB (7146632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a013d002e8fc3f1ea8f8163136dd79b575e5e3b3b42de2d5ff2d1002452ba3e3`  
		Last Modified: Sat, 30 Jan 2021 02:53:15 GMT  
		Size: 2.5 MB (2534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1006da743bef5cbc5d72b23679d701faa936f38109e12b387bb7dea0f3352632`  
		Last Modified: Sat, 30 Jan 2021 02:53:15 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6fe2307501536e3a26d4b4b74d7ca3cff7f2771dd8d536ad5852d85199fd81`  
		Last Modified: Sat, 30 Jan 2021 02:53:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3842b955a3710ca0a8e355c73ded14e3a7351ec1768e30e4458c99d0c285db`  
		Last Modified: Sat, 30 Jan 2021 02:53:32 GMT  
		Size: 196.8 MB (196773971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d90905dd0be998752a9d4221309440a9f410f1f7bc3d518e559c43704af92b`  
		Last Modified: Sat, 30 Jan 2021 02:53:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6fb6714b0b151429492c481c1830619a3a6f53481d1706945842abb21d8776`  
		Last Modified: Sat, 30 Jan 2021 02:53:13 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84112f717a5322ff3ff266ab0748439ae2eceedc50c6b2966ed13ff49fcb318`  
		Last Modified: Sat, 30 Jan 2021 02:53:13 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f683d11fed5617e5b359a923962ebdd9a3a8d83455423438d18dcbb9d8be77a2`  
		Last Modified: Sat, 30 Jan 2021 02:53:13 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1680e1846ebe2d65a2890a0c7d1690c0a1d636e306120dccd5df2173985c3f39`  
		Last Modified: Sat, 30 Jan 2021 02:53:59 GMT  
		Size: 722.0 MB (721953013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
