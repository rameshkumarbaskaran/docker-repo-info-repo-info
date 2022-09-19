## `jetty:9-jdk17-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:07ca2bdb2a4c2fe73038a04a57a4b9760a7f9b6e59705c3b5a00766c6503d0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `jetty:9-jdk17-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:3ef4f43811cb17ccc5921a0e6738c84d72bc2ca7b3cf7de52fab7b034709dbaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211753782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3890d711f117fc92d522a5b76914cd403ba7bd3d00ba48d10156c2feb3fcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 16 Aug 2022 23:21:36 GMT
ARG version=17.0.4.9.1
# Tue, 16 Aug 2022 23:21:42 GMT
# ARGS: version=17.0.4.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 16 Aug 2022 23:21:43 GMT
ENV LANG=C.UTF-8
# Tue, 16 Aug 2022 23:21:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Aug 2022 23:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 19 Sep 2022 17:20:15 GMT
ENV JETTY_VERSION=9.4.49.v20220914
# Mon, 19 Sep 2022 17:20:15 GMT
ENV JETTY_HOME=/usr/local/jetty
# Mon, 19 Sep 2022 17:20:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Mon, 19 Sep 2022 17:20:16 GMT
ENV TMPDIR=/tmp/jetty
# Mon, 19 Sep 2022 17:20:16 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Mon, 19 Sep 2022 17:20:16 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.49.v20220914/jetty-home-9.4.49.v20220914.tar.gz
# Mon, 19 Sep 2022 17:20:16 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Mon, 19 Sep 2022 17:20:26 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Mon, 19 Sep 2022 17:20:26 GMT
WORKDIR /var/lib/jetty
# Mon, 19 Sep 2022 17:20:27 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Mon, 19 Sep 2022 17:20:27 GMT
USER jetty
# Mon, 19 Sep 2022 17:20:27 GMT
EXPOSE 8080
# Mon, 19 Sep 2022 17:20:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 Sep 2022 17:20:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b870c08a78c6304ee7971a65c6153cc957829187674bc57448487a87fd273b`  
		Last Modified: Tue, 16 Aug 2022 23:27:15 GMT  
		Size: 191.7 MB (191662102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9754fde1cb012cf0bdaa0916041fe12b5ecd739788d5430863252c89758c38ba`  
		Last Modified: Mon, 19 Sep 2022 17:38:25 GMT  
		Size: 17.3 MB (17266726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3b6f6d776cb00e235187fbdc01f9516a176bdbedcbda38fd4e80f09a58b11`  
		Last Modified: Mon, 19 Sep 2022 17:38:24 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
