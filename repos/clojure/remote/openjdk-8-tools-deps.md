## `clojure:openjdk-8-tools-deps`

```console
$ docker pull clojure@sha256:32d44e0b875589782abdac5aff8f8f49f686c2d0c576882130710e844f860fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-8-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:322590d3970239e8f2709261c3694b22cfdc66c3f49df9ba53fe8e7f9148131e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261330459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ffdd1a063ae15272365607ffbdd8aed80603f6827691ab5033b3728e6b0ed0`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:40:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:41:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 22 Jul 2020 22:41:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:41:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 30 Jul 2020 22:26:02 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:26:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_linux_8u265b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 30 Jul 2020 23:05:08 GMT
ENV CLOJURE_VERSION=1.10.1.590
# Thu, 30 Jul 2020 23:05:09 GMT
WORKDIR /tmp
# Thu, 30 Jul 2020 23:05:39 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "92a606c1b373ddee338c209f9fecd6f0a40b3354b5eb762962b9cc64f226ce53 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Thu, 30 Jul 2020 23:05:39 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac34a4d7c330794ec24a76e7e58b50d4c8f6a2fc77ca958d83092c8962e7d6d7`  
		Last Modified: Wed, 22 Jul 2020 03:16:44 GMT  
		Size: 51.8 MB (51829832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29274a3f5752b9ce7fd03eece15ee836d2027e2d6817dc2c19f6f58f8cea805`  
		Last Modified: Wed, 22 Jul 2020 22:47:02 GMT  
		Size: 5.3 MB (5284673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b90ee88ecd559362bc94c14af582843163d703cab881bd65d5fba129e11f17a`  
		Last Modified: Wed, 22 Jul 2020 22:48:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d29dec66c715c8bbc1a9977a3cdbf8e442540543f8cc970d281c7b34a0ee6`  
		Last Modified: Thu, 30 Jul 2020 22:29:18 GMT  
		Size: 104.8 MB (104841709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38b3fdeb099fb97b74ef76b842991b9da9bc486ef702f6e23b8df4d996bacf9`  
		Last Modified: Thu, 30 Jul 2020 23:10:32 GMT  
		Size: 31.2 MB (31175688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
