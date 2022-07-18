## `openjdk:19-ea-31-jdk`

```console
$ docker pull openjdk@sha256:ff08c24ea6ee3fcc236621fc1623155458217abf5b83611197967c32ba43de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:19-ea-31-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:197d6e9aded737470059e477ecaf8d465c11bc053732335481e0ec5035139a85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247327033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d16cf3068f2b11491442afe8888f1ebea9fbcb3f4eeca0796d7a1b4284b29b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:04:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:06:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 05 Jul 2022 23:06:01 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:06:02 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:22:49 GMT
ENV JAVA_VERSION=19-ea+31
# Mon, 18 Jul 2022 19:23:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/31/GPL/openjdk-19-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='e75546f94c9380580e636f7c81483f121035c7936f7765855b17b20d942171fd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/31/GPL/openjdk-19-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='054d2baee1b88b5fcbb29cd1234c0454cd1d379d7ee46ee644f5a4afb22d9c69'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 18 Jul 2022 19:23:08 GMT
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
	-	`sha256:ad61ed73cfb60c46ed9e98cff3c74c51066d2c763abead27257ef6975694897f`  
		Last Modified: Mon, 18 Jul 2022 19:41:53 GMT  
		Size: 195.0 MB (195016410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
