## `clojure:openjdk-15-tools-deps-1.10.1.547-alpine`

```console
$ docker pull clojure@sha256:f9de34993056cfb5606276315c0a654166505380c2c44de09ca4bf7493a922a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-tools-deps-1.10.1.547-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:99b0029286c26aa0822500deb45a88cbff67e6bad6d0817f6392f0e2168466a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223038045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e82efae6a1483ce23e512277817943cc461a681aa66bc1ccf6b88e67c67243`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Wed, 22 Jul 2020 02:32:25 GMT
ENV CLOJURE_VERSION=1.10.1.547
# Wed, 22 Jul 2020 02:32:25 GMT
WORKDIR /tmp
# Wed, 22 Jul 2020 02:32:40 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "779ce3bd2aea008fa4d7a0569d00b1a1011b88662960355bab54fb86851ae5ad *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 22 Jul 2020 02:32:41 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:27e29b88664af03f870b1449ee420212d20a2f9696ee165e136d44f6d17c8e95`  
		Last Modified: Wed, 22 Jul 2020 02:35:07 GMT  
		Size: 22.5 MB (22518363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
