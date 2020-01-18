## `openjdk:15-ea-6-jdk-oracle`

```console
$ docker pull openjdk@sha256:35cc9062308fb5f1650d67f1cb6c1a5854f0c2e44f4d2e0060adadfba1a2a9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-6-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:77e1cc3ed09b8ce926225c2bf89d7ce28471168eddc39fd178d7cd9efa017e4d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256571232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067e208bb1279cd3333527a2107ff79e3de4ffe43bbc86d2a997f1bc17957704`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 20 Dec 2019 01:46:43 GMT
ADD file:e662b0d428c91ed028fec1db2cccbeddea848eb36b32c8bfad324619b8e57d9f in / 
# Fri, 20 Dec 2019 01:46:44 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2019 02:05:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 20 Dec 2019 02:05:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2019 02:05:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 20 Dec 2019 02:05:13 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2020 23:37:44 GMT
ENV JAVA_VERSION=15-ea+6
# Fri, 17 Jan 2020 23:37:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/6/GPL/openjdk-15-ea+6_linux-x64_bin.tar.gz
# Fri, 17 Jan 2020 23:37:45 GMT
ENV JAVA_SHA256=122a306f4bcf97ab06653d804fb6ff2cba6ef1943331a341193ec5d2b0f87587
# Fri, 17 Jan 2020 23:39:22 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 17 Jan 2020 23:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:822ace0353cbeeb23baa4e10b00916d8aae76c005023f5807d16cd97e6339b9b`  
		Last Modified: Fri, 20 Dec 2019 01:48:50 GMT  
		Size: 42.7 MB (42725372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf4d0631bf4e4c98ff5629cdf7958d9db134bbabd5a323f89f8fd783ca4c524`  
		Last Modified: Fri, 20 Dec 2019 02:10:52 GMT  
		Size: 14.8 MB (14793038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a513159a8eb129b7cdbd58c3f5ece7c117fc25ac681e39a36a014d53468d4889`  
		Last Modified: Fri, 17 Jan 2020 23:44:54 GMT  
		Size: 199.1 MB (199052822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
