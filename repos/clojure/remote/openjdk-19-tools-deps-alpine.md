## `clojure:openjdk-19-tools-deps-alpine`

```console
$ docker pull clojure@sha256:c7aad18180d4819337f0aa57501b2d0b2f003d151002d8d2e55a2ecf0b2aedba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9cf77469ac02d9a9f200e96b743ea63f8eee9ec1c91d2fb24193a46d6401a241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224160100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb0e952e0bababa5b850455c883718b829214b6ca85913d43a3eb811a0be898`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 00:53:12 GMT
RUN apk add --no-cache java-cacerts
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 29 Mar 2022 00:53:12 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 29 Mar 2022 00:53:23 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:53:24 GMT
CMD ["jshell"]
# Mon, 04 Apr 2022 21:30:52 GMT
ENV CLOJURE_VERSION=1.11.0.1100
# Mon, 04 Apr 2022 21:30:52 GMT
WORKDIR /tmp
# Mon, 04 Apr 2022 21:30:57 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a71bd520bd43d4be6e0cab0c525f5d1f85911fc276f3d0f37f00243fb0f1e594 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Mon, 04 Apr 2022 21:30:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 04 Apr 2022 21:30:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 04 Apr 2022 21:30:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 04 Apr 2022 21:30:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc6d90ffa98debe440e17dff9ae93f8fc2b8065f5e2d7bc0d2261f9651ae35b`  
		Last Modified: Tue, 29 Mar 2022 01:06:31 GMT  
		Size: 918.6 KB (918583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1650a84836207ca17554d4eebd9a03ac64a82705d0b490da64d2094be0481e6`  
		Last Modified: Tue, 29 Mar 2022 01:06:45 GMT  
		Size: 190.6 MB (190592769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ed03e1ca57e0cce8fab5b33c18db55c8d237112f1f2c3dcfd7fe1cb3881ee0`  
		Last Modified: Mon, 04 Apr 2022 21:41:08 GMT  
		Size: 29.8 MB (29833206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b1fe76c84797eb67e9f9f4b2107c24ec774adda36d699579a5bd27e7b1ca68`  
		Last Modified: Mon, 04 Apr 2022 21:41:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3454c1ba25d0678e613de9d49c86cca233e5d52917173809a6d01ed2ddb86d3a`  
		Last Modified: Mon, 04 Apr 2022 21:41:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
