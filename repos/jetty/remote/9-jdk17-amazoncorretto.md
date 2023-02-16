## `jetty:9-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:797ba330bbbff7fce0e27df710680fcbcad75bd1a92ceb99462dd2d24789bb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:393c5859ed1b4bf6c240df0216e74d00ccd050bf7948f7d137deec69a5fef736
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230112342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551ed6da2fd4b90afae91e9a0dae637a8c8e465d053d99f76fd549faa6645768`
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
# Thu, 26 Jan 2023 23:50:05 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Thu, 26 Jan 2023 23:50:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 26 Jan 2023 23:50:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 26 Jan 2023 23:50:06 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 26 Jan 2023 23:50:06 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Jan 2023 23:50:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Thu, 26 Jan 2023 23:50:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 26 Jan 2023 23:50:24 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 26 Jan 2023 23:50:24 GMT
WORKDIR /var/lib/jetty
# Thu, 26 Jan 2023 23:50:24 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 26 Jan 2023 23:50:24 GMT
USER jetty
# Thu, 26 Jan 2023 23:50:25 GMT
EXPOSE 8080
# Thu, 26 Jan 2023 23:50:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Jan 2023 23:50:25 GMT
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
	-	`sha256:0c7392ecf6d9c318aa8d41da358128f88e58d84a24107f98af5d3b47d538b095`  
		Last Modified: Thu, 26 Jan 2023 23:57:08 GMT  
		Size: 15.8 MB (15824590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c6a33ed3b855808743b070748204e6006edd34548e014d949c27c106516f08`  
		Last Modified: Thu, 26 Jan 2023 23:57:06 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:3a11ed7ef286844a5cc283575429d1310405f7b09d877dbe420352f951e21074
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230369152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954c3f1c7944ebadc18621d65eb93276678de47c784d4232824e6cbfa62482f4`
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
# Thu, 16 Feb 2023 21:25:53 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Thu, 16 Feb 2023 21:25:53 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 16 Feb 2023 21:25:53 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 16 Feb 2023 21:25:53 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 16 Feb 2023 21:25:53 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Feb 2023 21:25:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Thu, 16 Feb 2023 21:25:53 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 16 Feb 2023 21:26:10 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 16 Feb 2023 21:26:10 GMT
WORKDIR /var/lib/jetty
# Thu, 16 Feb 2023 21:26:10 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 16 Feb 2023 21:26:10 GMT
USER jetty
# Thu, 16 Feb 2023 21:26:10 GMT
EXPOSE 8080
# Thu, 16 Feb 2023 21:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Feb 2023 21:26:11 GMT
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
	-	`sha256:0aca5fabccdf894cc20ccdcc622867fc43bdefef0697b5633198460aab431e1f`  
		Last Modified: Thu, 16 Feb 2023 21:30:51 GMT  
		Size: 15.9 MB (15873485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3673ede395941b52d520c353aab1e5c29c7f9faef46393523660944c72b441`  
		Last Modified: Thu, 16 Feb 2023 21:30:50 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
