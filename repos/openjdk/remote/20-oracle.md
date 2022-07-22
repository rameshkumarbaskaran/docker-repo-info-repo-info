## `openjdk:20-oracle`

```console
$ docker pull openjdk@sha256:92c89e20f242b9efcade6331e49338faa9279676e9521aaf3cf1ab022f781faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:873e2456fbaef709adedb51589ff3799e1ba5825e921ad87da8c646b37f97ad7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249768626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36447b523a6b4f31c1db08afe928442b53a2989f31fc5fb95d50c1989cce4376`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:49:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:49:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 22:49:44 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 22:49:44 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:20:40 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:21:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:21:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e62647f09f0ab1a3ac2d84823777bead33aa8e201c13b86c063296e8268023`  
		Last Modified: Tue, 05 Jul 2022 22:58:01 GMT  
		Size: 13.5 MB (13505357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f686e62675201bb118541a9e816e985b783624aba87cbf7ab2f374ea70e87`  
		Last Modified: Thu, 21 Jul 2022 23:30:13 GMT  
		Size: 197.0 MB (197041148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7058dfc5bd6c646f4d3910ebf4830764e5f2e4b86af52539bf342db7c06e9a83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248198342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4540f84042a7cce58893601fb72a1ed0a3ba0eec765be3c8ec389428b93afb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:04:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:04:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 23:04:02 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:04:03 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jul 2022 23:40:38 GMT
ENV JAVA_VERSION=20-ea+7
# Thu, 21 Jul 2022 23:40:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='96ec967613c72b192b91ce5deab50de86df412b15407e5283d2bf6c815be410a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/7/GPL/openjdk-20-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='516042e08e69c4308e9e60b47b87ef3540e662b89f2dab3d47abee3bde6eb966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:40:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c622a5406eea6948259fe9d62dd3f3f40ef71254cb260355242ef51e23880970`  
		Last Modified: Tue, 05 Jul 2022 23:20:55 GMT  
		Size: 14.3 MB (14282866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6494d0350bebe5e159625bec2298d2e97b8dbeae5fb3a503a3eba9315e30b2`  
		Last Modified: Thu, 21 Jul 2022 23:56:30 GMT  
		Size: 195.9 MB (195887719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
