## `jetty:9-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:5286356c9d65f4933d2118d54e105344092d1bb29f584a0528cb5731aae85102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:d1213201fd974afe5e513e7cba6c9ebbeb328d6a84c3249fe4eec6e6d6dad9a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214479558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc18377655589e6fe33c7e3398f5ccb635c554c1953f8baf5ce2c634711d3425`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:25:16 GMT
ARG version=17.0.7.7.1
# Thu, 20 Apr 2023 18:25:22 GMT
# ARGS: version=17.0.7.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Thu, 20 Apr 2023 18:25:23 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:25:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:25:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 20 Apr 2023 18:56:50 GMT
ENV JETTY_VERSION=9.4.51.v20230217
# Thu, 20 Apr 2023 18:56:50 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 20 Apr 2023 18:56:50 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 20 Apr 2023 18:56:50 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 20 Apr 2023 18:56:50 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 20 Apr 2023 18:56:50 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.51.v20230217/jetty-home-9.4.51.v20230217.tar.gz
# Thu, 20 Apr 2023 18:56:50 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 20 Apr 2023 18:57:00 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 20 Apr 2023 18:57:00 GMT
WORKDIR /var/lib/jetty
# Tue, 02 May 2023 21:37:59 GMT
COPY multi:3772e82b7a226c88950ac6f41de72f5073a10dcc30ed75546216af96428dc261 in / 
# Tue, 02 May 2023 21:37:59 GMT
USER jetty
# Tue, 02 May 2023 21:37:59 GMT
EXPOSE 8080
# Tue, 02 May 2023 21:37:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 May 2023 21:37:59 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ad79ad89ec4c86880727482cb66c0780254c622d8827ceb87afd9552d8344d`  
		Last Modified: Thu, 20 Apr 2023 18:37:13 GMT  
		Size: 193.6 MB (193576571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae784d42de4a2e3bf9187cd288a09015979c318f9abe7a591511b98fb8d17ea`  
		Last Modified: Thu, 20 Apr 2023 19:03:13 GMT  
		Size: 17.5 MB (17526875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9038cab0b34d7f944298b34d23d4cee6dab227336b42a06ec5951ff0a79c6653`  
		Last Modified: Tue, 02 May 2023 21:50:36 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
