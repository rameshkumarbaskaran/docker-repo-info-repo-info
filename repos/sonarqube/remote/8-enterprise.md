## `sonarqube:8-enterprise`

```console
$ docker pull sonarqube@sha256:c8d3fa8de7762000eab6789adbb44a988c19ba82336439aa85d64984fdcb161f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:8-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:43eb0a861e46e435ad54421394bf3c932a274c421919c432d8022565b113bdf0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385723453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a848b722c3651c568c2028ea4917c727bb6597bbd3ae8e428fe810689d0e5d9c`
-	Entrypoint: `[".\/bin\/run.sh"]`
-	`SHELL`: `["\/bin\/bash","-c"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:02:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Apr 2020 04:02:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:02:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:02:24 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 23 Apr 2020 04:03:41 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 23 Apr 2020 04:03:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 24 Apr 2020 00:18:43 GMT
RUN apt-get update     && apt-get install -y curl unzip gnupg2 libfreetype6 libfontconfig1     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:18:43 GMT
EXPOSE 9000
# Fri, 24 Apr 2020 00:18:45 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Fri, 24 Apr 2020 00:18:46 GMT
ARG SONARQUBE_VERSION=8.2.0.32929
# Fri, 24 Apr 2020 00:19:53 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
# Fri, 24 Apr 2020 00:19:53 GMT
ENV SONAR_VERSION=8.2.0.32929 SONARQUBE_HOME=/opt/sonarqube
# Fri, 24 Apr 2020 00:19:53 GMT
SHELL [/bin/bash -c]
# Fri, 24 Apr 2020 00:19:55 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN sed -i -e "s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g"   "$JAVA_HOME/conf/security/java.security"
# Fri, 24 Apr 2020 00:20:20 GMT
# ARGS: SONARQUBE_VERSION=8.2.0.32929 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-8.2.0.32929.zip
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;   done     && set -x     && cd /opt     && curl -o sonarqube.zip -fsSL "${SONARQUBE_ZIP_URL}"     && curl -o sonarqube.zip.asc -fSL "${SONARQUBE_ZIP_URL}.asc"     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv "sonarqube-${SONARQUBE_VERSION}" sonarqube     && rm sonarqube.zip*     && chown --recursive sonarqube:sonarqube "$SONARQUBE_HOME"
# Fri, 24 Apr 2020 00:20:21 GMT
COPY --chown=sonarqube:sonarqubefile:b67f51917544737172cd7539a3a3c97397219c52ca27cd8feedde9b53f20a97c in /opt/sonarqube/bin/ 
# Fri, 24 Apr 2020 00:20:22 GMT
USER sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
WORKDIR /opt/sonarqube
# Fri, 24 Apr 2020 00:20:22 GMT
ENTRYPOINT ["./bin/run.sh"]
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
	-	`sha256:793cbc6f8a5918a32dc216bfcded294b39b466b134d11995092baf42f55bcdb2`  
		Last Modified: Thu, 23 Apr 2020 04:11:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0e9985dcd25fc717519eea5dad9cb025b2bf75697e0d68d3cced4b8a4e7f2`  
		Last Modified: Thu, 23 Apr 2020 04:12:21 GMT  
		Size: 42.2 MB (42214657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7021914086a179ca62363693d1c4ed3b0d3af0a77de2646abaec29284b12b`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 8.7 MB (8709087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe812280480d89b1a213d9874edb37a9446844b83fec4baf8dae873be0e4bd`  
		Last Modified: Fri, 24 Apr 2020 00:21:12 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c2d2ee1059102fea28d7c17b231af04d7fcb817edb4aa6ed6d36f00caf1df9`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0942ae2aaaaa6c7511ffb4dd90041949cd2cf81f331ff5c79ce7a460f0d076db`  
		Last Modified: Fri, 24 Apr 2020 00:22:49 GMT  
		Size: 304.4 MB (304434738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447de7a3791a81779bfa28404d3b72d26027aafa91ec2b53a447c8eccd8c591e`  
		Last Modified: Fri, 24 Apr 2020 00:22:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
