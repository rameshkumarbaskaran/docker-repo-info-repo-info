## `jetty:10-jre17-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:078119bac050abb5e05679bcce5e67fd491e35e17f53c215a21f9e0dbe86b03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:10-jre17-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:a6de7656885fb4974c5ccbfd0fccc7c59b815418bcf4238a4521eda47c29b060
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103438bb1f2c4009b318f7696f681c3d367f7977f41a5ef653e70d191458395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 24 May 2023 23:34:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 May 2023 23:34:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 23:34:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 May 2023 23:34:29 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 24 May 2023 23:35:41 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 24 May 2023 23:36:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='711f837bacf8222dee9e8cd7f39941a4a0acf869243f03e6038ca3ba189f66ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 24 May 2023 23:36:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 25 May 2023 00:08:02 GMT
ENV JETTY_VERSION=10.0.15
# Thu, 25 May 2023 00:08:02 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 25 May 2023 00:08:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 25 May 2023 00:08:02 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 25 May 2023 00:08:02 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 May 2023 00:08:02 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Thu, 25 May 2023 00:08:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 25 May 2023 00:08:12 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 25 May 2023 00:08:12 GMT
WORKDIR /var/lib/jetty
# Thu, 25 May 2023 00:08:12 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Thu, 25 May 2023 00:08:12 GMT
USER jetty
# Thu, 25 May 2023 00:08:12 GMT
EXPOSE 8080
# Thu, 25 May 2023 00:08:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 May 2023 00:08:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdde4a302e0d0ee2ef6760bf84344d762835ef2d38d2a1a1062c7d038fe2615b`  
		Last Modified: Wed, 24 May 2023 23:37:36 GMT  
		Size: 7.6 MB (7648427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96558b8a7ae6322ca4951c3b6506ad6e1a3da23ff08e18f2adc6fa5e6624a25`  
		Last Modified: Wed, 24 May 2023 23:39:24 GMT  
		Size: 46.8 MB (46776591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dd25fc4e3af74b54d3e79e13570d951834de7698d73ea49d90834f994c1ca7`  
		Last Modified: Wed, 24 May 2023 23:39:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744581e6b871517e35f19f4d63c5431c6aed8c158bf5a90b687a84462d1366e`  
		Last Modified: Thu, 25 May 2023 00:13:59 GMT  
		Size: 18.5 MB (18484340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61efd27af8764c4c2777602ae13f467ffcd796a82e30a1da89302ba4129960a7`  
		Last Modified: Thu, 25 May 2023 00:13:51 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
