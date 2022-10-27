## `openjdk:20-jdk-oracle`

```console
$ docker pull openjdk@sha256:51fd87db52c374d87066217b93a20e5ea1cae2bed8717add273a5bb4824baec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e01593d975793b087fe3025e5b89391661984985717c8e37ab66563070e65ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251075587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581a779eedd892d24f3fd5b2117cb266c4727151c8df70bcd4beb2d52aa5f715`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:44 GMT
ADD file:bb73a6f29d54ad7e2f7ec0aeeb404b06eee41432910aa60dd8f9ec5cdb904455 in / 
# Thu, 27 Oct 2022 17:21:44 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:39:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 Oct 2022 17:39:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 27 Oct 2022 17:39:38 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 17:39:38 GMT
ENV LANG=C.UTF-8
# Thu, 27 Oct 2022 21:22:46 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:22:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 21:23:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d67a603b911ada80815df642621203365c074f4903f50aed87dcf6df07e6e4c6`  
		Last Modified: Thu, 27 Oct 2022 17:23:23 GMT  
		Size: 40.6 MB (40581871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80422febbaefdcc8ba66af30635f777afc7bef13f71ad47f90af2a5da4e8099`  
		Last Modified: Thu, 27 Oct 2022 17:42:41 GMT  
		Size: 12.2 MB (12223871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba562cbe47a6bb043f25a99e398b9349457aee72968db982d21b151ff8310a`  
		Last Modified: Thu, 27 Oct 2022 21:27:16 GMT  
		Size: 198.3 MB (198269845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08ee5033175f58ef8df22958ffad3003d8ce06ab79c144235d8216b73b0948ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249303239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c68eebdb6c2228d851dbf32db6cc10f71522548db7f7552444fb4cf440db4b3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Oct 2022 17:48:04 GMT
ADD file:9972b7a185a3ff13a8ec0490c58d6e2b47d402e40b486eb32e78f2fd0919c27e in / 
# Thu, 27 Oct 2022 17:48:04 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 18:08:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 Oct 2022 18:08:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 27 Oct 2022 18:08:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 18:08:04 GMT
ENV LANG=C.UTF-8
# Thu, 27 Oct 2022 21:42:15 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:42:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 21:42:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67fb6ea658c323fd156e1a1606d34b6fb59066aa9985abaa0f6c60ad6e91fab1`  
		Last Modified: Thu, 27 Oct 2022 17:49:29 GMT  
		Size: 39.4 MB (39409912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f0bec0421380148673bf482c1454b86ac9d0915765c91eb8f6262fbf649809`  
		Last Modified: Thu, 27 Oct 2022 18:13:59 GMT  
		Size: 13.1 MB (13050232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc65fd77efa89717ade8827b0385eaf0df9a4f8be911481d70f1de6256165bad`  
		Last Modified: Thu, 27 Oct 2022 21:46:52 GMT  
		Size: 196.8 MB (196843095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
