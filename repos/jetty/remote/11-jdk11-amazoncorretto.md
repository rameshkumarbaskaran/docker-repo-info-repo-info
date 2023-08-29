## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:a1dda2daecd3a4dfc6d984205b9dee6ebd423af9d8889679a3dc9e4bb0cba8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:36cd10fd4c1f0ab0f9f4eafd6fb0784d235196421c7bdf0f242fc61c7d78e8b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230652824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5077757c8fd43197792c31cecb54e5fd85d5bdbef346217c5449ad1e64b069d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:41:57 GMT
ARG version=11.0.20.8-1
# Tue, 29 Aug 2023 19:42:20 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:42:21 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:42:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 29 Aug 2023 20:37:00 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 29 Aug 2023 20:37:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 20:37:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 20:37:00 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 20:37:00 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 20:37:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 29 Aug 2023 20:37:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 20:37:18 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 20:37:18 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 20:37:18 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 20:37:18 GMT
USER jetty
# Tue, 29 Aug 2023 20:37:18 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 20:37:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 20:37:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b86d24ecba67f2366bd89e5f22da6764ffd5527b8d86528eedde3330169058`  
		Last Modified: Tue, 29 Aug 2023 19:54:08 GMT  
		Size: 147.8 MB (147814313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8610961a8489eaf627c7183c73985e075afce402b219214ee0232f78d941bf99`  
		Last Modified: Tue, 29 Aug 2023 20:41:59 GMT  
		Size: 20.4 MB (20359615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f81cd0194c5fb804abd6a9b600b9f86367c442ecdfc991cae1d682ad9989461`  
		Last Modified: Tue, 29 Aug 2023 20:41:57 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:462126d57836a1b56be5774ff6711ab8995090370f6d87a868498abb120ae995
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229435833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7f91bc47d80e1b8cd6dac5eac8f4bb7260c0319fffc676886c8b7faf586617`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:08:04 GMT
ARG version=11.0.20.8-1
# Tue, 29 Aug 2023 19:08:31 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:08:32 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:08:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 29 Aug 2023 19:55:22 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 29 Aug 2023 19:55:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 29 Aug 2023 19:55:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 29 Aug 2023 19:55:23 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 29 Aug 2023 19:55:23 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Aug 2023 19:55:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 29 Aug 2023 19:55:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 29 Aug 2023 19:55:37 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 29 Aug 2023 19:55:37 GMT
WORKDIR /var/lib/jetty
# Tue, 29 Aug 2023 19:55:37 GMT
COPY multi:c035c96b7cca9122192288f871d2dc7a498e238bc45c278b47f6654057232d72 in / 
# Tue, 29 Aug 2023 19:55:37 GMT
USER jetty
# Tue, 29 Aug 2023 19:55:38 GMT
EXPOSE 8080
# Tue, 29 Aug 2023 19:55:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Aug 2023 19:55:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d7ea691a3e2667be4ac79aeac0b4834afd7282f70bee4fdf803317294f4aca`  
		Last Modified: Tue, 29 Aug 2023 19:17:54 GMT  
		Size: 144.9 MB (144929935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bfb491ea1aabeaf280c05b78205cd142cffe6509dc46c2f29511572e5f56a6`  
		Last Modified: Tue, 29 Aug 2023 19:58:56 GMT  
		Size: 20.4 MB (20374285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895a3d7514663cebb18672e58bc92fc4c8591c06fa98f0aa0d871e8bb17f4dd6`  
		Last Modified: Tue, 29 Aug 2023 19:58:55 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
