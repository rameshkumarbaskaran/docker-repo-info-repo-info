## `openjdk:18-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:87f2cbc50a90700bff7e1455924167aae46173d370bf9e782372fc16b8011f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:1b0af13f53faab1412bc4d0edad519260edfb9c2add8e05dd991a3b27b30c276
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251264736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6807c4d4596f4a3b79d864295b8214dc24b086a6af4a63772894ce723b175926`
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
# Thu, 15 Jul 2021 22:20:59 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:21:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:21:09 GMT
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
	-	`sha256:aa65a7fe48ca81cac39c203b409fa9f13b771018be334c212705f0d9bf34b0bd`  
		Last Modified: Thu, 15 Jul 2021 22:28:46 GMT  
		Size: 187.6 MB (187577313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:887959f39f782722e9df34b89c8702ebe30eb9ca0dbf47161ab01be8b8e06fd2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251589454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9298c2dd1e36bd0a7718de785293bef5f253bfe37a39ed4ab9cabf2f3dc8e6ad`
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
# Thu, 15 Jul 2021 22:41:00 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:41:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:41:23 GMT
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
	-	`sha256:c09daab32a4710c9b5ebf61ca8d90d84d2b1914c954c9429c1477457ad8f6c10`  
		Last Modified: Thu, 15 Jul 2021 22:55:22 GMT  
		Size: 186.3 MB (186311167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
