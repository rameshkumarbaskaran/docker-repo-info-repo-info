## `openjdk:20-oraclelinux7`

```console
$ docker pull openjdk@sha256:2693925c4cd7e0cf3fa154002e22093dd08a228b62fb46f17d7c8839097f98da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c063134a1c8c65ecafe20d87f7cc0548bd90fef03b6f7b14c899a64d0cf18d4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262371541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2115bcdefe261659ab6cb8fa6ddc969fc78faede2b485aa39a2209af2f71dd03`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Oct 2022 19:21:18 GMT
ADD file:33b52c7a287bb91adb106cbb8b7e7bd3d38684f4aa9d19b7ef1f1af5e7288aa3 in / 
# Fri, 21 Oct 2022 19:21:18 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:52:01 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 21 Oct 2022 19:52:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 21 Oct 2022 19:52:02 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 19:52:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 27 Oct 2022 21:23:05 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:23:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 21:23:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c19d5474d2cf2e83fc2be2ee3116c33e32d707b2ca5688ce2b086a0c318e62bd`  
		Last Modified: Fri, 21 Oct 2022 19:23:18 GMT  
		Size: 49.9 MB (49856127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b561046153e09b63218385e349097fc3f08c52087f7f0f58e33ab03ff6e3046`  
		Last Modified: Fri, 21 Oct 2022 19:56:06 GMT  
		Size: 14.2 MB (14242346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b021885efac08de02878cc69d116f9c5ed1cb0ab3a85497b9b67f88aae7f6e`  
		Last Modified: Thu, 27 Oct 2022 21:28:05 GMT  
		Size: 198.3 MB (198273068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d996f19117efa7d07f7c94c887ff4785a3fa74c354b1ba496150fdbca9f749b1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262542589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33884c417850aece1d9640870c93f091d3b7448289b55f5ced2bb7c8796a3e3a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Oct 2022 17:48:21 GMT
ADD file:4541eaa8394632e064f29982b181d348a272ef2413862ac71178a341243bce2e in / 
# Thu, 27 Oct 2022 17:48:21 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 18:10:22 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 27 Oct 2022 18:10:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 27 Oct 2022 18:10:23 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 18:10:23 GMT
ENV LANG=en_US.UTF-8
# Thu, 27 Oct 2022 21:42:35 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:42:45 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 21:42:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fdd4639925cb62e440f1f25d41e3d474d0afd52a63ddf021701ae8f260c928`  
		Last Modified: Fri, 21 Oct 2022 19:43:32 GMT  
		Size: 50.4 MB (50428227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e45151ebef28f688647370e198dfa565d8ff11cb7f067f0621fdf420ab3c09`  
		Last Modified: Thu, 27 Oct 2022 18:14:43 GMT  
		Size: 15.3 MB (15263621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41b7db99098e10361ecd85943ea392844b46effb5bef763c252ee9b202c9cf0`  
		Last Modified: Thu, 27 Oct 2022 21:47:37 GMT  
		Size: 196.9 MB (196850741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
