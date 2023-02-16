## `jetty:11-amazoncorretto`

```console
$ docker pull jetty@sha256:07e8cc6eb97949c7d076963fac85f0867ae6b0b516997b97e57909c450c1d9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:195e3591bc827b0d68cbb937c255538196512377bd37b718ca82e66254b67197
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234682679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e18824b022e4421a05214bcc48817941b7e1b66e0807370d36a37eba8a0d592`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 26 Jan 2023 22:20:04 GMT
ADD file:6ebab25a4f1aa82238dbf1a48f38d22c6421052d0d158cf88cbc1a4d01b5c5c1 in / 
# Thu, 26 Jan 2023 22:20:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 23:10:07 GMT
ARG version=17.0.6.10-1
# Thu, 26 Jan 2023 23:10:31 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 26 Jan 2023 23:10:32 GMT
ENV LANG=C.UTF-8
# Thu, 26 Jan 2023 23:10:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 26 Jan 2023 23:50:56 GMT
ENV JETTY_VERSION=11.0.13
# Thu, 26 Jan 2023 23:50:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 26 Jan 2023 23:50:56 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 26 Jan 2023 23:50:56 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 26 Jan 2023 23:50:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Jan 2023 23:50:56 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.13/jetty-home-11.0.13.tar.gz
# Thu, 26 Jan 2023 23:50:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 26 Jan 2023 23:51:15 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 26 Jan 2023 23:51:15 GMT
WORKDIR /var/lib/jetty
# Thu, 26 Jan 2023 23:51:15 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 26 Jan 2023 23:51:16 GMT
USER jetty
# Thu, 26 Jan 2023 23:51:16 GMT
EXPOSE 8080
# Thu, 26 Jan 2023 23:51:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Jan 2023 23:51:16 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1e78b99dd1fd1031c6513834c4b5f594fa3cec5d06cdeb4b65ee104180bc0d4c`  
		Last Modified: Thu, 26 Jan 2023 20:44:53 GMT  
		Size: 62.3 MB (62341068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfd36dfebc232a4f5bf45dbc71ccf768dfdaaac49a08bfd23f83263014fa104`  
		Last Modified: Thu, 26 Jan 2023 23:14:31 GMT  
		Size: 151.9 MB (151945242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13e4412babc41e30220c2d4cffaa616c4d3398ead40a9008bd0ca195c33089`  
		Last Modified: Thu, 26 Jan 2023 23:57:39 GMT  
		Size: 20.4 MB (20394929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532726eb764f84ed9b3459910accd4a8032cabe3a4ea1ae088edc51d76384ea7`  
		Last Modified: Thu, 26 Jan 2023 23:57:38 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:e2c0ae9e3d803abfd02716fdfe206d0bb0c79d5b663beb64844e6d05446b2d4f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234934824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342153ffc396332126712a9ecc9bb751c5c74b256fd59136a69e5ba9fc69964c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:06:20 GMT
ARG version=17.0.6.10-1
# Thu, 16 Feb 2023 21:06:40 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:06:41 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:06:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 16 Feb 2023 21:26:37 GMT
ENV JETTY_VERSION=11.0.13
# Thu, 16 Feb 2023 21:26:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 16 Feb 2023 21:26:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 16 Feb 2023 21:26:38 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 16 Feb 2023 21:26:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Feb 2023 21:26:38 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.13/jetty-home-11.0.13.tar.gz
# Thu, 16 Feb 2023 21:26:38 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 16 Feb 2023 21:26:54 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 16 Feb 2023 21:26:54 GMT
WORKDIR /var/lib/jetty
# Thu, 16 Feb 2023 21:26:54 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 16 Feb 2023 21:26:54 GMT
USER jetty
# Thu, 16 Feb 2023 21:26:54 GMT
EXPOSE 8080
# Thu, 16 Feb 2023 21:26:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Feb 2023 21:26:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf92e0a1fa9ebe43f0891ead56b5607927ddacca583cd73c0f3ac9d22bfd5278`  
		Last Modified: Thu, 16 Feb 2023 21:08:51 GMT  
		Size: 150.5 MB (150490421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94168f85c25af98f55582096dc82c16723d470a2bea04a732777dff028356b17`  
		Last Modified: Thu, 16 Feb 2023 21:31:21 GMT  
		Size: 20.4 MB (20439157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdfc6fb30486a920a8791f45c3af5f0151fa6f7a13a49ff5720642072fe217c`  
		Last Modified: Thu, 16 Feb 2023 21:31:19 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
