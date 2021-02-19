## `openjdk:17-ea-10-alpine3.13`

```console
$ docker pull openjdk@sha256:4d6ceaa55ed80e5ac6dcb69cf008850f67238cc63d6755aad53f867ac03ef59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-10-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:46611259db3d784ebd1b818670cfddc16ce3deac55a4cc0f009dc7007391abd9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190629424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1c895d5022a412edd137e92f9b1c5ac4218f3aaac71d273ad8ebdac5cfbe6c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 05:42:40 GMT
RUN apk add --no-cache java-cacerts
# Thu, 18 Feb 2021 05:42:40 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Thu, 18 Feb 2021 05:42:40 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Feb 2021 23:23:06 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:23:53 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/10/binaries/openjdk-17-ea+10_linux-x64-musl_bin.tar.gz'; 			downloadSha256='fc3ea4225030a5df6191b6027051e705e6c34b72115dfdb36d170d735cb409d5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Feb 2021 23:23:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155cb13c45d5b09951cf0b8e75c365b37550dce6b8ca7c5532d4bd491dd8f3f6`  
		Last Modified: Thu, 18 Feb 2021 05:48:13 GMT  
		Size: 928.2 KB (928245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f816cf83573c02fcf997a8bb0bae3065810e052f3e24cd800d48eb88ebd6b9`  
		Last Modified: Thu, 18 Feb 2021 23:29:59 GMT  
		Size: 186.9 MB (186889522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
