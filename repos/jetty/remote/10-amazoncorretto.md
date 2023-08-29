## `jetty:10-amazoncorretto`

```console
$ docker pull jetty@sha256:b122bf2c31277c39ca2aa59047e9c46b9053fa6bea22bdd82adb35e686dc538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:a106771e7c76809599db8cb71188583c05ab0d87815d8ef895b91a1a0b96a048
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231472359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72c1d87af88e41ee937a023c41e3943797adc554b650a00696775d97db5ed37`
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
# Tue, 29 Aug 2023 20:37:27 GMT
ENV JETTY_VERSION=10.0.15
# Tue, 29 Aug 2023 20:37:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 20:37:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 20:37:27 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 20:37:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 20:37:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Tue, 29 Aug 2023 20:37:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 20:37:45 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 20:37:45 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 20:37:45 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 20:37:45 GMT
USER jetty
# Tue, 29 Aug 2023 20:37:45 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 20:37:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 20:37:45 GMT
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
	-	`sha256:8651baeca2b6a34d3691659d1998c3733fa03c7a89997e9f4a987ce14227d24e`  
		Last Modified: Tue, 29 Aug 2023 20:42:12 GMT  
		Size: 16.9 MB (16857918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9859a43cc93c53aa686c2e9eaea252644dbe25857755b281461670a02e398d`  
		Last Modified: Tue, 29 Aug 2023 20:42:10 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:429a085eae9d213253687037e8ad128693667f97a9496d07d8e24e15a6071d74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231664375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef2c3e9ba443514132154ff78a272ac1c67c5514a8d0684a4b2d00e1e416813`
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
# Tue, 29 Aug 2023 19:55:42 GMT
ENV JETTY_VERSION=10.0.15
# Tue, 29 Aug 2023 19:55:42 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 19:55:42 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 19:55:42 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 19:55:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 19:55:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Tue, 29 Aug 2023 19:55:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 19:55:57 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 19:55:57 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 19:55:57 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 19:55:57 GMT
USER jetty
# Tue, 29 Aug 2023 19:55:57 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 19:55:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 19:55:57 GMT
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
	-	`sha256:57c752d236c962128954c31f7736e7eebcc4fcbae4bfdf965485e1e6c45261ea`  
		Last Modified: Tue, 29 Aug 2023 19:59:09 GMT  
		Size: 16.9 MB (16875210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d2758405d9bec7d44b80e5eee077bfddc28525b78b8ab4385668998422d46`  
		Last Modified: Tue, 29 Aug 2023 19:59:08 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
