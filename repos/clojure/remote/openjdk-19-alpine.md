## `clojure:openjdk-19-alpine`

```console
$ docker pull clojure@sha256:b682d2ce750c4651de412aba613dea9eacdf3f5f3b129a2d6f3a68ffe50f75c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:20b871c34bb628f2a9bfe33c2c45e0e4371997f08a111a1dc3933da4eca25eb0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223743479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42630105359916147e84b365722a95f481e6e2fe8d93d2c6bc296c118b3ec36d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Wed, 23 Mar 2022 21:44:21 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 23 Mar 2022 21:44:21 GMT
WORKDIR /tmp
# Wed, 23 Mar 2022 21:44:27 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Wed, 23 Mar 2022 21:44:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 23 Mar 2022 21:44:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 23 Mar 2022 21:44:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 23 Mar 2022 21:44:27 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:e362a85d5230dbbfeb529538f254a9e2b65f246b8cd2845fbf0d404c3b4b4695`  
		Last Modified: Wed, 23 Mar 2022 21:48:57 GMT  
		Size: 29.4 MB (29418366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fc848db367875cf0dfd20c4767a68ccaf57ea9e163b7a610fe231d91ffa6ce`  
		Last Modified: Wed, 23 Mar 2022 21:48:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a3662fab4d37f7ab439002e2dfc9917e7791b194f899a65a037eb04b94084`  
		Last Modified: Wed, 23 Mar 2022 21:48:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
