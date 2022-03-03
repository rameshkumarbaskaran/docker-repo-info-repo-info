## `clojure:openjdk-19-lein-alpine`

```console
$ docker pull clojure@sha256:6f2f662622fe6d40c19b4f377db8b09f4fbad9fc9e0939285309d2d54d43cf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:69e27ba7797c905f8804890ebeda4940d52ed96a83c6d7456b5592920c4ecc60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210956585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c722fb9ee5ca184b20751315be1d0e6d23d8fa7f2c5aaa61e988ec59ef2dafb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:45:32 GMT
RUN apk add --no-cache java-cacerts
# Tue, 01 Feb 2022 03:11:49 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 01 Feb 2022 03:11:49 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 03:11:49 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 01 Feb 2022 03:12:03 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 03:12:03 GMT
CMD ["jshell"]
# Thu, 03 Mar 2022 01:10:51 GMT
ENV LEIN_VERSION=2.9.8
# Thu, 03 Mar 2022 01:10:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Mar 2022 01:10:51 GMT
WORKDIR /tmp
# Thu, 03 Mar 2022 01:10:56 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 03 Mar 2022 01:10:56 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Mar 2022 01:10:56 GMT
ENV LEIN_ROOT=1
# Thu, 03 Mar 2022 01:11:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 03 Mar 2022 01:11:00 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 03 Mar 2022 01:11:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Mar 2022 01:11:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ae5de21b2241a24b653013bdda639de16f984789b28bbcb7108523b460d1e4`  
		Last Modified: Tue, 30 Nov 2021 04:55:25 GMT  
		Size: 932.2 KB (932205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4484433bf07bc9773d5624dba4e89c7038155b8c8a920e135d9c26d1e485cc7`  
		Last Modified: Tue, 01 Feb 2022 03:23:59 GMT  
		Size: 190.6 MB (190592749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c265969824b195ba02b935fcb31de3964e9c1918d17e4dd521245e61fb75e27a`  
		Last Modified: Thu, 03 Mar 2022 01:30:40 GMT  
		Size: 12.4 MB (12405620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ef7974e43108be0809e5b9df61f067697c0e92be17d6b6fb30e946f073377f`  
		Last Modified: Thu, 03 Mar 2022 01:30:40 GMT  
		Size: 4.2 MB (4207189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fe520996968a51ac4822f2c9f96fb5f0454a62bdd82b3aed538915323d5f55`  
		Last Modified: Thu, 03 Mar 2022 01:30:39 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
