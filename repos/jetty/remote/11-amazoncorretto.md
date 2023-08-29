## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:1715c63fedbd81a10e784e50550e966acca1485a2e8860ca8da5829b1aec3330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:1d4debd53d0e270f6cff55ab2f7205349da9cdcc04c324e01ada387b606d7c68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234966820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f14e5ed998a21b4db70f223e25dba53efa8db616299f446528b66414f1e0598`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:45:23 GMT
ARG version=17.0.8.7-1
# Tue, 29 Aug 2023 19:45:50 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:45:50 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:45:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 29 Aug 2023 20:36:33 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 29 Aug 2023 20:36:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 20:36:33 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 20:36:33 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 20:36:33 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 20:36:33 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 29 Aug 2023 20:36:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 20:36:51 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 20:36:51 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 20:36:51 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 20:36:51 GMT
USER jetty
# Tue, 29 Aug 2023 20:36:51 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 20:36:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 20:36:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf577b444ef591d0124f2a5bce176bb15a4d2d53dfe2a924554daf91396e0e8d`  
		Last Modified: Tue, 29 Aug 2023 19:56:24 GMT  
		Size: 152.1 MB (152135545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a122811441b1eabadcd4f821b6df1d64a9149da66e2694b67a450073de93d6a`  
		Last Modified: Tue, 29 Aug 2023 20:41:41 GMT  
		Size: 20.4 MB (20352379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38683ae5c515efd0e56bb68016a2c9f7ca7366d1e0beb00fa29e2d91963374f`  
		Last Modified: Tue, 29 Aug 2023 20:41:39 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:8d34b130af113ba8411750473a8bf47cd3d9ca67b2bf4468b1e9332319d39755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235158376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e50997c8b7766d853e6d1a8d2f249a6b6760c4b9056a3b6c529df062343708e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:10:58 GMT
ARG version=17.0.8.7-1
# Tue, 29 Aug 2023 19:11:19 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:11:21 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 29 Aug 2023 19:55:03 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 29 Aug 2023 19:55:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 19:55:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 19:55:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 19:55:03 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 19:55:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 29 Aug 2023 19:55:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 19:55:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 19:55:18 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 19:55:18 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 19:55:18 GMT
USER jetty
# Tue, 29 Aug 2023 19:55:18 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 19:55:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 19:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a99ef9c0dfbb2dfa6857b9c1caa283aa7ef47c19d2067c443afc1690fda8c1e`  
		Last Modified: Tue, 29 Aug 2023 19:19:59 GMT  
		Size: 150.7 MB (150657552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b247f0191fd719026f558f41127a8cd3230d90074858ab41f4231e8cc436bd`  
		Last Modified: Tue, 29 Aug 2023 19:58:40 GMT  
		Size: 20.4 MB (20369212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ec5cf5327f73c491d563e82b1cd28e90aa40e469a94ecb7176ca5cc2bf618`  
		Last Modified: Tue, 29 Aug 2023 19:58:38 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
