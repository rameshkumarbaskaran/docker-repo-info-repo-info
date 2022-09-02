## `maven:sapmachine`

```console
$ docker pull maven@sha256:de8bd7201af41031f47fd17db6619f8df9642a06c9ca1d4e1ea1b114f8402ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:a2ed8cec1deb8bb95c9f3339276d820a88e8582113249734df771430fff99adb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275047490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baecd627312afea8e53be28446c4f61898a00a69ce7573a9910cb8f2d8121145`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:22 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 02 Sep 2022 05:19:24 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 07:16:55 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 07:16:55 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 02 Sep 2022 07:16:55 GMT
ARG USER_HOME_DIR=/root
# Fri, 02 Sep 2022 07:16:55 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 02 Sep 2022 07:16:55 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 02 Sep 2022 07:16:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 02 Sep 2022 07:16:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 02 Sep 2022 07:16:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 02 Sep 2022 07:16:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 02 Sep 2022 07:16:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 02 Sep 2022 07:16:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 02 Sep 2022 07:16:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bfd7196d5bec726c806cc0c3a4ce44acfba55a52b7a148ef2c87fa58857af3`  
		Last Modified: Fri, 02 Sep 2022 05:20:52 GMT  
		Size: 197.8 MB (197764255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7caab736c068625d65526d6a0b21a3fedc981612b5b549249993de41bd6d689`  
		Last Modified: Fri, 02 Sep 2022 07:22:38 GMT  
		Size: 32.0 MB (32049563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8977b867d58bd23e23364450f52730309d7ba5ce08a8f272762c617e8603fed`  
		Last Modified: Fri, 02 Sep 2022 07:22:33 GMT  
		Size: 8.7 MB (8739497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5effb8bc63ff4960df00c87513be2747385f3d564d1673e73724fec88a2eaa`  
		Last Modified: Fri, 02 Sep 2022 07:22:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8d561d9440519324e68316b1a8c44e8152b94fbc4887db5a3246dca9a95299`  
		Last Modified: Fri, 02 Sep 2022 07:22:33 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
