## `openjdk:19-ea-16-buster`

```console
$ docker pull openjdk@sha256:8d3137d0c2ccd139573bfec30306904869136953b48be566df5dc25159bd94d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-16-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:ec5c7594036ce6783972ea8e259437ff083984abffac9b1ed737f4e9bfe55275
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327350286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f224de009bdda60342d8be19ddc35418b7a9930133c753fbec6162d3654fb1a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:31:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 23:07:47 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:07:47 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 01:25:40 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 01:26:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 01:26:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98d6bb51c7ccadb2f72a1498db713088ec7c3f449b3c810d95dbca6ba7511ba`  
		Last Modified: Tue, 29 Mar 2022 17:39:41 GMT  
		Size: 51.8 MB (51843446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355592f16f1c7af5aaf7bf2b59b429fc6d54e6a9d493142700d424847989c58`  
		Last Modified: Tue, 29 Mar 2022 23:20:09 GMT  
		Size: 13.9 MB (13921230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e130d15266f4238d2fa903d2bd7d09e0e8dcb25a56f8bbe52c2292aa24761`  
		Last Modified: Thu, 07 Apr 2022 01:35:02 GMT  
		Size: 193.3 MB (193294102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-16-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4544b1a7cd3c84dd3410291fe3085dc04529094b7ed920f9eb305fb17091a6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325740168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50b9ebefd2e544607ce24026b05513dab5b0c41841d1373f5b296a7a3ec315f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:59:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 30 Mar 2022 08:59:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:59:53 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 00:46:20 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 00:46:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 00:46:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bff08cf9734159a77ecf001874bfd910561517c9c87811003564d4a2f00421`  
		Last Modified: Wed, 30 Mar 2022 02:25:51 GMT  
		Size: 52.2 MB (52174968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b271ee6d3652db1e127606e48dbdddd1d0197d93f24fe910a41298350932c02d`  
		Last Modified: Wed, 30 Mar 2022 09:20:58 GMT  
		Size: 14.7 MB (14671177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eaf071777f92f08aab7b2d710b9581539bfeded51039b2756b5ace3d47e20f`  
		Last Modified: Thu, 07 Apr 2022 01:01:47 GMT  
		Size: 192.2 MB (192181350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
