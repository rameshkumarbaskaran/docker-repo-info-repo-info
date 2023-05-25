## `jetty:10-jre11-alpine-eclipse-temurin`

```console
$ docker pull jetty@sha256:94355774b632d11d4d4bcf4ff7633445872b8e1104b2edf7e4afb2d05ef6005d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:10-jre11-alpine-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:ae4f2d30e3368901b853273020700d51fcf1696b20463eeb2991951dc4f28d37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72661032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91954a5b9278b62a3225a3fed071785f40e6d46d2a1da7072edd58da7b417ce9`
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
# Wed, 24 May 2023 23:35:01 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 24 May 2023 23:35:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5d71cdf3032040e7d2a577712bf525e32e87686af3430219308a39878b98851';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 24 May 2023 23:35:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 25 May 2023 00:08:18 GMT
ENV JETTY_VERSION=10.0.15
# Thu, 25 May 2023 00:08:18 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 25 May 2023 00:08:18 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 25 May 2023 00:08:18 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 25 May 2023 00:08:18 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 May 2023 00:08:18 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Thu, 25 May 2023 00:08:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 25 May 2023 00:08:28 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 25 May 2023 00:08:28 GMT
WORKDIR /var/lib/jetty
# Thu, 25 May 2023 00:08:28 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Thu, 25 May 2023 00:08:28 GMT
USER jetty
# Thu, 25 May 2023 00:08:28 GMT
EXPOSE 8080
# Thu, 25 May 2023 00:08:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 May 2023 00:08:28 GMT
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
	-	`sha256:e366c2606994b8cef810a9d612454c46ba5ec35e2e87f9dbb8b98b58e66a18de`  
		Last Modified: Wed, 24 May 2023 23:38:38 GMT  
		Size: 43.1 MB (43129007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28965099d3b84bf210f9f81b09ee5f4971a3c02a42787d6c5316cd7d0256fadb`  
		Last Modified: Wed, 24 May 2023 23:38:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02344d023593b4a20f8e564aedf9d0b65d626d6b8a08c8e3fe2d9d275ccff0df`  
		Last Modified: Thu, 25 May 2023 00:14:18 GMT  
		Size: 18.5 MB (18484334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f590653c8fc027d4222c2aef43e321417c350a2986d88635ed1731d0248e8383`  
		Last Modified: Thu, 25 May 2023 00:14:16 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
