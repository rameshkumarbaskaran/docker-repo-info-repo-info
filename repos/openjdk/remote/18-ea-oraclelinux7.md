## `openjdk:18-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:87567d6adde2a7b4ae72f5f197b72058325b0ee852cd27defed445ecc2897922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:bcdff0fc80093862cfd3d388b60d643ece78093b3a7e6bdd6fac4ef2b921f7f7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251214206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dea71fd98af74f4c03a8ea7dedcb42ea9a8e66dcd2c915335f4835580285f1a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:20 GMT
ADD file:46efe0cb70a1c4f574c3b3e1fb9b9733930d246bb8077c4ec2160a840697e6c8 in / 
# Thu, 17 Jun 2021 16:51:21 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 17 Jun 2021 17:08:19 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:19 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Aug 2021 22:27:22 GMT
ENV JAVA_VERSION=18-ea+9
# Fri, 06 Aug 2021 22:27:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='892cb159ff07b80db4ac5b1e3343d740c5113d323aa2485aa2d931203e15af61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='35862c7271eec4456da50f777dafb216bcd8e9034e0b77ba8ca9cca9b317b3b8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Aug 2021 22:27:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7627bfb99533146fcb8374f557bc24c36505fb2ee8578ec6072a821200247bbb`  
		Last Modified: Thu, 17 Jun 2021 16:52:21 GMT  
		Size: 48.3 MB (48260810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70fb8946cabfaff2f43cee5915a69ad662b0294e9c91d8f545898e92ed32fd`  
		Last Modified: Thu, 17 Jun 2021 17:14:39 GMT  
		Size: 15.4 MB (15426613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bf481e0bec090db26b10adcbe8d3300b35f78d7001c80156e4938de2c96f86`  
		Last Modified: Fri, 06 Aug 2021 22:42:04 GMT  
		Size: 187.5 MB (187526783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5e589165a0d3b20b06f5407a36d6e61f329fc32e135a5ebf595d076a98aa5a04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251555822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf105a2bb4399857ebc9c1c24a15a96cb8a4215bff27f46623dc0b3bbf23159`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:08 GMT
ADD file:256f7e1c19fbbacd7c7650e1e9991f3617703ba349f259624d78e4393e945665 in / 
# Thu, 17 Jun 2021 16:51:08 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 17 Jun 2021 17:08:43 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:43 GMT
ENV LANG=en_US.UTF-8
# Sat, 07 Aug 2021 01:23:30 GMT
ENV JAVA_VERSION=18-ea+9
# Sat, 07 Aug 2021 01:23:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='892cb159ff07b80db4ac5b1e3343d740c5113d323aa2485aa2d931203e15af61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='35862c7271eec4456da50f777dafb216bcd8e9034e0b77ba8ca9cca9b317b3b8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 07 Aug 2021 01:23:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a3d615f016c21e1c5fef521352cdd990a61abfd09a26d7124c61e33b2cab56a`  
		Last Modified: Thu, 17 Jun 2021 16:52:10 GMT  
		Size: 48.9 MB (48858581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a33d75d2c35cdf1c0dc42b99124399c0375b12141be4bddb4b819732453cb`  
		Last Modified: Thu, 17 Jun 2021 17:23:33 GMT  
		Size: 16.4 MB (16419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc987060242d548d867c86e7c67219ac78ada2410a150169bbae2c1c45a9ae6`  
		Last Modified: Sat, 07 Aug 2021 01:35:48 GMT  
		Size: 186.3 MB (186277535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
