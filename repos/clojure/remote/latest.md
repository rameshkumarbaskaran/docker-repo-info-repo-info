## `clojure:latest`

```console
$ docker pull clojure@sha256:36a76c60489c099d6c48f9237e459feabbfc319af9e0f962cf800c999a0a3fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:a172975df0e59ec56812b59f98a1cf0859257812030e1877973daf529736e040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351939582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56aea8b7aed7c1202e9fcd22b5b304f3f807c431f67b7d9e2cf08a789d439f69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:54:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 29 Mar 2022 00:54:36 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:54:37 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:54:37 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 29 Mar 2022 00:54:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:54:50 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:33:04 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:33:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:33:04 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:33:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 29 Mar 2022 23:33:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:33:09 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:33:48 GMT
RUN boot
# Tue, 29 Mar 2022 23:33:49 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 29 Mar 2022 23:33:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:33:49 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:34:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 29 Mar 2022 23:34:00 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Tue, 29 Mar 2022 23:34:01 GMT
ENV LEIN_ROOT=1
# Tue, 29 Mar 2022 23:34:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 29 Mar 2022 23:34:04 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 29 Mar 2022 23:34:04 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:34:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 29 Mar 2022 23:34:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 29 Mar 2022 23:34:21 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:34:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:34:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc05f270bad654ee17f1143c48586c188a72929a128d61fd8ae15905d7b00`  
		Last Modified: Tue, 29 Mar 2022 01:04:32 GMT  
		Size: 1.6 MB (1582122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac74b14d9edbed131a8bcb34b9c4b9b53cca51a9fd82b0e7f0464377b13394`  
		Last Modified: Tue, 29 Mar 2022 01:09:19 GMT  
		Size: 187.9 MB (187900324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca1ee12b81fa5d521704ea389724ff319ed787f38b1afe2135e720eec55105a`  
		Last Modified: Tue, 29 Mar 2022 23:57:39 GMT  
		Size: 283.1 KB (283052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99204850c807848e559dfcf99dfdfb465346755c3e41a6a5603ab566c4beb61`  
		Last Modified: Tue, 29 Mar 2022 23:57:43 GMT  
		Size: 58.8 MB (58820896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebd60961a46a6fcf8e8930d9ef1ac6c7693fff20074ec11587ebeb6735ca13`  
		Last Modified: Tue, 29 Mar 2022 23:57:38 GMT  
		Size: 11.9 MB (11861576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbb6966bd5a238c8f4b8e0ec98aead113d1b8f4faebcbcf5ecb646280ac8efe`  
		Last Modified: Tue, 29 Mar 2022 23:57:37 GMT  
		Size: 4.2 MB (4207348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd9463dad33b478c196af2ae10df024ce1f57ffa5d817feff28326b8a6fce7a`  
		Last Modified: Tue, 29 Mar 2022 23:57:44 GMT  
		Size: 55.9 MB (55904778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae9f93354ca89be084adc90157c68d9af42f660d1a4c8c9e97dce728fd8efbb`  
		Last Modified: Tue, 29 Mar 2022 23:57:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7969d735a86d5ff40d3ee9b24556a143b8c1a51dbc8be6927d479b085eb2a7f`  
		Last Modified: Tue, 29 Mar 2022 23:57:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b845a4ce7658f3eaef44304abbe7fd881ae95d4402f66ddcc0c0d6709995c05c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348518992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7d0f5fcaf52bcaaf15cd61cb24c02b96ae9cfeeae20dd0c240e92bf42bd8c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:21:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 29 Mar 2022 01:21:25 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:21:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:21:27 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 29 Mar 2022 01:21:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:21:43 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 09:36:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 30 Mar 2022 09:36:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 09:36:42 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:36:48 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 30 Mar 2022 09:36:48 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 30 Mar 2022 09:36:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 30 Mar 2022 09:37:40 GMT
RUN boot
# Wed, 30 Mar 2022 09:37:40 GMT
ENV LEIN_VERSION=2.9.8
# Wed, 30 Mar 2022 09:37:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 09:37:42 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:37:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 30 Mar 2022 09:37:54 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Wed, 30 Mar 2022 09:37:55 GMT
ENV LEIN_ROOT=1
# Wed, 30 Mar 2022 09:38:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Wed, 30 Mar 2022 09:38:01 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 30 Mar 2022 09:38:02 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:38:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 30 Mar 2022 09:38:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 30 Mar 2022 09:38:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 09:38:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 09:38:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee14fdb7a0a09a9e31998d2906081734dba985b95da3f35b7bd79d79b73330`  
		Last Modified: Tue, 29 Mar 2022 01:37:54 GMT  
		Size: 1.4 MB (1361189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175d442985953956c6a8aadc00682f2f4468d782eafeca5eee97cceed189c2c3`  
		Last Modified: Tue, 29 Mar 2022 01:42:03 GMT  
		Size: 186.5 MB (186527583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1016a4248c42df785c6f10c06eb334aaabe2b7e312371b31ad9728b44a8d77`  
		Last Modified: Wed, 30 Mar 2022 10:12:10 GMT  
		Size: 67.3 KB (67257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92791d4d326dafcb2e497999f420b907cb8da6ea24aa899ead0e02bd15ab3646`  
		Last Modified: Wed, 30 Mar 2022 10:12:15 GMT  
		Size: 58.8 MB (58816568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41253b9a585f1a02bc34504cdbb338a9413c51d613473aa3ba13016a2372f7e6`  
		Last Modified: Wed, 30 Mar 2022 10:12:09 GMT  
		Size: 11.6 MB (11645578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edfb78565f42adfe9933a76295db8b19f1df84bca9438d292cba83e7098d4f4`  
		Last Modified: Wed, 30 Mar 2022 10:12:09 GMT  
		Size: 4.2 MB (4207128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9729fc140e03fe70627478a898ba33cd9af5eebfacca1734a2e046906ada1265`  
		Last Modified: Wed, 30 Mar 2022 10:12:15 GMT  
		Size: 55.8 MB (55828349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3d963994630448983c3fa362c69943f0ddfb7d646406845c08544f4c388d3`  
		Last Modified: Wed, 30 Mar 2022 10:12:07 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48967fef84f145aef6f4aebb2e0d14723f112bc6eec1146a0e17ffa7c2d04fd6`  
		Last Modified: Wed, 30 Mar 2022 10:12:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
