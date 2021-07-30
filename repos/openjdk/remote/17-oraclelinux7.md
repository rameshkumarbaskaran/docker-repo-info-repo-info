## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:317b95f4223de463cdb382a443ebd0d569680a39a46b135a00559e3cf83c44a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5670dfd24c1208f96ee50f35cdd2b48d96c9c9398298f7e23efc4cd26f67619a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250826033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e83b92183aa57cc6956dabb70e971e96b35f3f6047f68ca15c22a3267bfbe`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:20 GMT
ADD file:46efe0cb70a1c4f574c3b3e1fb9b9733930d246bb8077c4ec2160a840697e6c8 in / 
# Thu, 17 Jun 2021 16:51:21 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 17 Jun 2021 17:08:51 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:52 GMT
ENV LANG=en_US.UTF-8
# Fri, 30 Jul 2021 18:50:30 GMT
ENV JAVA_VERSION=17-ea+33
# Fri, 30 Jul 2021 18:50:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/33/GPL/openjdk-17-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='d89e04f161553560c454bf263924dc49c5c2529698ef8131baff632355baea18'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/33/GPL/openjdk-17-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='d361654c87bae6712f36d7f0d27914c63fbe31f10a9a0d5316072b3c69ed2263'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Jul 2021 18:50:40 GMT
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
	-	`sha256:7c3060f317b6c2e99d74260708a7852d70ce3c719f934c78710608b8be9d7505`  
		Last Modified: Fri, 30 Jul 2021 18:59:55 GMT  
		Size: 187.1 MB (187138610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a94605ec22b3fffc6bc7d4612b936c1c07c2e573694be9bb44d9aa72d66bca3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251206407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705883760fc58ca205dac1089c73c14a8acbb71e213df47a5fe47bd17a33bb00`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:08 GMT
ADD file:256f7e1c19fbbacd7c7650e1e9991f3617703ba349f259624d78e4393e945665 in / 
# Thu, 17 Jun 2021 16:51:08 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:10:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 17 Jun 2021 17:10:00 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:10:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Jul 2021 18:49:19 GMT
ENV JAVA_VERSION=17-ea+32
# Fri, 23 Jul 2021 18:49:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='9e5b6c4e27d2adda491036edeed79fafea2961c78a96265a34dd4bb82d7bbf0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='28445241fd8ac0a8572f1dc202f7b492389c3a28d510b8c23cf7538a53b17eab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 18:49:36 GMT
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
	-	`sha256:0a1193cbd93e76d7f952db2ff92937298b510847717bd7f28642d6f9e04dc097`  
		Last Modified: Fri, 23 Jul 2021 19:01:29 GMT  
		Size: 185.9 MB (185928120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
