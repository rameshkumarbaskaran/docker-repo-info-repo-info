## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:90d462c59a311e94647ec139f8dc40e8ff25b895fd3b6eaec2c255589c0ab07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:4aae6b9f0a60aa41f748d3459f9d3b74404e3e4097f8a30fd38656928808a551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225577017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b320973f9eced4251f5602d0011254720bf6c01e7c3e14ae06beaad5d61ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Aug 2022 01:19:36 GMT
ADD file:ebfd33425a17b16a9e560de15c91108bf2ee740f284a1482a7105b420ff22678 in / 
# Fri, 26 Aug 2022 01:19:37 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 02:03:37 GMT
ARG version=11.0.16.9-1
# Fri, 26 Aug 2022 02:04:01 GMT
# ARGS: version=11.0.16.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 02:04:02 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 02:04:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 19 Sep 2022 17:21:07 GMT
ENV JETTY_VERSION=9.4.49.v20220914
# Mon, 19 Sep 2022 17:21:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 19 Sep 2022 17:21:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 19 Sep 2022 17:21:07 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 19 Sep 2022 17:21:08 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Sep 2022 17:21:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.49.v20220914/jetty-home-9.4.49.v20220914.tar.gz
# Mon, 19 Sep 2022 17:21:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Mon, 19 Sep 2022 17:21:26 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 19 Sep 2022 17:21:26 GMT
WORKDIR /var/lib/jetty
# Mon, 19 Sep 2022 17:21:26 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Mon, 19 Sep 2022 17:21:26 GMT
USER jetty
# Mon, 19 Sep 2022 17:21:26 GMT
EXPOSE 8080
# Mon, 19 Sep 2022 17:21:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Sep 2022 17:21:26 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:fd06b60db4951fd95b43a9e73fb084fe7d2afcd4ff464472ead5548cd1c28717`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 62.3 MB (62326701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e806ef017442d9e0f611cb049e442935f8b228820877e1239ddba2e048b634`  
		Last Modified: Fri, 26 Aug 2022 02:07:46 GMT  
		Size: 147.4 MB (147449724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c835ada5919969547e7b81170864f983ccc36206c1db7a639e054b35499ac6`  
		Last Modified: Mon, 19 Sep 2022 17:39:12 GMT  
		Size: 15.8 MB (15799151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5611b5747232ac223a2d22dc18b7528311f4cad166f7be4ee8518821bb75a9`  
		Last Modified: Mon, 19 Sep 2022 17:39:11 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:1c6e21bbed8920c1136a6f716f3291d214b963f3a18dc50323aa5bb266f3d2a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224353712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a409661ff7b0e008916025f17a676fd6ded5f97e52689077e8009983958f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:01:26 GMT
ARG version=11.0.16.9-1
# Fri, 26 Aug 2022 01:01:39 GMT
# ARGS: version=11.0.16.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:01:40 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:01:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 19 Sep 2022 17:22:07 GMT
ENV JETTY_VERSION=9.4.49.v20220914
# Mon, 19 Sep 2022 17:22:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 19 Sep 2022 17:22:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 19 Sep 2022 17:22:09 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 19 Sep 2022 17:22:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Sep 2022 17:22:11 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.49.v20220914/jetty-home-9.4.49.v20220914.tar.gz
# Mon, 19 Sep 2022 17:22:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Mon, 19 Sep 2022 17:22:27 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 19 Sep 2022 17:22:27 GMT
WORKDIR /var/lib/jetty
# Mon, 19 Sep 2022 17:22:29 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Mon, 19 Sep 2022 17:22:29 GMT
USER jetty
# Mon, 19 Sep 2022 17:22:30 GMT
EXPOSE 8080
# Mon, 19 Sep 2022 17:22:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Sep 2022 17:22:32 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb91a4547e1bb6153357482beae6fd003894417903c684578e4fb0ebaeeab0`  
		Last Modified: Fri, 26 Aug 2022 01:04:09 GMT  
		Size: 144.6 MB (144573734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce22a921cc9bb4868d55df54b5d95f14510f85709dce3e0585faf89dd578f5c2`  
		Last Modified: Mon, 19 Sep 2022 17:36:21 GMT  
		Size: 15.8 MB (15839771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dbdafe2011284eac9dc5e78fe68061acf1ffa51f42965d557a2ce8f37d7749`  
		Last Modified: Mon, 19 Sep 2022 17:36:19 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
