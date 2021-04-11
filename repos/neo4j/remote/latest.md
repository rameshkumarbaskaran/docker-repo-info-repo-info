## `neo4j:latest`

```console
$ docker pull neo4j@sha256:bd4b1d7bd9aed5d3c27d536a709892b9d6650e56c31289891baf31873a807fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:7486efeee968395f9302e446d045a7d4aa891643555783a41dd32d5460bea3a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354658640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d45ab82e213e038a54307887a3c163e205952eb3c996183a78b0787a55017f4`
-	Entrypoint: `["\/sbin\/tini","-g","--","\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:47:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 10 Apr 2021 12:47:33 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 10 Apr 2021 12:47:34 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:47:34 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:47:34 GMT
ENV JAVA_VERSION=11.0.10
# Sat, 10 Apr 2021 12:47:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Apr 2021 12:47:55 GMT
CMD ["jshell"]
# Sun, 11 Apr 2021 02:00:43 GMT
ENV NEO4J_SHA256=6d9bb8e21a4b80f8edefff89d6fe592812ae26eaf105cbc967bce88b62290bfd NEO4J_TARBALL=neo4j-community-4.2.5-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 11 Apr 2021 02:00:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.2.5-unix.tar.gz
# Sun, 11 Apr 2021 02:00:43 GMT
ARG TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855
# Sun, 11 Apr 2021 02:00:44 GMT
ARG TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
# Sun, 11 Apr 2021 02:00:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.2.5-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 11 Apr 2021 02:00:45 GMT
COPY multi:036df619eeee70a762e1c411f9386c81834e8c049e5b509d291c299dd3c27252 in /tmp/ 
# Sun, 11 Apr 2021 02:00:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.2.5-unix.tar.gz TINI_SHA256=12d20136605531b09a2c2dac02ccee85e1b874eb322ef6baf7561cd93f93c855 TINI_URI=https://github.com/krallin/tini/releases/download/v0.18.0/tini
RUN apt update     && apt install -y curl wget gosu jq     && curl -L --fail --silent --show-error ${TINI_URI} > /sbin/tini     && echo "${TINI_SHA256}  /sbin/tini" | sha256sum -c --strict --quiet     && chmod +x /sbin/tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /tmp/neo4jlabs-plugins.json /neo4jlabs-plugins.json     && rm -rf /tmp/*     && rm -rf /var/lib/apt/lists/*     && apt-get -y purge --auto-remove curl
# Sun, 11 Apr 2021 02:00:56 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 11 Apr 2021 02:00:56 GMT
WORKDIR /var/lib/neo4j
# Sun, 11 Apr 2021 02:00:56 GMT
VOLUME [/data /logs]
# Sun, 11 Apr 2021 02:00:56 GMT
COPY file:1f612e4a1e8c1ac46ddb26d08eacd2e329f1f6f81fea1862bc5fcd3a8d302a54 in /docker-entrypoint.sh 
# Sun, 11 Apr 2021 02:00:57 GMT
EXPOSE 7473 7474 7687
# Sun, 11 Apr 2021 02:00:57 GMT
ENTRYPOINT ["/sbin/tini" "-g" "--" "/docker-entrypoint.sh"]
# Sun, 11 Apr 2021 02:00:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf4c47c8c6124c3089f3ed26410da9870ba18dd4bc68331e2b7e853116a6cad`  
		Last Modified: Sat, 10 Apr 2021 12:54:28 GMT  
		Size: 3.3 MB (3268764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810072571fafc7e3aa679b8d9c55a366c519def4429f84fe76b604d1714bb868`  
		Last Modified: Sat, 10 Apr 2021 12:59:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3fe8e4a3b911d68ca2362299831f1f23815ff08a043bee2e5a7bb7d7a539ca`  
		Last Modified: Sat, 10 Apr 2021 12:59:45 GMT  
		Size: 203.1 MB (203077438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0504459411cceb042add1530007c76807ed4f997a84a2089d7463115fea0179`  
		Last Modified: Sun, 11 Apr 2021 02:43:55 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34de8df7982137df2c4802f0e01644c7027277fcd59d4c23ce65ba9616de5c13`  
		Last Modified: Sun, 11 Apr 2021 02:43:55 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cee28f2eedde99c2a68e59bdfe20976a24f2213b3c6a52ae5f21f09c36b0d67`  
		Last Modified: Sun, 11 Apr 2021 02:44:04 GMT  
		Size: 121.2 MB (121162464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad8455357bf7104ff7752e4aa66a13b52f379dcc7053763d5324ca4dd16f248`  
		Last Modified: Sun, 11 Apr 2021 02:43:55 GMT  
		Size: 6.0 KB (5955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
