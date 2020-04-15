## `clojure:openjdk-14-tools-deps`

```console
$ docker pull clojure@sha256:3032a129c8d5f9b004c3e2365205241aca50c60210e2c00fefe51e397ec4ffaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:e101bf3db806d2870b4286b23d1c4a5423df9299fe2ee68be19ee4c43527e8da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274336635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617fdd97dfae825d5436e9a5a1fed4833fe880545394f0c6f87e19fc7cb4300f`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:31:09 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 01:32:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Tue, 31 Mar 2020 01:32:16 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:32:17 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 14 Apr 2020 21:29:35 GMT
ENV JAVA_VERSION=14.0.1
# Tue, 14 Apr 2020 21:29:35 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14.0.1/664493ef4a6946b186ff29eb326336a2/7/GPL/openjdk-14.0.1_linux-x64_bin.tar.gz
# Tue, 14 Apr 2020 21:29:35 GMT
ENV JAVA_SHA256=22ce248e0bd69f23028625bede9d1b3080935b68d011eaaf9e241f84d6b9c4cc
# Tue, 14 Apr 2020 21:29:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Tue, 14 Apr 2020 21:29:50 GMT
CMD ["jshell"]
# Tue, 14 Apr 2020 22:09:09 GMT
ENV CLOJURE_VERSION=1.10.1.502
# Tue, 14 Apr 2020 22:09:09 GMT
WORKDIR /tmp
# Tue, 14 Apr 2020 22:09:29 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get remove -y --purge curl wget
# Tue, 14 Apr 2020 22:09:29 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e36ba391601ebce2c22f34982f56ce9236ca9cfdef13b2bc60457881d84e8`  
		Last Modified: Tue, 31 Mar 2020 01:35:26 GMT  
		Size: 3.2 MB (3249089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b03299647a6d4610d7beba915b8ffec16df51b8e2e501abce6a9fe67e84a16`  
		Last Modified: Tue, 31 Mar 2020 01:35:59 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7710e1fc1a3ee9a5b8cde04e8acb2b81d708e790a555900414877931623b94a4`  
		Last Modified: Tue, 14 Apr 2020 21:32:41 GMT  
		Size: 199.5 MB (199526344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e07c639a4ceb5afd7f7b819d574ea37fd448e54c52e5304a5c8548ad63b081`  
		Last Modified: Tue, 14 Apr 2020 22:11:14 GMT  
		Size: 44.5 MB (44469128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
