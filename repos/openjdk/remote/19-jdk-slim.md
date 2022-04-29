## `openjdk:19-jdk-slim`

```console
$ docker pull openjdk@sha256:39438a66314fe7e391db92ce1247954d8206b4d5a1c09221caada089e4f055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:fd91f193b961a8d333c4a56aeebf46d2c54a5c0418b023a827b2399ec043e010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228003746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efd14849e103c01c64fad547f1cecf47f32a37b30b95e46f3135e84aa8467a4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:47:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 20 Apr 2022 10:47:39 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:47:40 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:21:05 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:21:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:21:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d3aa8d076675d49d85180b0ced9daef210fe4fdff4bdbb422b9cf384e591d0`  
		Last Modified: Wed, 20 Apr 2022 11:01:25 GMT  
		Size: 1.6 MB (1582162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cd45950ffdf703ff4a3b673d9ddb176de74ceb072341f024232603ea80ff5`  
		Last Modified: Thu, 28 Apr 2022 23:29:36 GMT  
		Size: 195.0 MB (195042605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a923c6b956eb7b6169c5fc15e8e797846668590df8ba6af2640dfb118534f1ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225117772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c1a1d4973f1e32346a5b316ab7c8e74edf4c88e3d3722515006dd02165f2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:24:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 20 Apr 2022 10:24:40 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 28 Apr 2022 23:41:56 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:42:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:42:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59f13dc084e185af417a4c6d1be2534adaff0c4f35ac2166a539260f4e8e945`  
		Last Modified: Wed, 20 Apr 2022 10:46:08 GMT  
		Size: 1.4 MB (1361221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fa2738b058fe85393cda7b425c5111845b346c8dd9658424ed354058d3cebf`  
		Last Modified: Thu, 28 Apr 2022 23:56:55 GMT  
		Size: 193.7 MB (193690750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
