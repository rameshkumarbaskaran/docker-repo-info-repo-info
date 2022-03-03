## `clojure:openjdk-19-alpine`

```console
$ docker pull clojure@sha256:3e71c6aec0789c057416cbb9d758db0fe0cc4dd5ccc171cf6f386657eb38e786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fc254278b31e81310cbff33d3ba92ebceadaa17642031bfdbd0b7d0dfc2207b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223762798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab7dad27107344e5183a6bc6f2f575508417bdcf0448380e3e16de88b92422c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Thu, 03 Mar 2022 01:11:31 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Thu, 03 Mar 2022 01:11:31 GMT
WORKDIR /tmp
# Thu, 03 Mar 2022 01:11:36 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 03 Mar 2022 01:11:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 03 Mar 2022 01:11:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 03 Mar 2022 01:11:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Mar 2022 01:11:37 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:4870711a0e156a8112f6d4eed857756b6199ac050b84bbfec1fe5e7ac1ceb019`  
		Last Modified: Thu, 03 Mar 2022 01:31:06 GMT  
		Size: 29.4 MB (29418403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a5b6738795c62a4c618e544b2966d84ec726dfb1893da3ace9e68b2d7556e`  
		Last Modified: Thu, 03 Mar 2022 01:31:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1166d3d60ef8b09e772030bfba094a5c8060e39d26b8626b4d47ee9e5d9e551`  
		Last Modified: Thu, 03 Mar 2022 01:31:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
