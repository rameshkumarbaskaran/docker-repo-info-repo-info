## `clojure:openjdk-19-lein-alpine`

```console
$ docker pull clojure@sha256:55ad8230e1ed4ae11678d638080c61fff79cea7c77237c0e651f4a9f90137f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:7e07571a18860f918d4ed9a33d4d282faeec5ed93a2c1a93653b3bcd19cbe81f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210937153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff769c66ba7d1eec391a159a8310265646d564c25e3376311a0181cc7e7d1ccb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:17:58 GMT
RUN apk add --no-cache java-cacerts
# Wed, 23 Mar 2022 17:17:58 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Wed, 23 Mar 2022 17:17:58 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:17:58 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 23 Mar 2022 17:18:23 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 23 Mar 2022 17:18:24 GMT
CMD ["jshell"]
# Wed, 23 Mar 2022 21:43:19 GMT
ENV LEIN_VERSION=2.9.8
# Wed, 23 Mar 2022 21:43:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 23 Mar 2022 21:43:19 GMT
WORKDIR /tmp
# Wed, 23 Mar 2022 21:43:25 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Wed, 23 Mar 2022 21:43:25 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 23 Mar 2022 21:43:25 GMT
ENV LEIN_ROOT=1
# Wed, 23 Mar 2022 21:43:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Wed, 23 Mar 2022 21:43:29 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 23 Mar 2022 21:43:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 23 Mar 2022 21:43:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69ef1ecbd183501e60a2f2d77ac0dfc0cce0aad98559de5dc3264f90c9c8cb2`  
		Last Modified: Wed, 23 Mar 2022 17:24:22 GMT  
		Size: 918.6 KB (918571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b15f3030896b3da0b09bd1151138a08c6c8efd3260da822bb3378f0a362cdfe`  
		Last Modified: Wed, 23 Mar 2022 17:24:36 GMT  
		Size: 190.6 MB (190592829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28f218cebdafd0e5c1050bf3472507def99da087fb778a4755873eca5e8bd56`  
		Last Modified: Wed, 23 Mar 2022 21:48:32 GMT  
		Size: 12.4 MB (12405453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8011a30a6a14084a1bb70bd2c567e9b667a8f64a7b09102b8a9e7e88169239`  
		Last Modified: Wed, 23 Mar 2022 21:48:32 GMT  
		Size: 4.2 MB (4207204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e47061393a35443bd0c0cf2d8cf36ecc1048b2b09052e0be6e105d52d2f535`  
		Last Modified: Wed, 23 Mar 2022 21:48:31 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
