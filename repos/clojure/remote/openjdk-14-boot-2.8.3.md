## `clojure:openjdk-14-boot-2.8.3`

```console
$ docker pull clojure@sha256:d5be32fac5190ac62f61222a948143ef3b56166d501e26246d43b22527dfffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:fb8704cd6a66891178852216c330a07ab233aae74aa1fc4fb2abf93685ac053a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (288972291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904c08980792df79d48f115db7eb48b515b3c884975499b8bfbe8bb4c0346bf3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:01:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Thu, 23 Apr 2020 04:01:07 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:01:09 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:01:09 GMT
ENV JAVA_VERSION=14.0.1
# Thu, 23 Apr 2020 04:01:09 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14.0.1/664493ef4a6946b186ff29eb326336a2/7/GPL/openjdk-14.0.1_linux-x64_bin.tar.gz
# Thu, 23 Apr 2020 04:01:10 GMT
ENV JAVA_SHA256=22ce248e0bd69f23028625bede9d1b3080935b68d011eaaf9e241f84d6b9c4cc
# Thu, 23 Apr 2020 04:01:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Thu, 23 Apr 2020 04:01:34 GMT
CMD ["jshell"]
# Thu, 23 Apr 2020 22:31:26 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Apr 2020 22:31:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Apr 2020 22:31:26 GMT
WORKDIR /tmp
# Thu, 23 Apr 2020 22:31:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Thu, 23 Apr 2020 22:31:32 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Apr 2020 22:31:32 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Apr 2020 22:31:55 GMT
RUN boot
# Thu, 23 Apr 2020 22:31:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cd17a79ec489916490053546560e5ffbbe3223daa30751613ba032f562f5bb`  
		Last Modified: Thu, 23 Apr 2020 04:09:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10aaecc16bec7b992c3f57303ec1f7b551be248b8a676733507e01239621e95d`  
		Last Modified: Thu, 23 Apr 2020 04:10:12 GMT  
		Size: 199.5 MB (199524933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa4b155772093f9bcdc749175fd880837d758b325242a96d3d87c0149ad541b`  
		Last Modified: Thu, 23 Apr 2020 22:35:33 GMT  
		Size: 279.6 KB (279630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41beeff94f159085d24d0f90ae470a3dded9e50b59bc1c89341798047a425fe9`  
		Last Modified: Thu, 23 Apr 2020 22:35:37 GMT  
		Size: 58.8 MB (58820198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
