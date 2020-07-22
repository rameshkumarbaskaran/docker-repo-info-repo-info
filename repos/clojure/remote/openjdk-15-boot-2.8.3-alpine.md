## `clojure:openjdk-15-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:051d0f33b013bbc74555e72f7f0eb2216d7843d1978400dd472ba06b8ab96981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:e79b453f6bab77384a60cf0ba1e8342aef1282e91601af37e09fc9f1078fa324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260132168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c16b116d62f312b1b01eac0e1bbf77975f7f31e8a138a35bc117573747e499`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 01:05:44 GMT
RUN apk add --no-cache java-cacerts
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Wed, 22 Jul 2020 01:07:14 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_VERSION=15-ea+31
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/31/binaries/openjdk-15-ea+31_linux-x64-musl_bin.tar.gz
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_SHA256=da7abd4d3b3511ed2da8aba25b7ff67863261a0c8b5e7e771cf0fbfadcc7f4fd
# Wed, 22 Jul 2020 01:08:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Wed, 22 Jul 2020 01:08:07 GMT
CMD ["jshell"]
# Wed, 22 Jul 2020 02:31:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 22 Jul 2020 02:31:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 22 Jul 2020 02:31:56 GMT
WORKDIR /tmp
# Wed, 22 Jul 2020 02:31:58 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 22 Jul 2020 02:31:58 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Jul 2020 02:31:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 22 Jul 2020 02:32:18 GMT
RUN boot
# Wed, 22 Jul 2020 02:32:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a2e4aad8c98294e53534e7aef0572d7a04cc37264f1b4b75d0878244e59c7f`  
		Last Modified: Wed, 22 Jul 2020 01:13:01 GMT  
		Size: 926.4 KB (926401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa15118984fa68e4bdb9010318493fccb170122e25dac619d5cefdb32c4d32b`  
		Last Modified: Wed, 22 Jul 2020 01:14:18 GMT  
		Size: 196.8 MB (196795740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7748f1ba1690bbc14eb84e4b7b68f553ed0f5971a94709e5b30fecdb8168bae3`  
		Last Modified: Wed, 22 Jul 2020 02:34:53 GMT  
		Size: 792.3 KB (792331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d907366f18a68293231e2954eb9bfd278fe258cf10cb027f327fba6ed16570`  
		Last Modified: Wed, 22 Jul 2020 02:34:59 GMT  
		Size: 58.8 MB (58820155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
