## `openjdk:15-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:a195dca548ce85e22aef20b009ebe8ccb8800e5e694006d9a7122c9290e64fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f558aa608f39eae320f0d7877ea86fba24e1c5707f99a8450d5f7680edbe91e1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250264952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f7b688774bffd9c846a04df961c14732305d28a994a208323d881c136540a5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:20:53 GMT
ADD file:d23891d2372d6aae3d738388c74dacd92f9406083ee0c1ac0e2bfd140f92ec2b in / 
# Mon, 04 May 2020 20:20:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 20:38:21 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 04 May 2020 20:38:21 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2020 20:38:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 04 May 2020 20:38:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2020 20:38:13 GMT
ENV JAVA_VERSION=15-ea+22
# Thu, 07 May 2020 20:38:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/22/GPL/openjdk-15-ea+22_linux-x64_bin.tar.gz
# Thu, 07 May 2020 20:38:14 GMT
ENV JAVA_SHA256=c123e6d67ef5be47d5cc9a9b2c2940e31a4bad55af56e34f50e52f4dfec07c78
# Thu, 07 May 2020 20:39:19 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Thu, 07 May 2020 20:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83755823a002357171a0b229ef5769a60db47a90b624adc45f8c6b7cd1d1394f`  
		Last Modified: Mon, 04 May 2020 20:22:07 GMT  
		Size: 43.5 MB (43455265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e105caaf23acf967db67aa1f683d428603dbb51e12295bfe8f5df6a4cce8bb`  
		Last Modified: Mon, 04 May 2020 20:40:58 GMT  
		Size: 14.8 MB (14758294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6448cfc8238af1a38d6bbc850f92281c5d8056dc6f3adfb7d34c7fbdcf9698`  
		Last Modified: Thu, 07 May 2020 20:42:03 GMT  
		Size: 192.1 MB (192051393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
