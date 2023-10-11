## `jetty:9-jdk11-amazoncorretto`

```console
$ docker pull jetty@sha256:3c5c4f0458d8bced446bbf3f84e4b42b3e0906e1b7c11a3668aee301b1a4edc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:9-jdk11-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:447fa7b44d58ca8bbf8fac98dcf980885b9341fe078cb3f6795794941d49921e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226061662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53674250f916a5663da5183e267bac1be87b40ba450e7354a0b42aa4f89c944e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:41:29 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 00:42:06 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 00:42:06 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:42:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Oct 2023 17:33:23 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Wed, 11 Oct 2023 17:33:23 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 11 Oct 2023 17:33:23 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 11 Oct 2023 17:33:24 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 11 Oct 2023 17:33:24 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 17:33:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Wed, 11 Oct 2023 17:33:24 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 11 Oct 2023 17:33:55 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 11 Oct 2023 17:33:55 GMT
WORKDIR /var/lib/jetty
# Wed, 11 Oct 2023 17:33:55 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 11 Oct 2023 17:33:55 GMT
USER jetty
# Wed, 11 Oct 2023 17:33:55 GMT
EXPOSE 8080
# Wed, 11 Oct 2023 17:33:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 17:33:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690581237f4b99c2e5fb4449e509fbee80aa97b1152155f2a93096baeffee662`  
		Last Modified: Sat, 23 Sep 2023 00:57:52 GMT  
		Size: 147.8 MB (147781222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a16363ba19646380e4390feb2947e5a41fe53d48cb8e6fa2461453ee7e724f5`  
		Last Modified: Wed, 11 Oct 2023 17:53:55 GMT  
		Size: 15.8 MB (15809128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f8c52a0ca595e4d541c0e088f03f47d599f049ea914df23ff2ed77e89f7650`  
		Last Modified: Wed, 11 Oct 2023 17:53:53 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jdk11-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:c7c42748eed0ca4fe111224cb589de739980b29d0a8fc5b6e90fe39f83076df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224962276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7505c206868c2fd5a699cd70f0593ec48a14a1cef9ae937ed52ed69c7298d384`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:47 GMT
COPY dir:5885a696cc03fd82c0c021dd701725b8b1bc11902dc8789780147154a555ba2a in / 
# Sat, 23 Sep 2023 00:39:48 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:13:35 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 01:14:03 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 01:14:05 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:14:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Oct 2023 17:48:50 GMT
ENV JETTY_VERSION=9.4.53.v20231009
# Wed, 11 Oct 2023 17:48:51 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 11 Oct 2023 17:48:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 11 Oct 2023 17:48:51 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 11 Oct 2023 17:48:51 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 17:48:51 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.53.v20231009/jetty-home-9.4.53.v20231009.tar.gz
# Wed, 11 Oct 2023 17:48:51 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 11 Oct 2023 17:49:14 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 11 Oct 2023 17:49:14 GMT
WORKDIR /var/lib/jetty
# Wed, 11 Oct 2023 17:49:15 GMT
COPY multi:6bf6ffc2c0ff756d51254f4ec987e84575c16c895c328c42a63bde92f8d5278a in / 
# Wed, 11 Oct 2023 17:49:15 GMT
USER jetty
# Wed, 11 Oct 2023 17:49:15 GMT
EXPOSE 8080
# Wed, 11 Oct 2023 17:49:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 17:49:15 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:0cd473df417d2282c9d0586281fb9293e3faf1fb6481fa584bac46295844f59e`  
		Last Modified: Mon, 18 Sep 2023 18:32:30 GMT  
		Size: 64.2 MB (64161861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddcf06761390c52a0ca2b7c821b3ad5f3508fc488880866c36aa6121d60f7d1`  
		Last Modified: Sat, 23 Sep 2023 01:26:21 GMT  
		Size: 144.9 MB (144934016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0e14a1451ff9c7629d207c3eb672c364dd8c817bf6331a43d31f8c4fc2a704`  
		Last Modified: Wed, 11 Oct 2023 18:02:19 GMT  
		Size: 15.9 MB (15864766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf4d934235f1fb19f17caaac071c6b131393003bc65e90eaf7c25f3b2733fff`  
		Last Modified: Wed, 11 Oct 2023 18:02:17 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
