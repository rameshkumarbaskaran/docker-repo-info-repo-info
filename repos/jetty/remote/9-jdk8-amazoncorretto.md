## `jetty:9-jdk8-amazoncorretto`

```console
$ docker pull jetty@sha256:4b7957799c792c3f9c829032988e147c5b845f9f5561815cdb2bec71bf325986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk8-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4848bc21d35e10e183a1c64cf6788fab8cb171838fce1441e55592e408910ce5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153708681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709a7cd049897e847ec93bf69851e850271ac1bd1fdf5bf6f620d5cd34daf08a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Aug 2022 01:19:36 GMT
ADD file:ebfd33425a17b16a9e560de15c91108bf2ee740f284a1482a7105b420ff22678 in / 
# Fri, 26 Aug 2022 01:19:37 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 02:02:55 GMT
ARG version=1.8.0_342.b07-4
# Fri, 26 Aug 2022 02:03:17 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 02:03:18 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 02:03:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 19 Sep 2022 17:19:52 GMT
ENV JETTY_VERSION=9.4.49.v20220914
# Mon, 19 Sep 2022 17:19:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 19 Sep 2022 17:19:52 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 19 Sep 2022 17:19:52 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 19 Sep 2022 17:19:52 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Sep 2022 17:19:52 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.49.v20220914/jetty-home-9.4.49.v20220914.tar.gz
# Mon, 19 Sep 2022 17:19:52 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Mon, 19 Sep 2022 17:20:11 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 19 Sep 2022 17:20:11 GMT
WORKDIR /var/lib/jetty
# Mon, 19 Sep 2022 17:20:11 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Mon, 19 Sep 2022 17:20:11 GMT
USER jetty
# Mon, 19 Sep 2022 17:20:11 GMT
EXPOSE 8080
# Mon, 19 Sep 2022 17:20:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Sep 2022 17:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fd06b60db4951fd95b43a9e73fb084fe7d2afcd4ff464472ead5548cd1c28717`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 62.3 MB (62326701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6626eeeb161e510cb277ee5c8edd4e8c33de2e80145c25c54050fc21e1d357e2`  
		Last Modified: Fri, 26 Aug 2022 02:07:06 GMT  
		Size: 75.6 MB (75579879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba4ca5be05ff34794a3b6607627ff8fd36b5e4ef74e402e59dd11edd861c312`  
		Last Modified: Mon, 19 Sep 2022 17:38:12 GMT  
		Size: 15.8 MB (15800660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237e85a7eef072ad4643c6cf77a16d93eca8ad9260976bff5438f32e495cd6d`  
		Last Modified: Mon, 19 Sep 2022 17:38:10 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk8-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e3c0c7259799faf0c690d47093cd334dbfb3481cbda10cb5a124017e1e2996bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139392264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a625ecb86aaca8aa19a18baa8604c91a585d637e7daa060e556d5cc2b5b7ef90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:01:01 GMT
ARG version=1.8.0_342.b07-4
# Fri, 26 Aug 2022 01:01:18 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:01:18 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:01:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 19 Sep 2022 17:21:04 GMT
ENV JETTY_VERSION=9.4.49.v20220914
# Mon, 19 Sep 2022 17:21:04 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 19 Sep 2022 17:21:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 19 Sep 2022 17:21:06 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 19 Sep 2022 17:21:07 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Sep 2022 17:21:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.49.v20220914/jetty-home-9.4.49.v20220914.tar.gz
# Mon, 19 Sep 2022 17:21:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Mon, 19 Sep 2022 17:21:23 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 19 Sep 2022 17:21:24 GMT
WORKDIR /var/lib/jetty
# Mon, 19 Sep 2022 17:21:26 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Mon, 19 Sep 2022 17:21:26 GMT
USER jetty
# Mon, 19 Sep 2022 17:21:27 GMT
EXPOSE 8080
# Mon, 19 Sep 2022 17:21:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Sep 2022 17:21:29 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851b3384c6fc6a4bb8506747a4edc13e891c8719d6ac5f3e846350bc2080b93b`  
		Last Modified: Fri, 26 Aug 2022 01:03:31 GMT  
		Size: 59.6 MB (59602242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e686eab1d34445b1531af4af073ec087f23e8a1c54f068601968d4ab7d22c5ad`  
		Last Modified: Mon, 19 Sep 2022 17:35:42 GMT  
		Size: 15.8 MB (15849815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4020a07d19d41730fa0bed9b5d4c4a164da7b011ddaef380d3cce3c45ad9faa4`  
		Last Modified: Mon, 19 Sep 2022 17:35:40 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
