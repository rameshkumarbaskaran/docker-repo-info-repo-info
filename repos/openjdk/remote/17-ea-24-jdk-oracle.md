## `openjdk:17-ea-24-jdk-oracle`

```console
$ docker pull openjdk@sha256:360f339380ba60a953d419cef5e251cdcb3818a1a6ce6d2a497ba6f67eb1a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:136f5625d48e7b826984c7a105c1859c97472db139bb65767c65aecd2645264d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241816735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3d45e079769c5f6b6484e9bc4c52848f99dbdddc418ad2a6678fd05049522c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 May 2021 18:22:12 GMT
ADD file:9e4bcf8e1c3b7657912e93a0b82bf37752a310fa3041ec461562c85d65529ad3 in / 
# Fri, 28 May 2021 18:22:12 GMT
CMD ["/bin/bash"]
# Fri, 28 May 2021 18:39:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 28 May 2021 18:39:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 28 May 2021 18:39:11 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 18:39:12 GMT
ENV LANG=C.UTF-8
# Fri, 28 May 2021 18:39:12 GMT
ENV JAVA_VERSION=17-ea+24
# Fri, 28 May 2021 18:39:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 May 2021 18:39:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:daa797b1cf01195cd47497fc9ddbf3fc4404f3fc012110f206b7fa3dd531e43d`  
		Last Modified: Fri, 28 May 2021 18:23:25 GMT  
		Size: 42.2 MB (42183040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7f736a217a7dd2e90a8ba647050e6374f7c3f746ad3256682302739a73ee7`  
		Last Modified: Fri, 28 May 2021 18:44:27 GMT  
		Size: 13.4 MB (13401079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f5d5c2a12a1ad5ac657bacf748f311f11f1e1c905d2fd30b0b3c83cea7be20`  
		Last Modified: Fri, 28 May 2021 18:44:45 GMT  
		Size: 186.2 MB (186232616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a0b122b209c7987919763ec0f31fa539a0e06b952eee3a43c73de86b6370d411
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238471987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924f1f38ad1cc79c6e156b44bd0504e942182d171fa592873c06754dd95bdf3f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 17 Apr 2021 00:43:47 GMT
ADD file:2afad2b68d4889be2ef517aea246957975145f8ad99a3e9e6a01baf79f67d5e2 in / 
# Sat, 17 Apr 2021 00:43:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 08:36:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 May 2021 08:36:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 27 May 2021 08:36:20 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 08:36:20 GMT
ENV LANG=C.UTF-8
# Fri, 28 May 2021 05:16:55 GMT
ENV JAVA_VERSION=17-ea+24
# Fri, 28 May 2021 05:19:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 May 2021 05:19:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b26d50a92155f32c82c580c6abd80083d4fff230a35ef647094df38f4475f9f`  
		Last Modified: Sat, 17 Apr 2021 00:45:12 GMT  
		Size: 42.0 MB (41996718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f165b404d40aab21b88837e6a2c21b279a81827c7f906a6c56c6690bf3425c`  
		Last Modified: Thu, 27 May 2021 08:52:17 GMT  
		Size: 14.2 MB (14184544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53f3663bbdf59a0e9eb3535002140f13412a1423b4aa76ad0094a952652a689`  
		Last Modified: Fri, 28 May 2021 05:30:54 GMT  
		Size: 182.3 MB (182290725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
