## `openjdk:18-ea-29-jdk-oracle`

```console
$ docker pull openjdk@sha256:2bd36f08c86261cbab2954208eaf36928f6215836806407560aa5d3891279489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:18-ea-29-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6b4d2cd5e45346bf19f40dbaba64064f87b4bb7e52343a8786eb77a1dea71d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243891698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffff35ad552165c09269e812a54ee1a51eb244ac8b990d63d9f10787afe2b2d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:40:45 GMT
ADD file:140d632303428d802f77f473aef33fa52daacdfc76b23edde4344be661c1d4b0 in / 
# Thu, 23 Dec 2021 02:40:46 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:58:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 23 Dec 2021 02:58:40 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:58:41 GMT
ENV LANG=C.UTF-8
# Mon, 27 Dec 2021 17:46:01 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 17:46:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='79501105196281bcb3b1c356529238c3f943a51a24e8695bcee0e3b3e1881507'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='cecaad040cc1f7b0507c8b62275e90ddc32a203da239dccfd5d711f47518bc3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 27 Dec 2021 17:46:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53f096d4aa0757c30613f325df1e03a90db9d9879ea251b394e3ab0a068b5610`  
		Last Modified: Thu, 23 Dec 2021 02:41:44 GMT  
		Size: 42.0 MB (42018351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921862a08fd8bc652539d62804daf06ab6464bd5b42061f5bedbdfa73bd62136`  
		Last Modified: Thu, 23 Dec 2021 03:11:46 GMT  
		Size: 14.3 MB (14303905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64917544b9dda1330e56699e4c99f22e1103cf64fb98f28b5c9b89b755f026`  
		Last Modified: Mon, 27 Dec 2021 18:04:18 GMT  
		Size: 187.6 MB (187569442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
