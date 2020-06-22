## `clojure:openjdk-15-lein-alpine`

```console
$ docker pull clojure@sha256:10e34b16a4e6676edbb1e647f37414f7d0f0a045c987ab9e1d5778cd11229070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4801c8076f1258bf63aab94cf9597b9e0fbcb667ac7fe04be63eaffa10a7fd0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221728068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e441a835c540277d139cc1cd5c3c10e7f55f34a9dd934377716e5f35b5e425`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2020 20:22:15 GMT
RUN apk add --no-cache java-cacerts
# Mon, 22 Jun 2020 20:22:15 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Mon, 22 Jun 2020 20:22:15 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_VERSION=15-ea+10
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Mon, 22 Jun 2020 20:22:57 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Mon, 22 Jun 2020 20:22:57 GMT
CMD ["jshell"]
# Mon, 22 Jun 2020 20:55:31 GMT
ENV LEIN_VERSION=2.9.3
# Mon, 22 Jun 2020 20:55:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2020 20:55:31 GMT
WORKDIR /tmp
# Mon, 22 Jun 2020 20:55:35 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Mon, 22 Jun 2020 20:55:36 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2020 20:55:36 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2020 20:55:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Mon, 22 Jun 2020 20:55:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121b9d547c5ad1e5b9845b4a6b9f44a4bb6c15e45cc609316809d19b5d27345`  
		Last Modified: Mon, 22 Jun 2020 20:26:56 GMT  
		Size: 971.8 KB (971778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ae062329c82bbdb09eb9b3ac5a9f754a1a9a4d7ffb87a547ffbefccb4ed628`  
		Last Modified: Mon, 22 Jun 2020 20:27:13 GMT  
		Size: 199.8 MB (199807555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5605957fb96f4aa6ea48880628797402147dbbe252a49eb63f2c3cb684ecf9a8`  
		Last Modified: Mon, 22 Jun 2020 20:58:43 GMT  
		Size: 14.0 MB (13967282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31858b04ca0b49a15e77dcbf68a91275b2fa441d2f4bd8a50e7ab0f3d52faed4`  
		Last Modified: Mon, 22 Jun 2020 20:58:39 GMT  
		Size: 4.2 MB (4168137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
