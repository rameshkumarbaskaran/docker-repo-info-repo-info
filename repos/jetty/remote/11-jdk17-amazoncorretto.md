## `jetty:11-jdk17-amazoncorretto`

```console
$ docker pull jetty@sha256:ac28010e0005f53d440508127dedd2db7e2606846171b3ad1ad619f8ca2a7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:11-jdk17-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:68bcdb4c48045ee2009ae402d53b49822083c39a6b37ea7029a18ac0daa34a7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234148223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d010a345c1811a77e0cee13034ad5affa8274e0989b8bdb486bae18a0472b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:36:55 GMT
ARG version=17.0.2.8-1
# Sat, 19 Mar 2022 00:37:27 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 00:37:28 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:37:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 05 Apr 2022 17:22:16 GMT
ENV JETTY_VERSION=11.0.9
# Tue, 05 Apr 2022 17:22:16 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 05 Apr 2022 17:22:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 05 Apr 2022 17:22:16 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 05 Apr 2022 17:22:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 17:22:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.9/jetty-home-11.0.9.tar.gz
# Tue, 05 Apr 2022 17:22:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Tue, 05 Apr 2022 17:22:33 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 05 Apr 2022 17:22:33 GMT
WORKDIR /var/lib/jetty
# Tue, 05 Apr 2022 17:22:34 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Tue, 05 Apr 2022 17:22:34 GMT
USER jetty
# Tue, 05 Apr 2022 17:22:34 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 17:22:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:22:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe6dac67102bcfdf5d509e6ecae60bc439768df7e02101826619b7b238cd3`  
		Last Modified: Sat, 19 Mar 2022 00:45:34 GMT  
		Size: 151.6 MB (151604861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4db32e02f9f02cf79c94cdc713ee4173fc77b544e4ea5082d5e295f14f7c1a`  
		Last Modified: Tue, 05 Apr 2022 17:41:56 GMT  
		Size: 20.3 MB (20336652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43feedc66b0b6b6fcd3093182c00ee01f1b1c4c19df3b5c36deeadf5a5b956d5`  
		Last Modified: Tue, 05 Apr 2022 17:41:54 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:11-jdk17-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:fcaed77271af6bff72a8bea46e3af3b5004297fa151010fe473f1a9ab59f1396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234359780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ef0ed12b22e7b4c257962570fedd7649df199071cff8124c8c5000381f41e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 15:03:43 GMT
ARG version=17.0.2.8-1
# Sat, 19 Mar 2022 15:03:59 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 15:03:59 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 15:04:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 05 Apr 2022 18:07:27 GMT
ENV JETTY_VERSION=11.0.9
# Tue, 05 Apr 2022 18:07:28 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 05 Apr 2022 18:07:29 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 05 Apr 2022 18:07:30 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 05 Apr 2022 18:07:31 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 18:07:32 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/11.0.9/jetty-home-11.0.9.tar.gz
# Tue, 05 Apr 2022 18:07:33 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Tue, 05 Apr 2022 18:07:46 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ;     yum install -y shadow-utils tar xz gzip && yum clean all ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 05 Apr 2022 18:07:46 GMT
WORKDIR /var/lib/jetty
# Tue, 05 Apr 2022 18:07:48 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Tue, 05 Apr 2022 18:07:48 GMT
USER jetty
# Tue, 05 Apr 2022 18:07:49 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 18:07:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 18:07:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f890b2334e8fec631b028cc4715d120348412f974e00dc0e06c0d9dfd5f8b7d`  
		Last Modified: Sat, 19 Mar 2022 15:06:03 GMT  
		Size: 150.2 MB (150174108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4075ecef7f17135200c9d52c6f094792f83dbc6f72c5e88c3ced0fdb0895d`  
		Last Modified: Tue, 05 Apr 2022 18:30:09 GMT  
		Size: 20.4 MB (20355343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d49904ced07bcc5372257c5c9cc7327bf9bea4bf502d4fc3395405674f74fc4`  
		Last Modified: Tue, 05 Apr 2022 18:30:07 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
