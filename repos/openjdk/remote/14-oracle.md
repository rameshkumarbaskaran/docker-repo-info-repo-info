## `openjdk:14-oracle`

```console
$ docker pull openjdk@sha256:f869aff41e0d28d5cf9f91101c20d80ee3cad9701671289ad2b209ec66f465bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f0af546c668cf509126c5ee10cb99636e798d605ff22e41d24a0aab90bac3659
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265694260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f87519703e6b842d31e0f4e58170b9b0ddf52e213c9d57c4d0d42f03d163b0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 11 Sep 2020 09:49:59 GMT
ADD file:50f1210cda2b0463fc72e0e56a1636cc26b6685c08c7e2cabf7fc2329b04537b in / 
# Fri, 11 Sep 2020 09:49:59 GMT
CMD ["/bin/bash"]
# Fri, 11 Sep 2020 10:23:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 11 Sep 2020 10:23:52 GMT
ENV LANG=C.UTF-8
# Fri, 11 Sep 2020 10:25:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 11 Sep 2020 10:25:58 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 10:25:58 GMT
ENV JAVA_VERSION=14.0.2
# Fri, 11 Sep 2020 10:26:28 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk14.0.2/205943a0976c4ed48cb16f1043c5c647/12/GPL/openjdk-14.0.2_linux-x64_bin.tar.gz; 			downloadSha256=91310200f072045dc6cef2c8c23e7e6387b37c46e9de49623ce0fa461a24623d; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 10:26:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4374a5c9a09aec3eb7169ecd4f7ff91fedce7aeb23b479e5f83af47ec91c5d7c`  
		Last Modified: Fri, 11 Sep 2020 09:51:53 GMT  
		Size: 53.2 MB (53194134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628f382586998761d4d6eaf3d2f5d56829c3099ff15ff17f86c2767c85530a14`  
		Last Modified: Fri, 11 Sep 2020 10:28:24 GMT  
		Size: 13.4 MB (13409452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081406f34c0329ffa0c268fa492659af1a340a5ff3c56605848b5491c8c3dcdc`  
		Last Modified: Fri, 11 Sep 2020 10:29:54 GMT  
		Size: 199.1 MB (199090674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
