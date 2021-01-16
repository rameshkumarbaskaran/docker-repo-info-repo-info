## `openjdk:16-alpine`

```console
$ docker pull openjdk@sha256:3d00835b2555f53e5175924f6b2994eb6337f83bf7ada0c57dfb49cc51ee5126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:16-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:57a316b50e54b0f197a71bb64f5a1eb47d5870ebcd31cb0a06e783650e4bc1a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189684117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a89307004658e5ac4e9cee4429a9cd6a057fb8ae7069e2e604c964b8fbf258`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:15:27 GMT
RUN apk add --no-cache java-cacerts
# Thu, 17 Dec 2020 13:15:27 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Thu, 17 Dec 2020 13:15:28 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Jan 2021 23:25:47 GMT
ENV JAVA_VERSION=16-ea+32
# Fri, 15 Jan 2021 23:26:43 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64) 			downloadUrl=https://download.java.net/java/early_access/alpine/32/binaries/openjdk-16-ea+32_linux-x64-musl_bin.tar.gz; 			downloadSha256=f9ec3071fdea08ca5be7b149d6c2f2689814e3ee86ee15b7981f5eed76280985; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Jan 2021 23:26:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7f0194508bfdf90c2d4c810091723a528db557a8f15dc3342de6f146b13a31`  
		Last Modified: Thu, 17 Dec 2020 13:21:09 GMT  
		Size: 927.2 KB (927220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222cdd7f57af7ea33595647ef8743e8ab04a9785bffbcb340f2df213c0ff355f`  
		Last Modified: Fri, 15 Jan 2021 23:38:06 GMT  
		Size: 186.0 MB (185957831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
