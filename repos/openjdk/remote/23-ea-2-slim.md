## `openjdk:23-ea-2-slim`

```console
$ docker pull openjdk@sha256:bd9852d987cfe2160c9044eb4f37a74e05d19cd00950d9f70362ae1fbe15eae6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-2-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a3e49f37c1043a5c7493338a8f1a0f7d2fa68a3541242bb69d6d938e871c1b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236091643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e50b92bea044ec9d4ca33cd2adf73322ca2574513cf43a272d8ae49406fb52`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96eae9d9d52dbadd849bb00a3bdf82e19d9d9d4831c06e2e927d54fe17bfd7e`  
		Last Modified: Sat, 16 Dec 2023 01:52:02 GMT  
		Size: 3.8 MB (3821584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11269820bd2a3d228482b793992302893b95ab15652965083184f2bf4f20e12`  
		Last Modified: Sat, 16 Dec 2023 01:52:06 GMT  
		Size: 203.1 MB (203120151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:873d0c79649454662a09c3a9283beebbaa27f46949e22539006a42cbfdfb87a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0f4d6edb9de4bcbfd650306f43446c55bc93ece45271e88cab783f80823f8`

```dockerfile
```

-	Layers:
	-	`sha256:125f063198f280e5fe9e07711a6019931c634a08471b2b2b007d5e062d4aa54c`  
		Last Modified: Sat, 16 Dec 2023 01:52:01 GMT  
		Size: 2.0 MB (2037093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c316b961c57fa19603e427b9b7d3c321c3753eafe653f658156aac5223e85ddb`  
		Last Modified: Sat, 16 Dec 2023 01:52:01 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-2-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4cb63200216dc2e1c52bd692a5c1b57934e8ea267a823c5205ec735a690e0101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233839890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0c05d928041c547cbac20274c127cc449a08dad60828579fd4460b8a3f750b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268bfd66b4e399c51afc9123b085a775b9a4a6eb628f71a7bd2f2955bf9a9f65`  
		Last Modified: Fri, 15 Dec 2023 23:23:20 GMT  
		Size: 3.6 MB (3629622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8bae2c43040edf6f4a8074da7a5903a1e1f2ad7c832e205ceb8c741890e519`  
		Last Modified: Sat, 16 Dec 2023 17:28:19 GMT  
		Size: 201.0 MB (201030991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:b9463f6d522593e5c7f408e741f91b609e98478aa1a2f57335a87423c44fdcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2751a7ab59e66963dd7bc577c6c2647d0b3f54a1715e50bd815a29ec2e5b9f32`

```dockerfile
```

-	Layers:
	-	`sha256:ac6e7386d4ea94d8731dc82fce6c446e1f892aa4ef55b60c446a4bb3d0f043dd`  
		Last Modified: Sat, 16 Dec 2023 17:28:16 GMT  
		Size: 2.0 MB (2036473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736eea63ab5d8eb6ad38b96cdcf3e392d30808566d08420dd94d90e296b6c513`  
		Last Modified: Sat, 16 Dec 2023 17:28:15 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.in-toto+json
