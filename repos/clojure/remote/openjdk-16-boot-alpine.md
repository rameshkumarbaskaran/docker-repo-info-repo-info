## `clojure:openjdk-16-boot-alpine`

```console
$ docker pull clojure@sha256:9bb8ad2acda6e8e94afa154d9fcd7ac649afd671439faf6b6a79263a15c6ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c8bf498a9c38ba84383f90d747f308c57883b3e2728bfb65f9850075311544a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247629454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec84ee64fbbb0c3f1fe40cbf7b8fa73e2373f8a60d32d74221e40b3d858e8cf`
-	Default Command: `["boot","repl"]`

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
# Sat, 12 Dec 2020 04:19:03 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 12 Dec 2020 04:19:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 12 Dec 2020 04:19:04 GMT
WORKDIR /tmp
# Sat, 12 Dec 2020 04:19:05 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Sat, 12 Dec 2020 04:19:05 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 12 Dec 2020 04:19:06 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 12 Dec 2020 04:19:28 GMT
RUN boot
# Sat, 12 Dec 2020 04:19:28 GMT
CMD ["boot" "repl"]
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
	-	`sha256:ab1d993bec704574300c8943c0a66f865174bd84c7ead5597affd651823e24bd`  
		Last Modified: Sat, 12 Dec 2020 04:24:50 GMT  
		Size: 792.3 KB (792314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c65609a631ef77a61d69f09dbb2593d81a2884340bea339192db5b41b2bc64`  
		Last Modified: Sat, 12 Dec 2020 04:24:55 GMT  
		Size: 58.8 MB (58820156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
