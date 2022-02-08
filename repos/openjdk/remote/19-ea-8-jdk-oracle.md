## `openjdk:19-ea-8-jdk-oracle`

```console
$ docker pull openjdk@sha256:86300ad40d45807234078487e736fabd8f70451c457e4c19c69b96e9f8e7dae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-8-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c498198ed516a526b4906178d35c8a2cc922cede42aa119cc0bc62b3d864b974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245755748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21544a77f5f9c87eeb203b8b6307b21db0102a523114df8a5da063ee5470542`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Feb 2022 05:30:31 GMT
ADD file:17957b69b27e30b1d860c0919546da181b5e126b4aca4e1935ab44fd1832578e in / 
# Fri, 04 Feb 2022 05:30:31 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 06:31:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 08 Feb 2022 03:42:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 08 Feb 2022 03:42:29 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Feb 2022 03:42:29 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:42:29 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 03:42:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='64f85aad4da5d214002ccbf442b38618b6fae689e66fec2f4a52253d1654683c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='55bc6f3f3db8a59c77e43ee8ee1ea99d3f121b48d3c7d54cf84f2660a008f047'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:42:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f431a76c5f59c48efd4a4076677acaae2b540a7562de00075162ef8a340fd69b`  
		Last Modified: Fri, 04 Feb 2022 05:31:30 GMT  
		Size: 42.1 MB (42102405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0509e57e85d3b85eac03c20f8f88d1cb2481d6122bdae0020851f7022e3b31`  
		Last Modified: Fri, 04 Feb 2022 08:22:45 GMT  
		Size: 13.5 MB (13513973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432790937fac54eb0d642ffbc9e27470b31f127d3889d6810f54056133b337e2`  
		Last Modified: Tue, 08 Feb 2022 03:53:28 GMT  
		Size: 190.1 MB (190139370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
