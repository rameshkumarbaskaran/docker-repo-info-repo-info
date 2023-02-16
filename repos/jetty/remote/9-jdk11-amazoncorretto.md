## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:124e35e04ec00a58a88d5c0ba09b5540265a761a899d6d5906a1780f8a37cd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:b64bc0d348af4ec20728dc3551f25821cb605baed92a1bfbf806f100ffd70357
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225941037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a867a1c6ccd38a01c05052a805b11e8a53e333512df3635c85b482f73d304ebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 26 Jan 2023 22:20:04 GMT
ADD file:6ebab25a4f1aa82238dbf1a48f38d22c6421052d0d158cf88cbc1a4d01b5c5c1 in / 
# Thu, 26 Jan 2023 22:20:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 23:09:27 GMT
ARG version=11.0.18.10-1
# Thu, 26 Jan 2023 23:09:50 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 26 Jan 2023 23:09:50 GMT
ENV LANG=C.UTF-8
# Thu, 26 Jan 2023 23:09:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 26 Jan 2023 23:50:31 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Thu, 26 Jan 2023 23:50:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 26 Jan 2023 23:50:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 26 Jan 2023 23:50:31 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 26 Jan 2023 23:50:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Jan 2023 23:50:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Thu, 26 Jan 2023 23:50:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 26 Jan 2023 23:50:49 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 26 Jan 2023 23:50:49 GMT
WORKDIR /var/lib/jetty
# Thu, 26 Jan 2023 23:50:49 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 26 Jan 2023 23:50:49 GMT
USER jetty
# Thu, 26 Jan 2023 23:50:50 GMT
EXPOSE 8080
# Thu, 26 Jan 2023 23:50:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Jan 2023 23:50:50 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1e78b99dd1fd1031c6513834c4b5f594fa3cec5d06cdeb4b65ee104180bc0d4c`  
		Last Modified: Thu, 26 Jan 2023 20:44:53 GMT  
		Size: 62.3 MB (62341068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c1044cf5aac0391975a9b7b11734d75476d2d947b8388a9b7023c77207e04`  
		Last Modified: Thu, 26 Jan 2023 23:13:53 GMT  
		Size: 147.8 MB (147783275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6e499eba5526c3c0880a2a13519aa0b9d4e36a49b7f27c4a641197bb2196ce`  
		Last Modified: Thu, 26 Jan 2023 23:57:27 GMT  
		Size: 15.8 MB (15815254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d514967cb0e6cc58dc1b2dca6afe89e5ee496001faa720f758d2895d434d32`  
		Last Modified: Thu, 26 Jan 2023 23:57:25 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:5e30327c9901cb862a0b0a02d84da71a8784e1c37ea9e3e904fe321cb7e12fcd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224837816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b9c94ca7592c4ea59e200fc967aff380865985a72ac9e76cd3a0f992439d61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:05:47 GMT
ARG version=11.0.18.10-1
# Thu, 16 Feb 2023 21:06:07 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:06:08 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:06:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 16 Feb 2023 21:26:16 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Thu, 16 Feb 2023 21:26:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 16 Feb 2023 21:26:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 16 Feb 2023 21:26:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 16 Feb 2023 21:26:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Feb 2023 21:26:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Thu, 16 Feb 2023 21:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 16 Feb 2023 21:26:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 16 Feb 2023 21:26:33 GMT
WORKDIR /var/lib/jetty
# Thu, 16 Feb 2023 21:26:33 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 16 Feb 2023 21:26:34 GMT
USER jetty
# Thu, 16 Feb 2023 21:26:34 GMT
EXPOSE 8080
# Thu, 16 Feb 2023 21:26:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Feb 2023 21:26:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2f94ae48211bd1a594568459c26544ed87add671819456bfa5fe2bc2f1d741`  
		Last Modified: Thu, 16 Feb 2023 21:08:24 GMT  
		Size: 145.0 MB (144955124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c153cc2a33dceab69334b25964fde3eb2ae07eb55ef7307761829a50360fcd`  
		Last Modified: Thu, 16 Feb 2023 21:31:09 GMT  
		Size: 15.9 MB (15877446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99364c6f66825faf7c808cd21b7a431ef6c95575acbe28f16c721ed4efe97f6c`  
		Last Modified: Thu, 16 Feb 2023 21:31:08 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
