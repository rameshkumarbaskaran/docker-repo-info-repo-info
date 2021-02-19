## `openjdk:17-jdk-alpine3.12`

```console
$ docker pull openjdk@sha256:44cf7d3a2bb42efc34e5afe04496dba1ab5df2c3e983798ce4db4a45443f2aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-jdk-alpine3.12` - linux; amd64

```console
$ docker pull openjdk@sha256:f8e2f12ca2d7a0d9825e34604e03448b2cd21b10ecf172400ce86da269e1827f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190615799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17148c936d6be48784fa75a7b0473af2f1d84f3d4339359883893048b00f095e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:15:27 GMT
RUN apk add --no-cache java-cacerts
# Mon, 01 Feb 2021 19:47:02 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Mon, 01 Feb 2021 19:47:03 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Feb 2021 23:24:00 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:24:15 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/10/binaries/openjdk-17-ea+10_linux-x64-musl_bin.tar.gz'; 			downloadSha256='fc3ea4225030a5df6191b6027051e705e6c34b72115dfdb36d170d735cb409d5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Feb 2021 23:24:15 GMT
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
	-	`sha256:c0918f7ac41a2f7c65dcb7ef3546d77c0adfd7c8a39b07db83b604e322dca4b0`  
		Last Modified: Thu, 18 Feb 2021 23:30:28 GMT  
		Size: 186.9 MB (186889513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
