## `clojure:openjdk-15-boot-alpine`

```console
$ docker pull clojure@sha256:0206a646348245b6eb82463baf25ef60268a5b137df8ebe2c32b5fb2fed4feff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:cc232f9ef35a9783fbeb65f041ff9a8413a0dab7a1fe918958afcd103ca5aefc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263207171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44731b3825969221560232d4a2b4ab061aa982abb276a7a09b583e322d768b3f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2020 20:22:15 GMT
RUN apk add --no-cache java-cacerts
# Mon, 22 Jun 2020 20:22:15 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Mon, 22 Jun 2020 20:22:15 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_VERSION=15-ea+10
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Mon, 22 Jun 2020 20:22:57 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Mon, 22 Jun 2020 20:22:57 GMT
CMD ["jshell"]
# Mon, 22 Jun 2020 20:55:47 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 22 Jun 2020 20:55:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2020 20:55:48 GMT
WORKDIR /tmp
# Mon, 22 Jun 2020 20:55:49 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 22 Jun 2020 20:55:50 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2020 20:55:50 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 22 Jun 2020 20:56:12 GMT
RUN boot
# Mon, 22 Jun 2020 20:56:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121b9d547c5ad1e5b9845b4a6b9f44a4bb6c15e45cc609316809d19b5d27345`  
		Last Modified: Mon, 22 Jun 2020 20:26:56 GMT  
		Size: 971.8 KB (971778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ae062329c82bbdb09eb9b3ac5a9f754a1a9a4d7ffb87a547ffbefccb4ed628`  
		Last Modified: Mon, 22 Jun 2020 20:27:13 GMT  
		Size: 199.8 MB (199807555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958c3eb345e1a3076c2302f43486362ba9861499b430444ab0c4cb26c874242`  
		Last Modified: Mon, 22 Jun 2020 20:58:48 GMT  
		Size: 794.3 KB (794270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce8e501748931624b7b6708acdadcbe8388616d6414fea1cef736adb281adc1`  
		Last Modified: Mon, 22 Jun 2020 20:58:54 GMT  
		Size: 58.8 MB (58820252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
