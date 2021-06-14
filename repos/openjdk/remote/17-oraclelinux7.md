## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:10afcfbfc523a82c86c001be74a09824a1ed541e42cd2ce18b5535b752ff4b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:d5e3b7e10410f27aa448180d22f0dec9b0523fd70cfa06e8e18f21a212709325
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250839961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753dc88ac817660a2ce97c6659cf13fb5bab47b40bb4d0d6f897232b968e5301`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 15:21:43 GMT
ADD file:6853efe982f87a3475099ab9aaa2ec9797afac58ee8dfc54d912b966bc3405ea in / 
# Tue, 01 Jun 2021 15:21:44 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 15:38:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 15:38:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 15:38:40 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 15:38:41 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Jun 2021 21:23:06 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:23:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:23:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbf629395cd4d267c366a2b3ac4cfbe6a6c5cfd5bdd8e89a7157e0901e898cf4`  
		Last Modified: Tue, 01 Jun 2021 15:22:47 GMT  
		Size: 48.3 MB (48260748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf25dc842172d49c0f45cec26c8fe86f7a083e2e5ce7a5e6d84d2b4cd2d46ba`  
		Last Modified: Tue, 01 Jun 2021 15:43:59 GMT  
		Size: 15.4 MB (15425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1593c7646ed953cc19d76546c8b121e256d6b23f87826da99db5d8e1cb2d115`  
		Last Modified: Mon, 14 Jun 2021 21:32:10 GMT  
		Size: 187.2 MB (187153277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f428e30f226064342b987a892b98564decf5231173fed845954d4de4d5863523
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251245600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444c857cfe276a642e3e1685885c251270a5d73c81bd67d5ba65883f63dd9746`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 14:41:12 GMT
ADD file:3f30763d6f4fa6cd26708a9eda4872cc48b0c874b7837e0682ea4b4ed7ac5fb2 in / 
# Tue, 01 Jun 2021 14:41:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 14:58:49 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 14:58:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 14:58:50 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 14:58:50 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Jun 2021 20:44:33 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 20:44:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:44:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5216e6356b12c39a03d420e358911905653d063185ac40b7250d625cfcd46024`  
		Last Modified: Tue, 01 Jun 2021 14:42:13 GMT  
		Size: 48.9 MB (48857508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104ba284443f9b2819e0f98ad5efb21b57c2cf4d49bd3d3cbd1af4ad0ac2c85`  
		Last Modified: Tue, 01 Jun 2021 15:09:33 GMT  
		Size: 16.4 MB (16419323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b75a093b0a61d6d7d16139b0fb33ff1266b50d863c7fea22dc514f40e89b60`  
		Last Modified: Mon, 14 Jun 2021 21:00:26 GMT  
		Size: 186.0 MB (185968769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
