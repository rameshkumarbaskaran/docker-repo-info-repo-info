## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:e4ed4d7010791c0abed51e01f60750a81576aa03e421a31b4a983aa3e82d7d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:51f8cd6d5e40c7e7aa75275dae8e8b548b4a20b413da702c1e1210a6f6174fd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230604432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015b7cee24f94f8564cbbb619908d998101abf090a5bee543ea43af967d78de0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 07 Aug 2023 19:59:12 GMT
COPY dir:a1cfeec8f9b5a4b857222f4bbc7f5fb80ef351168a5f48841d4545523a0a3e1c in / 
# Mon, 07 Aug 2023 19:59:13 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:52:28 GMT
ARG version=11.0.20.8-1
# Mon, 07 Aug 2023 20:52:50 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:52:51 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:52:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 07 Aug 2023 22:32:34 GMT
ENV JETTY_VERSION=11.0.15
# Mon, 07 Aug 2023 22:32:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 07 Aug 2023 22:32:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 07 Aug 2023 22:32:34 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 07 Aug 2023 22:32:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 22:32:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Mon, 07 Aug 2023 22:32:35 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 07 Aug 2023 22:32:52 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 07 Aug 2023 22:32:52 GMT
WORKDIR /var/lib/jetty
# Mon, 07 Aug 2023 22:32:52 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 07 Aug 2023 22:32:52 GMT
USER jetty
# Mon, 07 Aug 2023 22:32:52 GMT
EXPOSE 8080
# Mon, 07 Aug 2023 22:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Aug 2023 22:32:52 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c0184eb4a5d5dddba3605f9adcde7e4af58050e9e4ed44751e74957c2ad0f1b4`  
		Last Modified: Tue, 01 Aug 2023 21:03:56 GMT  
		Size: 62.5 MB (62467383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2479941f1565ecbb6cb9f7e72f6162f0f8a143fd3413e39c4f97636588d2a672`  
		Last Modified: Mon, 07 Aug 2023 21:04:23 GMT  
		Size: 147.8 MB (147800657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a72611fe21041553e0d9208193100ec6728a662463a45f4ddf53f6c7ebc9e5`  
		Last Modified: Mon, 07 Aug 2023 22:37:31 GMT  
		Size: 20.3 MB (20334779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3417b2ac59d0568e430dc8c4b9c75c13f30652540eeb75e3dc473afc4bcfc911`  
		Last Modified: Mon, 07 Aug 2023 22:37:29 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:cf3823b123f3ac420260910465a9c01a39d5750181a64ad3e611c3fdafcd59bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229435418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f0bb8fbd6794891e6f3f745dc1569621e1ef10e454b3f3bfe1ef356b8f881`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 07 Aug 2023 19:40:56 GMT
COPY dir:95dabd7a234aac70a826a1e3c0eafa3928b0be72717af1dea469f66b7db891d5 in / 
# Mon, 07 Aug 2023 19:40:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 20:23:42 GMT
ARG version=11.0.20.8-1
# Mon, 07 Aug 2023 20:24:00 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 07 Aug 2023 20:24:01 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:24:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 07 Aug 2023 21:33:49 GMT
ENV JETTY_VERSION=11.0.15
# Mon, 07 Aug 2023 21:33:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 07 Aug 2023 21:33:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 07 Aug 2023 21:33:49 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 07 Aug 2023 21:33:49 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 21:33:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.15/jetty-home-11.0.15.tar.gz
# Mon, 07 Aug 2023 21:33:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Mon, 07 Aug 2023 21:34:04 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 07 Aug 2023 21:34:04 GMT
WORKDIR /var/lib/jetty
# Mon, 07 Aug 2023 21:34:04 GMT
COPY multi:88ca540b9901ef22d614e919524f1d550a54166ea9880b0aa9695f8e0470c8f7 in / 
# Mon, 07 Aug 2023 21:34:04 GMT
USER jetty
# Mon, 07 Aug 2023 21:34:04 GMT
EXPOSE 8080
# Mon, 07 Aug 2023 21:34:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Aug 2023 21:34:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c3b5a1e75067e9d540ad8d844cad5a291a8cce89e1a3ed8e0f362a5736d3030c`  
		Last Modified: Wed, 02 Aug 2023 19:26:38 GMT  
		Size: 64.1 MB (64129548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a3a0d07b4307c3095a31a5157ca518dac44b2308ce7275f0882fb067b50449`  
		Last Modified: Mon, 07 Aug 2023 20:37:14 GMT  
		Size: 144.9 MB (144929977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb8e2b768d0ea2030d7428373e88df89e6e6342a9555f13b255f153012fb37b`  
		Last Modified: Mon, 07 Aug 2023 21:37:38 GMT  
		Size: 20.4 MB (20374282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c6f4a426e58ecfc4ee631334bd49708ef9a1f4ceb4f470a8a40aa0ab4e98fd`  
		Last Modified: Mon, 07 Aug 2023 21:37:35 GMT  
		Size: 1.6 KB (1611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
