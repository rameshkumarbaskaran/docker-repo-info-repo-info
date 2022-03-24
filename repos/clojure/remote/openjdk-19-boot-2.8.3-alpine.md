## `clojure:openjdk-19-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:246fc092502045fb4e7968ec3a91c7d1a298c1354908da3d0274eaebb27e0f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:40fdac51e974480ce11f1ac3a84e4cac55f49d4b79c13aa1ea61cb840d12d29d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253976622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3bc4718000855f54c98dcdc6932074cf8fc31eef8f2528b8da8af9bca78d63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 23 Mar 2022 21:43:33 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 23 Mar 2022 21:43:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 23 Mar 2022 21:43:33 GMT
WORKDIR /tmp
# Wed, 23 Mar 2022 21:43:34 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 23 Mar 2022 21:43:34 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 23 Mar 2022 21:43:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 23 Mar 2022 21:44:15 GMT
RUN boot
# Wed, 23 Mar 2022 21:44:15 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 23 Mar 2022 21:44:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 23 Mar 2022 21:44:15 GMT
CMD ["repl"]
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
	-	`sha256:236adb5be6b7bcc68c3c35cdcf5ec83dc37c5fc2dbaa8978d8a7bb013fe9b061`  
		Last Modified: Wed, 23 Mar 2022 21:48:42 GMT  
		Size: 831.3 KB (831326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614b9add6a0c8cef8ad11344eb24cf6ce7c6c0ecf17a8aaea455d24226c2b44d`  
		Last Modified: Wed, 23 Mar 2022 21:48:45 GMT  
		Size: 58.8 MB (58820800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86098e720c0c9ce7c88c9ffda18b0d65bd9c2f9bf316b9b56ef30fb737ea647`  
		Last Modified: Wed, 23 Mar 2022 21:48:42 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
