## `clojure:openjdk-14-boot-slim-buster`

```console
$ docker pull clojure@sha256:da05953233aeba0d186837bcbf84f13817aa8e104fa995b8ee8b5c28aead6401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:7837fe3a1613a11d94942d6061301a0e00d3ede70562236405067db7bdaafac7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288763158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e883d04039d04276b1a5341ff401beca1bdbcdba28500ca2bbf89f724ee6065d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:50:14 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:52:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Sat, 28 Dec 2019 08:52:35 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:52:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Mon, 30 Dec 2019 23:26:37 GMT
ENV JAVA_VERSION=14-ea+29
# Mon, 30 Dec 2019 23:26:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_linux-x64_bin.tar.gz
# Mon, 30 Dec 2019 23:26:37 GMT
ENV JAVA_SHA256=16981e7212ed6035580dff619f93356f707b75f6abfca9a3df7b45a290e8f521
# Mon, 30 Dec 2019 23:27:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Mon, 30 Dec 2019 23:27:06 GMT
CMD ["jshell"]
# Mon, 30 Dec 2019 23:51:39 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 30 Dec 2019 23:51:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 30 Dec 2019 23:51:39 GMT
WORKDIR /tmp
# Mon, 30 Dec 2019 23:51:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Mon, 30 Dec 2019 23:51:45 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 30 Dec 2019 23:51:45 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 30 Dec 2019 23:53:02 GMT
RUN boot
# Mon, 30 Dec 2019 23:53:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e866b0959566a21a8fa7eb2f7f12da0d12aa3498d6c31bb25a6ede1fa632ac2`  
		Last Modified: Sat, 28 Dec 2019 08:58:53 GMT  
		Size: 3.2 MB (3249103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab72a68614df7d0d9d800dc8bc5b3378c9d144c38bdf0865dbdb5d13bce631a`  
		Last Modified: Sat, 28 Dec 2019 08:59:58 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82730f34b12e64de2ef74d2035daaa4283757fa2dc1454542405f01d22b02287`  
		Last Modified: Mon, 30 Dec 2019 23:31:24 GMT  
		Size: 199.3 MB (199320742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32772348c883408cf0636c0ff8ac24ef1ca072746fee46d0f085bf564044e41f`  
		Last Modified: Mon, 30 Dec 2019 23:56:20 GMT  
		Size: 279.6 KB (279580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88197f88a4ee93da81759765154654db595b6303c7dbf2e22c93df61851e09e7`  
		Last Modified: Mon, 30 Dec 2019 23:56:29 GMT  
		Size: 58.8 MB (58821248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
