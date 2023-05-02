## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:ac7d66f50d53d8813f8cf8f35a828a90fbf7cdbd359ed93bd6727a7a2ce61c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:859cce64d99b9a778f7bc1bbd603bb9e7208ec4a0dfd4bf4c570a0954662079e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234787239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88abe0aca4854969d4c2c9f4efcc716dc42db8d1d31a85547e066ce4dfbbca6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:51 GMT
COPY dir:d74df4759bcd6e2619baa3ec354d8703c77c836345c6a887554df76aaf1d9965 in / 
# Tue, 28 Mar 2023 18:20:52 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 18:23:27 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 18:23:51 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Apr 2023 18:23:52 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:23:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 02 May 2023 21:38:22 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 02 May 2023 21:38:22 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 May 2023 21:38:22 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 May 2023 21:38:22 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 May 2023 21:38:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 21:38:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 02 May 2023 21:38:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 May 2023 21:38:42 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 02 May 2023 21:38:42 GMT
WORKDIR /var/lib/jetty
# Tue, 02 May 2023 21:38:42 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Tue, 02 May 2023 21:38:42 GMT
USER jetty
# Tue, 02 May 2023 21:38:42 GMT
EXPOSE 8080
# Tue, 02 May 2023 21:38:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 21:38:42 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:128d54f2c9b134270b406c5f3a41296da7c1111d3a6927f0b4451131d636151e`  
		Last Modified: Thu, 23 Mar 2023 21:24:22 GMT  
		Size: 62.5 MB (62483466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e31014b690dd2ee54ea3b7a7bd92073be9fb2dbac3c4274c71a7e30facd6e0`  
		Last Modified: Thu, 20 Apr 2023 18:34:30 GMT  
		Size: 151.9 MB (151949564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f64ef1b938ec10c911ef3933249b45e564f04dae0f40ba92e2b5dd768884cba`  
		Last Modified: Tue, 02 May 2023 21:51:32 GMT  
		Size: 20.4 MB (20352661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802dbf3c0b847919fab0e1c9c7cec71a060deade9ae01f514eb6247caf24d368`  
		Last Modified: Tue, 02 May 2023 21:51:30 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:35f10f1feace70e015f61637bb71ea42b88faf714056ffafc6c1a857def3ef21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235004975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6404a6f3fdb73bcfd09a8b690b62b0aacc48ed5467e4060de393656e5969079`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:42:46 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 17:43:06 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Apr 2023 17:43:08 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:43:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 02 May 2023 21:12:26 GMT
ENV JETTY_VERSION=11.0.15
# Tue, 02 May 2023 21:12:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 May 2023 21:12:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 May 2023 21:12:27 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 May 2023 21:12:27 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 21:12:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Tue, 02 May 2023 21:12:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 May 2023 21:12:43 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 02 May 2023 21:12:44 GMT
WORKDIR /var/lib/jetty
# Tue, 02 May 2023 21:12:44 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Tue, 02 May 2023 21:12:44 GMT
USER jetty
# Tue, 02 May 2023 21:12:44 GMT
EXPOSE 8080
# Tue, 02 May 2023 21:12:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 21:12:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d5f25839cc5d9c044ea00ba0de0880e3272fc9e31ae1d800e809913883f78b`  
		Last Modified: Thu, 20 Apr 2023 17:53:14 GMT  
		Size: 150.5 MB (150487733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10677c9657e5f813aea25ada4069c0b0963f26c8a3abc0305a2d79c768c6f8be`  
		Last Modified: Tue, 02 May 2023 21:19:52 GMT  
		Size: 20.4 MB (20388757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8935b0eddbb876fd8973085dfa02a0a00d9dd221dda2c83d8d2e997ef425b7`  
		Last Modified: Tue, 02 May 2023 21:19:50 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
