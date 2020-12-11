## `openjdk:16-ea-23-alpine`

```console
$ docker pull openjdk@sha256:7c65dc1d294298e6ce75a062d88d14df99c2c26f284970d7267c58dcaa0064f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:16-ea-23-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:99d5e38dd4a15adbbc9ce7b22b0ac47ff6a538a56bc8bfffba4fb9827013fad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188016984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc06434965edce175275550e45038a12aaa2a51fa56a9f4b186f58acc4db87`
-	Default Command: `["jshell"]`

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
