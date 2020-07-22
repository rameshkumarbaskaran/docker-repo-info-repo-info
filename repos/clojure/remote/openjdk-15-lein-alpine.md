## `clojure:openjdk-15-lein-alpine`

```console
$ docker pull clojure@sha256:622d8eed51e4ecf2b167a90768c66d76d8a8f17275d1814640e6b7e45f248bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:043e14558aac2e02424db7f1695b23c42004ec0beb459ef72fb84a32306dbe7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218654724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01af8427dac55c54ecfac4b3f67d0b78dd8bd97a321f29a1f13afb76fb728054`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 01:05:44 GMT
RUN apk add --no-cache java-cacerts
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Wed, 22 Jul 2020 01:07:14 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_VERSION=15-ea+31
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/31/binaries/openjdk-15-ea+31_linux-x64-musl_bin.tar.gz
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_SHA256=da7abd4d3b3511ed2da8aba25b7ff67863261a0c8b5e7e771cf0fbfadcc7f4fd
# Wed, 22 Jul 2020 01:08:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Wed, 22 Jul 2020 01:08:07 GMT
CMD ["jshell"]
# Wed, 22 Jul 2020 02:31:37 GMT
ENV LEIN_VERSION=2.9.3
# Wed, 22 Jul 2020 02:31:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Jul 2020 02:31:38 GMT
WORKDIR /tmp
# Wed, 22 Jul 2020 02:31:43 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Wed, 22 Jul 2020 02:31:44 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Jul 2020 02:31:44 GMT
ENV LEIN_ROOT=1
# Wed, 22 Jul 2020 02:31:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 22 Jul 2020 02:31:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a2e4aad8c98294e53534e7aef0572d7a04cc37264f1b4b75d0878244e59c7f`  
		Last Modified: Wed, 22 Jul 2020 01:13:01 GMT  
		Size: 926.4 KB (926401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa15118984fa68e4bdb9010318493fccb170122e25dac619d5cefdb32c4d32b`  
		Last Modified: Wed, 22 Jul 2020 01:14:18 GMT  
		Size: 196.8 MB (196795740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f55cb93bebe0f1c46e47eb868af3342b9b9c8230f9723ef4e7a694a1511562`  
		Last Modified: Wed, 22 Jul 2020 02:34:47 GMT  
		Size: 14.0 MB (13966816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b388c9ff8ed8917246e3ca8c3da8d4d9dd2183e3b0ac07d898960d1901b085`  
		Last Modified: Wed, 22 Jul 2020 02:34:46 GMT  
		Size: 4.2 MB (4168226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
