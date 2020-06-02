## `clojure:openjdk-15-lein`

```console
$ docker pull clojure@sha256:f2bc0369b56739bd29b049d77015af53e59b6923027ceb1acc452341aea6f017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-lein` - linux; amd64

```console
$ docker pull clojure@sha256:d85f11a1e087c17c902a08ef41037d3c791b3c3901825453f07105fedf9f62aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248093767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ca451da2a53eadc7aba54ab51b56256d361d09f8b85673d34a4fe34b237180`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 21:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:00:03 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 21:00:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 15 May 2020 21:00:04 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:00:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 30 May 2020 00:33:47 GMT
ENV JAVA_VERSION=15-ea+25
# Sat, 30 May 2020 00:34:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-aarch64_bin.tar.gz; 			downloadSha256=32bd13e6fc92dba80d7eb504435a7bd9cbdb0aec2246476eb893b3ef5c5e8f66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-x64_bin.tar.gz; 			downloadSha256=6380fb115db35eea50760346cb4828d7e4054481f025acd84e3b39a3bc2d61eb; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 30 May 2020 00:34:04 GMT
CMD ["jshell"]
# Tue, 02 Jun 2020 00:26:28 GMT
ENV LEIN_VERSION=2.9.3
# Tue, 02 Jun 2020 00:26:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 02 Jun 2020 00:26:28 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:26:37 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get remove -y --purge gnupg wget
# Tue, 02 Jun 2020 00:26:37 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 02 Jun 2020 00:26:37 GMT
ENV LEIN_ROOT=1
# Tue, 02 Jun 2020 00:26:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 02 Jun 2020 00:26:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee19e84e8bd1140527176689c9c1a75f28c0462c0c714e549536452708cbfb64`  
		Last Modified: Fri, 15 May 2020 21:07:16 GMT  
		Size: 3.2 MB (3249166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e2ad6cc28f75db2e56f69cadbd0229b730550706f322b80ca8ad45ce205dd`  
		Last Modified: Fri, 15 May 2020 21:07:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3348212e55a455bf2cc7d9dc79c034be1e26a6d15e1baf8ef57fb22e4ef992a`  
		Last Modified: Sat, 30 May 2020 00:36:58 GMT  
		Size: 195.7 MB (195744850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779f38094fd5193b008883aea5f1fc757f1e7b68204f68e28eeec6156ea084ac`  
		Last Modified: Tue, 02 Jun 2020 00:33:35 GMT  
		Size: 17.8 MB (17832568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44cb28f5c1561dc8db4498d8798393efd1c815e31c46ccb8270ae438a17b052`  
		Last Modified: Tue, 02 Jun 2020 00:33:32 GMT  
		Size: 4.2 MB (4168216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
