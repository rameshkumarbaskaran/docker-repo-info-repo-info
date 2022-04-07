## `clojure:openjdk-19-tools-deps-alpine`

```console
$ docker pull clojure@sha256:f937833a9b96201caf9c4a2d6dcedbf6b983f0d90787095b64608cecab4f7ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6c735131577826495a318a3e2c54e1df9274768f9d3507fa5494018b91b1ac9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224160768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dd14ac2b2d5441bf13f61378e7d238ca1f9ad28f5ad93d8a44a0fa57cde1eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:20:40 GMT
RUN apk add --no-cache java-cacerts
# Tue, 05 Apr 2022 10:20:40 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 05 Apr 2022 10:20:40 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:20:40 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 05 Apr 2022 10:20:51 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 05 Apr 2022 10:20:51 GMT
CMD ["jshell"]
# Thu, 07 Apr 2022 17:26:48 GMT
ENV CLOJURE_VERSION=1.11.1.1105
# Thu, 07 Apr 2022 17:26:48 GMT
WORKDIR /tmp
# Thu, 07 Apr 2022 17:26:55 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "5655c3ee3ea495d0778d8a87ce05a719045d3ceae9dd5cc29033379d8f82cce5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 07 Apr 2022 17:26:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Apr 2022 17:26:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Apr 2022 17:26:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Apr 2022 17:26:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652302906a15152c7ccbc20fb29082a3a6c23b32b20b1510eadc656e28474de8`  
		Last Modified: Tue, 05 Apr 2022 10:26:55 GMT  
		Size: 918.6 KB (918584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb589e67783e2a820d94ecc2fbc5976eabbacb7c7cdfe21d8195791f058c611`  
		Last Modified: Tue, 05 Apr 2022 10:27:09 GMT  
		Size: 190.6 MB (190592800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4c39d611646d3df933e0128059bc1b61eba1b37f4d1e53ed2ef8534f6b565`  
		Last Modified: Thu, 07 Apr 2022 17:58:24 GMT  
		Size: 29.8 MB (29833797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2fd5d0c82422c5bb1a98bf7f1ecdfb9d5badf5c964c2e3151b72cb26f28fa`  
		Last Modified: Thu, 07 Apr 2022 17:58:22 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f70afbc2c8c1a1afc415e577dcc99bf65fd565b2e8b6cde96f7432c85cee54`  
		Last Modified: Thu, 07 Apr 2022 17:58:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
