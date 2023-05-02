## `jetty:10-amazoncorretto`

```console
$ docker pull jetty@sha256:55215468df5992e6295e95fa1ef7bb23c7f3adc3d8229ea43f35effddf381610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b0bb63e0808fe7b771f66f578c9ebd25d43914643ec6c285ce5fcae672c1f246
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231286591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c80be9080e96059c6caaf9194a8c47a8640a9b5229064c4fdc539f8705a4b5f`
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
# Tue, 02 May 2023 21:39:37 GMT
ENV JETTY_VERSION=10.0.15
# Tue, 02 May 2023 21:39:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 May 2023 21:39:38 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 May 2023 21:39:38 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 May 2023 21:39:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 21:39:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Tue, 02 May 2023 21:39:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 May 2023 21:39:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 02 May 2023 21:39:55 GMT
WORKDIR /var/lib/jetty
# Tue, 02 May 2023 21:39:55 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Tue, 02 May 2023 21:39:55 GMT
USER jetty
# Tue, 02 May 2023 21:39:55 GMT
EXPOSE 8080
# Tue, 02 May 2023 21:39:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 21:39:56 GMT
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
	-	`sha256:82841b14b18f78267732262c3061df78865ca95c68abaeea7bf05a5572c081be`  
		Last Modified: Tue, 02 May 2023 21:52:24 GMT  
		Size: 16.9 MB (16852012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8068be38ff30e76ef614725e6b32fd4d34316e02b7aa4ecdf8bd83202227bf34`  
		Last Modified: Tue, 02 May 2023 21:52:22 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:a11e487cd97a688649b5506ea96a8a87ee59b156384964024813c89c3ff4ca28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231506535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b451e70d9c4570a831c3c7c2bcfb046d804c0aca2c544e38596decf72184ac`
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
# Tue, 02 May 2023 21:13:05 GMT
ENV JETTY_VERSION=10.0.15
# Tue, 02 May 2023 21:13:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 May 2023 21:13:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 May 2023 21:13:05 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 May 2023 21:13:05 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 May 2023 21:13:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.15/jetty-home-10.0.15.tar.gz
# Tue, 02 May 2023 21:13:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 May 2023 21:13:20 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 02 May 2023 21:13:20 GMT
WORKDIR /var/lib/jetty
# Tue, 02 May 2023 21:13:21 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Tue, 02 May 2023 21:13:21 GMT
USER jetty
# Tue, 02 May 2023 21:13:21 GMT
EXPOSE 8080
# Tue, 02 May 2023 21:13:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 21:13:21 GMT
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
	-	`sha256:4477b97aa0c2677d97e77e8be46f7bb7f9d267d315f15141ee6e163a4927e638`  
		Last Modified: Tue, 02 May 2023 21:20:22 GMT  
		Size: 16.9 MB (16890318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67cb159a3f988cfba04608d26d2c90011c6300ecd934175cbbb57645c8914e2`  
		Last Modified: Tue, 02 May 2023 21:20:20 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
