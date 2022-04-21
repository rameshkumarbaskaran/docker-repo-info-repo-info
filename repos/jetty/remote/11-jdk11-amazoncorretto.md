## `jetty:11-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:35924f36740ad2390c98e7a1766d4d9130e2098cc7ff51a433dd7a75e5fe4106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:fa409a5901b35443ac538aaf3007c69d2427c17eb39faa98ece6983eb155b174
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229519508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69e771115e75a98d3f27be160d409dd7b785978cb8bc89e447c4c454b5e9612`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Tue, 19 Apr 2022 22:23:46 GMT
ARG version=11.0.15.9-1
# Tue, 19 Apr 2022 22:24:11 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 19 Apr 2022 22:24:11 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 22:24:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 20 Apr 2022 03:58:12 GMT
ENV JETTY_VERSION=11.0.9
# Wed, 20 Apr 2022 03:58:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 20 Apr 2022 03:58:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 20 Apr 2022 03:58:12 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 20 Apr 2022 03:58:12 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 03:58:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.9/jetty-home-11.0.9.tar.gz
# Wed, 20 Apr 2022 03:58:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 20 Apr 2022 03:58:30 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 20 Apr 2022 03:58:31 GMT
WORKDIR /var/lib/jetty
# Wed, 20 Apr 2022 03:58:31 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 20 Apr 2022 03:58:31 GMT
USER jetty
# Wed, 20 Apr 2022 03:58:31 GMT
EXPOSE 8080
# Wed, 20 Apr 2022 03:58:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 03:58:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc29cbad79c9bc29a9b354015dfe8b079799bd5426b5a8c0f03816c7613e4193`  
		Last Modified: Tue, 19 Apr 2022 22:32:26 GMT  
		Size: 147.0 MB (146964197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e57c542f3315393fdd5b8a66c9b1e39a4faf568cc6bc397787192055cc0f7f6`  
		Last Modified: Wed, 20 Apr 2022 04:07:09 GMT  
		Size: 20.3 MB (20316230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298807725e58cfbd9c100acdb2ae4a0d82a077d9f67c1e100e02c5b67ec91bf1`  
		Last Modified: Wed, 20 Apr 2022 04:07:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:15d8c7b1f8bc38291124e852522c0101f29539d0b26962265078a2d11a198f30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228402681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90713da4ecef0ee49a792a835ba123ad6c6de9a7ebdf762a40727928e115635`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 19 Apr 2022 21:39:43 GMT
ARG version=11.0.15.9-1
# Tue, 19 Apr 2022 21:40:01 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 19 Apr 2022 21:40:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 21:40:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 21 Apr 2022 04:29:39 GMT
ENV JETTY_VERSION=11.0.9
# Thu, 21 Apr 2022 04:29:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 21 Apr 2022 04:29:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 21 Apr 2022 04:29:41 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 21 Apr 2022 04:29:42 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:29:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.9/jetty-home-11.0.9.tar.gz
# Thu, 21 Apr 2022 04:29:44 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 21 Apr 2022 04:29:59 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 21 Apr 2022 04:29:59 GMT
WORKDIR /var/lib/jetty
# Thu, 21 Apr 2022 04:30:01 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 21 Apr 2022 04:30:01 GMT
USER jetty
# Thu, 21 Apr 2022 04:30:02 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:30:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 04:30:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85077095d5a2c473594b77c6d23a963d73bf0a7e6accf188af15b4161ddc8213`  
		Last Modified: Tue, 19 Apr 2022 21:42:31 GMT  
		Size: 144.2 MB (144188940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6c4f2fd49e07fa2ee2cd8f769d8a59188361a5f720d70ce9829033a153021c`  
		Last Modified: Thu, 21 Apr 2022 04:49:15 GMT  
		Size: 20.3 MB (20342019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffea58b3463d959e1f5e9301be1b912b4d6c4e721dd16f45a352e951b94d76`  
		Last Modified: Thu, 21 Apr 2022 04:49:12 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
