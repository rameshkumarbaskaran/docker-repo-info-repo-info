## `openjdk:18-ea-alpine3.13`

```console
$ docker pull openjdk@sha256:2ba3d589e4b107ab21033b8847315383b151692f47d362b7f85cf2faa7ac84a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:0c12d28e7627a890cbc731099fd1e71a524fadf796ec72ceeb65b2abe36b977a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192450110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4b7f77866c92deb4b296174c736cd636d291bab632fd3b845acfa2ba3c755e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:32:47 GMT
RUN apk add --no-cache java-cacerts
# Sat, 13 Nov 2021 07:32:47 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Sat, 13 Nov 2021 07:32:47 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 07:32:48 GMT
ENV JAVA_VERSION=18-ea+11
# Sat, 13 Nov 2021 07:33:01 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 13 Nov 2021 07:33:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb1f2a8c1832af12b3b4df7a9b38d22fc1e7a7a20fb69ac04251a15d23a4be3`  
		Last Modified: Sat, 13 Nov 2021 07:40:59 GMT  
		Size: 928.0 KB (928044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06542ba5d2058899312e6418f24bc285aea63815567f4ac634fd8b88b79eed6c`  
		Last Modified: Sat, 13 Nov 2021 07:41:18 GMT  
		Size: 188.7 MB (188699641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
