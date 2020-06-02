## `clojure:openjdk-15-boot-alpine`

```console
$ docker pull clojure@sha256:ae2a3dc96b716c0706343e9da308767431bfd2d93d63e7679f282aaee5b2f143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fea410c5324c95f0744e09437975804d1b38e176c46893cf8ae769415ea1a67b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262297759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f785b41fe59325d1f82c5df8e57579ef49753fb129b0c53084449b1a9cf97f5a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Fri, 24 Apr 2020 16:13:45 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_VERSION=15-ea+10
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Fri, 24 Apr 2020 16:13:46 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Fri, 22 May 2020 01:23:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 22 May 2020 01:23:07 GMT
CMD ["jshell"]
# Tue, 02 Jun 2020 00:28:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 02 Jun 2020 00:28:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 02 Jun 2020 00:28:42 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:28:43 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 02 Jun 2020 00:28:43 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 02 Jun 2020 00:28:44 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 02 Jun 2020 00:29:01 GMT
RUN boot
# Tue, 02 Jun 2020 00:29:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63f940b2b97f71dd63758ea307855eda42b2ad6ad589e300590ccbc4d456b2`  
		Last Modified: Fri, 22 May 2020 01:27:30 GMT  
		Size: 199.9 MB (199877491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd1fc7b46f6d836b15c5f5391178b3c0784a017c761fb5aebb77a8983fab297`  
		Last Modified: Tue, 02 Jun 2020 00:34:47 GMT  
		Size: 786.9 KB (786945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e043a37e0e37289ffd9615ac7b760201c0021d8c5debca2a591a1dac944b4`  
		Last Modified: Tue, 02 Jun 2020 00:34:53 GMT  
		Size: 58.8 MB (58820007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
