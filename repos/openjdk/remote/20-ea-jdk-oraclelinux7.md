## `openjdk:20-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:6ac067abd4d42c8cfc811aff060bda6755187c4d4d2568021ed666aa45acc84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:bf883b8cb970cec279ffd0cc7a0ac95c5c7293b45d03d1f2fa9e9438e5c0081a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260053626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e2494c6ec8c846019b11a98adb3c64aaeac4a3f6b16ef44d74b5b41de88cee`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:50:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 22:50:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 22:50:16 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 22:50:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 21 Jul 2022 23:21:21 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:21:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:21:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f0f1eb3582fe120c104ded4086894e324ef46a631953f821f879e3e7a6a26`  
		Last Modified: Tue, 05 Jul 2022 22:58:49 GMT  
		Size: 14.2 MB (14245779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27141b0606c02e7aef6863882c64f11a0b4144bbcecadcb970aa8b24fba88028`  
		Last Modified: Thu, 21 Jul 2022 23:31:00 GMT  
		Size: 197.0 MB (197044952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ec3ccfa61691f847815569ad3ccdc582520f4bc50a34ba73414387c825e1c1d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260494999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221734f45e316ddb310391439640d27117993b5f7421faf7f19ffea99b973c99`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:37 GMT
ADD file:6d5eeb6c0921661dff8e0b6a89c3272aa52f72b5926d62ae482a85c8ef6458a3 in / 
# Tue, 05 Jul 2022 22:43:38 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:05:04 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 23:05:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 23:05:05 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:05:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 21 Jul 2022 23:41:12 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:41:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:41:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:456ca0cbf3e695c518e5d5c4cb5ff9f99bb999a28b5ec7da3b4ca48d3cf80e6b`  
		Last Modified: Tue, 05 Jul 2022 22:45:10 GMT  
		Size: 49.3 MB (49342729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981fd8b8b8e53f7977497096fa392e1d14f1e3dd10684ac47d3fa4688b887e7`  
		Last Modified: Tue, 05 Jul 2022 23:21:54 GMT  
		Size: 15.3 MB (15264543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb997e2534b0f894bd67b7c58fa9c2e167be4ec9303f9d3749c4dbf039ebb0d`  
		Last Modified: Thu, 21 Jul 2022 23:58:53 GMT  
		Size: 195.9 MB (195887727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
