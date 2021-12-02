## `clojure:openjdk-18-tools-deps-alpine`

```console
$ docker pull clojure@sha256:43346c113d5ece0e6fb6ce685c0d7eaf9b0ad3c861f1eca6c1704ef0cf339779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ffaa4b4150f1e9f1375266ca2471db99edae404fab1e34494facef844eb77f81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218607038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c6406f0f77fb3b2a4881e5e213e5126e27aa945ea17096767198d261a4444c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:45:32 GMT
RUN apk add --no-cache java-cacerts
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Tue, 30 Nov 2021 04:45:32 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_VERSION=18-ea+11
# Tue, 30 Nov 2021 04:45:45 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 30 Nov 2021 04:45:46 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 10:20:36 GMT
ENV CLOJURE_VERSION=1.10.3.1020
# Tue, 30 Nov 2021 10:20:36 GMT
WORKDIR /tmp
# Tue, 30 Nov 2021 10:20:43 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "afc87e2c8cfbf87e43553439c69a4c8e36bc2094405d08f39ca542b4cca0920a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 02 Dec 2021 02:34:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Dec 2021 02:34:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 Dec 2021 02:34:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 Dec 2021 02:34:56 GMT
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
	-	`sha256:3048de22201addf91c8f64e5382a33c2791d3c21a0906eefce3c4cb08d875839`  
		Last Modified: Tue, 30 Nov 2021 04:55:48 GMT  
		Size: 188.7 MB (188699653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3259960bbd492a65ce4a51fe312903b9de704827879685c2c81d94f8f81a59`  
		Last Modified: Tue, 30 Nov 2021 10:28:15 GMT  
		Size: 26.2 MB (26155739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b99eadf82eaf12604e8fcde6986706f1971d7c4c480c5f286ef7364b393eec`  
		Last Modified: Thu, 02 Dec 2021 02:46:58 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac58a7914e0fcf32571458478857d94b57dadb038c5d59db6dc2ce85f2b5eed`  
		Last Modified: Thu, 02 Dec 2021 02:46:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
