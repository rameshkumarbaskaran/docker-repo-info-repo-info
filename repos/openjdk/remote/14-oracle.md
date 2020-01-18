## `openjdk:14-oracle`

```console
$ docker pull openjdk@sha256:12a12980b0436d5c6f4c47e7641aad87e499df1d65e0cb56e464aaff109ad357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3a95815ba2a47b6b1bf203b7296d6b15be67242bbe9052f70d9f7716d2db3fa6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256576460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ad2c8fc85f3b5a19a403807a432500d3df431a6d9ce4945de3ac789f7e719`
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
# Fri, 20 Dec 2019 02:06:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 20 Dec 2019 02:06:57 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2020 23:40:24 GMT
ENV JAVA_VERSION=14-ea+32
# Fri, 17 Jan 2020 23:40:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/32/GPL/openjdk-14-ea+32_linux-x64_bin.tar.gz
# Fri, 17 Jan 2020 23:40:26 GMT
ENV JAVA_SHA256=a5ebd5f004508a1617849b598d8fe8c599ed1b255d34a2c4c4776cb00260a8e5
# Fri, 17 Jan 2020 23:41:23 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 17 Jan 2020 23:41:24 GMT
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
	-	`sha256:2220f632ab54f22aaf829e82d2e4ba8220f4ef4a3a81f8c24300949572af2403`  
		Last Modified: Fri, 17 Jan 2020 23:46:39 GMT  
		Size: 199.1 MB (199058050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
