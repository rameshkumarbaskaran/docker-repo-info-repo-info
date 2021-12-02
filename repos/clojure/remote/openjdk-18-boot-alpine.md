## `clojure:openjdk-18-boot-alpine`

```console
$ docker pull clojure@sha256:0fe765bd084cb186a6645f1eeda520dd7536aaa9dda228d3f4c8edaa72bbad77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:32c23a68d919e36ef4062cbf3ad1d9e909cd44e84170ab6833e43aa6960f204e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252102258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d32b68774398108639b0a75c5e923c07f84421f460ff525bca32a15c73917c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:45:32 GMT
RUN apk add --no-cache java-cacerts
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Tue, 30 Nov 2021 04:45:32 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:45:32 GMT
ENV JAVA_VERSION=18-ea+11
# Tue, 30 Nov 2021 04:45:45 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 30 Nov 2021 04:45:46 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 10:20:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 30 Nov 2021 10:20:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 30 Nov 2021 10:20:02 GMT
WORKDIR /tmp
# Tue, 30 Nov 2021 10:20:04 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 30 Nov 2021 10:20:05 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Nov 2021 10:20:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 30 Nov 2021 10:20:28 GMT
RUN boot
# Thu, 02 Dec 2021 02:34:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 02 Dec 2021 02:34:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 Dec 2021 02:34:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ae5de21b2241a24b653013bdda639de16f984789b28bbcb7108523b460d1e4`  
		Last Modified: Tue, 30 Nov 2021 04:55:25 GMT  
		Size: 932.2 KB (932205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3048de22201addf91c8f64e5382a33c2791d3c21a0906eefce3c4cb08d875839`  
		Last Modified: Tue, 30 Nov 2021 04:55:48 GMT  
		Size: 188.7 MB (188699653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a2e565f2fcdfd82130cf4d6d643540505cf01cb748b8b0d7becbd9505e6f12`  
		Last Modified: Tue, 30 Nov 2021 10:28:00 GMT  
		Size: 831.1 KB (831067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e716a0658b2ee6eda4e5eba746dcb0e5d4267a3ef15626b1533fb6de7f8efb17`  
		Last Modified: Tue, 30 Nov 2021 10:28:03 GMT  
		Size: 58.8 MB (58820514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc3e2673a2e4edd3f31345fc94c5b1934548d91d611ef45e4760db3df9ca21e`  
		Last Modified: Thu, 02 Dec 2021 02:46:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
