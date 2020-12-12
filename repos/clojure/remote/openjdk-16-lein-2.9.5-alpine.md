## `clojure:openjdk-16-lein-2.9.5-alpine`

```console
$ docker pull clojure@sha256:aac5f8c163664c1439edd60d44e5abf7a5987f57d4a8e1f65f4db7f77fa52013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-lein-2.9.5-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d73827d5292ab4032998d553f3d5689515198d715da61f50392dba8f03699a34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204498764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751bf7a527a29f0a8c037384252faefea3c830876fde4684ecba3e5499ca64f0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 15:37:11 GMT
RUN apk add --no-cache java-cacerts
# Fri, 11 Dec 2020 15:37:11 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Fri, 11 Dec 2020 15:37:12 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:37:12 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 11 Dec 2020 15:37:48 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64) 			downloadUrl=https://download.java.net/java/early_access/alpine/23/binaries/openjdk-16-ea+23_linux-x64-musl_bin.tar.gz; 			downloadSha256=4e1d9054a4407e63fbb74155b247cf3926cffe9491074ace6d8a51d78dd0958d; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Dec 2020 15:37:48 GMT
CMD ["jshell"]
# Sat, 12 Dec 2020 04:18:46 GMT
ENV LEIN_VERSION=2.9.5
# Sat, 12 Dec 2020 04:18:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 12 Dec 2020 04:18:47 GMT
WORKDIR /tmp
# Sat, 12 Dec 2020 04:18:50 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Sat, 12 Dec 2020 04:18:51 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 12 Dec 2020 04:18:51 GMT
ENV LEIN_ROOT=1
# Sat, 12 Dec 2020 04:18:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 12 Dec 2020 04:18:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3030ddbe078fa840b91b9c4cdecffd7efa208af278d07528dad2fec84d6fcd14`  
		Last Modified: Fri, 11 Dec 2020 15:43:38 GMT  
		Size: 926.4 KB (926397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b68ff00bbded1d7455a824d6f54c9d200746afa482ceaa4a54644064f00c0b`  
		Last Modified: Fri, 11 Dec 2020 15:43:54 GMT  
		Size: 184.3 MB (184293642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5ec741f2cd7f9e6b55316f2dbb5d8136277450723c5c22ab6f682e74189660`  
		Last Modified: Sat, 12 Dec 2020 04:24:44 GMT  
		Size: 12.3 MB (12301510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da227b6c3698372de5bad90bf66b32bba9dc1aa3baa59b93178b4df977729104`  
		Last Modified: Sat, 12 Dec 2020 04:24:44 GMT  
		Size: 4.2 MB (4180270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
