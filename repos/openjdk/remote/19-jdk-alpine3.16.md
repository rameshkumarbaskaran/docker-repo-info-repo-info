## `openjdk:19-jdk-alpine3.16`

```console
$ docker pull openjdk@sha256:272a59fd4d58fdcb7ebffa6a72e5cea591211710b22357b505327d322a24dd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-jdk-alpine3.16` - linux; amd64

```console
$ docker pull openjdk@sha256:900cf954703d9076ed0c147d5be2fa1893fa1808ee7001f95638c9d26a7453e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194310979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f87afb78e932834abd94b1f9cf660927266643a7aaf092c0a723f779e1dde29`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:08:24 GMT
RUN apk add --no-cache java-cacerts
# Mon, 18 Jul 2022 21:08:24 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Mon, 18 Jul 2022 21:08:24 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 21:08:25 GMT
ENV JAVA_VERSION=19-ea+5
# Mon, 18 Jul 2022 21:08:37 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 18 Jul 2022 21:08:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da38bb9be0b7f401137df7b59b4ef9a37950d07f82c1f15b1406789b7be2034`  
		Last Modified: Mon, 18 Jul 2022 21:15:02 GMT  
		Size: 919.4 KB (919425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b6a88185eddf293a8db2b2b1cbc26728a6a928199d4298055613ea0c27c999`  
		Last Modified: Mon, 18 Jul 2022 21:15:17 GMT  
		Size: 190.6 MB (190592748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
