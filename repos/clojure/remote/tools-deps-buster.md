## `clojure:tools-deps-buster`

```console
$ docker pull clojure@sha256:b6f4c77433a0d15d3065f634b1a07c1fe749284f3e7365437276f18be17b389d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-buster` - linux; amd64

```console
$ docker pull clojure@sha256:b0a60496ff25bf050c639bc622417ed1802b79bd9d61a4d8ff7fe0b97c7cf870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352887904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1447d683449d69c3aab5acaff4aaf8b99d7454c0a7179ca504837cb9cafa95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:47 GMT
ADD file:a290acee3581e1e9c42c0a37b53086a8f070cb0730179be81a6ba24a620b6ee4 in / 
# Wed, 26 Jan 2022 01:40:47 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:13:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:23:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 26 Jan 2022 09:23:06 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:23:06 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:23:06 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 26 Jan 2022 09:23:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:23:21 GMT
CMD ["jshell"]
# Fri, 04 Feb 2022 23:48:21 GMT
ENV CLOJURE_VERSION=1.10.3.1075
# Fri, 04 Feb 2022 23:48:21 GMT
WORKDIR /tmp
# Fri, 04 Feb 2022 23:48:33 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a6b72c9b23d348a0636813c5f59db5dda622e3b8dbb86124cbb51e3aced714d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Fri, 04 Feb 2022 23:48:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Feb 2022 23:48:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 04 Feb 2022 23:48:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 04 Feb 2022 23:48:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a024302f8a017855dd20a107ace079dd543c4bdfa8e7c11472771babbe298d2b`  
		Last Modified: Wed, 26 Jan 2022 01:47:01 GMT  
		Size: 50.4 MB (50437057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289773030fdc98afe6cc53bdd0c05332ea8ff21ad836afa1d3042388953c43f8`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 7.8 MB (7833856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb8b3399fe8dd0b83bd5e32a97e5183ab235d6fb4cc0b5dfabb20e6653e715`  
		Last Modified: Wed, 26 Jan 2022 02:23:32 GMT  
		Size: 10.0 MB (9997205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c63da771697b362929cecc84777e8cfbb716ff3d575b999854d83ada039b695`  
		Last Modified: Wed, 26 Jan 2022 02:23:53 GMT  
		Size: 51.8 MB (51839910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c88c63b5d1adc4c1a364370b244e9b042b780d79deb1240bd7dc938953636b`  
		Last Modified: Wed, 26 Jan 2022 09:42:29 GMT  
		Size: 13.9 MB (13921285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f878c9d76bc2eb342b65c61d600b052434ec299ecb90bd9c6ceabd1fd6d356f1`  
		Last Modified: Wed, 26 Jan 2022 09:49:31 GMT  
		Size: 187.6 MB (187632457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef9944127e36f3e2cb2a1c46aa1dd395d743023efbffefde2ec70ee83a278cf`  
		Last Modified: Sat, 05 Feb 2022 01:39:02 GMT  
		Size: 31.2 MB (31225101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe057d6c21073e67cce21fff33bcc17f1407f99ebd6fc8416df214a36ded18`  
		Last Modified: Sat, 05 Feb 2022 01:38:57 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cd0f9e4ce814ea7fa062862ed813b38924f99d7a90bb4795fd4435f557e844`  
		Last Modified: Sat, 05 Feb 2022 01:38:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:addd8d408263cda133fdf36ce638ded708940c9937abf6a6d566c04abe9c3ef7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350579392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163a2fc08b43d3e4cdbeddcba5c46347f1a3b1b2def036a914cc6a17df47b7dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:35:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:53:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 01 Mar 2022 13:53:02 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:53:03 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 13:53:04 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 01 Mar 2022 13:53:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:53:16 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:35:14 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 02 Mar 2022 08:35:15 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:35:26 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Wed, 02 Mar 2022 08:35:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 02 Mar 2022 08:35:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:35:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:35:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93053a54416be8288cbcc300d0a929f1279cceff9eb11ad9c080fe5439d62dbd`  
		Last Modified: Tue, 01 Mar 2022 10:45:39 GMT  
		Size: 7.7 MB (7695236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2387f0e2dcc6f4271b34d3158d1768015e4424839f06ae428f4e22de8a5c1542`  
		Last Modified: Tue, 01 Mar 2022 10:45:40 GMT  
		Size: 9.8 MB (9767253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8752c30aea58b7ac6dd29ed3dee03ac8ecb3aedcc6e23ba5ddaac39d89f0b`  
		Last Modified: Tue, 01 Mar 2022 10:45:58 GMT  
		Size: 52.2 MB (52174602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11179061655cbc71dfb8c2d9d6954e03aa8a708c9a8ff9b742ae15384aae5e3c`  
		Last Modified: Tue, 01 Mar 2022 14:14:02 GMT  
		Size: 14.7 MB (14671030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37555f06af09b0be337a88573107daa7f8a6a939da86e7fc9cba5e6043c92851`  
		Last Modified: Tue, 01 Mar 2022 14:20:01 GMT  
		Size: 186.5 MB (186479950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c887935e0375e6ff7be1c516d4f02ea050c9fd676ad43cbc792ee437dc1c8f`  
		Last Modified: Wed, 02 Mar 2022 09:03:32 GMT  
		Size: 30.6 MB (30567271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30823bbc44d99fab04d95b5bdc1aa9d5b548fced973bf6b379d08fec54ada6b6`  
		Last Modified: Wed, 02 Mar 2022 09:03:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b5924322507204ce1093344b974e1b37f11cf97952107d252d4a4a1b0682cc`  
		Last Modified: Wed, 02 Mar 2022 09:03:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
