## `clojure:openjdk-19-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:a0d05635f46fc42d978eb49b49255ac25951bdbbb0762d1ed1297a2291265a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:daf2422f93efa02db054beb2a23aa7404c6ca3dc426926d47c9ba1da748c4be0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253995675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e96c3afe2c4fd58c5aca14be739aaced8762bb70ee911f94570c4d7cd0d73a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:45:32 GMT
RUN apk add --no-cache java-cacerts
# Tue, 01 Feb 2022 03:11:49 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 01 Feb 2022 03:11:49 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 03:11:49 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 01 Feb 2022 03:12:03 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 03:12:03 GMT
CMD ["jshell"]
# Thu, 03 Mar 2022 01:11:03 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 03 Mar 2022 01:11:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 03 Mar 2022 01:11:03 GMT
WORKDIR /tmp
# Thu, 03 Mar 2022 01:11:04 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 03 Mar 2022 01:11:05 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Mar 2022 01:11:05 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 03 Mar 2022 01:11:28 GMT
RUN boot
# Thu, 03 Mar 2022 01:11:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 03 Mar 2022 01:11:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Mar 2022 01:11:29 GMT
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
	-	`sha256:e4484433bf07bc9773d5624dba4e89c7038155b8c8a920e135d9c26d1e485cc7`  
		Last Modified: Tue, 01 Feb 2022 03:23:59 GMT  
		Size: 190.6 MB (190592749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248f16f70c75e65e1021e507d01866cb1ab3156963286bf1941b5e4c75ef7ac7`  
		Last Modified: Thu, 03 Mar 2022 01:30:50 GMT  
		Size: 831.4 KB (831442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e1b064052ce6b785071472d1c1c2364f697e71565c57f5507af03f5e06ac2c`  
		Last Modified: Thu, 03 Mar 2022 01:30:54 GMT  
		Size: 58.8 MB (58820455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1882262c03117a98fe6763feef45ddef5f2f26feb7964dedb49dda56408e5001`  
		Last Modified: Thu, 03 Mar 2022 01:30:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
