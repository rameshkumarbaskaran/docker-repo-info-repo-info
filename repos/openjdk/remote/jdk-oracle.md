## `openjdk:jdk-oracle`

```console
$ docker pull openjdk@sha256:5983698258e46611cc8278815fc9bec55ad7b85dd4b1386c6a67bcafdf349934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bade689b107f43329fbec7f453bcc55563140a40dde4be2c375e32a07c98d91a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241565321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef80c8b433f694728b3e2be2030d83710ade6469e06f0cf0e1fa932e88a1d720`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Oct 2022 21:20:42 GMT
ADD file:ceac4c0bc6dd71b3868d5af15bdaab832a2f61b45c12116b2df42ef8cfbf9fa1 in / 
# Wed, 12 Oct 2022 21:20:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 21:40:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 12 Oct 2022 21:41:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Oct 2022 21:41:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Oct 2022 21:41:25 GMT
ENV LANG=C.UTF-8
# Wed, 12 Oct 2022 21:41:25 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 12 Oct 2022 21:41:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Oct 2022 21:41:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ed150ed0abef03007b46722de75bcb3e517f22532a46146fcec4fb1761d4347`  
		Last Modified: Wed, 12 Oct 2022 21:22:08 GMT  
		Size: 40.6 MB (40589408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8fce0a0221dc76ef1ed6d64872744f5f3b00d86ec9efaa593d6f606dbd55ab`  
		Last Modified: Wed, 12 Oct 2022 21:44:03 GMT  
		Size: 12.2 MB (12231062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1ab00442e1823799fd319248209689c83674a36012ff2268d313be4207fab9`  
		Last Modified: Wed, 12 Oct 2022 21:45:19 GMT  
		Size: 188.7 MB (188744851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a8359d6b74815e32e6a0ff21b3adec3dac768d0856f244442c4c52187208746d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240123474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc32630b1cf3ed4446013eeb7114cd283e03fb4f72c72b5061f00cf791264a82`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Oct 2022 20:40:56 GMT
ADD file:049ff2e28998fde860d1a12f43ec245d10345a71953f67108180c23c237ce26e in / 
# Wed, 12 Oct 2022 20:40:56 GMT
CMD ["/bin/bash"]
# Wed, 12 Oct 2022 20:58:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 12 Oct 2022 21:15:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Oct 2022 21:15:45 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Oct 2022 21:15:46 GMT
ENV LANG=C.UTF-8
# Wed, 12 Oct 2022 21:15:47 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 12 Oct 2022 21:15:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Oct 2022 21:15:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:828689dcde4b0fe396ab27cf3a6d5f71ee01d48891421ec4381d74ed415be5d0`  
		Last Modified: Wed, 12 Oct 2022 20:42:33 GMT  
		Size: 39.4 MB (39409290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f742b2cfb7e7c72c98123d08c444932851dc28c95bdb7a2a6a4ebfbcd5456bd`  
		Last Modified: Wed, 12 Oct 2022 21:20:59 GMT  
		Size: 13.1 MB (13054769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642e9a9e0a5fb5861127a7b90ed2c284e64d3a692dfb0a11821127b99c9985d6`  
		Last Modified: Wed, 12 Oct 2022 21:22:37 GMT  
		Size: 187.7 MB (187659415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
